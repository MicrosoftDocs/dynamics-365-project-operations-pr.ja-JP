---
title: Finance 環境で Project Operations を更新する
description: この記事は、Dynamics 365 Finance 環境で Project Operations を更新する方法について説明します。
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030041"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Finance 環境で Project Operations を更新する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_


この記事は、Dynamics 365 Finance 環境で Dynamics 365 Project Operations を更新する方法について説明します。 Project Operationsを Update 5 (UR5) に更新するために必要な手順は 3 つあります。

- [パッケージをプレビュー プロジェクトにインポートする](#import)
- [更新プログラムを適用する](#apply)
- [Dataverse 環境を更新する](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>パッケージを LCS プロジェクトにインポートする

1. [Lifecycle Services (LCS)](https://lcs.dynamics.com/) にプロジェクト オーナーまたは環境マネージャーとしてログインします。
2. プロジェクトのリストから、LCS プロジェクトを選択します。
3. **プロジェクト** ページの **環境** グループで、更新する環境を開きます。
4. 環境が実行されていることを確認します。 起動していない場合は、環境を起動してください。
5. **利用可能な更新プログラム** の **新しいリリース** 下のセクションで、 10.0.15 に対する **更新の表示** を選択します。

![[更新] ボタンを表示する。](media/view-update.png)

6. **バイナリ更新** ページで、**パッケージの保存** を選択します。
7. **更新のレビューと保存** ページで、**パッケージの保存** を選択します。
8. **パッケージをアセット ライブラリに保存** ペインが表示されたら、名前を入力し、**パッケージの保存** を選択します。
9. LCS がパッケージの保存を完了すると、**完了** ボタンが有効になります。 **完了** を選択します。 LCS がパッケージを検証します。 確認には数分から最大 1 時間かかる場合があります。


## <a name="apply-the-package-update"></a><a name="apply"></a>パッケージ更新プログラムを適用する

1. LCS の **環境の詳細** ページで、**メンテナンス** > **更新プログラムの適用** を選択します。
2. リストから、前に保存したパッケージを選択してから、**適用** を選択します。
3. **はい** をクリックして、パッケージを展開することを確認します。

![パッケージ展開ダイアログ ボックスを確認する。](media/confirm-package-deployment.png)

4. **はい** をクリックして、アプリケーションを更新することを確認します。

![アプリケーションの更新ダイアログ ボックスを確認する。](media/confirm-application-update.png)

展開とアプリケーションの更新が開始されます。 

**環境の詳細** ページの右上隅に、環境ステータスが **サービス提供中** に更新されます。 約 2 時間で、更新が完了します。 アプリケーション リリース情報は **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** に更新され、環境ステータスは **展開済み** に更新されます。


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Dataverse 環境を更新する

1. [Power Platform 管理センター](https://admin.powerplatform.com/) にサインインします。
2. リストで、Project Operations のインストールに使用した環境を見つけて開きます。
3. **環境** ページで、**リソース** > **Dynamics 365アプリ** を選択します。
4. リストで、**Microsoft Dynamics 365 Project Operations** を探し、**ステータス** 列で、**利用可能な更新があります** を選択します。
5. **サービス利用条件に同意する** チェック ボックスをオンにして、**更新** を選択します。 ソリューションの最新バージョンがインストールされます。

インストールが完了すると、バージョン 4.5.0.134 がインストールされた状態になります。

## <a name="configure-new-features"></a>新機能の構成

### <a name="enable-dual-write-mapping"></a>二重書き込みマッピングを有効にする

Finance と Dataverse 環境で更新を完了した後、必要な二重書き込みマッピングを有効にできます。 次の手順で、二重書き込みマッピングを有効にします。

- [Customer Engagement 環境のセキュリティ設定を更新する](#security)
- [更新エンティティを更新する](#refresh)
- [二重書き込みマッピングを更新して実行する](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Dataverse 環境のセキュリティ設定を更新する

UR5 の更新の一部として、エンティティのセキュリティ権限に対する次の更新が必要です。

1. Dataverse 環境で、**設定** に移動し、**システム** グループで **セキュリティ** を選択します。

![Dataverse 環境の設定。](media/Picture21.png)

2. **セキュリティ ロール** を選択します。
3. ロール リストから、**二重書き込みアプリ ユーザー** を選択してから、**カスタム エンティティ** タブを選択します。 
4. ロールに、次の **読み込み** と **追加先** 権限があることを確認します。

      - **通貨為替レートのタイプ**
      - **勘定科目表** 
      - **会計カレンダー** 
      - **Ledger**

5. セキュリティ ロールが更新されたら、**設定** > **セキュリティ** > **チーム** に移動します。 **二重書き込みアプリ ユーザー** ロールがチームに適用されたことを確認します。 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>更新からデータ エンティティを更新します

1. Finance 環境で、**データ管理** ワークスペースを開き、**フレームワーク パラメーター** ページを開きます。
2. **エンティティ設定** タブで、**エンティティ リストの更新** を選択します。
3. **閉じる** を選択して、エンティティの更新を確認します。

 > [!NOTE]
 > このプロセスが完了するまでに、約 20 分かかります。 更新が完了すると通知されます。

### <a name="update-dual-write-mappings"></a><a name="run"></a>二重書き込みマッピングを更新する

1. **データ管理** ワークスペースで、**二重書き込み** を選択します。
2. **ソリューションを適用する** を選択して、リストから両方のソリューションを選択してから、**適用** を選択します。
3. **二重書き込み** ページで、次のテーブル マップを選択してから、**停止** を選択します。

    - **Project Operations 統合実績 (msdyn_actuals)**
    - **Project Operations 統合プロジェクト経費カテゴリ (msdyn_expensecategories)**
    - **Project Operations 統合実績プロジェクト経費カテゴリのエクスポート エンティティ (msdyn_expense)**

4. **テーブル マップ バージョン** ページで、3 つのエンティティのそれぞれに新しいバージョンのマップを適用します。
5. **二重書き込み** ページで、実行を選択してマップを再起動します。
6. マップのリストから、すべての前提条件を満たす **元帳 (msdyn_ledgers)** マップを選択し、**初期同期** チェック ボックスをオンにします。 
7. **初期同期のマスター** フィールドで、**財務と運用アプリ** を選択してから、**実行** を選択します。
 
 ![台帳マップの同期。](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]