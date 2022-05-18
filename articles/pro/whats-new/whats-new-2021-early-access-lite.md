---
title: 2021 年サイクル 2 早期アクセスの新機能 - Project Operations ライト展開
description: このトピックでは、Project Operations ライト展開の 2021 サイクル 2 早期アクセス リリースで利用できる品質更新についての情報を提供します。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723682"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>2021 年サイクル 2 早期アクセスの新機能 - Project Operations ライト展開

_適用対象: ライト展開 - 見積もり請求の取引_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

  - Dataverse 環境バージョン 4.23.0.4 での Project Operations

このリリースは、環境が[早期アクセスを選択している](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates)場合のみ適用されます。

## <a name="features-included-in-this-release"></a>このリリースが含む機能

[外注管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - この機能により、プロジェクトの作業のすべての側面に対する可視性と制御が向上します。 外注管理のプレビューには、以下の機能が含まれています。

  - プロジェクト マネージャーは、ベンダーとの下請け契約を作成できます。 既定では、ベンダー レコードに添付されている価格表が外注に使用されます。 ベンダー勘定の関係タイプは、**ベンダー** または **サプライヤー** です。
  - プロジェクト マネージャーは、すべての購入を外注の品目として項目化できます。 外注品目は、時間、費用、または製品の場合があります。 外注品目のトランザクション クラスによって、その行の目的が決まります。
  - ベンダー アカウント マネージャーとプロジェクト マネージャーは、外注を繰り返すことができます。 価格は、外注に添付された購買価格表で調整することができます。
  - このプロセス中、外注品目が時間の場合、ベンダー アカウント マネージャーは仕入先連絡先を各外注品目に関連付けることができます。 この関連付けは、外注に対応しているプロジェクト マネージャーに役立つ情報です。 仕入先連絡先が外注品目に関連付けられている場合、予約可能リソースがまだ存在しない場合は、取引先企業から予約可能リソースが自動的に作成されます。
  - 各外注品目の請求方法は、固定価格または時間と材料です。 固定価格の外注品目の場合、マイルストーンベースの請求書スケジュールが設定されます。
