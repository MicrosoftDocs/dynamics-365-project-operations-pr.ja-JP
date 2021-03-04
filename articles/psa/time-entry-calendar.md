---
title: 時間エントリ カレンダー
description: このトピックでは、時間エントリ カレンダーの使用方法に関する情報を提供します。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 94e580955b83b9f2eaf6c0487cc9fe8a30f51ce0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150179"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="19838-103">時間エントリ カレンダー</span><span class="sxs-lookup"><span data-stu-id="19838-103">Time entry calendar</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="19838-104">**時間エントリ** ページで **表示方法** \> **カレンダー コントロール** を選択すれば、カレンダーの時刻エントリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="19838-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="19838-105">カレンダー コントロールの更新</span><span class="sxs-lookup"><span data-stu-id="19838-105">Updated calendar control</span></span>

<span data-ttu-id="19838-106">Dynamics 365 Project Service Automation では、新規および拡張可能時間エントリ エクスペリエンスをご楽しみいただけます。</span><span class="sxs-lookup"><span data-stu-id="19838-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="19838-107">この新しいエクスペリエンスによって、旧バージョンで使用されたカスタム カレンダー コントロールが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="19838-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="19838-108">ただし、まだ、統一インターフェイス フレームワークから日毎、週毎、あるいは月毎のビューで提供されている読み取り専用カレンダー コントロールを使用して時間エントリを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="19838-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="19838-109">カレンダーは個々のカレンダー アイテムの操作をサポートしていないため、送信または削除する場合に 1 つ以上のカレンダー アイテムは選択できません。</span><span class="sxs-lookup"><span data-stu-id="19838-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="19838-110">代わりに、カレンダーの項目を選択して、必要な操作を完了できる **時間エントリ** のエンティティ ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="19838-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="19838-111">機能拡張</span><span class="sxs-lookup"><span data-stu-id="19838-111">Extensibility</span></span>

<span data-ttu-id="19838-112">時間エントリ グリッドのある **時間エントリ** ページで、ユーザー定義フィールドを追加して、検索フィールドを設定し、カスタム ビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="19838-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="19838-113">カスタム フィールドで選択済みまたは入力済みの値に基づくカスタム ビジネス ロジックを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="19838-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
