---
title: デモ データを Finance クラウド ホスト環境に適用する
description: このトピックは、Project Operations からのデモ データを Dynamics 365 Finance のクラウド ホスト環境に適用する方法を説明しています。
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009672"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>デモ データを Finance クラウド ホスト環境に適用する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

> [!IMPORTANT]
> このトピックは Microsoft Dynamics 365 Finance バージョン 10.0.13 にのみ適用され、クラウド ホスト型環境でのみ実行できます。 環境に品質更新を適用する **前** に、このトピックの手順を完了します。

1. LCS プロジェクトで、**環境の詳細** ページを開きます。 リモート デスクトップ プロトコル (RDP) を使用して環境に接続するために必要な詳細が含まれていることに注意してください。

![環境の詳細。](./media/1EnvironmentDetails.png)

強調表示された資格情報の最初のセットはローカル アカウントの資格情報であり、リモート デスクトップ接続へのハイパーリンクが含まれています。 資格情報には、環境管理者のユーザー名とパスワードが含まれます。 2 番目の資格情報のセットは、この環境で SQL Server にログインするために使用されます。

2. **ローカル アカウント** のハイパーリンクで環境にリモート接続し、**ローカルアカウントの資格情報** を使用して認証します。
3. **インターネット インフォメーション サービス** > **アプリケーション プール** > **AOSService** に移動し、サービスを停止します。 この時点でサービスを停止しているので、SQL データベースの置き換えを続行できます。

![AOS の停止。](./media/2StopAOS.png)

4. **サービス** に移動し、次の 2 つの項目を停止します。

- Microsoft Dynamics 365 Unified Operations: バッチ管理サービス
- Microsoft Dynamics 365 Unified Operations: データのインポート/エクスポート フレームワーク

![サービスの停止。](./media/3StopServices.png)

5. Microsoft SQL Server Management Studio を開きます。 SQL サーバーの資格情報を使用してログインし、LCS **環境の詳細** ページの axdbadmin ユーザーとパスワードを使用します。

![SQL Server Management Studio。](./media/4SSMS.png)

6. オブジェクト エクスプローラーで、**データベース** を選択し、**AXDB** を見つけます。 データベースを、[ダウンロード センター](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) にある新しいデータベースに置き換えます。 
7. リモート先の VM に zip ファイルをコピーし、zip コンテンツを抽出します。
8. SQL Server Management Studio で、**AxDB** を右クリックし、次に **タスク** > **復元** > **データベース** を選択します。

![データベースの復元。](./media/5RestoreDatabase.png)

9. **ソース デバイス** を選択し、コピーした zip から抽出したファイルに移動します。

![ソース デバイス。](./media/6SourceDevice.png)

10. **オプション** を選択し、次に **既存のデータベースの上書き** と **宛先データベースへの既存の接続を閉じる** を選択します。 
11. **OK** を選択します。

![設定を復元。](./media/7RestoreSetting.png)

AXDB の復元が成功したという確認が表示されます。 この確認が表示された後、SQL Services Management Studio を閉じることができます。

12. **インターネット インフォメーション サービス** > **アプリケーション プール** > **AOSService** に戻り、AOSService を開始します。
13. **サービス** に移動し、以前に停止した 2 つのサービスを開始します。

14. この VM で AdminUserProvisioning ツールを見つけます。 K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe の下をご覧ください。
15. **電子メール アドレス** フィールドのユーザー アドレスを使用して .ext ファイルを実行します。 
16. **送信** を選択します。

![管理者ユーザー プロビジョニング。](./media/8AdminUserProvisioning.png)

これが完了するまでに数分かかります。 管理者ユーザーが正常に更新されたことを示す確認メッセージが表示されます。

17. 最後に、コマンド プロンプトを管理者として実行し、iisreset を実行します

![IIS リセット。](./media/9IISReset.png)

18. リモート デスクトップ セッションを閉じて、LCS **環境の詳細** ページを使用して環境にログインし、期待どおりに機能していることを確認します。

![Finance and Operations。](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]