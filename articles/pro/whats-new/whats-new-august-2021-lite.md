---
title: 新機能 2021 年 8 月 - Project Operations ライト展開
description: このトピックでは、2021 年 8 月にリリースされた Project Operations ライト展開で利用できる品質更新についての情報を提供します。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323512"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>新機能 2021 年 8 月 - Project Operations ライト展開

_適用対象: ライト展開 - 見積もり請求の取引_

このトピックは、次の Dynamics 365 Project Operations コンポーネントとバージョンに適用されます:

  - Dataverse 環境バージョン 4.13.0.152 での Project Operations

## <a name="features-included-in-this-release"></a>このリリースが含む機能

このリリースは以下の機能を含みます。

- **承認セット**: 承認は、グループの時間、費用、または材料用途の承認要求を、操作のより小さなサブセットにまとめて設定します。 このグループ化により、承認をプロジェクトごとに特定の順序で処理し、再試行と順序付けを行うことができるようになります。 リクエストをグループ化すると、大量の承認に対する承認処理の信頼性と追跡可能性が向上します。 詳しくは、[承認セット](../../approvals/approval-sets.md)を確認してください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 請求および価格設定 | 2295625 | マイルストーン名は、請求書スケジュールから請求書明細の詳細にコピーする必要があります。 |
| 請求および価格設定 | 2316323 | リソースベースのシナリオでは、Project Operations の見積もり請求で割引を編集できないようにする必要があります。 |
|  営業案件管理 | 2338619 | **機会** と **見積もり** ビジネス ルールはページでのみ呼び出す必要があります。 |
| リソース管理 | 2316523 | 役割がアタッチされているリソース要件から **リクエストを送信** を使用すると、エラーが表示されません。 |
| リソース管理 | 2326885 | プロジェクトを介してリソース要件を作成すると、エラーは表示されません。 |
| 時間と経費 | 2335584 | 時間エントリにおける非推奨のタスク フロー。 |
| 時間と経費 | 2336884 | **週のコピー** 時間エントリ ボタンは、現在のユーザー以外にも機能する必要があります。 |
