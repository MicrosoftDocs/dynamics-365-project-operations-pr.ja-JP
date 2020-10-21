---
title: 新しい環境をプロビジョニングする
description: このトピックは、新しい Project Operations 環境でプロビジョニングする方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949368"
---
# <a name="provision-a-new-environment"></a>新しい環境をプロビジョニングする

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、リソース/非在庫ベースのシナリオ用に新しい Dynamics 365 Project Operations をプロビジョニングする方法について説明します。

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>LCS プロジェクトで Project Operations の自動プロビジョニングを有効にします

次の手順を使用して、LCS プロジェクトの ProjectOperations の自動プロビジョニング フローを有効にします。

1. [LCS](https://lcs.dynamics.com/v2) に移動し、**プレビュー機能の管理**タイルを選択します。
2. **プレビュー機能**リストで、**Project Operations**を選択し、Project Operations を有効にするために**プレビュー機能の有効**を選択します。

> [!NOTE]
> このステップは、LCS プロジェクトごとに 1 回だけ実行されます。

## <a name="provision-a-project-operations-environment"></a>Project Operations 環境をプロビジョニングする

1. 新しい Dynamics 365 Finance[デモ環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) または[サンドボックス/運用環境](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) の展開を開きます。 
2. **環境プロビジョニング** ウィザードを検証します。 

> [!IMPORTANT]
> 選択したアプリケーションのバージョンが 10.0.13 以降であることを確認してください。

3. Project Operations をプロビジョニングするには、**詳細設定**で、**Common Data Service** を選択します。 
4. **はい**を選択して **Common Data Service 設定**を有効にし、必須項目フィールドに情報を入力します。

  - 件名
  - リージョン
  - 言語
  - 通貨
 
5. **Common Data Service テンプレート** フィールドで、**Project Operations** を選択します 

6. 展開の環境タイプを選択します。 サブスクリプション ベースのトライアルでは、CDS 環境を 30 日間展開できます。 

![展開の設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> **同意する**を選択して利用規約サービスの利用条件を確認し、**完了**を選択して展開の設定に戻ります。

![展開の同意](./media/2DeploymentConsent.png)

7. ウィザードの残りの必須フィールドを完了し、展開を確認します。 環境プロビジョニングの時間は、環境タイプによって異なります。 プロビジョニングには最大 6 時間かかる場合があります。

  展開が正常に完了すると、環境は**展開**として表示されます。

8. 環境が正常に展開されたことを確認するには、**ログイン**を選択し、確認のために環境にログオンします。

![ 環境の詳細](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance のデモ データを適用する (オプションのステップ)

[この記事](resource-apply-finance-demo-data.md) で説明されているように、Project Operations Finance のデモ データを10.0.13 サービス リリースのクラウド ホスト環境に適用します。

## <a name="apply-updates-to-the-finance-environment"></a>Finance 環境に更新を適用する

Project Operations には、**10.0.13 (10.0.569.20009)** 以上のアプリケーション バージョンを備えた Finance 環境が必要です。

このバージョンを受け取るには、Finance 環境に品質更新を適用する必要がある場合があります。

1. LCS では、**環境の詳細**ページの、**利用可能な更新**セクションで、**更新の表示**を選択します。

![ビューの更新](./media/5ViewUpdates.png)

2. **バイナリ更新**ページで、**パッケージの保存**を選択します。

![パッケージの保存](./media/6SavePackage.png)

3. **すべて選択**をクリックし、**パッケージの保存**を選択します。

![レビューと更新の保存](./media/7ReviewAndSaveUpdates.png)

4. パッケージの名前と説明を入力し、**保存**を選択します。 インターネット接続によっては、このプロセスに時間がかかる場合があります。

![パッケージを資産ライブラリにアップロード](./media/8UploadPackageToAssetsLibrary.png)

5. パッケージが保存されたら、**完了**を選択し、このパッケージを LCS プロジェクトの資産ライブラリに保存します。

パッケージの保存と検証には 15 分ほどかかる場合があります。

6. 更新を適用するには、LCS の**環境の詳細**ページで、**メンテナンス** > **更新の適用**を選択します。

![環境のメンテナンス](./media/9MaintainEnvironment.png)

7. 更新リストで、作成したパッケージを選択し、**適用**を選択します。

![更新の適用する](./media/10ApplyUpdates.png)

環境サービスには時間がかかります。 完了すると、環境は展開された状態に戻ります。

![展開された環境](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>二重書き込み接続の確立 

1. LCS プロジェクトで、**環境の詳細**ページに移動します。
2. **Common Data Service 環境情報**で、**アプリの CDS へのリンク**を選択します。
3. リンクが完了したら、もう一度**アプリの CDS へのリンク**を選択します。 Finance の二重書き込みにリダイレクトされます。

![CDS にリンク](./media/12LinktoCDS.png)

4. **ソリューションの適用**を選択し、統合でマップされるエンティティにアクセスします。

![ソリューションを適用する](./media/13ApplySolutions.png)

5. **Dynamics 365 Finance and Operations 二重書き込みエンティティ マップ**と **Dynamics 365 Project Operations 二重書き込みエンティティ マップ**の両方を選択し、次に**適用**を選択します。

![ソリューションの確認](./media/14ConfirmSolutions.png)

ソリューションが適用された後、二重書き込みエンティティが環境に適用されます。

![ソリューションの適用](./media/15ApplyingSolutions.png)

エンティティが適用されると、使用可能なすべてのマッピングが環境に一覧表示されます。

![二重書き込みマップ](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>更新後にデータ エンティティを最新の情報に更新

1. Finance で、**データ管理**ワークスペースに移動します。

![データ管理のワークスペース](./media/16DataManagement.png)

2. **フレームワーク パラメータ** タイルを選択します。

![フレームワーク パラメータ](./media/17FrameworkParameters.png)

3. **エンティティ設定**ページで、**エンティティ　リストを最新の情報に更新**を選択します。

![エンティティ リストを最新の情報に更新](./media/18RefreshEntityList.png)

最新の情報に更新するには約 20 分かかります。 完了するとアラート通知が表示されます。

![最新の情報に更新を確認](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Project Operations の二重書き込みマップを実行する

1. LCS プロジェクトで、**環境の詳細**ページに移動します。
2. **Common Data Service 環境情報**で、**アプリの CDS へのリンク**を選択します。 リンクを選択すると、マッピングでエンティティのリストにリダイレクトされます。
3. 次の表の説明に従って、マップを開始します。 記載されている順序に従ってください。

| **エンティティ マップ** | **エンティティを最新の情報に更新** | **初期同期** | **初期同期のマスター** | **前提条件の実行** | **前提条件の初期同期** |
| --- | --- | --- | --- | --- | --- |
| **すべての会社のプロジェクト リソース ロール (bookableresourcecategories)** | 無効 | 有効 | Common Data Service | 無効 | N\A |
| **法人 (cdm\_companies)** | 無効 | 有効 | Finance and Operations アプリ | 無効 | N\A |
| **Project Operations 統合実績 (msdyn\_actuals)** | 無効 | 無効 | N\A | 有効 | 無効 |
| **プロジェクト 契約品目 (salesorderdetails)** | 無効 | 無効 | N\A | 無効 | 無効 |
| **プロジェクト トランザクションの関連付けにおける統合エンティティ (msdyn\_transactionconnections)** | 無効 | 無効 | N\A | 無効 | N\A |
| **Project Operations 統合契約品目のマイルストーン (msdyn\_contractlinesscheduleofvalues)** | 無効 | 無効 | N\A | 無効 | N\A |
| **経費見積もりのための Project Operations 統合エンティティ (msdyn\_estimateslines)** | 無効 | 無効 | N\A | 無効 | N\A |
| **時間見積もりのための Project Operations 統合エンティティ (msdyn\_resourceassignments)** | 無効 | 無効 | N\A | 無効 | N\A |
| **Project Operations 統合プロジェクト経費エクスポート エンティティ (msdyn\_expenses)** | 有効 | 無効 | N\A | 無効 | N\A |
| **時間見積もりのための Project Operations 統合エンティティ (msdyn\_resourceassignments)** | 有効 | 無効 | N\A | 無効 | N\A |

4. エンティティを最新の情報に更新するには、マップ名を選択してから、**エンティティを最新の状態に更新**を選択します。 
5. 最新の情報に更新が完了したら、マップの実行に進みます。

![マップを最新の情報に更新](./media/20RefreshMapping.png)

次のマップを有効にする前に、テーブル内のマップが**実行**の状態にあることを確認してください。 前提条件の数が多いマップの実行には、時間がかかる場合があります。

前提条件を使用してマップを実行するには、**関連するエンティティ マップの表示**切り替えを有効にします。 テーブルに**前提条件の初期同期**が**いいえ**を示している場合、実行する前に、すべての前提条件マップで**初期同期**フラグが**オフ**であることを確認してください。

![マップを実行](./media/21RunMap.png)

6. プロジェクトに関連するすべてのマップが実行状態にあることを検証します。

![実行中のすべてのマップ](./media/22AllMapsRunning.png)

これで、Project Operations環境がプロビジョニングおよび構成されました。
