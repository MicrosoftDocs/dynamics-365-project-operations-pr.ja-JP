---
title: デモのセットアップと構成データを適用する (ライト)
description: この記事では、Project Operations のデモのセットアップと設定データを適用する方法について説明します。
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811031"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operations に向けたデモの設定と構成データを適用する (ライト) 

_**ライト デプロイメント - 見積もり請求の取引_



## <a name="prerequisites"></a>前提条件

構成を開始する前に、Dynamics 365 Project Operations 用にプロビジョニングされた Dataverse 環境が必要です。


## <a name="instructions"></a>方法

1. [設定データ パッケージ](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) をダウンロードします。 
1. フォルダー *ProjOpsSampleSetupData - CE のみの CMT* に移動し、実行可能ファイル *DataMigrationUtility* を実行します。
1. Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、**データのインポート** を選び、**続行** を選択します。

    ![構成の移行。](./media/1ConfigurationMigration.png)

1. CMT Wizard の 2 ページで、**展開の種類** として **Microsoft 365** を選択します。
1. **利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。
1. テナントの地域を選択し、資格情報を入力してから、**ログイン** を選択します。

   ![構成サインイン。](./media/2ConfigurationSignin.png)

1. 3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、**ログイン** を選択します。
1. 4 ページ目で zip ファイル *SampleSetupAndConfigData* を、解凍したフォルダ *ProjOpsSampleSetupData - CE のみの CMT* から選択します。

   ![Zip ファイル。](./media/3ZipFile.png)

   ![ファイルを選択します。](./media/4SelectAFile.png)

1. zip ファイルを選択したら、**データのインポート** を選択します。

   ![インポート データ。](./media/5ImportData.png)

1. インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。 完了後、CMT Wizard を終了します。 
1. 次の 18 エンティティのデータについて組織を確認してください。

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
