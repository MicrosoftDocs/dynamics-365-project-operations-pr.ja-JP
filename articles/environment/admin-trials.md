---
title: Project Operations の試用版にサインアップする
description: このトピックは、Dynamics 365 Project Operations の試用版をデプロイする方法に関する情報を提供します。
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418463"
---
# <a name="sign-up-for-project-operations-trials"></a>Project Operations の試用版にサインアップする 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations、Lite 展開 - 見積もり請求の取引、在庫/製造ベースのシナリオ向け Project Operations_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックは、プレビュー パートナー オファーにサブスクライブして Dynamics 365 Project Operations 環境を展開する方法を説明しています。

新しい Project Operations 試用版では、最適な展開アプローチを推奨するアンケートに回答することで、サポートされている 3 つの展開シナリオのいずれかを自動的に展開できます。 このトピックでは、以下の方法について説明します。

- 試用版オファーを引き換える。
- プロビジョニングを開始する。
- 二重書き込みを構成する。
- Project Operations の詳細を確認する。 

次の表に、新しい試用版オファーの詳細の概要を示します。

| **オファー アイテム**               | **詳細情報**                                  |
|------------------------------|----------------------------------------------|
| オファーの種類                   | このオファー タイプは管理者リードであるため、引き換えるにはテナント管理者が必要です。 |
| オファーの使用                    | テナントごとに 1 回                          |
| オファー期間               | 30 暦日                             |
| テナントごとの引き換え       | 6                                            |
| ユーザー数              | 25                                           |
| 拡張                    | 1 回の延長、30 暦日               |
| 試用版環境の数 | 3                                            |


## <a name="admin-trial-details"></a>管理者試用版の詳細
次の表に、試用版の詳細と、それらが各展開タイプにどのように適用されるかを示します。

| **品目**                      | **ライト**                                     | **非在庫材料** | **在庫材料** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| 提供されるセットアップ データ           | 有効                                          | 有効                       | はい (USSI)            |
| トランザクション データ            | 無効                                           | 無効                        | 無効                    |
| プロビジョニング時間 (分)  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>前提条件
Dynamics 365 Project Operations の試用版を展開するには、次の前提条件が必要です。

- [Dynamics 365 Project Operations - プレビュー試用版](https://www.aka.ms/try-po)にサインアップします。
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人、つまりテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - プレビュー試用版 

開始する前に、Project Operations のプレビューが必要なテナントのユーザー職場アカウントを使用してブラウザーにログインします。

1. ブラウザの URL 欄に貼り付けて最初のオファー コード **Dynamics 365 Project Operations - プレビュー試用版** を引き換えます。

    ![オファーの引き換え](./media/16RedeemFirstOfferNew.png)

2. 注文を確認します。

    ![注文を確認する](./media/17ConfirmOrderNew.png)

  オファーが正常に引き換えられたことを示す確認メッセージが表示されます。

   ![確認](./media/18OrderConfirmationNew.png)

  [Power Platform 管理センター](https://admin.powerplatform.microsoft.com/projectoperationstrial)にリダイレクトされます。

## <a name="questionnaire-and-provisioning"></a>アンケートとプロビジョニング

1.  [Power Platform 管理センター](https://admin.powerplatform.com/projectoperationstrial)に移動し、アンケートに記入します。  
2.  推奨される展開タイプを確認し、**セットアップの開始** を選択してプロビジョニングを開始します。
3.  利用条件を確認し、**開始** を選択します。

   プロビジョニングが開始されると、Power Platform 管理センターの環境リストにリダイレクトされます。 プロビジョニングの進行中、環境の状態は **PreparingInstance** になります。
 
  プロビジョニングが完了すると、環境の状態は **準備完了** になります。
 
4.  プロビジョニングが完了したら、対応する Microsoft Dataverse URL と Finance and Operations アプリ URL を選択して展開を検証します。

## <a name="demo-data-installation"></a>デモ データのインストール

次のリンクを使用して、非在庫材料とライト展開シナリオの両方のデモ データ パッケージにアクセスします。 
- [非在庫材料デモ データ](resource-apply-pro-setup-config-data.md)
- [ライト デモ データ](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>二重書き込みの構成
非在庫材料の展開の場合のみ、二重書き込みマッピングを構成します。 詳細については、[Project Operations 二重書き込みマップ バージョン](resource-dual-write-maps.md)を参照してください。

## <a name="assign-licenses"></a>ライセンスの割り当て

次の手順を完了するには、組織の Microsoft 365 ポータルへの管理アクセスが必要です。

1. [Microsoft 365 管理センター](https://portal.office.com/)に移動して、ライセンスをユーザーに割り当てます。

   ![管理センター ホーム ページ](./media/14AdminPortal.png)

2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。

   ![ライセンスの割り当て](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations プレビュー** のライセンスが選択されていることを確認し、**変更を保存** を選択します。

## <a name="additional-resources"></a>追加リソース

次のリソースは、Project Operations の体験を始める際に役立つガイダンスを提供します。

- [ビデオ シリーズ - Project Operations の概要、機能の詳細とロードマップ](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [展開の種類を決定する](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Finance and Operations アプリ環境に ALM または ELM が必要な場合はどうなりますか?

- 完全な環境ライフサイクル管理機能を必要とするパートナーの場合、[パートナー サンドボックス ライセンス リクエスト](https://experience.dynamics.com/requestlicense)を参照して、新しいパートナー オファーを確認します。 
- 内部使用権の詳細をお求めのパートナーの場合、[内部使用権クラウドおよびソフトウェアのメリット (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software) を参照してください。

### <a name="can-i-extend-my-trial-beyond-30-days"></a>試用期間を 30 日超に延長できますか?
試用期間を延長するには、次の手順を実行します。

1. **Microsoft 365 管理センター** で **請求** > **製品** に移動します。
2. **Dynamics 365 Project Operations (CE) - プレビュー試用版** を選択します。
3. **有効期限** で、**日付の延長** を選択します。

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>ライト展開からリソース/非在庫ベースのシナリオ展開にアップグレードできますか?
現在、環境をライトベースの展開から非在庫ベースの展開にアップグレードするためのサポートはありません。

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Finance 環境の Lifecycle Services (LCS) にアクセスできますか?  
番号 これらの試用版では、展開は Power Platform 管理センターを通じて処理されます。 Finance 環境へのアクセスは制限されています。

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>試用版を既存の環境にインストールできますか?
既存の環境がある場合、Power Platform 管理センターから既存の営業 Dataverse 環境にライト展開をインストールできます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]