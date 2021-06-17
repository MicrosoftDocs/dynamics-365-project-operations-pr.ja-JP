---
title: iOS および Android 上の Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドを実装する
description: このトピックでは、拡張機能を使用してカスタム フィールドを実装するための一般的なパターンについて説明します。
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003044"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>iOS および Android 上の Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドを実装する

[!include [banner](../includes/banner.md)]

このトピックでは、拡張機能を使用してカスタム フィールドを実装するための一般的なパターンについて説明します。 次のトピックについて説明します。

- カスタム フィールド フレームワークがサポートするさまざまなデータ型
- タイムシート エントリ上の読み取り専用または編集可能なフィールドを表示し、ユーザーが入力した値をデータベースに保存する方法
- タイムシート ヘッダーに読み取り専用のフィールドを表示する方法
- 他のカスタム ビジネス ロジックを統合してフィールドに既定値を入力し、追加の検証を行う方法

## <a name="audience"></a>対象者

このトピックは、カスタム フィールドを Apple iOS および Google Android で利用可能な Microsoft Dynamics 365 Project Timesheet モバイルアプリケーションに統合する開発者を対象にしています。 X ++ 開発およびプロジェクト タイムシート機能に精通していることが前提です。

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>データ契約 – TSTimesheetCustomField X++ クラス

**TSTimesheetCustomField** クラスは、タイムシート機能のカスタム フィールドに関する情報を表す X++ データ コントラクト クラスです。 カスタム フィールド オブジェクトのリストは、TSTimesheetDetails データ コントラクトおよび TSTimesheetEntry データ コントラクトの両方で渡され、モバイル アプリ内でカスタム フィールドを表示します。

- **TSTimesheetDetails** - タイムシート ヘッダー コントラクト。
- **TSTimesheetEntry** - タイムシート トランザクション契約。 同じプロジェクト情報を持つこれらのオブジェクトおよび **timesheetLineRecId** 値が行を構成します。

### <a name="fieldbasetype-types"></a>fieldBaseType (種類)

**TsTimesheetCustom** オブジェクトの **FieldBaseType** プロパティにより、アプリに表示されるフィールドの種類が決定されます。 次の **種類** の値がサポートされています。

| 種類の値 | 型              | メモ​​ |
|-------------|-------------------|-------|
| 0           | 文字列 (列挙型) | フィールドはテキスト フィールドとして表示されます。 |
| 1           | Integer           | 値は、小数点以下の桁数がない数値として表示されます。 |
| 2           | 実数              | 値は、小数点以下の桁数を含む数値として表示されます。<p>アプリで通貨として実数値を表示するには、**fieldExtenededType** プロパティを使用します。 **numberOfDecimals** プロパティを使用し、表示される小数点以下の桁数を設定することができます。</p> |
| 3           | 日              | 日付の書式は、ユーザーが **ユーザー オプション** の **言語と国/地域の基本設定** の下で指定した **日付、時間、および数値書式** により決定されます。 |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- **stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されていない場合、ユーザーには自由書式のフィールドが提供されます。

    **stringLength** プロパティを使用して、ユーザーが入力できる文字列の最大長を設定できます。

- **stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されている場合、それらのリスト要素が、ユーザーがオプション ボタン (ラジオ ボタン) を使用して選択できる唯一の値になります。

    この場合、文字列フィールドは、ユーザー入力を目的とする列挙値として使用できます。 値を列挙型としてデータベースに保存するには、コマンド チェーンを使用してデータベースに保存する前に、手動で文字列値を列挙値にマップします (例については、このトピックの後半の「TSTimesheetEntryService クラスのコマンド チェーンを使用してアプリからデータベースにタイムシート エントリを保存する」のセクションを参照してください)。

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

このプロパティを使用して、実数値の書式を通貨として設定することができます。 この方法は、**fieldBaseType** 値が **実数** である場合にのみ適用されます。

- **TSCustomFieldExtendedType:None** – 書式設定は適用されません。
- **TSCustomFieldExtendedType::Currency** – 値の書式は通貨として設定されます。

    通貨の書式設定がアクティブな場合、**stringValue** フィールドを使用して、アプリに表示する必要がある通貨コードを渡すことができます。 値は、読み取り専用の値です。

    **realValue** フィールドには、データベースに保存する必要がある金額が含まれます。

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

