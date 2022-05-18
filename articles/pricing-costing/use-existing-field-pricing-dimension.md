---
title: 価格設定のディメンションとしてのプロジェクト オペレーションフィールド
description: このトピックは Dynamics 365 Project Operations でフィールドを価格ディメンションとして使用することに関する情報を提供します。
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
ms.openlocfilehash: 6a68bfe5a61f032f28f69c1aaed29f12cbea285d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594124"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>価格ディメンションとしての Project Operations フィールド

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

**実績** エンティティには、リソースベースの料金設定に使用する料金設定ディメンションとして使用できる多くのフィールドがあります。 たとえば、一つの共通フィールドは **予約可能リソース** です。 20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。 ただし、請求対象の労働力が増大するにつれて、リソースに応じたレートを維持することが非現実的になる可能性があります。 リソースのコストと請求レートは、リソースが昇進したり、より多くの経験を積んだり、異なるセットのスキルを身につけることで変化し始めます。 

もう一つの例がトランザクション カテゴリです。 顧客と実施者は、トランザクション カテゴリを使用して作業を分類し、フィールドを使用して作業カテゴリに基づいて価格とコストを設定します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]