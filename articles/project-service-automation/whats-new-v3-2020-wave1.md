---
title: 2020年 リリース予定 第1群 Project Service Automation バージョン 3.x の最新情報または変更事項
description: このトピックでは、Project Service Automation バージョン 3、2020年 リリース予定 第1群の新機能と変更点について説明します。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752851"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>2020年 リリース予定 第1群 Project Service Automation バージョン 3 の最新情報または変更事項
トピックは、2020年 リリース予定 第1群 Project Service Automation（PSA）バージョン3.x の最新リリースに移行する際の、アップグレードに関する重要な考慮事項を説明します。

## <a name="time-entry"></a>時間エントリ
時間エントリのエクスペリエンスが拡張されており、より多くの顧客のシナリオに時間エントリを拡張する機能が提供されています。 これには、入力タイプを追加する機能が含まれており、 **時間ソース** として表示されるフィールドのスキーマ名 **時間エントリ設定** に基づいて特定の動作が実行されるようになります。

### <a name="upgrade-consideration"></a>アップグレードに関する考慮事項
この機能に対応するにあたり、PSA 内のロールが更新され、新しい権限が含まれるようになりました。 これらの権限は、新たなエンティティである **時間エントリ設定** の読み取り権限を付与します。

時間を記録する機能を必要とするユーザーには、既存の役割に加えてユーザー役割 **時間エントリ ユーザー** を付与する必要があります。 このロールには新しい機能が含まれており、時間エントリが引き続き動作するように機能します。

### <a name="currently-extended-time-entry-changes"></a>現行の拡張時間エントリにおける変更点
時間エントリの現在のユーザーへの影響を最小限に抑えるために、このロールにされた変更は時間エントリを継続して使用するにあたって必要となる唯一の主要要件です。 カスタム ビューまたは個別の時間エントリ エクスペリエンスを作成している場合は、 **時間エントリ設定** フィールドに正しい PSA 値を設定する必要があります。
