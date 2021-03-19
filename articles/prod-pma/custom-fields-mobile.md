---
title: iOS および Android 上の Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドを実装する
description: このトピックでは、拡張機能を使用してカスタム フィールドを実装するための一般的なパターンについて説明します。
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270999"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="f4949-103">iOS および Android 上の Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドを実装する</span><span class="sxs-lookup"><span data-stu-id="f4949-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4949-104">このトピックでは、拡張機能を使用してカスタム フィールドを実装するための一般的なパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f4949-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="f4949-105">次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f4949-105">The following topics are covered:</span></span>

- <span data-ttu-id="f4949-106">カスタム フィールド フレームワークがサポートするさまざまなデータ型</span><span class="sxs-lookup"><span data-stu-id="f4949-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="f4949-107">タイムシート エントリ上の読み取り専用または編集可能なフィールドを表示し、ユーザーが入力した値をデータベースに保存する方法</span><span class="sxs-lookup"><span data-stu-id="f4949-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="f4949-108">タイムシート ヘッダーに読み取り専用のフィールドを表示する方法</span><span class="sxs-lookup"><span data-stu-id="f4949-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="f4949-109">他のカスタム ビジネス ロジックを統合してフィールドに既定値を入力し、追加の検証を行う方法</span><span class="sxs-lookup"><span data-stu-id="f4949-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="f4949-110">対象者</span><span class="sxs-lookup"><span data-stu-id="f4949-110">Audience</span></span>

<span data-ttu-id="f4949-111">このトピックは、カスタム フィールドを Apple iOS および Google Android で利用可能な Microsoft Dynamics 365 Project Timesheet モバイルアプリケーションに統合する開発者を対象にしています。</span><span class="sxs-lookup"><span data-stu-id="f4949-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="f4949-112">X ++ 開発およびプロジェクト タイムシート機能に精通していることが前提です。</span><span class="sxs-lookup"><span data-stu-id="f4949-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="f4949-113">データ契約 – TSTimesheetCustomField X++ クラス</span><span class="sxs-lookup"><span data-stu-id="f4949-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="f4949-114">**TSTimesheetCustomField** クラスは、タイムシート機能のカスタム フィールドに関する情報を表す X++ データ コントラクト クラスです。</span><span class="sxs-lookup"><span data-stu-id="f4949-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="f4949-115">カスタム フィールド オブジェクトのリストは、TSTimesheetDetails データ コントラクトおよび TSTimesheetEntry データ コントラクトの両方で渡され、モバイル アプリ内でカスタム フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="f4949-116">**TSTimesheetDetails** - タイムシート ヘッダー コントラクト。</span><span class="sxs-lookup"><span data-stu-id="f4949-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="f4949-117">**TSTimesheetEntry** - タイムシート トランザクション契約。</span><span class="sxs-lookup"><span data-stu-id="f4949-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="f4949-118">同じプロジェクト情報を持つこれらのオブジェクトおよび **timesheetLineRecId** 値が行を構成します。</span><span class="sxs-lookup"><span data-stu-id="f4949-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="f4949-119">fieldBaseType (種類)</span><span class="sxs-lookup"><span data-stu-id="f4949-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="f4949-120">**TsTimesheetCustom** オブジェクトの **FieldBaseType** プロパティにより、アプリに表示されるフィールドの種類が決定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="f4949-121">次の **種類** の値がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f4949-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="f4949-122">種類の値</span><span class="sxs-lookup"><span data-stu-id="f4949-122">Types value</span></span> | <span data-ttu-id="f4949-123">型</span><span class="sxs-lookup"><span data-stu-id="f4949-123">Type</span></span>              | <span data-ttu-id="f4949-124">メモ​​</span><span class="sxs-lookup"><span data-stu-id="f4949-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="f4949-125">0</span><span class="sxs-lookup"><span data-stu-id="f4949-125">0</span></span>           | <span data-ttu-id="f4949-126">文字列 (列挙型)</span><span class="sxs-lookup"><span data-stu-id="f4949-126">String (and Enum)</span></span> | <span data-ttu-id="f4949-127">フィールドはテキスト フィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="f4949-128">6</span><span class="sxs-lookup"><span data-stu-id="f4949-128">1</span></span>           | <span data-ttu-id="f4949-129">Integer</span><span class="sxs-lookup"><span data-stu-id="f4949-129">Integer</span></span>           | <span data-ttu-id="f4949-130">値は、小数点以下の桁数がない数値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="f4949-131">2</span><span class="sxs-lookup"><span data-stu-id="f4949-131">2</span></span>           | <span data-ttu-id="f4949-132">実数</span><span class="sxs-lookup"><span data-stu-id="f4949-132">Real</span></span>              | <span data-ttu-id="f4949-133">値は、小数点以下の桁数を含む数値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="f4949-134">アプリで通貨として実数値を表示するには、**fieldExtenededType** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4949-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="f4949-135">**numberOfDecimals** プロパティを使用し、表示される小数点以下の桁数を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="f4949-136">3</span><span class="sxs-lookup"><span data-stu-id="f4949-136">3</span></span>           | <span data-ttu-id="f4949-137">日</span><span class="sxs-lookup"><span data-stu-id="f4949-137">Date</span></span>              | <span data-ttu-id="f4949-138">日付の書式は、ユーザーが **ユーザー オプション** の **言語と国/地域の基本設定** の下で指定した **日付、時間、および数値書式** により決定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="f4949-139">4</span><span class="sxs-lookup"><span data-stu-id="f4949-139">4</span></span>           | <span data-ttu-id="f4949-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="f4949-140">Boolean</span></span>           | |
| <span data-ttu-id="f4949-141">15</span><span class="sxs-lookup"><span data-stu-id="f4949-141">15</span></span>          | <span data-ttu-id="f4949-142">GUID</span><span class="sxs-lookup"><span data-stu-id="f4949-142">GUID</span></span>              | |
| <span data-ttu-id="f4949-143">16</span><span class="sxs-lookup"><span data-stu-id="f4949-143">16</span></span>          | <span data-ttu-id="f4949-144">Int64</span><span class="sxs-lookup"><span data-stu-id="f4949-144">Int64</span></span>             | |

