---
title: 価格ディメンションとしての Project Operations フィールド
description: この記事では、Dynamics 365 Project Operations で価格ディメンションとしてフィールドを使用することについて説明します。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: baf2145d4df23893953a099ca3837160fa8ac764
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932808"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>価格ディメンションとしての Project Operations フィールド

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

**実績** エンティティには、リソースベースの料金設定に使用する料金設定ディメンションとして使用できる多くのフィールドがあります。 たとえば、一つの共通フィールドは **予約可能リソース** です。 20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。 ただし、請求対象の労働力が増大するにつれて、リソースに応じたレートを維持することが非現実的になる可能性があります。 リソースのコストと請求レートは、リソースが昇進したり、より多くの経験を積んだり、異なるセットのスキルを身につけることで変化し始めます。 

もう一つの例がトランザクション カテゴリです。 顧客と実施者は、トランザクション カテゴリを使用して作業を分類し、フィールドを使用して作業カテゴリに基づいて価格とコストを設定します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]