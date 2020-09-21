---
title: 価格設定のディメンションとして Project Service 内の既存のフィールドを使用する
description: このトピックでは、価格設定のディメンションとして既存の Project Service フィールドを使用する方法について説明します。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752862"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>価格設定のディメンションとして Project Service 内の既存のフィールドを使用する

Project Service Automation (PSA) の組織には、プロジェクト組織のリソース ベースの価格設定ディメンションとして使用できる **実績** エンティティに多数のフィールドがあります。 たとえば、一つの共通フィールドは **予約可能リソース** です。 20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。 ただし、請求対象の従業員が増加して、リソースが昇進し、経験が増え、あるいは異なるスキルセットを取得するにつれ、リソースのコストと請求レートは変化し始め、これを維持することは非動現実的となります。 この方法は依然として特定の規模の会社に機能しているため、[価格設定のディメンションとして予約可能リソースを使用する](bookable-resource-pricing-dimension.md) のトピックを参照して、既存の Project Service フィールドが価格設定ディメンションとして使用できるのかを理解してください。

もう一つの例がトランザクション カテゴリです。 顧客、および実装者は、PSA でトランザクション カテゴリを使用して作業を分類してきました。また、作業のカテゴリに基づく価格とコストのフィールドを使用しています。 詳細については、 [価格設定のディメンションとして、トランザクション カテゴリを使用する](transaction-category-pricing-dimension.md) を参照してください。
