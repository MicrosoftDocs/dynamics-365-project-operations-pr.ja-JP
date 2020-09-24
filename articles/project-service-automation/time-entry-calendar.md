---
title: 時間エントリ カレンダー
description: このトピックでは、時間エントリ カレンダーの使用方法に関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752897"
---
# <a name="time-entry-calendar"></a>時間エントリ カレンダー

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

**時間エントリ** ページで **表示方法** \> **カレンダー コントロール** を選択すれば、カレンダーの時刻エントリを表示できます。

## <a name="updated-calendar-control"></a>カレンダー コントロールの更新

Dynamics 365 Project Service Automation では、新規および拡張可能時間エントリ エクスペリエンスをご楽しみいただけます。 この新しいエクスペリエンスによって、旧バージョンで使用されたカスタム カレンダー コントロールが置き換えられます。 ただし、まだ、統一インターフェイス フレームワークから日毎、週毎、あるいは月毎のビューで提供されている読み取り専用カレンダー コントロールを使用して時間エントリを表示することもできます。

カレンダーは個々のカレンダー アイテムの操作をサポートしていないため、送信または削除する場合に 1 つ以上のカレンダー アイテムは選択できません。 代わりに、カレンダーの項目を選択して、必要な操作を完了できる **時間エントリ** のエンティティ ページを開きます。

## <a name="extensibility"></a>機能拡張

時間エントリ グリッドのある **時間エントリ** ページで、ユーザー定義フィールドを追加して、検索フィールドを設定し、カスタム ビューを作成できます。 カスタム フィールドで選択済みまたは入力済みの値に基づくカスタム ビジネス ロジックを設定することもできます。