- <span data-ttu-id="f4949-145">**stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されていない場合、ユーザーには自由書式のフィールドが提供されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="f4949-146">**stringLength** プロパティを使用して、ユーザーが入力できる文字列の最大長を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="f4949-147">**stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されている場合、それらのリスト要素が、ユーザーがオプション ボタン (ラジオ ボタン) を使用して選択できる唯一の値になります。</span><span class="sxs-lookup"><span data-stu-id="f4949-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="f4949-148">この場合、文字列フィールドは、ユーザー入力を目的とする列挙値として使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="f4949-149">値を列挙型としてデータベースに保存するには、コマンド チェーンを使用してデータベースに保存する前に、手動で文字列値を列挙値にマップします (例については、このトピックの後半の「TSTimesheetEntryService クラスのコマンド チェーンを使用してアプリからデータベースにタイムシート エントリを保存する」のセクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f4949-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="f4949-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="f4949-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="f4949-151">このプロパティを使用して、実数値の書式を通貨として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="f4949-152">この方法は、**fieldBaseType** 値が **実数** である場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="f4949-153">**TSCustomFieldExtendedType:None** – 書式設定は適用されません。</span><span class="sxs-lookup"><span data-stu-id="f4949-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="f4949-154">**TSCustomFieldExtendedType::Currency** – 値の書式は通貨として設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="f4949-155">通貨の書式設定がアクティブな場合、**stringValue** フィールドを使用して、アプリに表示する必要がある通貨コードを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="f4949-156">値は、読み取り専用の値です。</span><span class="sxs-lookup"><span data-stu-id="f4949-156">The value is a read-only value.</span></span>

    <span data-ttu-id="f4949-157">**realValue** フィールドには、データベースに保存する必要がある金額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4949-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="f4949-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="f4949-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="f4949-159">このプロパティを使用して、アプリのどこにカスタム フィールドを表示するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="f4949-160">**TSCustomFieldSection::Header** – フィールドはアプリの **詳細** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="f4949-161">これらのフィールドは、常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="f4949-161">These fields are always read-only.</span></span>
