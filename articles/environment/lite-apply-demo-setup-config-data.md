---
title: デモ設定および構成データを適用する
description: このトピックでは、Project Operations のデモ設定および構成データを適用する方法に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079133"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Project Operations ライト デプロイメントのデモ設定および構成データを適用します - プロフォーマ インボイスに対処

_**ライト デプロイメント - 見積もり請求の取引_

1. [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) をダウンロードします。 
2. フォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* に移動し、実行可能ファイル *DataMigrationUtility* を実行します。
3. Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、 **データのインポート** を選び、 **続行** を選択します。

![構成の移行](./media/1ConfigurationMigration.png)

4. CMT Wizard の 2 ページで、 **展開の種類** として **Microsoft 365** を選択します。
5. **利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。
6. テナントの地域を選択し、資格情報を入力してから、 **ログイン** を選択します。

![構成サイン イン](./media/2ConfigurationSignin.png)

7. 3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、 **ログイン** を選択します。
8. 4 ページで、解凍されたフォルダ *ProjOpsDemoDataSetupAndMaster - 統合 CMT* から、zip ファイル *MasterAndSetupData* を選択します。

![Zip ファイル](./media/3ZipFile.png)

![ファイルの選択](./media/4SelectAFile.png)

9. zip ファイルを選択したら、 **データのインポート** を選択します。

![データをインポート](./media/5ImportData.png)

10. インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。 完了後、CMT Wizard を終了します。 
11. 次の 20 エンティティのデータについて組織を確認してください。

- 通貨
- 組織単位
- 連絡先
- 税務グループ
- 顧客グループ
- 単位
- 出荷単位一覧 
- 価格表 
- プロジェクト パラメーター価格表
- 請求頻度
- 請求頻度の詳細
- 予約可能リソース カテゴリ
- トランザクション カテゴリ
- 経費カテゴリ
- ロール価格
- トランザクション カテゴリ価格
- 特性
- 予約可能リソース
- 予約可能リソース カテゴリ関連
- 予約可能リソースの特性

![インポートの完了](./media/6CompleteImport.png)
