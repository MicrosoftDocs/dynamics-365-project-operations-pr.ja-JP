---
title: リソース管理モードの概要
description: このトピックは、Dynamics 365 Project Operations でのリソース管理機能に関する情報を提供します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118524"
---
# <a name="resource-management-modes-overview"></a>リソース管理モードの概要

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


Dynamics 365 Project Operations は、予約フロー全体を実行するために 2 つのモードをサポートしています。 管理モードはプロジェクト パラメータとして定義されており、ビジネス ニーズが変更する場合は修正可能です。    

## <a name="central-mode"></a>セントラル モード
プロジェクトへのリソースの割り当てを一元管理する組織の場合、セントラル モードは、プロジェクト マネージャーがプロジェクト レベルでリソース要件を定義できるようにする方法を提供します。 リソース要件の履行は、リソース マネージャーに委任されます。 プロジェクト マネージャーは、リソース マネージャーによって提案されたリソースを承認または拒否できます。

![セントラル モード](./media/resource-management-central.png)

セントラル モードでリソースを管理するには、以下を参照してください。

- [予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [リソース要件から名前付きリソースを予約する](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [リソース要求の送信](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [リソース要求を実行](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [リソース要求から提案されたプロジェクト リソースの承諾または拒否](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>ハイブリッド モード
リソースの割り当てに柔軟性が必要な組織の場合、ハイブリッド モードでは、プロジェクト マネージャーとリソース マネージャーの両方がリソースを予約できます。

![ハイブリッド モード](./media/resource-management-hybrid.png)

サポートされているセントラル モード プロセスに加えて、ハイブリッド モードでサポートされている他のすべての予約フローを管理するには、次のトピックを参照してください。

プロジェクトにリソースを直接予約する:
- [名前付き予約可能リソースをプロジェクト チームに予約して、タスクを割り当てる](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

リソース要件からリソースを予約する:
- [予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [リソース要件から名前付きリソースを予約する](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
