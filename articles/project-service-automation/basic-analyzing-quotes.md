---
title: プロジェクトの見積もりの分析
description: このトピックでは、プロジェクトの見積もりの分析に関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752797"
---
# <a name="analysis-of-project-quotes"></a>プロジェクトの見積もりの分析

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation はプロジェクトの見積もりを分析して、収益性を予測します。 また、納期、完了日、予算に関する顧客の要求に、見積りがどの程度合致しているか分析します。

## <a name="profitability-analysis"></a>利益性分析

Project Service Automation は、粗利と調整後の粗利を使用して収益性を分析します。

- 粗利は次の式を使用して計算します。

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- 調整後の粗利は次の式を使用して計算します。

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

粗利と調整後の粗利の値が大幅に異なる場合、見積もり中の作業の多くは非請求に分類されます。

## <a name="analysis-of-customer-expectations"></a>顧客の要求の分析

次のフィールドに値を入力すると、見積もりを分析してスケジュールと予算に関する顧客の要求に関するチャートを生成できます。

- 見積もりヘッダーの **配送指定日** フィールド。
- (プロジェクト ベースの行と製品ベースの行に対する) 各見積もり行の **顧客予算** フィールド。

スケジュールに関する顧客要求の分析は、見積もりラインの詳細の最新の終了日を、見積もり内のすべての見積もりラインにわたって要求された納期と比較することで行われます。

予算に関する顧客要求の分析は、顧客の総予算の合計をすべての見積もり行の見積もり金額と比較することで行われます。
