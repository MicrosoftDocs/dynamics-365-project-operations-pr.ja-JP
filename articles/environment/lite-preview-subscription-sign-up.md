---
title: プレビューのサブスクリプションにサインアップする (ライト)
description: このトピックでは、Project Operations ライト デプロイメントの購読および展開方法に関する情報を提供します - 見積もり請求の取引を行います。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588006"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>プレビュー サブスクリプションにサインアップする (ライト) 

このトピックでは、試用版のオファーに登録し、Dynamics 365 Project Operations ライトのデプロイから、プロフォーマ請求書への対応を行う方法について説明します。

> [!NOTE]
> このプロセスは、Project Operations の今後のリリースで変更されます。

## <a name="prerequisites"></a>前提条件
- プレビューを展開するユーザーは、Azure テナント グローバル 管理者権限を持っている必要があります。 最初のオファーの引き換え時にテナントを作成できます。

> [!IMPORTANT]
> このタスクを実行する必要があるのは、組織内の 1 人のテナント管理者だけです。 このリリースのサブスクライバーでない場合は、組織がサインアップしてユーザー資格情報を受け取るまで待ちます。
> 
> 試用版はテナントでの単一回の使用となります。 試用版は 1 度しか実行できません。 試用版に特化した、新しいテナントを作成することをお勧めします。

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations 試用版 

開始する前に、Project Operations のプレビューが必要なテナントでユーザーの業務用アカウントを使用してブラウザーにログインしていることを確認してください。

1. [Project Operations 試用版](https://aka.ms/try-po)にアクセスし、**Dynamics 365 Project Operations** の最初のオファーコードを引き換えます。
2. 注文を確認します。

  オファーが正常に引き換えられたことを示す確認メッセージが表示されます。

## <a name="assign-licenses"></a>ライセンスの割り当て

> [!IMPORTANT]
> 次の手順を完了するためには、組織の Microsoft 365 のポータルへの管理アクセスが必要です。


1. [Microsoft 365 管理センター](https://portal.office.com/)にアクセスし、ユーザーにライセンスを割り当てます。
2. **アクティブ ユーザー** ページで、ライセンスを割り当てるユーザーを選択します。
3. **Dynamics 365 Project Operations** ライセンスが選択されていることを確認します。 
4. **変更を保存** を選択します。

## <a name="create-a-new-dataverse-environment"></a>Dataverse 環境を作成する

1. トピック [Dataverse デプロイ モデル](lite-deployment.md) の指示に従って、新しい Project Operations Dataverse デプロイ環境をプロビジョニングします。 環境タイプを選択するときは、**試用 (サブスクリプション ベース)** を必ず使用してください。

  ![新しい環境。](./media/19CreateEnvironment.png)

2. **Dynamics 365 アプリを有効にする** の設定を選択し、**これらのアプリを自動的に展開** を空白のままにします。  
3. **保存** を選択して、環境を作成します。

  ![データベースの追加。](./media/20CreateEnvironment1.png)

4. 環境が作成されたら、**Microsoft Dynamics 365 Project Operations** ソリューションをインストールします。 

![ソリューションのインストール。](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS コンフィグレーションをインストールし、デモ データを設定する

トピックの手順 [デモの設定および構成データを適用する](lite-apply-demo-setup-config-data.md) に従い、CDS 構成をインストールし、デモ データを設定します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
