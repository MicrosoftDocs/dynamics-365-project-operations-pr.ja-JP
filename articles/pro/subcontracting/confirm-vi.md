---
title: プロジェクトのベンダーの請求書を確認する
description: このトピックでは、Microsoft Dynamics 365 Project Operations でプロジェクト ベンダーの請求書を確認する方法と、プロジェクト ベンダーの請求書を確認した場合の財務上の影響について説明します。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595734"
---
# <a name="confirm-a-project-vendor-invoice"></a>プロジェクトのベンダーの請求書を確認する

[!include [banner](../../includes/dataverse-preview.md)]

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
