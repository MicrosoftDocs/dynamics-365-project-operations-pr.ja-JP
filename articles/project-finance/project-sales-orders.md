---
title: 時間および実費払プロジェクトのプロジェクト受注
description: このトピックでは、時間および実費払プロジェクトのプロジェクト ベースの受注を作成する方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752810"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>時間および実費払プロジェクトのプロジェクト受注

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

このトピックでは、プロジェクトの受注を作成する方法について説明します。 受注は、タイプが**時間および実費払**のプロジェクトに対してのみ作成できます。

時間および実費払プロジェクトがプロジェクト契約に複数の資金調達ソースがある場合、**プロジェクト管理および会計パラメーター**ページの**複数の資金調達ソースがあるプロジェクトの受注を許可する**パラメーターを有効にする必要があります。 

> [!NOTE]
> - 複数の資金調達ソースがあるプロジェクト受注のサポートは、アプリケーション リリース 10.0.2 以降で使用可能です。
> - 複数の資金調達ソースを使用してのプロジェクトの受注のサポートを有効にするパラメーターは、2020 年 4 月のリリース ウェーブで削除され、その後、機能は常に有効になります。

プロジェクトベースの受注は、次の 2 つの方法で作成できます。

- プロジェクト自体に移動します。 アクションのウィンドウで、**管理 > 品目のタスク > 受注**を選択します。 プロジェクト情報は、プロジェクトの受注に既定で設定されます。 プロジェクト契約に複数の資金調達ソースがある場合は、受注の顧客を設定する資金調達ソースを選択する必要があります。 プロジェクトの資金調達ソースが 1 つしかない場合、顧客は自動的に設定されます。
- **すべての受注**の一覧ページに移動し、新規の受注を作成します。 受注のプロジェクトを選択する必要があります。 プロジェクトが選択されると、顧客は資金調達ソースから設定されるか、またはプロジェクト契約に複数の資金調達ソースがある場合は、資金調達ソースを選択する必要があります。
