---
title: Project Operations におけるベンダーと購入価格表の管理
description: このトピックでは、外注のベンダー データと購入価格表を作成および維持するのに役立つ情報について説明します。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576736"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Project Operations におけるベンダーと購入価格表の管理

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

## <a name="vendors-in-project-operations"></a>Project Operations のベンダー

Microsoft Dynamics 365 Project Operations では、ベンダー勘定の関係タイプは、**ベンダー** または **サプライヤー** です。 外注のベンダーとして、関係タイプのいずれかを持つ取引先企業レコードのみを選択することができます。

1 つ以上の購入価格表をベンダー レコードに関連付けることができます。 ただし、ベンダー レコードに関連付けられている各購入価格表には、異なる日付の有効性が必要です。 プロジェクト価格表の日付の有効性の重複は、Project Operations ではサポートされていません。

既定では、ベンダー レコードの以下のフィールドと概念が、ベンダー用に登録された外注に使用されます。

- 支払条件
- 請求先担当者
- 取引先責任者

    > [!NOTE]
    > 既定では、外注ベンダーの取引先企業マネージャーとしてベンダーの取引先担当者が使用されます。

- 通貨
- 最新の購買価格表

## <a name="purchase-price-lists-in-project-operations"></a>Project Operations の購入価格表

**コンテキスト** フィールドが **購入** に設定されている価格表は、購入価格表と見なされます。 購入価格表を定義して、時間、費用、材料の購入率のカタログを表すことができます。 購入価格表は、Project Operations のコストおよび販売価格表に似ています。 次の概念は、コストおよび販売価格表に適用されるのと同じ方法で、購入価格リストに適用されます。

- **日付の有効性** – 購入価格表には日付の有効性があります。 日付の有効性は、各価格表の開始日フィールドと終了日フィールドで表されます。 開始日から終了日までの期間が有効期間です。
- **通貨** – 価格表ヘッダーの通貨は、カタログ内の人件費、経費カテゴリ、製品の購入価格が表される通貨として使用されます。
- **既定の時間単位** – 既定の時間単位は、購入の人件費を表します。 価格表の時間単位フィールドは、既定値を提供するためにのみ使用されます。 その値は、個々の役割の価格行で変更できます。

購入価格表は、プロジェクト価格表と呼ばれる関連付けとしてベンダー レコードに添付できます。 これらの価格表は、外注品目の既定価格を入力するために使用されます。 既定では、複数の購入価格表がベンダー レコードに添付されている場合、ベンダー用に作成された外注には最新の価格表が使用されます。 **コンテキスト** フィールドが **購入** に設定されている価格表のみがベンダー レコードに添付できます。

### <a name="subcontract-specific-purchase-price-lists"></a>外注固有の購入価格表

購入価格表は、プロジェクト価格表と呼ばれる関連付けとして外注にも添付できます。 これらの価格表は、外注品目の既定価格を入力するために使用されます。 既定では、複数の購入価格表が外注に添付されている場合、それぞれに異なる日付の有効性が必要です。 重複する日付の有効性がある購入価格表は、Project Operations ではサポートされていません。 **コンテキスト** フィールドが **購入** に設定されている価格表のみが外注に添付できます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
