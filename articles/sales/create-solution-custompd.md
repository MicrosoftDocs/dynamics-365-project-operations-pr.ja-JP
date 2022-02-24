---
title: カスタム価格ディメンションのソリューションを作成する
description: このトピックでは、カスタム価格ディメンションに対するソリューションの作成方法を説明します。
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513997"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>カスタム価格ディメンションのソリューションを作成する

 _**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_ 

>[!IMPORTANT]
>すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行う必要があります。 この重要なベスト プラクティスは、必要に応じて変更を更新や削除する柔軟性を実現し、作業の再利用に役立ち、変更を他のインスタンスに簡単に移植可能にします。 必要な変更を加えたら、このソリューションを **マネージド型** ソリューションとしてエクスポートし、他のインスタンスにインポートして再利用します。

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>カスタム価格ディメンションのソリューションを作成する

1.  **設定** > **ソリューション** を選択し、次に **新規** を選択します。
2.  ソリューションに *<your organization name> 価格ディメンション* と名前を付けます。
3. その他の必要情報を入力し、 **保存** を選択します。

  ![カスタム価格ディメンション ソリューションを作成する](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する

次の Project Service エンティティを価格ソリューションに追加して、この価格ソリューションで重要なスキーマの変更を行います。 この手順を完了すると、エンティティが新しい価格ディメンションを認識します。

1.  **設定** > **ソリューション** を順に選択してから **<*組織名*> 価格ディメンション** をダブルクリックします。
2.  ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ** を選択します。
3.  **ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:
 
   - **実績**
   - **予約可能リソース**
   - **見積行**
   - **プロジェクト タスク**
   - **請求明細行の詳細**
   - **仕訳帳明細行**
   - **プロジェクト契約品目の詳細**
   - **プロジェクト チーム メンバー**
   - **見積依頼明細行の詳細**
   - **ロール価格利幅**
   - **ロール価格**
   - **時間入力**
 
   ![既存のエンティティのカスタム価格ディメンション ソリューションを追加する](./media/Existing-entities-to-PD-solution.png)
 
 4. 各エンティティについて、追加するコンポーネントと各エンティティに対するエンティティ資産の最終一覧を確認します。 

   >[!NOTE]
   > 選択した各エンティティに対してフォームとビューをすべて含めます。

  ![追加したエンティティ](./media/solution-component-selection.png)


5.  選択したエンティティに依存エンティティを含めるようプロンプトが表示されたら **いいえ、必須コンポーネントを含めません** を選択します。

    ![依存エンティティを含める](./media/Do-not-include-required.png)
