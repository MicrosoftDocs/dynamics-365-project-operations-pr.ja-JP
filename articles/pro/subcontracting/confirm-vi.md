---
title: プロジェクトのベンダーの請求書を確認する
description: この記事では、Microsoft Dynamics 365 Project Operations でプロジェクト ベンダーの請求書を確認する方法と、プロジェクト ベンダーの請求書を確認した場合の財務上の影響について説明します。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261517"
---
# <a name="confirm-a-project-vendor-invoice"></a>プロジェクトのベンダーの請求書を確認する

_**適用対象:** ライト展開 - 見積もり請求の取引_

Microsoft Dynamics 365 Project Operations でベンダーの請求書のすべての行を確認した後、確認アクションを使用してベンダーの請求書を確認することができます。

ベンダーの請求書で **確認** を選択した場合、以下の動作が発生します:

1. ベンダーの請求書の状態が **確認済** に更新されます。
2. 確認された請求書とその関連レコードは読み取り専用となり、編集や削除ができなくなります。
3. 照合プロセスの一環として、原価実績がベンダーの請求書の明細行を参照した場合、参照されたベンダーの請求書の明細行に関連するすべての原価実績が取り消されます。
4. 新しい原価実績は、ベンダー請求書明細行の情報を使用して作成されます。
5. ベンダーの請求書を確認した後、修正仕訳帳の作成、時間エントリのリコール処理、取り消された元の時間、費用、材料の実績の承認を取り消すことはできなくなります。

> [!NOTE]
> ベンダー請求書のいずれかの行の検証ステータスが **完了** 以外の場合、当該のベンダー請求書を確認することはできません。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
