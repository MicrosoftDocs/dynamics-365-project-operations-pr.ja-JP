---
title: 試プレビュー サブスクリプションにサインアップする
description: このトピックでは、Project Operations ライト デプロイメントの購読および展開方法に関する情報を提供します - 見積もり請求の取引を行います。
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948939"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>ライト展開のプレビュー サブスクリプションにサインアップ – 見積もり請求の取引

このトピックでは、プレビュー パートナー オファーの購読方法および Dynamics 365 Project Operations の展開方法を説明します - 見積もり請求の取引を行います。

> [!NOTE]
> このプロセスは、Project Operations の今後のリリースで変更されます。

## <a name="prerequisites"></a>前提条件

- プレビューへの参加を招待するメールが届きます。 [Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。
- プレビューを展開するユーザーには、電話番号と有効なクレジット カードが必要です。 サイン アップ中、6 ヶ月間はカードへの請求がありません。 6 ヶ月後、サブスクリプションをキャンセルする必要があります。 
- すべての利用規約を確認してください。

## <a name="subscribe"></a>購読

[プレビュー リクエスト](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) 承認を受け取ると、電子メールにより Microsoft から 2 つのオファーが送信されます。 これらのオファーを使用すると、Project Operations プレビューを展開できます。

- Dynamics 365 Customer Service プレビュー トライアル – シングル ユース コード
- Dynamics 365 Project Operations – プレビュー トライアル

### <a name="dynamics-365-customer-service-paid-offer"></a>Dynamics 365 Customer Service 有料オファー

1. InPrivate/Incognito ブラウザー ウィンドウを使用して、Dynamics 365 Customer Service の最初のオファー コードを利用します。 Customer Service にサイン アップするには、次のものが必要です。

- 電話番号
- クレジット カード。 サイン アップすると、6 ヶ月間はカードへの請求がありません。 6 ヶ月後、サブスクリプションをキャンセルする必要があります。
- すべての利用規約を確認してください。

2. 連絡先を提供します。

![連絡先情報](./media/1ContactInformation.png)

3. 新しいテナントの詳細を提供します。

![ユーザー ID を作成](./media/2CreateUserID.png)

4. ID 確認を行い、新しいユーザー ID を保存してから、**設定**を選択します。

![情報を保存](./media/3SaveInfo.png)

5. クレジット カードの申し込みを完了し、すべての利用規約を確認してください。 

![クレジット カードを完了する](./media/4CompleteCreditCard.png)

![クレジット カードの清算](./media/5CreditCardCheckout.png)

![受注の保存](./media/6SaveOrder.png)

![クレジット カードの確認](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Dynamics 365 Customer Service エンタープライズ オファーをキャンセル

Dynamics 365 Customer Service Enterprise Offer は、6 ヶ月間無料で提供されます。 オファーは、6 ヶ月の期間の終わりにフル レートで更新されます。 更新日より前にキャンセルするには、次の手順を実行してください。 

> [!NOTE]
> これらの手順を完了すると、Project Operations のパブリック プレビュー環境を使用できなくなります。

1. [管理ポータル](https://admin.microsoft.com/) へ移動し、**請求先**の下で、**製品**を選択します。

![Admin Portal、製品ぺージ](./media/8AdminPortal.png)

2. **Dynamics 365 Customer Service Enterprise Offer** を選択します。

![サブスクリプションのキャンセル](./media/9CancelSubscription.png)

3. **設定** > **アクション** > **サブスクリプションのキャンセル** を選択します。
4. **サブスクリプションのキャンセル**フォームで、必須フィールドに情報を入力します。
5. **キャンセル** > **サブスクリプション** の順で選択します。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – プレビュー 試用版

1. 2 番目のオファーである、Dynamics 365 Project Operations 試用版を、歓迎メールに記載されている URL で利用します。

![オファー 2 の引き換え](./media/10RedeemOffer2.png)

2. 最初のオファー コードを使用して、サブスクライブしたのと同じ組織に属するユーザーとしてログ インしていることを確認してから、オファーの引き換えに進みます。 
3. **はい、アカウントに追加**を選択します。

![取引先企業を追加](./media/11AddToAccount.png)

![今すぐ試すスクリーン](./media/12TryNow.png)

![受注の詳細](./media/13Confirmation.png)

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するためには、組織の Office 365 のポータルへの管理アクセスが必要です。

1. [Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。

![管理センター ホーム ページ](./media/14AdminPortal.png)

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

![ライセンスの割り当て](./media/15AssignLicenses.png)

3. **Customer Service Enterprise** および**プロジェクトの営業案件**が選択されていることを確認し、**変更を保存する**を選びます。

## <a name="create-a-new-cds-environment"></a>新しい CDS 環境の作成

トピックの手順 [CDS 展開モデル](lite-deployment.md) に従い、新しい Project Operations CDS の展開環境をプロビジョニングします。

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS コンフィグレーションをインストールし、デモ データを設定する

トピックの手順 [デモの設定および構成データを適用する](lite-apply-demo-setup-config-data.md) に従い、CDS 構成をインストールし、デモ データを設定します。
