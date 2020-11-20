---
title: 2020年 リリース予定 第1群 Project Service Automation バージョン 3.x の最新情報または変更事項
description: このトピックでは、Project Service Automation バージョン 3、2020年 リリース予定 第1群の新機能と変更点について説明します。
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126489"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="39279-103">2020年 リリース予定 第1群 Project Service Automation バージョン 3 の最新情報または変更事項</span><span class="sxs-lookup"><span data-stu-id="39279-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="39279-104">トピックは、2020年 リリース予定 第1群 Project Service Automation（PSA）バージョン3.x の最新リリースに移行する際の、アップグレードに関する重要な考慮事項を説明します。</span><span class="sxs-lookup"><span data-stu-id="39279-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="39279-105">時間エントリ</span><span class="sxs-lookup"><span data-stu-id="39279-105">Time entry</span></span>
<span data-ttu-id="39279-106">時間エントリのエクスペリエンスが拡張されており、より多くの顧客のシナリオに時間エントリを拡張する機能が提供されています。</span><span class="sxs-lookup"><span data-stu-id="39279-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="39279-107">これには、入力タイプを追加する機能が含まれており、 **時間ソース** として表示されるフィールドのスキーマ名 **時間エントリ設定** に基づいて特定の動作が実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="39279-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="39279-108">この機能をサポートするために、時間、経費、ステータス、および承認 (TESA) と呼ばれる新しいソリューションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="39279-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="39279-109">アップグレードに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="39279-109">Upgrade consideration</span></span>
<span data-ttu-id="39279-110">この機能に対応するにあたり、PSA 内のロールが更新され、新しい権限が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="39279-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="39279-111">これらの権限は、新たなエンティティである **時間エントリ設定** の読み取り権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="39279-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="39279-112">時間を記録する機能を必要とするユーザーには、既存の役割に加えてユーザー役割 **時間エントリ ユーザー** を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39279-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="39279-113">このロールには新しい機能が含まれており、時間エントリが引き続き動作するように機能します。</span><span class="sxs-lookup"><span data-stu-id="39279-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="39279-114">さらに、時間エントリ エンティティのすべてのフォームを含むカスタム アプリ モジュールがある場合、モジュールから **TESA 時間エントリの簡易作成フォーム** を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39279-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="39279-115">現行の拡張時間エントリにおける変更点</span><span class="sxs-lookup"><span data-stu-id="39279-115">Currently extended time entry changes</span></span>
<span data-ttu-id="39279-116">時間エントリの現在のユーザーへの影響を最小限に抑えるために、このロールにされた変更は時間エントリを継続して使用するにあたって必要となる唯一の主要要件です。</span><span class="sxs-lookup"><span data-stu-id="39279-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="39279-117">カスタム ビューまたは個別の時間エントリ エクスペリエンスを作成している場合は、 **時間エントリ設定** フィールドに正しい PSA 値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39279-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
