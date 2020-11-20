---
title: 完了時予測の更新
description: このトピックでは、プロジェクトの作業量予測の更新に関する説明をします。
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127209"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="872f2-103">完了時予測の更新</span><span class="sxs-lookup"><span data-stu-id="872f2-103">Update estimate at completion</span></span>

<span data-ttu-id="872f2-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="872f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="872f2-105">プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。</span><span class="sxs-lookup"><span data-stu-id="872f2-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="872f2-106">プロジェクトの再プロジェクションは、プロジェクトの現在の状態による、プロジェクト マネージャーの予測の認識です。</span><span class="sxs-lookup"><span data-stu-id="872f2-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="872f2-107">ただし、プロジェクトのベースラインは、プロジェクトのスケジュールおよびコスト見積もりに関する公表済みの真実のソースを表しており、これはプロジェクトの全利害関係者が既に合意しているため、プロジェクト マネージャーがベースライン値を変更することは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="872f2-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="872f2-108">プロジェクト マネージャーがタスクの工数を再プロジェクトするには 2 つの方法があります:</span><span class="sxs-lookup"><span data-stu-id="872f2-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="872f2-109">規定の完了見込み (ETC) をタスクの実際の残り工数の新たな見積もりで上書きします。</span><span class="sxs-lookup"><span data-stu-id="872f2-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="872f2-110">規定の進捗率をタスクの実際の残り工数の新しい見込みで上書きします。</span><span class="sxs-lookup"><span data-stu-id="872f2-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="872f2-111">これらのアプローチではそれぞれ、タスクの ETC、完了時予測 (EAC)、進捗率の再計算やタスクの予測工数差異を発生させます。</span><span class="sxs-lookup"><span data-stu-id="872f2-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="872f2-112">サマリー タスクの EAC、ETC、進捗率が再計算され、新たな工数分散の予測が作成されます。</span><span class="sxs-lookup"><span data-stu-id="872f2-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
