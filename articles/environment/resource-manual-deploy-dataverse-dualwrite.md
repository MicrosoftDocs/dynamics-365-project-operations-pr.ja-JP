---
title: デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする
description: このトピックは、デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする方法について説明します。
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591226"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>デュアル書き込みに対応する Project Operations の Dataverse アプリを手動でデプロイする

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、デュアル書き込みに対応する Microsoft Dataverse の Microsoft Dynamics 365 Project Operations を手動でデプロイする方法について説明します。 Project Operations は、環境の構成を検出し、前提条件が満たされていれば、デュアル書き込みの対応を追加します。

Microsoft Dynamics Lifecycle Services (LCS) によるデプロイメントの際は、このトピックで説明する手順を使用することで、Microsoft Power Platform 統合 (旧名 Common Data Service 環境) のデプロイを省略できます。

Dataverse に Project Operations を展開してデュアル書き込みに対応させるには、大きく分けて 4 つのステップがあります:

1. [Dataverse でデュアル書き込みに対応した新しい環境を作る](#create)。
2. [デュアル書き込みの前提条件を環境に追加する](#prerequisites)。
3. [Project Operations Dataverse アプリを追加する](#dataverse)。
4. [ご利用の環境をリンクする](#link)。

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Dataverse でデュアル書き込みに対応した新しい環境を作る

この手順を完了するには、システム管理者でサインインする必要があります。

1. [Power Platform管理センター](https://admin.powerplatform.com)を開き、管理者としてログインします。
2. 新しい環境を作成し、名前を付けます。
3. 環境の種類を選択する。 試用版のオファーにサインアップした場合は、**試用版 (サブスクリプション ベース)** を選択します。
4. 展開するリージョンを確認します。
5. **この環境にデータベースを作成する** オプションを有効化します。 
6. 言語を確認してから、通貨が財務と運用アプリの通貨と一致することを確認します。
7. **Dynamics 365 アプリ** のオプションを有効にし、**これらのアプリを自動的にデプロイする** のフィールドが **無し** になっていることを確認します。
8. セキュリティ グループが必要な場合は、セキュリティ グループを追加します。
9. **保存** を選択して、環境を作成します。
10. デプロイが完了し、環境が **準備完了** の状態になるまで待機します。

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>デュアル書き込みの前提条件を環境に追加する

デュアル書き込み対応では、**会社** エンティティなどの主要なエンティティに追加されるフィールド含まれます。 既存の環境にデュアル書き込みのサポートを追加する場合、サポートを有効にするためにデータの更新が必要となる場合があります。 データをブートストラップする方法については、[会社のデータをブートストラップする](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)を参照してください。 デュアル書き込みの詳細については、[デュアル書き込みのシステム要件](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)を参照してください。

この手順を実行して、環境にデュアル書き込みの前提条件を追加します。

1. 作成したばかりの環境を開き、**リソース**\>**Dynamics 365 アプリ** に移動します。
2. アプリ リストで **デュアル書き込みコア ソリューション** を選択し、インストールします。
3. インストールが完了するまで待機します。 アプリ リストで **デュアル書き込みアプリのオーケストレーション ソリューション** を選択し、インストールします。

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Project Operations Dataverse  アプリを追加します

この手順は、Project Operations をインストールする前に前の手順を完了している場合にのみ行うことができます。 インストール時に環境構成を分析し、必要に応じてデュアル書き込みへの対応を追加しています。

1. 上記手順で作成した環境を開き、**リソース**\>**Dynamics 365 アプリ** に移動します。
2. **Microsoft Dynamics 365 Project Operations** アプリ リストに追加してインストールします。

## <a name="link-your-environments"></a><a name="link"></a>ご利用の環境をリンクする

Dataverse 環境がデプロイされた後、財務と運用アプリでリンクを設定できます。 [デデュアル書き込みの設定ウィザードを使用して環境をリンクする](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)に記載の手順に従ってください。
