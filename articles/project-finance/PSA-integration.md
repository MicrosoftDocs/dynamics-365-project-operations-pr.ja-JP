---
title: Project Service Automation の概要
description: このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance への統合ソリューションについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752878"
---
# <a name="project-service-automation-overview"></a>Project Service Automation の概要

[!include[banner](../includes/banner.md)]

Project Service Automation から Finance への統合ソリューションは、データ統合機能を使用して、Dynamics 365 Finance および Dynamics 365 Project Service Automation のインスタンス間で、Common Data Service を経由してデータを同期します。 データ統合機能で使用可能な統合テンプレートを使用すると、Project Service Automation から Finance への、プロジェクト、プロジェクト契約、プロジェクト契約品目、プロジェクト契約品目のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間の見積もり、および経費の見積もりのフローを実行できます。

> [!NOTE]
> - バージョン 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。 その後、固定価格プロジェクトを統合できます。
> - バージョン 7.3.0 を使用していて、Project Service Automation から料金のトランザクションを引き継いでいる場合、プロジェクト請求書にこれらの料金を含めるために、KB 4345320 をインストールする必要があります。
> - バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、費用の見積もり、および機能のロックを使用できます。
> - バージョン 8.0.1 以降を使用している場合は、実績を同期することができます。

Project Service Automation Finance を統合する前に、Project Service Automation 統合パラメーターを構成する必要があります。 詳細については、[Project Service Automation 統合パラメーター](PSA-parameters.md) を参照してください。

この統合ソリューションにより、次のシナリオで直接同期が可能になります。

- Project Service Automation でプロジェクト契約を維持して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクトを作成して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクト契約品目を維持して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクト契約品目のマイルストーンを維持して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクト タスクを維持して、Project Service Automation から Finance に直接同期します。
- Finance で経費トランザクション カテゴリを維持して、Finance から Project Service Automation に直接同期します。
- Project Service Automation でプロジェクト時間の見積もりを作成して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクト経費の見積もりを作成して、Project Service Automation から Finance に直接同期します。
- Project Service Automation でプロジェクト時間、費用、料金の実績を作成し、Project Service Automation 統合ジャーナルでプロジェクト トランザクションを作成して、Finance に転記できるようにします。

## <a name="data-synchronization"></a>データの同期

次の図は、Project Service Automation と Finance の統合の一部としてデータを同期する方法を示しています。

> [!NOTE]
> 現在利用できないテンプレートもあります。 テンプレートは完成次第リリースされます。

[![Project Service Automation と Finance の統合](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance のシステム要件

Project Service Automation から Finance への統合ソリューションを使用するには、Enterprise Edition 7.3 と Platform update 12 以降をインストールする必要があります。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation のシステム要件

Project Service Automation から Finance への統合ソリューションを使用するには、次のコンポーネントをインストールする必要があります。

- Dynamics 365 Project Service Automation バージョン 9.0.0.0 またはそれ以降
- Dynamics 365 Sales の見込顧客の現金化、バージョン 1.14.0.0 (v14) 以降
- Dynamics 365 Project Service Automation の Project Service Automation から Finance へのソリューション バージョン 1.0.0.0 以降

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation インスタンスに、Project Service Automation から Finance への統合ソリューションをインストールする

[Microsoft ダウンロード センター](https://www.microsoft.com/download/details.aspx?id=57016)から Project Service Automation から Finance への統合ソリューションをダウンロードして、ソリューションに含まれる指示に従います。
