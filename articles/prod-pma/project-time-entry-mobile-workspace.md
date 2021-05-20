---
title: プロジェクト時間エントリ モバイル ワークスペース
description: このトピックでは、プロジェクト時間エントリ モバイル ワークスペースに関する情報を提供します。 このワークスペースを使用すると、ユーザーはモバイル デバイスを使用して、プロジェクトに時間を入力および保存できます。
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 78bb696a39a6ec126d7de01f170edbd07677a314
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950180"
---
# <a name="project-time-entry-mobile-workspace"></a>プロジェクト時間エントリ モバイル ワークスペース

[!include [banner](../includes/banner.md)]

このトピックでは、**プロジェクト時間エントリ** モバイル ワークスペースに関する情報を提供します。 このワークスペースを使用すると、ユーザーはモバイル デバイスを使用して、プロジェクトに時間を入力および保存できます。

このモバイル ワークスペースは、Dynamics 365 Unified Operations Mobile アプリと共に使用することを目的としています。 

## <a name="overview"></a>概要
日々の業務の一環として、プロジェクト リソースは多くの場合、オンサイトまたは出張中です。 **プロジェクト時間入力** モバイル ワークスペースを使用すると、ユーザーが選択したモバイル デバイスでプロジェクトに対して支払請求可能な時間または支払請求可能でない時間を入力できます。 したがって、プロジェクト リソースは、時間エントリをいつでも、どこでも記録できます。 また、既に記録されている時間エントリを表示できます。 

具体的には、**プロジェクト時間エントリ** モバイル ワークスペースで、ユーザーは次のタスクを実行できます。

-   選択した日付に対して、特定のタスクに費やした時間数を入力します。
-   時間を入力するプロジェクトをプロジェクト名または顧客で検索します。
-   費やした時間のカテゴリと活動を指定します。
-   プロジェクトの時間を請求可能または請求不可能として記録します。
-   必要に応じて、外部または内部のコメントを入力します。

## <a name="prerequisites"></a>前提条件
前提条件は、組織に展開されている Microsoft Dynamics 365 のバージョンによって異なります。

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance を使用する場合の前提条件
Finance が組織に展開されている場合、システム管理者は **プロジェクト時間エントリ** モバイル ワークスペースを発行する必要があります。 詳細については、[モバイル ワークスペースの発行](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace) を参照してください。

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Platform update 3 以降のバージョン 1611 を使用する場合の前提条件
プラットフォーム更新プログラム 3 以降のバージョン 1611 が組織に展開されている場合、システム管理者は次の前提条件を満たす必要があります。 

<table>
<thead>
<tr class="header">
<th>前提条件</th>
<th>ロール</th>
<th>内容</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>サポート情報 4018050 を実装する。</td>
<td>システム管理者</td>
<td>サポート情報 4018050 は、<strong>プロジェクト時間エントリ</strong> モバイル ワークスペースを含む X++ 更新またはメタデータ修正プログラムです。 サポート情報 4018050 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします</a>。</li>
<li><strong>ApplicationSuite</strong> および <strong>ProjectMobile</strong> モデルを含む<a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">展開可能なパッケージを作成</a>してから、展開可能なパッケージを LCS にアップロードします。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">展開可能なパッケージを適用します</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>プロジェクト時間エントリ</strong> モバイル ワークスペースを発行します。</td>
<td>システム管理者</td>
<td><a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの発行</a>を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール

Finance and Operations モバイル アプリのダウンロードとインストール:

-   [Android 電話用](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhones 用](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにサインインします。
1.  モバイル デバイスからアプリを起動します。
2.  Dynamics 365 の URL を入力します。
3.  初めてサインインするときに、ユーザー名とパスワードを入力するように求められます。 資格情報を入力します。
4.  サインインすると、会社で使用可能なワークスペースが表示されます。 システム管理者が後で新しいワークスペースを発行した場合は、モバイル ワークスペースのリストを更新する必要がありますのでご注意ください。

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>プロジェクト時間エントリ モバイル ワークスペースを使用した時間の入力
1.  モバイル デバイスで、**プロジェクト時間エントリ** ワークスペースを選択します。
2.  **時間エントリ** を選択します。 現在の週のカレンダー日付が表示されます。
3.  選択した日付で、**操作** &gt; **新しいエントリ** を選択します。
4.  記録する時間数を入力します。
5.  時間エントリのプロジェクトを選択します。 一覧には、オフラインで使用するためにアプリに読み込まれているプロジェクトが表示されます。 既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。 詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。
6.  プロジェクトが一覧にない場合は、**検索** を選択します。 名前で検索するか、プロジェクト名または顧客別検索に切り替えます。
7.  カテゴリを選択します。 一覧には、オフラインで使用するためにアプリに読み込まれているカテゴリが表示されます。 既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。 詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。
8.  カテゴリが一覧にない場合は、**検索** を選択します。 カテゴリで検索するか、カテゴリ名別検索に切り替えます。
9.  活動を選択してください。 一覧には、オフラインで使用するためにアプリに読み込まれている活動が表示されます。 既定では 50 項目が読み込まれていますが、開発者はこの数を変更できます。 詳細については、[モバイル プラットフォーム](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) を参照してください。
10. 活動が一覧にない場合は、**検索** を選択します。 活動番号で検索するか、目的別検索に切り替えます。

11. ライン プロパティを選択します。
12. 任意: 外部および内部のコメントを入力します。
13. **完了** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]