このプロパティを使用して、アプリのどこにカスタム フィールドを表示するかを指定できます。

- **TSCustomFieldSection::Header** – フィールドはアプリの **詳細** セクションに表示されます。 これらのフィールドは、常に読み取り専用です。
- **TSCustomFieldSection::Line** – フィールドは、タイムシート エントリのすべての標準明細行の後に表示されます。 これらのフィールドは編集可能な場合も、読み取り専用の場合もあります。

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

このプロパティは、アプリが提供する値がデータベースに保存されるときにフィールドを識別します。

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

このプロパティは、アプリが提供する値がデータベースに保存されるときにフィールドを識別します。

### <a name="iseditable-noyes"></a>isEditable (NoYes)

このプロパティを **はい** に設定し、タイムシート エントリ セクションのフィールドをユーザーが編集できるように指定します。 プロパティを **いいえ** に設定し、フィールドを読み取り専用にします。

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

このプロパティを **はい** に設定し、タイムシート エントリ セクションのフィールドを必須として指定します。

### <a name="label-str"></a>label (str)

このプロパティは、アプリでフィールドの次に表示されるラベルを指定します。

### <a name="stringoptions-list-of-strings"></a>stringOptions (文字列のリスト)

このプロパティは、**fieldBaseType** が **文字列** に設定されている場合にのみ適用されます。 **stringOptions** が設定されている場合、オプション ボタン (ラジオ ボタン) を介して選択できる文字列値は、リスト内の文字列によって指定されます。 文字列が指定されていない場合、文字列フィールドに自由書式の入力が許可されます (例については、このトピックの後半の「TSTimesheetEntryService クラスのコマンド チェーンを使用してアプリからデータベースにタイムシート エントリを保存する」のセクションを参照してください)。

### <a name="stringlength-int"></a>stringLength (int)

このプロパティは、文字列フィールドの最大長を指定します。 **fieldBaseType** が **文字列** に設定されている場合にのみ適用されます。

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

このプロパティは、実数のフィールドに表示される小数点以下の桁数を指定します。 **fieldBaseType** が **実数** に設定されている場合にのみ適用されます。

### <a name="ordersequence-int"></a>orderSequence (int)

このプロパティは、複数のカスタム フィールドが指定されている場合に、アプリにカスタム フィールドが表示される順序を制御します。 より低い値のフィールドが最初に表示されます。

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドのブール値を渡します。

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドのグローバル一意識別子 (GUID) を渡します。

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの int64 値を渡します。

### <a name="intvalue-int"></a>intValue (int)

**Int** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの int 値を渡します。

### <a name="realvalue-real"></a>realValue (real)

**Real** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの実数値を渡します。

### <a name="stringvalue-str"></a>stringValue (str)

**String** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの文字列値を渡します。 通貨として書式設定された **Real** 型のフィールドにも使用されます。 それらのフィールドについては、プロパティを使用して通貨コードをアプリに渡します。

### <a name="datevalue-date"></a>dateValue (date)

**Date** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの日付の値を渡します。

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>タイムシート エントリ セクションのカスタム フィールドを表示し、保存する

タイムシート エントリ作成のモバイル アプリのスクリーンショットを次に示します。 すでに設定されている「2 番目のオプション」の列挙値と「テスト文字列」と呼ばれる「時間エントリ」セクションの標準フィールドとカスタム フィールドを示しています。

![アプリのテスト文字列のカスタム フィールド](media/timesheet-entry.jpg)



「テスト文字列」のカスタム フィールドで使用可能な列挙型のオプションの 1 つを選択しているユーザーのモバイル アプリのスクリーンショットを次に示します。  ラジオ ボタンとして表示されている「最初のオプション」と「2 番目のオプション」の 2 つのオプションがあります。 現在、2 番目のオプションが選択されています。

