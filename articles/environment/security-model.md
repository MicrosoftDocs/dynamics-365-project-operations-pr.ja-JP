---
title: セキュリティ モデル
description: このトピックは Dynamics 365 Project Operations のセキュリティ モデルに関する情報を提供します。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642909"
---
# <a name="security-model"></a>セキュリティ モデル

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations は独自のセキュリティモデルを含み、Microsoft Office グループと連携するロール ベースのビジネス セキュリティ モデルを利用できます。 


## <a name="security-roles"></a>セキュリティ ロール
Project Operations のフロントエンド機能には、次のロールが含まれます。

| ロール                          | 内容                                                                                                                                                                 | 範囲 |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| プラクティス マネージャー              | プロジェクト間のレポートをサポートします。                                                                                                            | 部署              |
| プロジェクト承認者              | プロジェクトに対する時間と経費を承認します。                                                                                                                              | 部署 |
| プロジェクトの課金管理者 | 請求書の提案を作成します。                                                                                                                                                 | 部署 |
| プロジェクト マネージャー               | プロジェクト計画を作成し、リソースを要求します。                                                                                                                              | 部署 |
| プロジェクト リソース              | 予約して時間を報告できるチーム メンバー。                                                                                                          | 部署|
| リソース マネージャー              | リソース要求や予約の実行など、すべてのリソース管理機能は、ハイブリッド プロジェクト マネージャー + リソース マネージャー構成と単一の集中型リソース マネージャーのロールをサポートするために分離されています。 | 部署 |


Web 向けの Microsoft Project には、次のロールが含まれています。

| ロール           | 内容                                                                                                        | 範囲  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| プロジェクト ユーザー   | 自分達のプロジェクトを作成し、共有されているプロジェクトを表示できる、プロジェクトの共同作業ユーザー。 | ユーザー    |
| プロジェクト システム | アプリケーション コンテキストに使用されるロール。 お客様は、このシステムのロールを使用しないでください。                                    | グローバル |

## <a name="security-enforcement"></a>セキュリティの実施
プロジェクト レベルで実行されるアクションは、ログインしたユーザーのコンテキストで実行されます。 つまり、プロジェクトを作成、開く、または削除するには、ユーザーは CDS で使用可能なアクセス権を持っている必要があります。 CDS でのアクセスは、プラットフォームに含まれている可能なメカニズムのいずれかを介して許可される場合があります。 たとえば、より広いスコープを持つユーザーがプロジェクトにアクセスしたり、ユーザーにアクセスを許可する明示的なプロジェクト共有アクションが実行された場合などです。

Project Operations でプロジェクトを作成するときは、これを考慮することが重要です。

## <a name="modern-group-collaboration-with-project-operations"></a>Project Operations とモダン グループの共同作業
Web 向けの Project と Project Operations は、共同作業のためのモダン グループをサポートします。 グループを介してプロジェクトに追加されたユーザーは、プロジェクト計画を編集できます。

Web 向けの Project は、割り当て時にユーザーをグループに自動的に追加します。

グループを使用すると、プロジェクトのアクセス許可とサポートするコラボレーション成果物を共同で作業できます。 次の図は、グループ割り当てプロセス中に発生するイベントと状態の変化を示しています。

Project Operations は、暗黙的なアクションによってグループを作成するのではなく、グループを押すという明示的なアクションを介してのみ作成します。

**グループ管理** ダイアログでのグループ メンバーの検索は、環境のセキュリティ グループの一部として設定されているユーザーに限定されています。 詳細については、[環境へのユーザー アクセスのコントロール: セキュリティ グループおよびライセンス](https://docs.microsoft.com/power-platform/admin/control-user-access) を参照してください。

![グループモード](./media/groupsmode.png)

1. プロジェクトは、作成するユーザーによって作成および所有されます。
2. プロジェクトの所有者がチームに更新されます。
3. 所有者チームは、指定または作成された Office グループにマップされます。
4. プロジェクトの元の所有者が Office グループに追加されます。

## <a name="deployment-recommendation"></a>展開に関する推奨事項
Office グループのコラボレーション モデルが拡張するにつれて、時間の経過とともにより詳細なコントロールを提供する機能が追加されます。 今日 Project Operations を展開しているお客様は、従来の Microsoft Dynamics 365 セキュリティ モデルに集中することをお勧めします。

詳細については、[Common Data Service のセキュリティ](https://docs.microsoft.com/power-platform/admin/wp-security) を参照してください。

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations と Microsoft Dynamics 365 Finance セキュリティ
Project Operations には次のロールが含まれます:

- プロジェクト マネージャー
- プロジェクト経理担当者

Finance のセキュリティの詳細については、[ロールベースのセキュリティ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security) を参照してください。




[!INCLUDE[footer-include](../includes/footer-banner.md)]