- <span data-ttu-id="f4949-162">**TSCustomFieldSection::Line** – フィールドは、タイムシート エントリのすべての標準明細行の後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="f4949-163">これらのフィールドは編集可能な場合も、読み取り専用の場合もあります。</span><span class="sxs-lookup"><span data-stu-id="f4949-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="f4949-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="f4949-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="f4949-165">このプロパティは、アプリが提供する値がデータベースに保存されるときにフィールドを識別します。</span><span class="sxs-lookup"><span data-stu-id="f4949-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="f4949-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="f4949-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="f4949-167">このプロパティは、アプリが提供する値がデータベースに保存されるときにフィールドを識別します。</span><span class="sxs-lookup"><span data-stu-id="f4949-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="f4949-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f4949-168">isEditable (NoYes)</span></span>

<span data-ttu-id="f4949-169">このプロパティを **はい** に設定し、タイムシート エントリ セクションのフィールドをユーザーが編集できるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="f4949-170">プロパティを **いいえ** に設定し、フィールドを読み取り専用にします。</span><span class="sxs-lookup"><span data-stu-id="f4949-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="f4949-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f4949-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="f4949-172">このプロパティを **はい** に設定し、タイムシート エントリ セクションのフィールドを必須として指定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="f4949-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="f4949-173">label (str)</span></span>

<span data-ttu-id="f4949-174">このプロパティは、アプリでフィールドの次に表示されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="f4949-175">stringOptions (文字列のリスト)</span><span class="sxs-lookup"><span data-stu-id="f4949-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="f4949-176">このプロパティは、**fieldBaseType** が **文字列** に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="f4949-177">**stringOptions** が設定されている場合、オプション ボタン (ラジオ ボタン) を介して選択できる文字列値は、リスト内の文字列によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="f4949-178">文字列が指定されていない場合、文字列フィールドに自由書式の入力が許可されます (例については、このトピックの後半の「TSTimesheetEntryService クラスのコマンド チェーンを使用してアプリからデータベースにタイムシート エントリを保存する」のセクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f4949-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="f4949-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="f4949-179">stringLength (int)</span></span>

<span data-ttu-id="f4949-180">このプロパティは、文字列フィールドの最大長を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="f4949-181">**fieldBaseType** が **文字列** に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="f4949-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="f4949-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="f4949-183">このプロパティは、実数のフィールドに表示される小数点以下の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="f4949-184">**fieldBaseType** が **実数** に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="f4949-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="f4949-185">orderSequence (int)</span></span>

<span data-ttu-id="f4949-186">このプロパティは、複数のカスタム フィールドが指定されている場合に、アプリにカスタム フィールドが表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="f4949-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="f4949-187">より低い値のフィールドが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="f4949-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="f4949-188">booleanValue (boolean)</span></span>

<span data-ttu-id="f4949-189">**Boolean** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドのブール値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="f4949-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="f4949-190">guidValue (guid)</span></span>

<span data-ttu-id="f4949-191">**GUID** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドのグローバル一意識別子 (GUID) を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="f4949-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="f4949-192">int64Value (int64)</span></span>

<span data-ttu-id="f4949-193">**Int64** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの int64 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="f4949-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="f4949-194">intValue (int)</span></span>

<span data-ttu-id="f4949-195">**Int** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの int 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="f4949-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="f4949-196">realValue (real)</span></span>

<span data-ttu-id="f4949-197">**Real** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの実数値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="f4949-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="f4949-198">stringValue (str)</span></span>

<span data-ttu-id="f4949-199">**String** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの文字列値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="f4949-200">通貨として書式設定された **Real** 型のフィールドにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="f4949-201">それらのフィールドについては、プロパティを使用して通貨コードをアプリに渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="f4949-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="f4949-202">dateValue (date)</span></span>

