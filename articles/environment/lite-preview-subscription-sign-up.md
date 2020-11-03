---
title: 試プレビュー サブスクリプションにサインアップする
description: このトピックでは、Project Operations ライト デプロイメントの購読および展開方法に関する情報を提供します - 見積もり請求の取引を行います。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079131"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>ライト展開のプレビュー サブスクリプションにサインアップ – 見積もり請求の取引

このトピックでは、プレビュー パートナー オファーの購読方法および Dynamics 365 Project Operations の展開方法を説明します - 見積もり請求の取引を行います。

> [!NOTE]
> このプロセスは、Project Operations の今後のリリースで変更されます。

## <a name="prerequisites"></a>前提条件

- プレビューへの参加を招待するメールが届きます。 [Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。
- すべての利用規約を確認してください。

## <a name="subscribe"></a>購読

[プレビュー リクエスト](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) 承認を受け取ると、電子メールにより Microsoft から 2 つのオファーが送信されます。 これらのオファーを使用すると、Project Operations プレビューを展開できます。

- Dynamics 365 Project Operations (CRM) – プレビュー試用版
- Office 365 Project Operations - プレビュー試用版

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – プレビュー試用版 

開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。

1. 最初のオファー コードである **Dynamics 365 Project Operations (CRM) – プレビュー試用版** をブラウザー URLに貼り付けて引き換えます。

![オファーの引き換え](./media/16RedeemFirstOfferNew.png)

2. 注文を確認します。
![注文を確認](./media/17ConfirmOrderNew.png)

オファーが正常に引き換えられたことが確認できます。

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - プレビュー試用版

最初のオファー コードと同じ手順を繰り返します。 最初のオファー コードで使用したのと同じユーザー アカウントを使用して、2 番目のオファー コードを必ず追加してください。

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。


1. [Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。

![管理センター ホーム ページ](./media/14AdminPortal.png)

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

![ライセンスの割り当て](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations (CRM) プレビュー** と **Office 365 Project Operations - プレビュー** のライセンスが選択されていることを確認します。 
4. **変更を保存** を選択します。

## <a name="create-a-new-cds-environment"></a>新しい CDS 環境の作成

1. トピックの手順 [CDS 展開モデル](lite-deployment.md) に従い、新しい Project Operations CDS の展開環境をプロビジョニングします。 環境タイプを選択するときは、 **試用 (サブスクリプション ベース)** を必ず使用してください。
![新しい環境](./media/19CreateEnvironment.png)

2. **Dynamics 365 アプリを有効にする** の設定を選択し、 **これらのアプリを自動的に展開** を空白のままにします。  
3. **保存** を選択して、環境を作成します。

![データベースの追加](./media/20CreateEnvironment1.png)

4. 環境が作成されたら、 **Microsoft Dynamics 365 Project Operations** ソリューションをインストールします。 

![ソリューションのインストール](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS コンフィグレーションをインストールし、デモ データを設定する

トピックの手順 [デモの設定および構成データを適用する](lite-apply-demo-setup-config-data.md) に従い、CDS 構成をインストールし、デモ データを設定します。
