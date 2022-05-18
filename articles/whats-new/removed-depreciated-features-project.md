---
title: Dynamics 365 Project Operations の削除済み、または非推奨の機能
description: このトピックでは、Dynamics 365 Project Operations から削除された、または削除される予定の機能について説明します。
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601576"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Dynamics 365 Project Operations の削除済み、または非推奨の機能

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations、Lite 展開 - 見積もり請求の取引、在庫/製造ベースのシナリオ向け Project Operations_

このトピックでは、Dynamics 365 Project Operations から削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品で使用できなくなりました。
- *非推奨* の機能は現在開発中ではなく、将来のアップデートで削除される可能性があります。

この一覧は、これらの削除と非推奨を検討する際の参考にすることを目的としています。

> [!NOTE]
> 財務と運用アプリ内のオブジェクトに関する詳細情報については、[**技術参照レポート**](/dynamics/s-e/global/axtechrefrep_61) を参照してください。 これら異なるバージョンのレポートを比較し、財務と運用アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operations 2022 年 3 月リリースで削除、非推奨となる機能

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>プロジェクト管理と会計 "常に調整トランザクションを作成する" パラメータ

| &nbsp; | &nbsp; |
|--------|--------|
| **非推奨/削除の理由** | 監査目的で調整トランザクションが必要です。 非推奨になると、このパラメータは非表示になります。 パラメータが **はい** に設定されている場合と同様に、システムは常に調整トランザクションを作成します。 |
| **別の機能に置き換えられましたか？** | 番号 |
| **影響を受ける製品領域** | アプリケーション |
| **展開オプション** | 在庫/製造指示のシナリオ向け Project Operations |
| **状況** | 非推奨: 2023 年 3 月 1 日までに、パラメータは非表示になり、システム動作を変更することで、調整トランザクションが常に作成されるようになります。 |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>プロジェクト管理と会計 "調整日を新しいプロジェクト日として使用する" パラメータ

| &nbsp; | &nbsp; |
|--------|--------|
| **非推奨/削除の理由** | このパラメーターは元々、会計期間が閉じられたときに調整できるようにするために使用されていました。 ただし、トランザクションの会計日は、構成されている場合、オープン期間の最初の日付に変更できるため、不要になりました。 プロジェクトの日付は、トランザクションが発生した日付を表すため、変更しないでください。 |
| **別の機能に置き換えられましたか？** | 番号 |
| **影響を受ける製品領域** | アプリケーション |
| **展開オプション** | 在庫/製造指示のシナリオ向け Project Operations |
| **状況** | 非推奨: 2023 年 3 月 1 日までに、パラメータは非表示になり、システム動作を変更することで、プロジェクト日が調整で変更されることがないようにします。 |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>在庫/製造ベースのシナリオ向け Project Operations のリソース要求ワークフロー

| &nbsp; | &nbsp; |
|--------|--------|
| **非推奨/削除の理由** | 使用量とトランザクション量の制限が少ないため、非推奨になりました。 |
| **別の機能に置き換えられましたか？** | 番号 |
| **影響を受ける製品領域** | アプリケーション |
| **展開オプション** | 在庫/製造指示のシナリオ向け Project Operations |
| **状況** | 非推奨: 2023 年 3 月 1 日までに、ワークフローを使用してプロジェクトのリソースをリクエストするオプションを無効にします。 |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>ヘッダー ビューと明細行ビューのないプロジェクト請求書提案ページ

| &nbsp; | &nbsp; |
|--------|--------|
| **非推奨/削除の理由** | **ヘッダーと行のビューでプロジェクトの請求書提案と請求書仕訳フォームを使用する** 機能キーと一緒に導入されたページの改善のために非推奨となりました。 |
| **別の機能に置き換えられましたか？** | 有効 |
| **影響を受ける製品領域** | アプリケーション |
| **展開オプション** | 実稼働/在庫シナリオ用 Project Operations; リソース/ 非在庫シナリオ用Project Operations |
| **状況** | 非推奨: 2023 年 3 月 1 日までに、以前の (レガシ) ページをオフにして、規定で **ヘッダーと行のビューでプロジェクトの請求書提案と請求書仕訳フォームを使用する** 機能キーをオンにします。 |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Project Operations 2021 年 12 月のリリースで削除、非推奨となる機能

### <a name="collaboration-workspaces"></a>コラボレーション ワークスペース

[コラボレーション ワークスペースの作成、またはリンク (プロジェクト)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **非推奨/削除の理由** | 使用率が低いため、非推奨となりました。 リソースや在庫のないシナリオで Project Operations を使用している顧客は、[オフィス グループとのコラボレーション](../project-management/collaboration-groups.md) を活用することができます。 |
| **別の機能に置き換えられましたか？** | 番号 |
| **影響を受ける製品領域** | アプリケーション  |
| **展開オプション** | 在庫/製造指示のシナリオ向け Project Operations |
| **状況** | 非推奨: 2022 年 12 月 1 日までに、コラボレーション ワークスペースのサポートを終了する予定です。 |
