---
title: リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします
description: このトピックは、リソース/非在庫ベースのシナリオ向け Project Operations をサブスクライブして展開する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948942"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、プレビュー/パートナー オファーをサブスクライブし、リソース/非在庫ベースのシナリオ向け Project Operations 環境を展開する方法を説明しています。

## <a name="prerequisites"></a>前提条件

- プレビューへの参加を招待するメールが届きます。 [Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。
- Finance 環境を展開するには、環境ごとに請求される有効な Azure サブスクリプションが必要です。 組織の既存のサブスクリプションを使用するか、[Azure トライアル](https://azure.microsoft.com/en-us/free/) を使用して開始できます。 CDS 環境は、30 日間限定で無料で提供されます。

## <a name="subscribe"></a>購読

[プレビュー要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) が承認されると、メールで Microsoft から 2 つのオファーが送信されますを受け取ります。 これらのオファーを使用すると、Project Operations プレビューを展開できます。

- Dynamics 365 Project Operations – プレビュー 試用版
- Dynamics 365 for Finance and Operations プレビュー 試用版。

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – プレビュー 試用版

1. 最初のオファーである、**Dynamics 365 Project Operations 試用版**を、歓迎メールに記載されている URL で利用します。

![最初のオファー](./media/1FirstOffer.png)

2. サービスにサブスクライブする組織に属するユーザーとしてログインしていることを確認します。
3. オファーの引き換えに進みます。 
4. **はい、アカウントに追加**を選択します。

![オファーの引き換え](./media/2RedeemFirstOffer.png)

![オファーの確認](./media/3ConfirmFirstOffer.png)

![引き換え済みオファー](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance プレビュー 試用版

歓迎メールの 2 番目のオファーで同じ手順を繰り返します。

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するためには、組織の Office 365 のポータルへの管理アクセスが必要です。

1. [Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。

![Office 管理ポータル](./media/5OfficeAdminPortal.png)

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

![ライセンスの割り当て](./media/6AssignLicenses.png)

3. Project Operations ライセンスが選択されていることを確認し、**変更の保存**を選択します。 

> [!NOTE]
> Finance 試用版オファーをユーザーに割り当てる必要はありません。

## <a name="start-a-new-project-in-lcs"></a>LCS で新しいプロジェクトを開始する

トピック[LCS で新しいプロジェクトの開始](create-lcs-project.md) の説明に従って、新しい LCS プロジェクトを作成します

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS プロジェクトに Azure サブスクリプションを追加する

このタスクを完了するには、トピック[LCS プロジェクトに Azure サブスクリプションを追加する](resource-add-azure-subscription-lcs-project.md) の手順に従ってください。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>リソース/非在庫のシナリオの Project Operations で Finance デモ環境を展開する

トピック[新しい環境をプロビジョニングする](resource-provision-new-environment.md) のガイダンスに従い、展開を完了します。 プレビューの[デモ環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) の展開の種類を使用します。

## <a name="install-cds-setup-and-configuration-data"></a>CDS 設定および構成データをインストールする

トピック[Common Data Service で構成データを設定および適用](resource-apply-pro-setup-config-data.md) の説明に従って、CDS の設定および構成データをインストールします。