![テスト文字列のカスタムフィールドのオプション ボタン (ラジオ ボタン)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>カスタム フィールドを持つように TSTimesheetLine テーブルを拡張する

一般的なシナリオでは、タイムシート エントリ セクションのカスタム フィールドのデータが TSTimesheetLine テーブルに保存される可能性があります。 ただし、指定されている TSTimesheetTrans レコードに基づいてデータを取得できる場合、または特定のレコード コンテキストがない場合 (たとえば、プロジェクト パラメーターでフィールドが読み取り専用に設定されている場合)、他のテーブルが使用されます。

カスタム フィールドにバッキング データベース レコードは必要ではないことに注意してください。 X++ ロジックに基づいて動的に生成されます。 この方法は、読み取り専用のシナリオで有効です (動的に生成されるカスタム フィールド値の例については、「TSTimesheetDetails クラスのコマンド チェーン buildCustomFieldListForHeader メソッドを使用して、タイムシートの詳細を入力する」のセクションを参照してください。)

アプリケーション オブジェクト ツリーの Visual Studio のスクリーンショットを次に示します。 カスタム フィールドとして追加されている TestLineString フィールドのある、TSTimesheetLine テーブルの拡張機能を示しています。

![明細行の文字列](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、タイムシート エントリ セクションのフィールドを表示する

このコードは、アプリのフィールドの表示設定を制御します。 たとえば、フィールドの種類、ラベル、フィールドが必須かどうか、およびフィールドが表示されるセクションを制御します。

時間エントリの文字列フィールドの例を次に示します。 このフィールドには、**最初のオプション** および **2 番目のオプション** の 2 つのオプションがあり、オプション ボタン (ラジオ ボタン) により使用することができます。 アプリのフィールドは、TSTimesheetLine テーブルに追加される **TestLineString** フィールドに関連付けられています。

**TSTimesheetCustomField::newFromMetatdata()** メソッドを使用して、カスタム フィールド プロパティ **fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength**、および **numberOfDecimals** の初期化を簡略化することに注意してください。 必要に応じて、これらのパラメーターを手動で設定することもできます。

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>TSTimesheetEntry クラスの buildCustomFieldListForEntry メソッドのコマンド チェーンを使用して、タイムシート エントリに値を入力する

**buildCustomFieldListForEntry** メソッドを使用して、モバイル アプリに保存されたタイムシート明細行に値を入力します。 TSTimesheetTrans レコードをパラメーターとして受け取ります。 そのレコードからのフィールドを使用して、アプリのカスタム フィールド値を入力することができます。

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>TSTimesheetEntryService クラスでコマンド チェーンを使用して、アプリからデータベースにタイムシート エントリを保存する

一般的な使用方法でカスタム フィールドをデータベースに保存するには、複数のメソッドを拡張する必要があります。

- **timesheetLineNeedsUpdating** メソッドを使用して、ユーザーによりラインのレコードが変更され、データベースに保存する必要があるかどうかを確認します。 パフォーマンスが問題にならない場合、このメソッドを単純化して常に **True** を返すようにすることができます。
- **populateTimesheetLineFromEntryDuringCreate** および **populateTimesheetLineFromEntryDuringUpdate** メソッドを拡張し、指定された TSTimesheetEntry データ契約レコードから TSTimesheetLine データベース レコードに値を入力できます。 次の例で、データベース フィールドと入力フィールド間でのマップが X++ コードを介して手動で行われていることを確認してください。
- **TSTimesheetEntry** オブジェクトにマップされたカスタム フィールドを TSTimesheetLineweek データベース テーブルに書き込む必要がある場合、**populateTimesheetWeekFromEntry** メソッドを拡張することもできます。

> [!NOTE]
> 次の例では、ユーザーが生の文字列値としてデータベースに選択した **firstOption** または **secondOption** 値を保存します。 データベース フィールドが **列挙** 型のフィールドの場合、それらの値を手動で列挙値にマップし、データベース テーブルの列挙フィールドに保存することができます。

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>タイムシート ヘッダー セクションのカスタム フィールドを表示する

タイムシートを確認しているユーザーのモバイル アプリのスクリーンショットを次に示します。 右上隅で「詳細」ボタンが選択され、「詳細を表示」オプションが表示されています。  

![詳細を表示コマンド](media/show-more.png)

タイムシートの「詳細」セクションを表示しているモバイル アプリのスクリーンショットを次に示します。 「このタイムシートの稼働率 (計算されたカスタム フィールド)」と呼ばれるカスタム フィールドがタイムシート ヘッダー セクションに追加されました。 カスタム フィールドに読み取り専用の値「0.667」が設定されています。

![詳細セクション](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>カスタム フィールドを持つように TSTimesheetTable テーブルを拡張する

一般的なシナリオでは、ヘッダー セクションのカスタム フィールドのデータが TSTimesheetHeader テーブルから取得される可能性があります。 ただし、指定されている TSTimesheetTable レコードに基づいてデータを取得できる場合、または特定のレコード コンテキストがない場合 (たとえば、プロジェクト パラメーターでフィールドが読み取り専用に設定されている場合)、他のテーブルが使用されます。

カスタム フィールドにバッキング データベース レコードは必要ではないことに注意してください。 X++ ロジックに基づいて動的に生成されます。 次の例は、この方法を示しています。

アプリでは、ヘッダー セクションのフィールドは常に読み取り専用です。

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、ヘッダー セクションのフィールドを表示する

このコードは、アプリのフィールドの表示設定を制御します。 たとえば、フィールドの種類、ラベル、フィールドが必須かどうか、およびフィールドが表示されるセクションを制御します。

次の例は、アプリのヘッダー セクションの計算された値を示しています。

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>TSTimesheetDetails クラスの buildCustomFieldListForHeader メソッドのコマンド チェーンを使用して、タイムシートの詳細を入力する

**buildCustomFieldListForHeader** メソッドを使用して、モバイル アプリのタイムシート ヘッダーの詳細を入力します。 TSTimesheetTable レコードをパラメーターとして受け取ります。 そのレコードからのフィールドを使用して、アプリのカスタム フィールド値を入力することができます。 次の例では、データベースから値を読み込みません。 代わりに、X++ ロジックを使用して、アプリに表示される計算された値を生成します。


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>他の構成可能性/拡張性の機会

### <a name="adding-additional-validation-for-the-app"></a>アプリに追加の検証を追加する

データベース レベルでのタイムシート機能に対する既存のロジックは、引き続き期待どおりに機能します。 保存または送信操作の完了を中断し、特定のエラー メッセージを表示するには、**エラーのスロー (「ユーザーへのメッセージ」)** をコマンド チェーン拡張機能を介してコードに追加できます。 拡張可能な有効なメソッドの例を 3 つ示します。

- タイムシート ラインの保存操作の間に TSTimesheetLine テーブルの **validateWrite** が **false** を返す場合、モバイル アプリにエラー メッセージが表示されます。
- アプリのタイムシートの送信中に TSTimesheetTable テーブルの **validateSubmit** が **false** を返す場合、エラー メッセージがユーザーに表示されます。
- TSTimesheetLine テーブルの **insert** メソッド中、フィールド (たとえば、**Line プロパティ**) に入力するロジックは引き続き実行されます。

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>標準フィールドを非表示にし、構成を介して読み取り専用としてマークする

プロジェクト パラメーターから、標準フィールドを読み取り専用にするか、モバイル アプリで非表示にすることができます。 **プロジェクト管理および会計パラメーター** ページの **タイムシート** タブにある **モバイル タイムシート** のセクションのオプションを設定します。

![プロジェクト パラメーター](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>拡張機能を介して選択できる活動を変更する

プロジェクトに選択できる活動は **TsTimesheetProjectService** クラスにある **getActivitiesForProject()** および **getActivityQuery()** メソッドを介して入力されます。 コマンド チェーンを使用してこの動作を変更し、特定のプロジェクトに対して選択できる活動のビジネス シナリオに一致させることができます。

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>タイムシート エントリに既定のプロジェクト カテゴリを入力する

タイムシート エントリの既定のプロジェクト カテゴリのエントリは、3 つのレベルで発生します。 コマンド チェーンを使用し、これらのレベルのいずれかまたはすべてにおいて動作を拡張して、希望する動作を実現できます。 次の階層が使用されます。

1. アプリは、プロジェクト リソースから既定のカテゴリを配置しようとします。 この既定のカテゴリは、**TSTimesheetSettingsService** クラスの **getCurrentUserResource** および **getDelegatedResourcesForCurrentUser** メソッドで設定されます。
2. 既定のカテゴリがプロジェクト リソース レベルで指定されていない場合、アプリはプロジェクト活動から取得しようとします。 この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getActivitiesForProject** メソッドで設定されます。
3. 既定のカテゴリがプロジェクト活動レベルで指定されていない場合、既定のカテゴリはプロジェクト パラメーターから取得されます。 この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getProjectDetailsbyRule** メソッドで設定されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]