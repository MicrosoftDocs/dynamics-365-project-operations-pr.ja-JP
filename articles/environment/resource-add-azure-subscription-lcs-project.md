---
title: LCS プロジェクトに Azure サブスクリプションを追加する
description: このトピックは、Azure サブスクリプションを LCS プロジェクトに接続する方法に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948941"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>LCS プロジェクトに Azure サブスクリプションを追加する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

クラウド ホスト環境は、既存の Azure サブスクリプションを使用して展開する必要があります。 このトピックは、既存の Azure サブスクリプションを LCS プロジェクトに接続する方法を説明します。 

## <a name="grant-admin-consent"></a>管理者の同意を与える

1. LCS プロジェクトの、**環境**セクションで、**Microsoft Azure 設定**を選択します。

![Microsoft Azure の設定](./media/1MicrosoftAzureSettings.png)

2. **プロジェクト設定**ページの、**Azure コネクタ** タブで、**承認**を選択します。 これにより、環境をこのプロジェクトに展開できます。

![Azure コネクタ](./media/2AzureConnectors.png)

3. もう一度**承認**を選択して、管理者の同意を提供します。

![管理者の同意を与える](./media/3GrantAdminConsent.png)

4. アクセス許可の要求を受け入れます。

![アクセス許可の要求を受け入れます](./media/4AcceptPermissionRequest.png)

これで承認は完了です。 

![承認に成功しました](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a> Dynamics Deployment Services に Azure サブスクリプションへのアクセスを提供します

1. [Microsoft Azure 請求](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) に移動し、サブスクリプションを選択します。 Dynamics Deployment Servicesは、環境を展開できるようにするために、このサブスクリプションにアクセスする必要があります。

![Azure のサブスクリプションの詳細](./media/6AzureSubscription.png)

2. ナビゲーション ウィンドウで**アクセス制御 (IAM)** を選択し、**ロールの割り当ての追加**を選択します。
3. 右側のスライダーで、**共同作成者ロール**を選択し、提供されたリストで、**Dynamics Deployment Services** を検索して選択します。 
4. **保存**を選択します。

![サブスクリプション アクセス](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>LCS プロジェクトにサブスクリプション コネクタを追加する

1. LCS プロジェクトの、**Microsoft Azure 設定**ページで、**追加**を選択して、新しいコネクタを追加します。
2. Azure サブスクリプション ID を入力してください。 [Azure portal](https://ms.portal.azure.com/)の、画面の左下にある**設定**で Azure サブスクリプション ID を見つけることができます。
3. **Azure Resource Manager を使用するための構成**フィールドで、**はい**を選択します。
4. Azure のサブスクリプション AAD テナント ドメインが、使用しているドメイン所有の Azure サブスクリプションと一致することを確認し、**次へ**を選択します。
5. **Microsoft Azure セットアップ**画面で、確認のために**次へ**を選択します。 この画面でエラーが発生した場合は、このトピックの[Dynamics Deployment Servicesに Azure サブスクリプションへのアクセスを提供する](#provide) セクションに戻り、すべての手順を完了していることを確認してください。
6. Azure 管理証明書 をコンピューターのローカル フォルダーにダウンロードし、**設定** > **管理証明書**に移動して Azure 管理ポータルにアップロードします。 この証明書により、LCS がユーザーに代わって Azure と通信できるようになります。 ユーザーがサブスクリプションにアクセスできる場合は、この手順をスキップできます。
7. **次へ**を選択します。
8. 展開する Azure リージョンを選択し、このシステムを使用する予定の場所に近いデータ センターを選択します。
9.  **接続**を選択します。

これで、Azure サブスクリプションが正常に接続されました。 これで、Dynamics 365 Finance のクラウド ホスト環境を展開できます。


