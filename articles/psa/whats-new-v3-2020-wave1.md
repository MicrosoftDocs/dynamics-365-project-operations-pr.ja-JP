---
title: 2020年 リリース予定 第1群 Project Service Automation バージョン 3.x の最新情報または変更事項
description: このトピックでは、Project Service Automation バージョン 3、2020年 リリース予定 第1群の新機能と変更点について説明します。
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577886"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>2020年 リリース予定 第1群 Project Service Automation バージョン 3 の最新情報または変更事項

[!include [banner](../includes/psa-now-project-operations.md)]

トピックは、2020年 リリース予定 第1群 Project Service Automation（PSA）バージョン3.x の最新リリースに移行する際の、アップグレードに関する重要な考慮事項を説明します。

## <a name="time-entry"></a>時間エントリ
時間エントリのエクスペリエンスが拡張されており、より多くの顧客のシナリオに時間エントリを拡張する機能が提供されています。 これには、入力タイプを追加する機能が含まれており、 **時間ソース** として表示されるフィールドのスキーマ名 **時間エントリ設定** に基づいて特定の動作が実行されるようになります。 この機能をサポートするために、時間、経費、ステータス、および承認 (TESA) と呼ばれる新しいソリューションが追加されました。

### <a name="upgrade-consideration"></a>アップグレードに関する考慮事項
この機能に対応するにあたり、PSA 内のロールが更新され、新しい権限が含まれるようになりました。 これらの権限は、新たなエンティティである **時間エントリ設定** の読み取り権限を付与します。

時間を記録する機能を必要とするユーザーには、既存の役割に加えてユーザー役割 **時間エントリ ユーザー** を付与する必要があります。 このロールには新しい機能が含まれており、時間エントリが引き続き動作するように機能します。

さらに、時間エントリ エンティティのすべてのフォームを含むカスタム アプリ モジュールがある場合、モジュールから **TESA 時間エントリの簡易作成フォーム** を削除する必要があります。

### <a name="currently-extended-time-entry-changes"></a>現行の拡張時間エントリにおける変更点
時間エントリの現在のユーザーへの影響を最小限に抑えるために、このロールにされた変更は時間エントリを継続して使用するにあたって必要となる唯一の主要要件です。 カスタム ビューまたは個別の時間エントリ エクスペリエンスを作成している場合は、 **時間エントリ設定** フィールドに正しい PSA 値を設定する必要があります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
