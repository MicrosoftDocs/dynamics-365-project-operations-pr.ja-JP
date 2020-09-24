---
title: リソースの稼働率を表示する
description: このトピックでは、リソースの稼働率ビューについて説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752804"
---
# <a name="view-chargeable-utilization-for-resources"></a>リソースの稼働率を表示する
 
**Project Service リソースの稼働率** ページの **稼働率ビュー** では、それぞれの予約可能リソースの稼働率を表示します。 このビューはスケジュール ボードに基づいているため、共通する機能があります。

> ![稼働率ビューのスクリーンショット](media/FAQ-utilization-1.png)
 

請求可能稼働率の計算のしくみは次のとおりです。

   稼働率 = (実際に割当可能な時間) / (リソース キャパシティ)

セルには、選択した期間 (日、週、または月) で按分計算された稼働率を表します。

各セルの色は、ターゲットの請求可能稼働率と比べた、リソースの請求可能稼働率が表示されます。 

ターゲット稼働率は、リソースのデフォルトの役割または個々のリソース自体に設定できます。 この計算では、まずターゲットの個人を調べ、次にリソースの既定のロールを調べます。

## <a name="set-target-on-a-resource"></a>リソースにターゲットを設定する

1. **リソース** \> **リソース**へ移動します。 
2. リソースを選択してレコードを開きます。 
3. **Project Service** タブでは、リソースの目標稼働率を設定することができます。

> ![[Project Service] タブを使用してターゲット稼働率を設定するスクリーンショット](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>ロールの目標稼働率を設定する

1. **リソース** \> **リソースのロール**へ移動します。 
2. ロールを選択してレコードを開きます。 
3. ロールのターゲット稼働率を設定します。

> ![[リソースのロール] を使用してターゲット稼働率を設定するスクリーンショット](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>リソースの可能稼働率を計算する

リソースの可能稼働率を計算するには、いくつかの前提条件を満たす必要があります。 

### <a name="set-default-role-for-individual-resource"></a>個々のリソースの既定ロールを設定する

まず、目標稼働率がそれぞれのリソース、またはリソースのロールで設定されている必要があります。 ターゲットのリソース ロールを使用する場合、個別のリソースには既定のロールが必要です。 

1. これを設定するには、 **リソース** \> **リソース**へと移動します。 
2. リソースを選択してから、レコードを開き、 **Project Service** タブを選択します。 
3. **リソース ロール** グリッドにて、リソースに1つのロールが設定されていて、 **これを既定とする** が **はい**に設定されていることを確認してください。
 
### <a name="change-billing-type-for-resource-role"></a>リソースのロールに対する請求の種類を変更する

リソースロールの請求の種類は、 **請求可能**に設定する必要があります。 

1. **リソース** \> **リソースのロール**へ移動します。 
2. 更新を行うレコードを開き、請求種類の既定値を **請求可能** に設定します。

### <a name="set-working-hours-for-resource-role"></a>リソースロールの作業時間を設定する
 
キャパシティ計算のため、リソースは作業時間を持つ必要があります。 

1. **リソース** \> **リソース**へ移動します。 
2. リソースを選択してレコードを開き、 **作業時間の表示** を選択します。 
3. **リソースの一覧** ビューから **作業時間テンプレート** を適用することで、リソースの一覧を一括更新することができます。

## <a name="troubleshooting-chargeable-actual-hours"></a>割り当て可能な実際の時間に関するトラブルシューティング

割り当て可能な実績時間は、 **実績** エンティティから提供されます。 請求タイプが **請求可能** となる実績が計算に含まれているため、実績が請求可能なプロジェクトが必要です。

請求可能稼働率が表示されない場合、以下の点をチェックすると役立つことがあります。

- リソースのキャパシティに作業時間が定義されている。
- リソースには、個別に定義されたターゲット稼働率があるか、既定のロールが割り当てられている。 ロールにはターゲット稼働率が定義されている。
- 実績の請求タイプは、稼働状況計算の対象となる期間に対して **請求可能** となります。 請求タイプに請求可能以外の実績が表示されている場合は、以下を確認してください。

  - 実績で使用されるロールの既定の請求の種類が請求可能以外になっている。
  - プロジェクトを支えるプロジェクト契約品目のロールが請求不可に設定されている。
  - プロジェクトに関連する契約品目がない。