<span data-ttu-id="f4949-203">**Date** 型のフィールドについては、このプロパティは、サーバーとアプリ間でフィールドの日付の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="f4949-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f4949-204">タイムシート エントリ セクションのカスタム フィールドを表示し、保存する</span><span class="sxs-lookup"><span data-stu-id="f4949-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="f4949-205">タイムシート エントリ作成のモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="f4949-206">すでに設定されている「2 番目のオプション」の列挙値と「テスト文字列」と呼ばれる「時間エントリ」セクションの標準フィールドとカスタム フィールドを示しています。</span><span class="sxs-lookup"><span data-stu-id="f4949-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![アプリのテスト文字列のカスタム フィールド](media/timesheet-entry.jpg)



<span data-ttu-id="f4949-208">「テスト文字列」のカスタム フィールドで使用可能な列挙型のオプションの 1 つを選択しているユーザーのモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="f4949-209">ラジオ ボタンとして表示されている「最初のオプション」と「2 番目のオプション」の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f4949-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="f4949-210">現在、2 番目のオプションが選択されています。</span><span class="sxs-lookup"><span data-stu-id="f4949-210">The second option is currently selected.</span></span>

![テスト文字列のカスタムフィールドのオプション ボタン (ラジオ ボタン)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f4949-212">カスタム フィールドを持つように TSTimesheetLine テーブルを拡張する</span><span class="sxs-lookup"><span data-stu-id="f4949-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="f4949-213">一般的なシナリオでは、タイムシート エントリ セクションのカスタム フィールドのデータが TSTimesheetLine テーブルに保存される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4949-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="f4949-214">ただし、指定されている TSTimesheetTrans レコードに基づいてデータを取得できる場合、または特定のレコード コンテキストがない場合 (たとえば、プロジェクト パラメーターでフィールドが読み取り専用に設定されている場合)、他のテーブルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f4949-215">カスタム フィールドにバッキング データベース レコードは必要ではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f4949-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f4949-216">X++ ロジックに基づいて動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f4949-217">この方法は、読み取り専用のシナリオで有効です (動的に生成されるカスタム フィールド値の例については、「TSTimesheetDetails クラスのコマンド チェーン buildCustomFieldListForHeader メソッドを使用して、タイムシートの詳細を入力する」のセクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="f4949-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="f4949-218">アプリケーション オブジェクト ツリーの Visual Studio のスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="f4949-219">カスタム フィールドとして追加されている TestLineString フィールドのある、TSTimesheetLine テーブルの拡張機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="f4949-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![明細行の文字列](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f4949-221">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、タイムシート エントリ セクションのフィールドを表示する</span><span class="sxs-lookup"><span data-stu-id="f4949-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="f4949-222">このコードは、アプリのフィールドの表示設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="f4949-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f4949-223">たとえば、フィールドの種類、ラベル、フィールドが必須かどうか、およびフィールドが表示されるセクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="f4949-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f4949-224">時間エントリの文字列フィールドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="f4949-225">このフィールドには、**最初のオプション** および **2 番目のオプション** の 2 つのオプションがあり、オプション ボタン (ラジオ ボタン) により使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="f4949-226">アプリのフィールドは、TSTimesheetLine テーブルに追加される **TestLineString** フィールドに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f4949-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="f4949-227">**TSTimesheetCustomField::newFromMetatdata()** メソッドを使用して、カスタム フィールド プロパティ **fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength**、および **numberOfDecimals** の初期化を簡略化することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f4949-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="f4949-228">必要に応じて、これらのパラメーターを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4949-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="f4949-229">TSTimesheetEntry クラスの buildCustomFieldListForEntry メソッドのコマンド チェーンを使用して、タイムシート エントリに値を入力する</span><span class="sxs-lookup"><span data-stu-id="f4949-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="f4949-230">**buildCustomFieldListForEntry** メソッドを使用して、モバイル アプリに保存されたタイムシート明細行に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4949-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="f4949-231">TSTimesheetTrans レコードをパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f4949-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="f4949-232">そのレコードからのフィールドを使用して、アプリのカスタム フィールド値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="f4949-233">TSTimesheetEntryService クラスでコマンド チェーンを使用して、アプリからデータベースにタイムシート エントリを保存する</span><span class="sxs-lookup"><span data-stu-id="f4949-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="f4949-234">一般的な使用方法でカスタム フィールドをデータベースに保存するには、複数のメソッドを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4949-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="f4949-235">**timesheetLineNeedsUpdating** メソッドを使用して、ユーザーによりラインのレコードが変更され、データベースに保存する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4949-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="f4949-236">パフォーマンスが問題にならない場合、このメソッドを単純化して常に **True** を返すようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="f4949-237">**populateTimesheetLineFromEntryDuringCreate** および **populateTimesheetLineFromEntryDuringUpdate** メソッドを拡張し、指定された TSTimesheetEntry データ契約レコードから TSTimesheetLine データベース レコードに値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="f4949-238">次の例で、データベース フィールドと入力フィールド間でのマップが X++ コードを介して手動で行われていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4949-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="f4949-239">**TSTimesheetEntry** オブジェクトにマップされたカスタム フィールドを TSTimesheetLineweek データベース テーブルに書き込む必要がある場合、**populateTimesheetWeekFromEntry** メソッドを拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4949-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="f4949-240">次の例では、ユーザーが生の文字列値としてデータベースに選択した **firstOption** または **secondOption** 値を保存します。</span><span class="sxs-lookup"><span data-stu-id="f4949-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="f4949-241">データベース フィールドが **列挙** 型のフィールドの場合、それらの値を手動で列挙値にマップし、データベース テーブルの列挙フィールドに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="f4949-242">タイムシート ヘッダー セクションのカスタム フィールドを表示する</span><span class="sxs-lookup"><span data-stu-id="f4949-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="f4949-243">タイムシートを確認しているユーザーのモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="f4949-244">右上隅で「詳細」ボタンが選択され、「詳細を表示」オプションが表示されています。</span><span class="sxs-lookup"><span data-stu-id="f4949-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![詳細を表示コマンド](media/show-more.png)

<span data-ttu-id="f4949-246">タイムシートの「詳細」セクションを表示しているモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="f4949-247">「このタイムシートの稼働率 (計算されたカスタム フィールド)」と呼ばれるカスタム フィールドがタイムシート ヘッダー セクションに追加されました。</span><span class="sxs-lookup"><span data-stu-id="f4949-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="f4949-248">カスタム フィールドに読み取り専用の値「0.667」が設定されています。</span><span class="sxs-lookup"><span data-stu-id="f4949-248">A read-only value of "0.667" is set on the custom field.</span></span>

![詳細セクション](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f4949-250">カスタム フィールドを持つように TSTimesheetTable テーブルを拡張する</span><span class="sxs-lookup"><span data-stu-id="f4949-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="f4949-251">一般的なシナリオでは、ヘッダー セクションのカスタム フィールドのデータが TSTimesheetHeader テーブルから取得される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4949-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="f4949-252">ただし、指定されている TSTimesheetTable レコードに基づいてデータを取得できる場合、または特定のレコード コンテキストがない場合 (たとえば、プロジェクト パラメーターでフィールドが読み取り専用に設定されている場合)、他のテーブルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f4949-253">カスタム フィールドにバッキング データベース レコードは必要ではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f4949-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f4949-254">X++ ロジックに基づいて動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f4949-255">次の例は、この方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f4949-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="f4949-256">アプリでは、ヘッダー セクションのフィールドは常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="f4949-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="f4949-257">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、ヘッダー セクションのフィールドを表示する</span><span class="sxs-lookup"><span data-stu-id="f4949-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="f4949-258">このコードは、アプリのフィールドの表示設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="f4949-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f4949-259">たとえば、フィールドの種類、ラベル、フィールドが必須かどうか、およびフィールドが表示されるセクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="f4949-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f4949-260">次の例は、アプリのヘッダー セクションの計算された値を示しています。</span><span class="sxs-lookup"><span data-stu-id="f4949-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="f4949-261">TSTimesheetDetails クラスの buildCustomFieldListForHeader メソッドのコマンド チェーンを使用して、タイムシートの詳細を入力する</span><span class="sxs-lookup"><span data-stu-id="f4949-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="f4949-262">**buildCustomFieldListForHeader** メソッドを使用して、モバイル アプリのタイムシート ヘッダーの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4949-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="f4949-263">TSTimesheetTable レコードをパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f4949-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="f4949-264">そのレコードからのフィールドを使用して、アプリのカスタム フィールド値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="f4949-265">次の例では、データベースから値を読み込みません。</span><span class="sxs-lookup"><span data-stu-id="f4949-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="f4949-266">代わりに、X++ ロジックを使用して、アプリに表示される計算された値を生成します。</span><span class="sxs-lookup"><span data-stu-id="f4949-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="f4949-267">他の構成可能性/拡張性の機会</span><span class="sxs-lookup"><span data-stu-id="f4949-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="f4949-268">アプリに追加の検証を追加する</span><span class="sxs-lookup"><span data-stu-id="f4949-268">Adding additional validation for the app</span></span>

<span data-ttu-id="f4949-269">データベース レベルでのタイムシート機能に対する既存のロジックは、引き続き期待どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="f4949-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="f4949-270">保存または送信操作の完了を中断し、特定のエラー メッセージを表示するには、**エラーのスロー (「ユーザーへのメッセージ」)** をコマンド チェーン拡張機能を介してコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="f4949-271">拡張可能な有効なメソッドの例を 3 つ示します。</span><span class="sxs-lookup"><span data-stu-id="f4949-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="f4949-272">タイムシート ラインの保存操作の間に TSTimesheetLine テーブルの **validateWrite** が **false** を返す場合、モバイル アプリにエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="f4949-273">アプリのタイムシートの送信中に TSTimesheetTable テーブルの **validateSubmit** が **false** を返す場合、エラー メッセージがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="f4949-274">TSTimesheetLine テーブルの **insert** メソッド中、フィールド (たとえば、**Line プロパティ**) に入力するロジックは引き続き実行されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="f4949-275">標準フィールドを非表示にし、構成を介して読み取り専用としてマークする</span><span class="sxs-lookup"><span data-stu-id="f4949-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="f4949-276">プロジェクト パラメーターから、標準フィールドを読み取り専用にするか、モバイル アプリで非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="f4949-277">**プロジェクト管理および会計パラメーター** ページの **タイムシート** タブにある **モバイル タイムシート** のセクションのオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="f4949-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![プロジェクト パラメーター](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="f4949-279">拡張機能を介して選択できる活動を変更する</span><span class="sxs-lookup"><span data-stu-id="f4949-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="f4949-280">プロジェクトに選択できる活動は **TsTimesheetProjectService** クラスにある **getActivitiesForProject()** および **getActivityQuery()** メソッドを介して入力されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="f4949-281">コマンド チェーンを使用してこの動作を変更し、特定のプロジェクトに対して選択できる活動のビジネス シナリオに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="f4949-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="f4949-282">タイムシート エントリに既定のプロジェクト カテゴリを入力する</span><span class="sxs-lookup"><span data-stu-id="f4949-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="f4949-283">タイムシート エントリの既定のプロジェクト カテゴリのエントリは、3 つのレベルで発生します。</span><span class="sxs-lookup"><span data-stu-id="f4949-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="f4949-284">コマンド チェーンを使用し、これらのレベルのいずれかまたはすべてにおいて動作を拡張して、希望する動作を実現できます。</span><span class="sxs-lookup"><span data-stu-id="f4949-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="f4949-285">次の階層が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="f4949-286">アプリは、プロジェクト リソースから既定のカテゴリを配置しようとします。</span><span class="sxs-lookup"><span data-stu-id="f4949-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="f4949-287">この既定のカテゴリは、**TSTimesheetSettingsService** クラスの **getCurrentUserResource** および **getDelegatedResourcesForCurrentUser** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="f4949-288">既定のカテゴリがプロジェクト リソース レベルで指定されていない場合、アプリはプロジェクト活動から取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="f4949-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="f4949-289">この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getActivitiesForProject** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="f4949-290">既定のカテゴリがプロジェクト活動レベルで指定されていない場合、既定のカテゴリはプロジェクト パラメーターから取得されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="f4949-291">この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getProjectDetailsbyRule** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4949-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]