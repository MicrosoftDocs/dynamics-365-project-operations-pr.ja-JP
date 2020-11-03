---
title: Project Operations の Common Data Service で構成データを設定し適用する
description: このトピックでは、Project Operations の構成データの設定と適用に関する情報を提供します。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079141"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Project Operations の Common Data Service で構成データを設定し適用する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

## <a name="install-setup-and-configuration-data"></a>設定および構成データをインストールする

1. [設定および構成データ パッケージ](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip) をダウンロード、ブロック解除および解凍します。
2. 解凍したフォルダに移動し、実行可能ファイル *DataMigrationUtility* を実行します。
3. Common Data Service 構成の移行 (CMT) ウィザードの 1 ページで、 **データのインポート** を選び、 **続行** を選択します。

![構成の移行](./media/1ConfigurationMigration.png)

4. CMT Wizard の 2 ページで、 **展開の種類** として **Microsoft 365** を選択します。
5. **利用可能な組織のリストを表示する** および **詳細の表示** チェック ボックスを選択します。
6. テナントの地域を選択し、資格情報を入力してから、 **ログイン** を選択します。

![構成サイン イン](./media/2ConfigurationSignin.png)

7. 3 ページで、テナントの組織リストから、デモ データをインポートする組織を選び、 **ログイン** を選択します。
8. 4 ページで、解凍されたフォルダから、zip ファイル *SampleSetupAndConfigData* を選択します。

![Zip ファイルの選択](./media/3ZipFile.png)

![ファイルの選択](./media/4SelectAFile.png)

9. zip ファイルを選択したら、 **データのインポート** を選択します。

![データの​​インポート](./media/5ImportData.png)

10. インポートは、ネットワーク速度にもよりますが、約 2 から 10分間実行されます。 インポートの完了後、CMT Wizard を終了します。 
11. 次の 19 エンティティのデータについて組織を確認してください。

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

## <a name="update-project-operations-configurations"></a>Project Operations 構成の更新

1. CE 環境に移動します。 [Power Platform 管理センター](https://admin.powerplatform.microsoft.com/environments) を開き、環境を選択してから、 **環境を開く** を選択すると、見つかります。 

![環境を開く](./media/7OpenEnvironment.png)

2. **プロジェクト** > **リソース** に移動し、次に **新規** を選択して、ユーザーの予約可能なリソースを作成します。

![予約可能リソース](./media/8BookableResources.png)

3. **全般** タブで、管理者ユーザーを選択します。 タイム ゾーンが現在のタイム ゾーンと一致していることを確認します。 

![新規予約可能リソース](./media/9NewBookableResource.png)

4. **スケジュール設定** タブの、 **会社** フィールドで、 **USPM** 会社を選び、 **保存** を選択します。 

![スケジュール タブ](./media/10SchedulingTab.png)

5. **作業時間** タブを選択します。  

![作業時間](./media/11WorkHours.png)

6. カレンダーの任意の値をダブルクリックして、 **編集** > **シリーズのすべてのイベント** を選択します。 

![作業カレンダー](./media/12WorkCalendar.png)

7. 作業時間を 8 時間作業日に変更し、週末を非作業日としてマークし、タイム ゾーンが自分のタイム ゾーンと一致することを確認します。 
8. **保存して閉じる** を選択します。

![カレンダーの更新](./media/13UpdateCalendar.png)

9. **設定** > **カレンダー テンプレート** に移動し、 **新規** を選択します。
 
 ![カレンダー テンプレート](./media/14CalendarTemplates.png)
 
 10. 名前を入力し、作成したテンプレート リソースを選択してから、 **保存** を選択します。 
 
 ![カレンダー テンプレートの保存](./media/15SaveCalendarTemplate.png)
 
 11. **パラメーター** に移動し、レコードをダブルクリックします。 
 
 ![プロジェクト パラメーター](./media/16ProjectParameters.png)
 
12. 次のフィールドを更新します。

 - **既定の会社** : USPM
 - **既定のの組織単位** : Contoso Robotics Global
 - **請求書の頻度** : 7日目と最終日
 - **作業時間テンプレート** : 作成したテンプレートに変更します。

13. **保存** を選択します。 

![更新されるプロジェクト パラメーター](./media/17UpdatedProjectParameters.png)
