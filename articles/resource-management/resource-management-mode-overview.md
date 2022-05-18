---
title: リソース管理モードの概要
description: このトピックは、Dynamics 365 Project Operations のリソース管理機能に関する情報を提供します。
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: f30bac95b2beb92345cbe25332963c58d2bde4bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585062"
---
# <a name="resource-management-modes-overview"></a>リソース管理モードの概要

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations は、全体的な予約フローを実行する 2 つのモードをサポートしています。 管理モードはプロジェクト パラメータとして定義されており、ビジネス ニーズが変更する場合は修正可能です。    

## <a name="central-mode"></a>セントラル モード
プロジェクトへのリソースの割り当てを一元管理する組織の場合、セントラル モードは、プロジェクト マネージャーがプロジェクト レベルでリソース要件を定義できるようにする方法を提供します。 リソース要件の履行は、リソース マネージャーに委任されます。 プロジェクト マネージャーは、リソース マネージャーによって提案されたリソースを承認または拒否できます。

![中央モード。](./media/resource-management-central.png)

セントラル モードでリソースを管理するには、以下を参照してください。

- [予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する](/dynamics365/project-service/assign-generic-bookable-resource)
- [リソース要件から名前付きリソースを予約する](/dynamics365/project-service/book-named-resource)
- [リソース要求の送信](/dynamics365/project-service/submit-resource-request)
- [リソース要求を実行](/dynamics365/project-service/resource-management-fulfill-requests)
- [リソース要求から提案されたプロジェクト リソースの承諾または拒否](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>ハイブリッド モード
リソースの割り当てに柔軟性が必要な組織の場合、ハイブリッド モードでは、プロジェクト マネージャーとリソース マネージャーの両方がリソースを予約できます。

![ハイブリッド モード。](./media/resource-management-hybrid.png)

サポートされているセントラル モード プロセスに加えて、ハイブリッド モードでサポートされている他のすべての予約フローを管理するには、次のトピックを参照してください。

プロジェクトにリソースを直接予約する:
- [名前付き予約可能リソースをプロジェクト チームに予約して、タスクを割り当てる](/dynamics365/project-service/assign-named-bookable-resource)

リソース要件からリソースを予約する:
- [予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する](/dynamics365/project-service/assign-generic-bookable-resource)
- [リソース要件から名前付きリソースを予約する](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]