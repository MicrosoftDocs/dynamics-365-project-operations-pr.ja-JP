---
title: 外注コンポーネントの時間、経費、材料使用量を記録する
description: この記事では、下請けコンポーネントのプロジェクトで記録された時間、費用、材料の使用量が、Microsoft Dynamics 365 Project Operations でどのように追跡されるかについて説明します。
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261142"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>外注コンポーネントのプロジェクトにおける時間、経費、材料使用量の記録する

_**適用対象:** ライト展開 - 見積もり請求の取引_

この記事では、下請けコンポーネントのプロジェクトで記録された時間、費用、材料の使用量が、Microsoft Dynamics 365 Project Operations でどのように追跡されるかについて説明します。

## <a name="costing-for-subcontractor-time-on-projects"></a>プロジェクトの外注業者の時間のコスト
Project Operations では、契約労働者が従業員と同様の方法でプロジェクトの時間を記録することができます。 プロジェクトおよび/またはプロジェクト タスクの時間を入力する際、契約作業員は特定の外注および外注ラインを選択できます。

契約労働者が提出した時間が承認されると、その契約労働者のリソースに設定されている単価を使って、外注の購入価格表の **役割の価格** セクションでプロジェクト コストが計上されます。

## <a name="costing-for-subcontracted-expenses-on-projects"></a>プロジェクトにおける外注費用の原価計算
プロジェクトで発生した費用を入力する際に、費用入力で外注と外注ラインを選択できます。 

この経費エントリが提出されて承認されると、下請契約の購入価格表の **カテゴリー価格** でその取引カテゴリーに設定されている単価に基づいて、プロジェクトに経費が計上されます。

## <a name="costing-for-subcontracted-materials-on-projects"></a>プロジェクトにおける外注資材の原価計算
プロジェクトで資材の使用量を入力する際に、資材使用量のログで外注先と外注明細行を選択することができます。 資材の使用ログが提出され承認されると、外注価格表の **価格表項目** でその製品に設定されている単価に基づいて、材料費がプロジェクトに計上されます。

また、プロジェクトにおける書き込み製品についても、資材の使用量を記録することができます。 このような資材の使用量は、外注先や外注明細にもリンクできます。 書き換え製品の資材使用量を計上する際には、書き換え製品の単価を入力する必要があります。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
