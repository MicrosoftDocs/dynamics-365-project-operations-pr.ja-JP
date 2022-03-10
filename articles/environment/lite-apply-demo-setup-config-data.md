---
title: デモのセットアップと構成データを適用する (ライト)
description: このトピックでは、Project Operations のデモ設定および構成データを適用する方法に関する情報を提供します。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e25d358f1fd7705d580855d372d85690f6a5e265d3ba2b60fc26742bf3edc86f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993292"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operations に向けたデモの設定と構成データを適用する (ライト) 

_**ライト デプロイメント - 見積もり請求の取引_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>前提条件

構成を開始する前に、Dynamics 365 Project Operations 用にプロビジョニングされた Common Data Service (CDS) 環境が必要になります。


## <a name="instructions"></a>方法

1. [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) をダウンロードします。 
2. フォルダー *ProjOpsSampleSetupData - CE のみの CMT* に移動し、実行可能ファイル *DataMigrationUtility* を実行します。
3. Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、**データのインポート** を選び、**続行** を選択します。

    ![構成の移行。](./media/1ConfigurationMigration.png)

4. CMT Wizard の 2 ページで、**展開の種類** として **Microsoft 365** を選択します。
5. **利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。
6. テナントの地域を選択し、資格情報を入力してから、**ログイン** を選択します。

   ![構成サインイン。](./media/2ConfigurationSignin.png)

7. 3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、**ログイン** を選択します。
8. 4 ページ目で zip ファイル *SampleSetupAndConfigData* を、解凍したフォルダ *ProjOpsSampleSetupData - CE のみの CMT* から選択します。

   ![Zip ファイル。](./media/3ZipFile.png)

   ![ファイルを選択します。](./media/4SelectAFile.png)

9. zip ファイルを選択したら、**データのインポート** を選択します。

   ![インポート データ。](./media/5ImportData.png)

10. インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。 完了後、CMT Wizard を終了します。 
11. 次の 18 エンティティのデータについて組織を確認してください。

    -   通貨
    -   アカウント
    -   組織単位
    -   連絡先
    -   単位
    -   出荷単位一覧 
    -   価格表 
    -   プロジェクト パラメーター価格表 
    -   請求頻度
    -   予約可能リソース カテゴリ
    -   トランザクション カテゴリ
    -   経費カテゴリ
    -   ロール価格
    -   トランザクション カテゴリ価格
    -   特性
    -   予約可能リソース
    -   予約可能リソース カテゴリ関連
    -   予約可能リソースの特性

    ![インポートの完了。](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
