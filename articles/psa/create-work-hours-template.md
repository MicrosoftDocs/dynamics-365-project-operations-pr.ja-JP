---
title: 作業時間テンプレートの作成
description: Project Service での作業時間テンプレートの作成方法
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a0fce327587940e557e0214c8c0897116ac91901
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133059"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="cecd9-103">作業時間テンプレートの作成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="cecd9-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cecd9-104">プロジェクト スケジュールを作成できるようにするには、スケジュールおよび休業日で、1 日分に対応する作業時間数を定義するプロジェクト カレンダーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cecd9-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="cecd9-105">1 日の作業時間、休暇、およびその他の休業日に関する詳細を含む、作業時間テンプレートでこれを行います。</span><span class="sxs-lookup"><span data-stu-id="cecd9-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="cecd9-106">プロジェクトを作成するとき、作業テンプレートをプロジェクト カレンダーに関連付けて、プロジェクトのスケジュールを適用します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="cecd9-107">作業時間テンプレートを作成する方法は 2 つあります:</span><span class="sxs-lookup"><span data-stu-id="cecd9-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="cecd9-108">リソースのカレンダーに基づいて作業時間テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="cecd9-109">新しい作業時間テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="cecd9-110">リソースのカレンダーに基づいて作業時間テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="cecd9-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="cecd9-111">**Project Service > リソース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="cecd9-112">作業時間に基づかせるリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="cecd9-113">**カレンダーに名前を付けて保存** をクリックして、作業時間テンプレートに名前を入力してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cecd9-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="cecd9-114">オプションの変更を終了したら、**保存して閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cecd9-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="cecd9-115">画面の右下隅の **保存** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cecd9-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="cecd9-116">新しい作業時間テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="cecd9-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="cecd9-117">**Project Service > 作業時間テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cecd9-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="cecd9-118">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cecd9-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="cecd9-119">作業時間テンプレートに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="cecd9-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="cecd9-120">作業時間を基づかせるするリソースを選択してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cecd9-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cecd9-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="cecd9-121">See Also</span></span>  
 [<span data-ttu-id="cecd9-122">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="cecd9-122">Set up resources</span></span>](../psa/set-up-resources.md)
