---
title: プロジェクト ベンダーの請求書をキャンセルする
description: この記事では、Microsoft Dynamics 365 Project Operations でプロジェクト ベンダーの請求書をキャンセルする方法と、プロジェクト ベンダーの請求書をキャンセルした場合の財務上の影響について説明します。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911556"
---
# <a name="cancel-a-project-vendor-invoice"></a>プロジェクト ベンダーの請求書をキャンセルする

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

ベンダーの請求書を確定した後は、編集や削除ができません。 確定したベンダーの請求書にエラーがあった場合、キャンセル アクションを使用して、そのベンダーの請求書の影響を取り消し、新しいベンダーの請求書を作成することができます。

ベンダーの請求書で **キャンセル** を選択した場合、以下の動作が発生します:

1. ベンダーの請求書の状態が **キャンセル済** に更新されます。
2. キャンセルされた請求書とその関連レコードは読み取り専用となり、編集や削除ができなくなります。
3. 仕入先請求書の確認の一部として仕入先請求書明細に基づいて作成された原価実績は取り消されます。
4. 照合プロセスの一環として、ベンダーの請求書明細にコストの実績がリンクされていた場合、元のベンダーの請求書確認書ではそれが取り消されます。 ベンダーの請求書の取消時に、これらの原価実績が再作成されます。 原点は、時間、費用、または材料使用量のエントリを指します。
5. ベンダーの請求書をキャンセルした後、再び修正ジャーナルを作成し、時間エントリのリコールを処理し、元の時間、費用、材料の実績の承認をキャンセルすることができます。

> [!NOTE]
> 確認済みプロジェクトのベンダー請求書のみ取り消しできます。 他の状態のベンダーの請求書はキャンセルできません。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
