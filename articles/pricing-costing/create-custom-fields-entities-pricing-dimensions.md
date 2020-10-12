---
title: 価格ディメンションとしてカスタム フィールドとエンティティを作成する
description: このトピックは、ユーザー定義のオプションセットまたはエンティティの作成方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898267"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>価格ディメンションとしてカスタム フィールドとエンティティを作成する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

ユーザー定義のオプション セットやエンティティを作成するには以下の手順に従ってください。

> [!IMPORTANT]
> すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行うことを推奨します。 この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。 必要な変更をすべて行った後、このソリューションを **管理ソリューション** としてエクスポートします。これを別のインスタンスにインポートして価格設定を再利用します。


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>価格設定ディメンションのカスタムソリューションを作成する
1. **設定** > **ソリューション**に移動し、 **新規** を選択して新規ソリューションを作成します。 
2. **\<your organization name> 価格設定ディメンション**ソリューションの名称を決定し、その他必要な情報を入力し、 **保存**を選択します。
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>価格設定のディメンションのソリューションにカスタム フィールドとオプション セットを作成します。

価格設定のディメンションは、オプション セット、あるいはエンティティである場合があります。 いずれも価格設定のソリューションにて作成されている必要があります。 この手順では、エンティティ ベースのディメンションと、オプション セット ベースのディメンションを作成する方法について説明します。

### <a name="entity-based-dimensions"></a>エンティティ ベースのディメンション

1. **設定** > **ソリューション**に移動し、続いて**\<your organization name>価格ディメンション**をダブルクリックします。
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、 **エンティティ**を選択します。
3. **新規** を選択して、 **スタンダード タイトル**と呼ばれる新しいエンティティを作成します。 
4. その他の必要情報を入力し、 **保存**を選択します。


### <a name="option-set-based-dimensions"></a>オプション セット ベースのディメンション 
2つのオプション セット ベースのディメンションを作成することができます。 **リソースの作業場所** を使用して、 **ホーム** と **オンサイト** の各作業場所の価格を追跡します。 **リソースの作業時間** に **Regular** and **Overtime** の値を使用して、作業完了時の利幅を適用します。


1. **設定** > **ソリューション**に移動し、**\<your organization name>価格ディメンション**をダブルクリックします。 
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、  **オプション セット**を選択します。 
3. **新規** を選択して新たなオプション セットを作成し、その他の必要な情報を入力し、 **保存**を選択します。

## <a name="create-data-for-entity-based-dimensions"></a>エンティティ ベースのディメンションのデータを作成する

エンティティ ベースのディメンションのデータは手動での作成、あるいは Microsoft Excel にてインポートやサービス呼び出しを使用して作成することが出来ます。 この手順では、エンティティ ベースのディメンションである **スタンダード タイトル**を使用して次の2つのスタンダード タイトルを作成します。 **システム エンジニア** と **シニア システム エンジニア** 。 以下の例に示すように、作成するデータが小さい場合は、標準フォームを使用することができます。

1. **高度な検索**を選択し、エンティティに**スタンダード タイトル**を選択します。続いて**結果**を選択します。 **スタンダード タイトル** エンティティのすべての行が表示されます。
2. **新規**を選択し、**名称**フィールドで、 「システムエンジニア」と入力し **保存**をクリックします。
3. フォームを閉じます。 
4. 手順1から3を繰り返し、他のスタンダード タイトル 「シニア システム エンジニア」を作成します。

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する
価格設定ソリューションには、以下のエンティティを追加する必要があります。 この手順を使用して、エンティティが新しい価格設定ディメンションを認識できるよう、価格設定ソリューションで重要なスキーマ変更を行います。

1. **設定** > **ソリューション**を選択し、**\<your organization name>価格ディメンション**をダブルクリックします。 
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ**を選択します。
3. **ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:

  - 実績
  - 予約可能リソースです
  - 見積行
  - 請求明細行の詳細
  - 仕訳帳明細行
  - プロジェクト契約品目の詳細
  - プロジェクト チーム メンバー
  - 見積依頼明細行の詳細
  - ロール価格利幅
  - ロール価格 
  - 時間入力 


> [!NOTE]
> 選択した各エンティティのすべてのフォームとビューが含まれていることを確認してください。

4. 上記で選択したエンティティに依存するエンティティを含めるかどうかを確認するダイアログが表示された場合、 **いいえ**を選択してください。
