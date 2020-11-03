---
title: 他のユーザーがタイム エントリまたは経費を入力することを許可する
description: Project Service で他のユーザーがタイム エントリまたは経費を入力することを許可する方法
author: revathiMuthiah
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 7/31/2018
ms.topic: article
ms.author: revathim
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f56fae115b383d66a59cbcb08fffe95c83c83e17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079241"
---
# <a name="allow-someone-else-to-enter-your-time-entry-or-expense-project-service"></a><span data-ttu-id="cf1b7-103">他のユーザーがタイム エントリまたは経費を入力することを許可する (Project Service)</span><span class="sxs-lookup"><span data-stu-id="cf1b7-103">Allow someone else to enter your time entry or expense (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cf1b7-104">委任を設定し、誰か他のユーザーが [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] の代理になって時間または経費エントリを作成することを許可します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-104">Set up a delegate to let someone else make time or expense entries on your behalf in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  
  
## <a name="create-a-delegate"></a><span data-ttu-id="cf1b7-105">委任の作成</span><span class="sxs-lookup"><span data-stu-id="cf1b7-105">Create a delegate</span></span>  
  
1.  <span data-ttu-id="cf1b7-106">メイン メニューから、 **Project Service** > **委任** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-106">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="cf1b7-107">コマンド バーで、 **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-107">On the command bar, click **New**.</span></span>  
  
3. <span data-ttu-id="cf1b7-108">**名前** : レコードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-108">**Name** : Enter a name for the record.</span></span>  
  
4. <span data-ttu-id="cf1b7-109">**種類** : 代理人がユーザーの代わりに時間または経費のエントリを入力できるかどうかを選びます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-109">**Type** : Select whether the delegate can enter time or expense entries on your behalf.</span></span>  
  
5. <span data-ttu-id="cf1b7-110">**委任** : 代表人に選ぶ人の名前を選びます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-110">**Delegate** : Select the name of the person you want to be the delegate.</span></span>  
  
6. <span data-ttu-id="cf1b7-111">**開始および終了日** : 委任が始まるおよび終わる日付を選びます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-111">**Start and end dates** : Choose dates when delegation starts and ends.</span></span>  
  
7.  <span data-ttu-id="cf1b7-112">終了したら、 **保存して閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-112">When you're done, click **Save & Close**.</span></span>  
  
## <a name="turn-off-delegation"></a><span data-ttu-id="cf1b7-113">委任の無効化</span><span class="sxs-lookup"><span data-stu-id="cf1b7-113">Turn off delegation</span></span>  
  
1.  <span data-ttu-id="cf1b7-114">メイン メニューから、 **Project Service** > **委任** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-114">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="cf1b7-115">無効化する委任レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-115">Select the delegation record you want to turn off.</span></span>  
  
3.  <span data-ttu-id="cf1b7-116">コマンド バーで、 **非アクティブ化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-116">On the command bar, click **Deactivate**.</span></span>  
  
4.  <span data-ttu-id="cf1b7-117">**非アクティブ化の確認** ダイアログ ボックスで、 **非アクティブ化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-117">On the **Confirm Deactivation** dialog box, click **Deactivate**.</span></span>  
  
## <a name="enter-time-for-someone-else"></a><span data-ttu-id="cf1b7-118">誰か他のユーザーの時間を入力する</span><span class="sxs-lookup"><span data-stu-id="cf1b7-118">Enter time for someone else</span></span>  
  
1.  <span data-ttu-id="cf1b7-119">メイン メニューから、 **Project Service** > **時間エントリ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-119">From the main menu, click **Project Service** > **Time Entries**.</span></span>  
  
2.  <span data-ttu-id="cf1b7-120">コマンド バーで、 **リソース名** ドロップダウン・メニューを選び、自分が時間を入力しているユーザーの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-120">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering time for.</span></span>  
  
3.  <span data-ttu-id="cf1b7-121">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-121">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="cf1b7-122">これによりカレンダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-122">This brings up the calendar.</span></span> <span data-ttu-id="cf1b7-123">前の週または翌週のカレンダーを表示するには、 **前へ** または **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-123">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="cf1b7-124">現在の週に戻るには、 **今日** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-124">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="cf1b7-125">時間を入力するには、 **新規** をクリックするか、または時間を入力する日をカレンダーから探し、そこをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-125">To enter your time, either click **New** or double-click in the calendar under the day you want to enter time for.</span></span>  
  
6.  <span data-ttu-id="cf1b7-126">**時間入力** フォームのフィールドに記入し、 **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-126">Fill in the fields in the **Time Entry** form and click **Save**.</span></span>  
  
7.  <span data-ttu-id="cf1b7-127">週の時間の入力を続けます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-127">Continue entering time for the week.</span></span> <span data-ttu-id="cf1b7-128">入力を完了し、すべてが正しく思えたら、 **送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-128">When you’re done and everything looks correct, click **Submit**.</span></span>  
  
## <a name="enter-expenses-for-someone-else"></a><span data-ttu-id="cf1b7-129">他のユーザーの経費を入力する</span><span class="sxs-lookup"><span data-stu-id="cf1b7-129">Enter expenses for someone else</span></span>  
  
1.  <span data-ttu-id="cf1b7-130">メイン メニューから、 **Project Service** > **経費** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-130">From the main menu, click **Project Service** > **Expenses**.</span></span>  
  
2.  <span data-ttu-id="cf1b7-131">コマンド バーで、 **リソース名** ドロップダウン・メニューを選び、自分が経費を入力しているユーザーの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-131">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering expenses for.</span></span>  
  
3.  <span data-ttu-id="cf1b7-132">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-132">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="cf1b7-133">前の週または翌週のカレンダーを表示するには、 **前へ** または **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-133">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="cf1b7-134">現在の週に戻るには、 **今日** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-134">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="cf1b7-135">経費を入力するには、 **新規** を入力する</span><span class="sxs-lookup"><span data-stu-id="cf1b7-135">To enter an expense, either click **New**</span></span>  
  
6.  <span data-ttu-id="cf1b7-136">**新規経費** フォームのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-136">Fill in the fields in the **New Expense** form.</span></span> <span data-ttu-id="cf1b7-137">また、受領書も追加できます。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-137">You can also add receipts.</span></span>  
  
7.  <span data-ttu-id="cf1b7-138">終了してから **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b7-138">When you’re done, click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cf1b7-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf1b7-139">See Also</span></span>  
 [<span data-ttu-id="cf1b7-140">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="cf1b7-140">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
