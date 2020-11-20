---
title: リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします
description: このトピックは、リソース/非在庫ベースのシナリオ向け Project Operations をサブスクライブして展開する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121134"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、プレビュー/パートナー オファーをサブスクライブし、リソース/非在庫ベースのシナリオ向け Project Operations 環境を展開する方法を説明しています。

## <a name="prerequisites"></a>前提条件

- プレビューへの参加を招待するメールが届きます。 [Project Operations Web サイト](https://dynamics.microsoft.com/en-us/project-operations/overview/) でプレビューを要求できます。
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。
- Finance 環境を展開するには、環境ごとに請求される有効な Azure サブスクリプションが必要です。 組織の既存のサブスクリプションを使用するか、[Azure トライアル](https://azure.microsoft.com/en-us/free/) を使用して開始できます。 CDS 環境は、30 日間限定で無料で提供されます。

## <a name="subscribe"></a>購読

[プレビュー要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) が承認されると、メールで Microsoft から 3 つのオファーが送信されますを受け取ります。 これらのオファーを使用すると、Project Operations プレビューを展開できます。

- Dynamics 365 Project Operations (CRM) – プレビュー試用版
- Office 365 Project Operations - プレビュー試用版
- Dynamics 365 Finance - プレビュー 試用版

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – プレビュー試用版 

開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。

1. 最初のオファー コードである **Dynamics 365 Project Operations (CRM) – プレビュー試用版** をブラウザー URLに貼り付けて引き換えます。

![オファーの引き換え](./media/16RedeemFirstOfferNew.png)

2. 注文を確認します。

![注文を確認する](./media/17ConfirmOrderNew.png)

オファーが正常に引き換えられたことを確認します。

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - プレビュー試用版

最初のオファー コードと同じ手順を繰り返します。 最初のオファー コードで使用したのと同じユーザー アカウントを使用して、2 番目のオファー コードを必ず追加してください。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance プレビュー 試用版

歓迎メールから最後のオファーで同じ手順を繰り返します。

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。

1. [Microsoft 365 管理センター](https://portal.office.com/) に移動し、ユーザーにライセンスを割り当てます。

![管理センター ホーム ページ](./media/14AdminPortal.png)

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

![ライセンスの割り当て](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations (CRM) プレビュー** と **Office 365 Project Operations - プレビュー** ライセンスが選択されていることを確認して、**変更を保存する** を選択します。

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
このステップは、Finance デモ環境がデプロイされ、FO のデモデータの準備ができた後でのみ完了してください。
