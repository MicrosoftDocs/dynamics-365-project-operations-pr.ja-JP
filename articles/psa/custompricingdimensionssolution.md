---
title: 価格設定ディメンションのカスタム ソリューションを作成する
description: このトピックでは、カスタム価格設定ディメンションを作成するときにカスタム ソリューションを作成する方法について説明します。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012322"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>価格設定ディメンションのカスタム ソリューションを作成する

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> すべてのカスタム価格設定ディメンションの変更は、個別のソリューションで行う必要があります。 この重要なベスト プラクティスにより、将来的に必要に応じた変更を更新、あるいは削除することができる柔軟性が提供され、作業内容の再利用に役立てることができ、これら変更を別のインスタンスに容易に移植することができます。 必要な変更を行った後、このソリューションを **管理ソリューション** としてエクスポートし、別のインスタンスにインポートして価格設定を再利用します。

1. **設定** > **ソリューション** を選択し、次に **新規** を選択します。 
2. **\<your organization name> 価格設定ディメンション** ソリューションの名称を決定し、その他必要な情報を入力し、 **保存** を選択します。

> ![価格設定ディメンションのカスタムソリューションを作成する](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>価格設定ディメンション ソリューションにすべての必須エンティティと、関連するコンポーネントを追加する
価格設定ソリューションには、以下の Project Service エンティティを追加する必要があります。 この手順を完了して、エンティティが新しい価格設定ディメンションを認識できるよう、価格設定ソリューションで重要なスキーマ変更を行います。

1. **設定** > **ソリューション** を選択し、続いて **\<your organization name>価格ディメンション** をダブルクリックします。 
2. ソリューション エクスプローラーの左側のナビゲーションパネルで、 **既存項目の追加** > **エンティティ** を選択します。
3. **ソリューション コンポーネント** ダイアログ ボックスで、以下のエンティティを選択します:

- 実績
- 予約可能リソース
- 見積行
- プロジェクト タスク
- 請求明細行の詳細
- 仕訳帳明細行
- プロジェクト契約品目の詳細
- プロジェクト チーム メンバー
- 見積依頼明細行の詳細
- ロール価格利幅
- ロール価格 
- 時間入力 

> ![価格設定ディメンション ソリューションに既存のエンティティを追加します。](media/Existing-entities-to-PD-solution.png)

> ![ソリューション コンポーネントの選択](media/Dimension-Components.png)

> [!NOTE]
> 選択した各エンティティのすべてのフォームとビューが含まれていることを確認してください。

4. 選択したエンティティの依存エンティティを含めるかどうかを確認するダイアログが表示された場合、**いいえ** を選択してください。

> ![すべての関連コンポーネントを含めない](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]