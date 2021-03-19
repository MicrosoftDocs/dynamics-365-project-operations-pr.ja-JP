---
title: プロジェクトの状態について
description: このトピックは、Dynamics 365 Project Operations のプロジェクトに割り当てられたステータスに関する情報を提供します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286479"
---
# <a name="understand-project-status"></a><span data-ttu-id="d65dc-103">プロジェクトの状態について</span><span class="sxs-lookup"><span data-stu-id="d65dc-103">Understand project status</span></span>

<span data-ttu-id="d65dc-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="d65dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d65dc-105">**プロジェクト エンティティ** ページの **状態** セクションには、コストと労力に基づいたプロジェクトの正常性の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d65dc-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="d65dc-106">ステータス サマリー フィールド</span><span class="sxs-lookup"><span data-stu-id="d65dc-106">Status summary fields</span></span>

- <span data-ttu-id="d65dc-107">**プロジェクト全体のステータス** フィールドは、プロジェクト全体のステータスを表示する、編集可能なフィールドです。</span><span class="sxs-lookup"><span data-stu-id="d65dc-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="d65dc-108">このフィールドは、リスクの拡大を示す、緑、黄色、赤などの色分けも使用します。</span><span class="sxs-lookup"><span data-stu-id="d65dc-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="d65dc-109">**コメント** フィールドでは、プロジェクト マネージャーはステータスについて特定のコメントを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="d65dc-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="d65dc-110">**状態更新日** フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="d65dc-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="d65dc-111">このフィールドの値は、状態が最後に更新された日時を示すタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="d65dc-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="d65dc-112">**スケジュール効率** フィールドと **コスト効率** フィールドは追跡グリッドから設定されます。</span><span class="sxs-lookup"><span data-stu-id="d65dc-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="d65dc-113">**工数の追跡** ビューのルート ノードのスケジュールとコスト差異がプラスの場合、これらのフィールドは **先行** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="d65dc-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="d65dc-114">ルート ノードのスケジュールとコスト差異がマイナスの場合、これらのフィールドは **遅延** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d65dc-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]