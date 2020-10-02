---
title: 価格設定のディメンションとしてのプロジェクト オペレーションフィールド
description: このトピックでは、Dynamics 365 プロジェクト オペレーションでフィールドを価格ディメンションとして使用する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896422"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>価格設定のディメンションとしてのプロジェクト オペレーションフィールド

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

**実績**エンティティには、リソースベースの料金設定に使用する料金設定ディメンションとして使用できる多くのフィールドがあります。 たとえば、一つの共通フィールドは **予約可能リソース** です。 20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。 ただし、請求対象の労働力が増大するにつれて、リソースに応じたレートを維持することが非現実的になる可能性があります。 リソースのコストと請求レートは、リソースが昇進したり、より多くの経験を積んだり、異なるセットのスキルを身につけることで変化し始めます。 

もう一つの例がトランザクション カテゴリです。 顧客と実施者は、トランザクション カテゴリを使用して作業を分類し、フィールドを使用して作業カテゴリに基づいて価格とコストを設定します。
