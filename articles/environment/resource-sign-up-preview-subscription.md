---
title: リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします
description: この記事では、リソース/非在庫ベースのシナリ向けに Project Operations を購読および展開する方法について説明します。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842021"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>リソース/在庫のないシナリオ向け Project Operations プレビュー サブスクリプションにサインアップします

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_



この記事では、試用版の購読とリソース/非在庫ベースのシナリ向けに Project Operations 環境を展開する方法について説明します。

## <a name="prerequisites"></a>前提条件
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。 最初のオファーの引き換え時にテナントを作成できます。 
- Finance 環境を展開するには、環境ごとに請求される有効な Azure サブスクリプションが必要です。 組織の既存のサブスクリプションを使用するか、[Azure トライアル](https://azure.microsoft.com/free/) を使用して開始できます。 CDS 環境は、30 日間限定で無料で提供されます。

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。
> 
> 試用版はテナントでの単一回の使用となります。 試用版は 1 度しか実行できません。 試用版に特化した、新しいテナントを作成することをお勧めします。


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - プレビュー試用版 

開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。

1. [Project Operations 試用版](https://aka.ms/try-po)にアクセスし、 最初のオファーコードを **Dynamics 365 Project Operations** こちらで引き換えます。
2. 注文を確認します。

  オファーが正常に引き換えられたことを確認します。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance プレビューの試用版

[Dynamics 365 for Finance プレビューの試用版](https://aka.ms/trypoche)にアクセスし、「クラウドホスト環境に登録する」のオファーを使用して、前述のセクションに記載の手順を繰り返します。  

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するためには、組織の Microsoft 365 のポータルへの管理アクセスが必要です。

1. [Microsoft 365 管理センター](https://portal.office.com/)にアクセスし、ユーザーにライセンスを割り当てます。

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

3. **Dynamics 365 Project Operations** のライセンスが選択されていることを確認し、**変更を保存** を選択します。

> [!NOTE]
> Finance 試用版オファーをユーザーに割り当てる必要はありません。

## <a name="start-a-new-project-in-lcs"></a>LCS で新しいプロジェクトを開始する

記事、[LCS で新しいプロジェクトを開始する](create-lcs-project.md) の説明にある通り、新規 LCS プロジェクトを作成する

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS プロジェクトに Azure サブスクリプションを追加する

このタスクを完了するには、記事、[LCS プロジェクトに Azure サブスクリプションを追加する](resource-add-azure-subscription-lcs-project.md) の手順に従ってください。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>リソース/非在庫のシナリオの Project Operations で Finance デモ環境を展開する

記事、[新しい環境をプロビジョニングする](resource-provision-new-environment.md) のガイダンスに従って、展開を完了させます。 プレビューの[デモ環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) の展開の種類を使用します。 

## <a name="install-cds-setup-and-configuration-data"></a>CDS 設定および構成データをインストールする

記事、[Common Data Service で構成データを設定して適用する](resource-apply-pro-setup-config-data.md) の説明に従って、CDS のセットアップおよび構成データをインストールします。
この手順は、Finance のデモ環境がデプロイされ、デモデータの準備ができてから行ってください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
