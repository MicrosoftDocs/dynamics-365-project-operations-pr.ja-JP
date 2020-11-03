---
title: プロジェクトの状態について
description: このトピックでは、Dynamics 365 Project Operations においてプロジェクトに割り当てられた状態ついて説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079140"
---
# <a name="understand-project-status"></a><span data-ttu-id="1a8ff-103">プロジェクトの状態について</span><span class="sxs-lookup"><span data-stu-id="1a8ff-103">Understand project status</span></span>

<span data-ttu-id="1a8ff-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1a8ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1a8ff-105"> **プロジェクト エンティティ**  ページの **状態** セクションに、コストと労力に基づいたプロジェクトの正常性の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="1a8ff-106">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="1a8ff-106">Status summary fields</span></span>

- <span data-ttu-id="1a8ff-107"> **プロジェクト全体のステータス**  フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="1a8ff-108">このフィールドは、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="1a8ff-109"> **コメント**  フィールドでは、プロジェクト マネージャーは状態について特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="1a8ff-110"> **状態更新日** フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="1a8ff-111">このフィールドの値は、状態が最後に更新された日時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="1a8ff-112"> **スケジュール パフォーマンス**  フィールドと **コスト パフォーマンス**  フィールドは追跡グリッドから設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="1a8ff-113"> **工数の追跡**  ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドは **先行** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="1a8ff-114">ルート ノードのスケジュールとコスト差異がマイナスの場合、これらのフィールドは **遅延** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
