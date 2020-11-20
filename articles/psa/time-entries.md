---
title: 時間エントリを作成する
description: このトピックでは、時間エントリ カレンダーの作成方法に関して説明します。
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
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131284"
---
# <a name="create-time-entries"></a><span data-ttu-id="9affc-103">時間エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="9affc-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9affc-104">Dynamics 365 Project Service Automation の以前のバージョンでは、時間エントリを週に一度のベースで実行しました。</span><span class="sxs-lookup"><span data-stu-id="9affc-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="9affc-105">Project Service Automation のバージョン 3 では、時間エントリを毎日入力します。</span><span class="sxs-lookup"><span data-stu-id="9affc-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="9affc-106">ただし、若干の時間エントリが作成された後、それらを一括作成する、またはコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9affc-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="9affc-107">時間エントリの作成</span><span class="sxs-lookup"><span data-stu-id="9affc-107">Create a time entry</span></span>

<span data-ttu-id="9affc-108">時間エントリを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9affc-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="9affc-109">**時間エントリ** のページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="9affc-110">**簡易作成: 時間エントリ** ダイアログ ボックスで、分数、時数、または日数単位で時間エントリの期間を入力します。</span><span class="sxs-lookup"><span data-stu-id="9affc-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="9affc-111">期間は *X* 分、*X* 時間、および *X* 日の形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9affc-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="9affc-112">時数および日数は、小数点を使用して、たとえば、*x.x* 時間または *x.x* 日などと入力できます。</span><span class="sxs-lookup"><span data-stu-id="9affc-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="9affc-113">時間エントリを入力する対象の時間エントリの種類およびプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="9affc-114">**プロジェクト タスク** フィールドでは、この時間エントリに関する作業を検索できます。</span><span class="sxs-lookup"><span data-stu-id="9affc-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9affc-115">ユーザーに割り当てられていないタスクに必要な時間エントリを作成する場合は、**プロジェクト タスク** フィールドで、**検索** ボタンをクリックして、**ビューを変更** を選択し、**すべてのアクティブなプロジェクト タスク** を選択してすべてのタスクをリストアップします。</span><span class="sxs-lookup"><span data-stu-id="9affc-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="9affc-116">説明が必要な場合、[説明] を選択し、**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="9affc-117">時間エントリを作成および保存すると、時刻エントリ グリッドで編集できます。</span><span class="sxs-lookup"><span data-stu-id="9affc-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="9affc-118">時間エントリ グリッドは、二つの形式をサポートします:</span><span class="sxs-lookup"><span data-stu-id="9affc-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="9affc-119">**hh: mm** フォームに時間エントリを入力できます。</span><span class="sxs-lookup"><span data-stu-id="9affc-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="9affc-120">この形式は、時数および端数に変換されます。</span><span class="sxs-lookup"><span data-stu-id="9affc-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="9affc-121">時数、端数を直接入力できます。</span><span class="sxs-lookup"><span data-stu-id="9affc-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="9affc-122">注意: 1 時間の端数は分単位ではありません。</span><span class="sxs-lookup"><span data-stu-id="9affc-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="9affc-123">したがって、1.5 時間は、1 時間 30 分を表します。</span><span class="sxs-lookup"><span data-stu-id="9affc-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="9affc-124">同一のルールがその日の端数に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9affc-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="9affc-125">1 日は 24 時間を表し、0.5 日は 12 時間を表します。</span><span class="sxs-lookup"><span data-stu-id="9affc-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="9affc-126">時間エントリを一括作成する</span><span class="sxs-lookup"><span data-stu-id="9affc-126">Bulk create time entries</span></span>

<span data-ttu-id="9affc-127">若干の時間エントリが作成された後にそれらをコピーして、別の時間エントリを一括作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="9affc-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="9affc-128">**時間エントリ** のページで、**週のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="9affc-129">**期間開始** フィールドのグループ内、**開始日** および **終了日** フィールドで、時間エントリをコピーする対象の日付範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="9affc-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="9affc-130">フィールド **期間に** フィールドのグループ内の **開始日** フィールドで、時間エントリを作成する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="9affc-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="9affc-131">**コピー** を選択して、**対象期間** フィールド グループで指定済みの曜日に対応している時間エントリのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9affc-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="9affc-132">たとえば、先週月曜日のエントリは、**対象期間** フィールド グループで指定された週の [月曜日] にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9affc-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="9affc-133">時間エントリのデータをインポートする</span><span class="sxs-lookup"><span data-stu-id="9affc-133">Import data for time entries</span></span>

<span data-ttu-id="9affc-134">プロジェクトの予約や割り当てからデータをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="9affc-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="9affc-135">データをインポートする場合、予約の日付範囲を指定してインポートし、その後、**下書き** 時間エントリとして作成されるべき予約を明示的に選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="9affc-136">グループ化、並べ替え、検索、およびフィルター機能</span><span class="sxs-lookup"><span data-stu-id="9affc-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="9affc-137">列で指定したディメンションによる時間エントリのグループ化およびフィルター処理ができます。</span><span class="sxs-lookup"><span data-stu-id="9affc-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="9affc-138">**グループ化** フィールドに、時間エントリのフィルター処理も使用するようにディメンションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9affc-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="9affc-139">列見出しの並べ替え矢印を使用して、時間軸の昇降順でエントリ レコードを並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="9affc-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="9affc-140">また、列見出しの **フィルター** ボタンを選び、さらに、**検索** ボックスで、時間エントリをプロジェクト名、プロジェクト タスク、時間エントリ、またはリソース別に、時間エントリの検索に使用するテキストを入力することによってエントリの表示/非表示の切り替えができます。</span><span class="sxs-lookup"><span data-stu-id="9affc-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
