---
title: 新しい環境をプロビジョニングする
description: このトピックは、新しい Project Operations 環境でプロビジョニングする方法について説明します。
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7f63b144b6fe3eb848d0c303b64237516a97cb56
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501422"
---
# <a name="provision-a-new-environment"></a>新しい環境をプロビジョニングする

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、リソース/非在庫ベースのシナリオについて Dynamics 365 Project Operations の新しい環境をプロビジョニングする方法を説明します。

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>LCS プロジェクトで Project Operations の自動プロビジョニングを有効にします

次の手順を使用して、LCS プロジェクトの ProjectOperations の自動プロビジョニング フローを有効にします。

1. [LCS](https://lcs.dynamics.com/v2) に移動し、**プレビュー機能の管理** タイルを選択します。
2. **プレビュー機能** リストで、**Project Operations** 機能を選択し、Project Operations を有効にするために **プレビュー機能を有効する** を選択します。

   > [!NOTE]
   > このステップは、LCS プロジェクトごとに 1 回だけ実行されます。

## <a name="provision-a-project-operations-environment"></a>Project Operations 環境をプロビジョニングする

1. 新しい Dynamics 365 Finance[デモ環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) または[サンドボックス/運用環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) の展開を開きます。 
2. **環境プロビジョニング** ウィザードを検証します。 

   > [!IMPORTANT]
   > 選択したアプリケーションのバージョンが 10.0.13 以降であることを確認してください。

3. Project Operations をプロビジョニングするには、**詳細設定** で、**Common Data Service** を選択します。 
4. **はい** を選択して **Common Data Service 設定** を有効にし、必須項目フィールドに情報を入力します。

  - 件名
  - リージョン
  - 言語
  - 通貨
 
5. **Common Data Service テンプレート** フィールドで、**Project Operations** を選択します 
6. 展開の環境タイプを選択します。 サブスクリプション ベースのトライアルでは、CDS 環境を 30 日間展開できます。 

     ![展開の設定。](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > **同意する** を選択して利用規約サービスの利用条件を確認し、**完了** を選択して展開の設定に戻ります。
    >
    >![展開の同意。](./media/2DeploymentConsent.png)

7. オプション - デモ データを環境に適用します。 **高度な設定** に移動して、**SQL データベース構成のカスタマイズ** を選択して、**アプリケーション データベースにデータセットを指定する** を **デモ** に設定します。
8. ウィザードの残りの必須フィールドを完了し、展開を確認します。 環境をプロビジョニングする時間は、環境の種類によって異なります。 プロビジョニングには最大 6 時間かかる場合があります。

   展開が正常に完了すると、環境は **展開** として表示されます。

9. 環境が正常に展開されたことを確認するには、**ログイン** を選択して、確認のために環境にログオンします。

    ![環境の詳細。](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Finance 環境に更新を適用する

Project Operations には、**10.0.13 (10.0.569.20009)** 以上のアプリケーション バージョンを備えた Finance 環境が必要です。

このバージョンを受け取るには、Finance 環境に品質更新を適用する必要がある場合があります。

1. LCS では、**環境の詳細** ページの、**利用可能な更新** セクションで、**更新の表示** を選択します。

    ![ビューの更新。](./media/5ViewUpdates.png)

2. **バイナリ更新** ページで、**パッケージの保存** を選択します。

    ![パッケージの保存。](./media/6SavePackage.png)

3. **すべて選択** をクリックし、**パッケージの保存** を選択します。

    ![更新をレビューして保存。](./media/7ReviewAndSaveUpdates.png)

4. パッケージの名前と説明を入力し、**保存** を選択します。 インターネット接続によっては、このプロセスに時間がかかる場合があります。

    ![パッケージを資産ライブラリにアップロード。](./media/8UploadPackageToAssetsLibrary.png)

5. パッケージが保存されたら、**完了** を選択し、このパッケージを LCS プロジェクトの資産ライブラリに保存します。

   パッケージの保存と検証には 15 分ほどかかる場合があります。

6. 更新を適用するには、LCS の **環境の詳細** ページで、**メンテナンス** > **更新の適用** を選択します。

    ![環境のメンテナンス。](./media/9MaintainEnvironment.png)

7. 更新リストで、作成したパッケージを選択し、**適用** を選択します。

    ![更新を適用する。](./media/10ApplyUpdates.png)

   環境サービスには時間がかかります。 完了すると、環境は展開された状態に戻ります。

    ![展開された環境。](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>二重書き込み接続の確立 

1. LCS プロジェクトで、**環境の詳細** ページに移動します。
2. **Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。
3. リンクが完了したら、もう一度 **アプリの CDS へのリンク** を選択します。 Finance の二重書き込みにリダイレクトされます。

    ![CDS にリンク。](./media/12LinktoCDS.png)

4. **ソリューションの適用** を選択し、統合でマップされるエンティティにアクセスします。

    ![ソリューションを適用する。](./media/13ApplySolutions.png)

5. **Dynamics 365 Finance and Operations 二重書き込みエンティティ マップ** と **Dynamics 365 Project Operations 二重書き込みエンティティ マップ** のソリューションを両方選択してから **適用** を選択します。

    ![ソリューションの確認。](./media/14ConfirmSolutions.png)

    ソリューションが適用された後、二重書き込みエンティティが環境に適用されます。

    ![ソリューションの適用。](./media/15ApplyingSolutions.png)

    エンティティが適用されると、使用可能なすべてのマッピングが環境に一覧表示されます。

    ![二重書き込みマップ。](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>更新後にデータ エンティティを最新の情報に更新

1. Finance で、**データ管理** ワークスペースに移動します。

    ![データ管理のワークスペース。](./media/16DataManagement.png)

2. **フレームワーク パラメータ** タイルを選択します。

    ![フレームワーク パラメーター。](./media/17FrameworkParameters.png)

3. **エンティティ設定** ページで、**エンティティ　リストを最新の情報に更新** を選択します。

    ![エンティティ リストを最新の情報に更新。](./media/18RefreshEntityList.png)

最新の情報に更新するには約 20 分かかります。 完了するとアラート通知が表示されます。

  ![確認を最新の情報に更新する。](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Dataverse 上の Project Operations のセキュリティ設定を更新する

1. Dataverse 環境で Project Operations に移動します。 
2. **設定** >  **セキュリティ** > **セキュリティ ロール** へ移動します。 
3. **セキュリティ ロール** ページのロールのリストで、**二重書き込みアプリ ユーザー** を選択してから、**カスタム エンティティ** タブを選択します。  
4. 役割が次のエンティティに対して、**読込み** と **追加先** のアクセス許可を持っていることを確認します:
      
      - **通貨為替レートのタイプ**
      - **勘定科目表**
      - **会計カレンダー**
      - **Ledger**
      - **会社**
      - **通貨為替レートのタイプ**
      - **経費**

5. セキュリティ ロールが更新されたら、**設定** > **セキュリティ** > **チーム** に移動し、**ローカル ビジネス オーナー** チーム ビューで既定のチームを選択します。
6. **ロールの管理** を選択して、**二重書き込みアプリ ユーザー** のセキュリティ特権がこのチームに適用されることを確認します。

## <a name="run-project-operations-dual-write-maps"></a>Project Operations の二重書き込みマップを実行する

1. LCS プロジェクトで、**環境の詳細** ページに移動します。
2. **Common Data Service 環境情報** で、**アプリの CDS へのリンク** を選択します。 リンクを選択すると、マッピングでエンティティのリストにリダイレクトされます。
3. マップを開始します。 詳細については、[Project Operations 二重書き込みマップ バージョン](resource-dual-write-maps.md#project-operations-dual-write-maps) を参照してください
4. プロジェクトに関連するすべてのマップが実行状態にあることを検証します。

    ![実行中のすべてのマップ。](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Project Operations 用の CDS で構成データを適用する (オプション)

Finance 環境にデモ データを適用した場合は、デモ データを CD S環境に適用するために [Project Operations 用の Common Data Service で構成データの設定と適用](resource-apply-pro-setup-config-data.md) を参照してください。


これで、Project Operations環境がプロビジョニングおよび構成されました。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
