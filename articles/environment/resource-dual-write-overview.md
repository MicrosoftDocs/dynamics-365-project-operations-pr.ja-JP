---
title: Project Operations の二重書き込みの統合
description: このトピックでは、Project Operations の二重書き込みの統合の概要について説明します。
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582762"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations の二重書き込みの統合の概要

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Project Operations は、[二重書き込み機能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) を使用して、Microsoft Dataverse および Dynamics 365 Finance 全体でデータを同期します。

次の図は、この Dataverse と Finance の統合の一環としてデータが同期される様子を示しています。

![Project Operations データ フローの概要。](./media/ProjectOperationsFlows.jpg)

Dataverse での Project Operations は、最新のユーザーインターフェース (UI) と、Power Platform の機能を使った簡単なノーコード/ローコードの拡張性を提供します。 プロジェクト マネージャー、リソース マネージャー、プロジェクト チームのメンバーなどのフロント オフィスのペルソナは、Project Operations on Dataverse で自身の活動を行います。

Project Operations in Finance は、プロジェクトの会計と収益認識のサポートを提供します。 Project Operations は、Finance の財務フレーム ワークに接続して、売上税の計算、為替レート、財務指標の報告などを行います。 プロジェクト会計士の経験は、主に Finance に基づきます。

Project Operations の統合は、以下のコンポーネントの統合で構成されています:


- [Project Operations のセットアップと構成データの統合](resource-dual-write-setup-integration.md) 
- [プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md)
- [プロジェクトの請求書](resource-dual-write-project-invoice.md)
- [経費管理](resource-dual-write-expense.md)
- [ベンダー請求書](resource-dual-write-vendor-invoice.md)
