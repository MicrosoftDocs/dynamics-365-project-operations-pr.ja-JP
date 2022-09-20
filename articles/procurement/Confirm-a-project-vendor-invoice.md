---
title: プロジェクトのベンダー請求書の確認
description: この記事では、Microsoft Dynamics 365 Project Operations でプロジェクト ベンダーの請求書を確認する方法と、プロジェクト ベンダーの請求書を確認した場合の財務上の影響について説明します。
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475425"
---
# <a name="confirm-project-vendor-invoices"></a>プロジェクトのベンダー請求書の確認

_ **適用対象:** リソース/非在庫ベースのシナリオの Project Operations

**PM による手動確認が必須** パラメーターが有効な場合、Microsoft Dataverse で作成されたベンダー インボイスは **下書き** 状態になります。 この方法で作成されたベンダーの請求書は、レビューし、手動で確認する必要があります。 **PM による手動確認が必須** パラメーターが無効な場合、Dataverse で作成されたベンダーの請求書が自動的に確認されます。 これ以上のアクションは不要です。 

Dynamics 365 Project Operations でベンダーの請求書のすべての行を確認した後、**確認** を選択することでベンダーの請求書を確認することができます。

ベンダーの請求書で **確認** を選択した場合、以下の動作が発生します:

1. ベンダーの請求書の状態が **確認済** に更新されます。
1. 確認された請求書とその関連レコードは読み取り専用となり、編集や削除ができなくなります。
1. 照合プロセスの一環として、原価実績がベンダーの請求書の明細行を参照した場合、参照されたベンダーの請求書の明細行に関連するすべての原価実績が取り消されます。
1. 新しい原価実績は、ベンダー請求書明細行の情報を使用して作成されます。
1. 修正仕訳帳の作成、時間エントリのリコール処理、取り消された元の時間、費用、材料の実績の承認の取り消しができなくなります。
1. Dynamics 365 Finance では、プロジェクト統合仕訳帳を使用して **プロジェクト コスト** 値を更新し、プロジェクト統合ジャーナルを計上した後に調達統合仕訳帳を *取り消し* ます。

> [!NOTE]
> ベンダー請求書のいずれかの行の検証ステータスが **完了** 以外の場合、当該のベンダー請求書を確認することはできません。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
