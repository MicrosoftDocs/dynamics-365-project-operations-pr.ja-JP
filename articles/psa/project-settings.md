---
title: プロジェクト設定
description: このトピックでは、プロジェクト管理の設定について説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998327"
---
# <a name="project-settings"></a><span data-ttu-id="673ea-103">プロジェクト設定</span><span class="sxs-lookup"><span data-stu-id="673ea-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="673ea-104">プロジェクト計画機能にアクセスするには、次の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="673ea-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="673ea-105">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="673ea-105">Work template</span></span>

<span data-ttu-id="673ea-106">プロジェクト スケジュールを作成するには、1 日分に対応する作業時間数と休業日を定義するプロジェクト カレンダー テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="673ea-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="673ea-107">プロジェクトのカレンダー テンプレートを作成するには、プロジェクトの **カレンダー テンプレート** フィールドで、作業テンプレートを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="673ea-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="673ea-108">作業テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="673ea-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="673ea-109">PSA の左ナビゲーション ウィンドウで、**リソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673ea-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="673ea-110">**リソース** リスト ページで、ユーザー レコードを開き、**作業時間を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="673ea-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="673ea-111">ブラウザー ページでポップアップを許可していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="673ea-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="673ea-112">これにより、そのリソースに設定された作業時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="673ea-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="673ea-113">**月単位ビュー** タブで、**設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673ea-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="673ea-114">次の 3 つのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="673ea-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="673ea-115">新しい週単位スケジュール</span><span class="sxs-lookup"><span data-stu-id="673ea-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="673ea-116">1 日の作業スケジュール</span><span class="sxs-lookup"><span data-stu-id="673ea-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="673ea-117">休暇</span><span class="sxs-lookup"><span data-stu-id="673ea-117">Time Off</span></span>

> ![オプションの設定](media/project-13.png)

4. <span data-ttu-id="673ea-119">**新規週単位スケジュール** を選択し、このリソース スケジュールのオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="673ea-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="673ea-120">定期的な週単位のスケジュール、毎日の時間パラメーター、休業日の設定などを設定できます。</span><span class="sxs-lookup"><span data-stu-id="673ea-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="673ea-121">日付の範囲を設定して、**保存** を選択し、**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673ea-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="673ea-122">**リソース** リストページへ戻り、作業時間のために設定するリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="673ea-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="673ea-123">作業テンプレートを設定するには、**カレンダーを次のとおり設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="673ea-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="673ea-124">**作業テンプレート** ダイアログ ボックスで、作業テンプレートの名前を入力し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="673ea-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="673ea-125">ここで、プロジェクトのカレンダー テンプレートがある作業テンプレートを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="673ea-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="673ea-126">リソースのロール</span><span class="sxs-lookup"><span data-stu-id="673ea-126">Resource roles</span></span>

<span data-ttu-id="673ea-127">*リソース ロール* という用語は、プロジェクトで特定のタスク セットを実行するために必要なスキル、コンピテンシー、および認定資格のセットを指します。</span><span class="sxs-lookup"><span data-stu-id="673ea-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="673ea-128">PSA は、リソースが関連付けられているロールに基づいたリソースの時間のコストと請求を可能にします。</span><span class="sxs-lookup"><span data-stu-id="673ea-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="673ea-129">どの組織も **Project Service** メニューの左ナビゲーションを使用して、これらのロールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="673ea-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="673ea-130">どの組織も **アクティブなリソース カテゴリ** ページで、これらのロールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="673ea-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="673ea-131">このページを開くには、左のナビゲーション ウィンドウで、**リソース ロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="673ea-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="673ea-132">価格表</span><span class="sxs-lookup"><span data-stu-id="673ea-132">Price lists</span></span>

<span data-ttu-id="673ea-133">価格表は、リソース ロール、経費カテゴリ、製品、そして組織のその他要素のコストと販売価格の設定ができます。</span><span class="sxs-lookup"><span data-stu-id="673ea-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="673ea-134">プロジェクトに届ける必要がある財務見積もりを設定する前に、バッキング コストと販売価格表を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="673ea-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="673ea-135">パラメーター セクションでは、組織で作成されたすべてのプロジェクトに適用される既定のコストと販売価格表も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="673ea-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="673ea-136">**アクティブなプロジェクト パラメーター** ページで、既定のコストと販売価格リストを必ず設定してください。</span><span class="sxs-lookup"><span data-stu-id="673ea-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]