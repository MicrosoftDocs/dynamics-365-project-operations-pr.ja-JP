---
title: Microsoft Project Client の統合
description: プロジェクト スケジュールの計画と管理は複雑になる可能性があるため、プロジェクト マネージャーはこのタスクの管理に役立つツールを使用する必要があります。 Microsoft Project Client との統合により、プロジェクトの WBS (作業分解構造) を開いて管理するためのサポートが提供されます。
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079329"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client の統合

[!include [banner](../includes/banner.md)]

プロジェクト スケジュールの計画と管理は複雑になる可能性があるため、プロジェクト マネージャーはこのタスクの管理に役立つツールを使用する必要があります。 Microsoft Project Client との統合により、プロジェクトの WBS (作業分解構造) を開いて管理するためのサポートが提供されます。 プロジェクト マネージャーは、変更内容を Dynamics 365 Finance プロジェクト WBS (作業分解構造) に公開できます。

> [!NOTE]
> 7 月の更新 (バージョン 10.0.4) を使用している場合は、サポート情報 4054797 および 4055884 をインストールする必要があります。

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project Client アドインの構成
Microsoft Project Client との統合を有効にするには、Microsoft Dynamics 365 アドインをユーザーのクライアント Microsoft Project アプリケーションにインストールする必要があります。 これは、 **プロジェクト管理ワークスペース** を開いて行います。

•ワークスペースの **リンク** > **セットアップ** セクションから **プロジェクト クライアント アドインを構成する** をクリックします。

• **開く** をクリックし、確認メッセージが表示されたら **実行** をクリックします。

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Project Client で既存のドラフト WBS (作業分解構造) を開いて編集する
Dynamics 365 Finance のプロジェクトで既に WBS (作業分解構造) が作成されている場合、WBS (作業分解構造) がドラフト状態の場合は Microsoft Project Client アプリケーションで WBS (作業分解構造) を開くことができます。 **プロジェクト** ページから開くには、 **計画** タブの **Microsoft Projectで開く** のリンクをクリックします。このページは、 **Microsoft Dynamics 365** タブの **開く** をクリックして Microsoft Project Client アプリケーションから開くこともできます。一覧で、 **法人** および **プロジェクト** を選択します。

> [!NOTE]
> ブラウザーとして Internet Explorer を使用している場合、ファイルがダウンロードされた場所から手動で開くには **保存** をクリックする必要があります。 または、 **保存して開く** をクリックして Microsoft Project Client でファイルを開きます。 保存時にファイル名を変更しないでください。

Microsoft Project Client を使用してファイルを編集する前に、ファイルを確認する必要があります。 **Microsoft Dynamics 365** タブで **チェックアウト** をクリックします。これにより、他のユーザーが同時に Finance で WBS (作業分解構造) を編集することができなくなります。 編集の完了後に WBS (作業分解構造) を公開するには、 **Microsoft Dynamics 365** タブの **チェックイン** をクリックします。

プロジェクト チームが既に Finance のプロジェクトに追加されている場合、リソース リストにはチーム メンバーが設定されます。 プロジェクト チームがまだプロジェクトに追加されていない場合は、 **Microsoft Dynamics 365** タブの **リソース** ボタンをクリックしリソースを選択して Microsoft Project Client 内でチームを構築できます。 

次のデータは、チェックイン プロセスの一環として、Finance に同期されます。

• タスク名

• 開始日

• 終了日

• 前のタスク

• リソース名

• カテゴリ

• リソース カテゴリ

• 作業時間

• メモ

• 優先度

> [!NOTE]
> Microsoft Project Client ファイルに他の列を追加しても、それらの列はファイルに保存されずファイルを再度開いたときに表示されません。

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client を使用した既存プロジェクトの WBS (作業分解構造) の作成
Microsoft Project Client を使用して新しい WBS (作業分解構造) を作成するには、次の手順を実行します。


1.  Microsoft Project Client を開きます。

2.  **Microsoft Dynamics 365** タブで、 **開く** をクリックします。

3.  プロジェクトの **法人** を選択します。

4.  **プロジェクト** を選択します。

5.  **Microsoft Dynamics 365** タブの **チェックアウト** をクリックします。

6.  財務に公開する準備ができたら、 **Microsoft Dynamics 365** タブの **チェックイン** をクリックします。

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client を使用した既存プロジェクトの既存 WBS (作業分解構造) の置換
Microsoft Project Client を使用して新しい WBS (作業分解構造) を作成し、既存プロジェクトの既存 WBS (作業分解構造) を置き換えるには、次の手順に従います。

1.  Microsoft Project Client を開きます。

2.  Microsoft Project Client でスケジュールを作成します。

3.  **Microsoft Dynamics 365** タブで、 **変更の保存** > **既存のプロジェクトを置き換え** をクリックします。

4.  プロジェクトの **法人** を選択します。

5.  **プロジェクト** を選択します。

6.  **OK** をクリックします。

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Microsoft Project Client からの新しいプロジェクト作成


1.  Microsoft Project Client を開きます。

2.  Microsoft Project Client でスケジュールを作成します。

3.  **Microsoft Dynamics 365** タブで、 **変更の保存** > **新しいプロジェクトに保存** をクリックします。

4.  プロジェクトの **法人** を選択します。

5.  必要であれば、 **プロジェクト ID** を入力します。

6.  **プロジェクト名** を入力します。

7.  **プロジェクト タイプ** 、 **プロジェクト グループ** および **プロジェクト契約 ID** を選択します。 または、 **新規** をクリックして新しいプロジェクト契約を作成することもできます。

8.  リソースで使用する **カレンダー** を選択します。

11. **OK** をクリックします。
