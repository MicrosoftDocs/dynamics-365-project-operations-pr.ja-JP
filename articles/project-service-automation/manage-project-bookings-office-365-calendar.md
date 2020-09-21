---
title: Office 365 カレンダーでプロジェクトおよび予約を管理する
description: Office 365 カレンダーでプロジェクトおよび予約を管理する方法
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752772"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="dee5e-103">カレンダーでプロジェクトおよび予約を管理する (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dee5e-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="dee5e-104">廃止: この機能は廃止され、使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="dee5e-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="dee5e-105">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーを使用して個人的な予定、プロジェクト ワークの予約、および Field Service の作業指示書の割り当てを表示します。</span><span class="sxs-lookup"><span data-stu-id="dee5e-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="dee5e-106">1 つの場所にすべてがあるので、1 日の管理が容易です。</span><span class="sxs-lookup"><span data-stu-id="dee5e-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="dee5e-107">あなたの会議、予定、予約およびタスクはすべて [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーで利用できます。</span><span class="sxs-lookup"><span data-stu-id="dee5e-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="dee5e-108">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用している場合、Project Service の時間エントリ ビュー内で個人的な予定も入力できます。</span><span class="sxs-lookup"><span data-stu-id="dee5e-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="dee5e-109">これにより、プロジェクトおよびリソースの管理者は、プロジェクトにあなたが参加可能かどうかを知ることができます。</span><span class="sxs-lookup"><span data-stu-id="dee5e-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="dee5e-110">これにより、個人の予定を 2 回入力する必要がないために、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="dee5e-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="dee5e-111">カレンダーから Project Service の時間エントリ ビューに個人の予定をインポートするだけです。</span><span class="sxs-lookup"><span data-stu-id="dee5e-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="dee5e-112">カレンダーは今日から次の 4 週間のプロジェクトと作業指示書の予約を同期します。</span><span class="sxs-lookup"><span data-stu-id="dee5e-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="dee5e-113">この設定は変更できません。</span><span class="sxs-lookup"><span data-stu-id="dee5e-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="dee5e-114">同期は、PSA から [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーへの 1 方向のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="dee5e-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="dee5e-115">逆の順序での同期ができます。</span><span class="sxs-lookup"><span data-stu-id="dee5e-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="dee5e-116">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーの使用方法に関する詳細は、「[ビジネス用 Outlook on the web カレンダー](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dee5e-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="dee5e-117">セットアップ</span><span class="sxs-lookup"><span data-stu-id="dee5e-117">Setup</span></span>  
 <span data-ttu-id="dee5e-118">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーで予約の表示および管理をする前に、いくつかの事柄を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee5e-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="dee5e-119">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] のグローバル管理者、またはシステム管理者の資格情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="dee5e-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="dee5e-120">管理者は、電子メール サーバー のプロファイルを設定する必要があります。また各ユーザーは各自のメールボックスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee5e-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dee5e-121">[サーバー側の同期による電子メールの処理のセットアップ](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="dee5e-121">[Set up email processing through server-side synchronization](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="dee5e-122">自分の組織の同期を有効にする (管理者のタスク)</span><span class="sxs-lookup"><span data-stu-id="dee5e-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="dee5e-123">メイン メニューから**設定** >  **管理**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="dee5e-124">**システムの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="dee5e-125">**同期**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="dee5e-126">**リソース予約の同期を、何と有効にするかどうかを選択する**で、**リソース予約を Outlook と同期する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="dee5e-127">ユーザー プロファイルに対する同期を有効にする (ユーザー タスク)</span><span class="sxs-lookup"><span data-stu-id="dee5e-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="dee5e-128">画面の右上にある**設定**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="dee5e-129">**オプション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="dee5e-130">**同期**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="dee5e-131">**リソース予約を Outlook と同期する**で、**Outlook とリソース予約の同期**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="dee5e-132">個人の予定をインポートする (ユーザー タスク)</span><span class="sxs-lookup"><span data-stu-id="dee5e-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="dee5e-133">カレンダーから Project Service Automation の時間エントリ ビューに個人の予定をインポートします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="dee5e-134">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーを開き、**データのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="dee5e-135">フィルター画面で、**Exchange の予定**を選択し、次に**適用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="dee5e-136">システムは、現在の週から推奨されたエントリとして、時間エントリ ビューから予定を取得します。</span><span class="sxs-lookup"><span data-stu-id="dee5e-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="dee5e-137">別の週のためのエントリを追加するには、**前へ**または**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="dee5e-138">Project Service Automation の時間エントリ ビューに加える予定を選択して下さい。</span><span class="sxs-lookup"><span data-stu-id="dee5e-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="dee5e-139">**時間入力**ポップアップ ボックスで、適切なオプションを選択して、Project Service Automation の時間エントリ ビューに予定を変換します。</span><span class="sxs-lookup"><span data-stu-id="dee5e-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="dee5e-140">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee5e-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dee5e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="dee5e-141">See Also</span></span>  
 [<span data-ttu-id="dee5e-142">時間、経費、および共同作業ガイド</span><span class="sxs-lookup"><span data-stu-id="dee5e-142">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
