---
title: 価格設定のディメンションとして Project Service 内の既存のフィールドを使用する
description: この記事では、価格ディメンションとして既存の Project Service フィールドを使用する方法について説明します。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: abc3a3a2b61ea6f8dd34d82bf91546f8f7552a61
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925218"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>価格設定のディメンションとして Project Service 内の既存のフィールドを使用する

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) の組織には、プロジェクト組織のリソース ベースの価格設定ディメンションとして使用できる **実績** エンティティに多数のフィールドがあります。 たとえば、一つの共通フィールドは **予約可能リソース** です。 20 ～ 30 未満の請求可能なリソースがある中小企業の場合、請求およびコストの割合を各リソースに特有のものとして保持することが簡単な方法であることが理解できる場合があります。 ただし、請求対象の従業員が増加して、リソースが昇進し、経験が増え、あるいは異なるスキルセットを取得するにつれ、リソースのコストと請求レートは変化し始め、特定のレートを維持することは非動現実的となります。 この方法は依然として特定の規模の会社に機能しているため、[価格設定のディメンションとして予約可能リソースを使用する](bookable-resource-pricing-dimension.md)を参照して、既存の Project Service フィールドが価格設定ディメンションとして使用できるのかを理解してください。

もう一つの例がトランザクション カテゴリです。 顧客、および実装者は、PSA でトランザクション カテゴリを使用して作業を分類してきました。また、作業のカテゴリに基づく価格とコストのフィールドを使用しています。 詳細については、 [価格設定のディメンションとして、トランザクション カテゴリを使用する](transaction-category-pricing-dimension.md) を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
