---
title: Project Service Automation 更新プログラム リリース 33、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 33、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334560"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="a2555-103">Project Service Automation 更新プログラム リリース 33、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="a2555-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a2555-104">Microsoft Dynamics 365 Project Service Automation アプリの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="a2555-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="a2555-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2555-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a2555-106">Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="a2555-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a2555-107">このリリースに更新するには、Dynamics 365 管理センターのオンライン ソリューション ページにアクセスし、更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a2555-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="a2555-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2555-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a2555-109">このトピックには、Project Service Automation V3 更新プログラム 33 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="a2555-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="a2555-110">このバージョンのビルド番号は V3.10.54.98 で、一般的に 2021 年 7 月の自己更新プログラムを通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="a2555-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="a2555-111">更新プログラム 33</span><span class="sxs-lookup"><span data-stu-id="a2555-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a2555-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="a2555-112">Bug fixes</span></span>

<span data-ttu-id="a2555-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="a2555-113">**Time and Expense**</span></span>

<span data-ttu-id="a2555-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="a2555-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2555-115">2 つのロックされたフィールド、**msdyn_description** と **msdyn_externaldescription** は、送信後に編集可能です。</span><span class="sxs-lookup"><span data-stu-id="a2555-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="a2555-116">プロジェクトに関連しない経費を作成すると、エラーメッセージが表示される。</span><span class="sxs-lookup"><span data-stu-id="a2555-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="a2555-117">時間入力が作成されると、リソースロールが既定で非アクティブなロールとなる。</span><span class="sxs-lookup"><span data-stu-id="a2555-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="a2555-118">回収・削除された支出に関連する仕訳明細が削除されない。</span><span class="sxs-lookup"><span data-stu-id="a2555-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="a2555-119">**時間入力のクイック作成フォーム** で、**プロジェクト タスク リスト** のビューを更新して、既定で表示される日付をタスクの開始日に変更される。</span><span class="sxs-lookup"><span data-stu-id="a2555-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="a2555-120">予約可能なリソースの **関連** タブから時間入力を作成すると、親のブッキング可能なリソースではなく、サインインしているユーザーの時間入力が誤って作成されてしまうという問題が発生していました。</span><span class="sxs-lookup"><span data-stu-id="a2555-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="a2555-121">**一括承認 MDD** ダイアログ ボックスに新しいフィールドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a2555-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="a2555-122">**プロジェクト計画**</span><span class="sxs-lookup"><span data-stu-id="a2555-122">**Project planning**</span></span>

<span data-ttu-id="a2555-123">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="a2555-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="a2555-124">プロジェクトの作業時間テンプレートを複雑なカレンダーに適用すると、プロジェクトの作成パフォーマンスが低下してしまう問題がありました。</span><span class="sxs-lookup"><span data-stu-id="a2555-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="a2555-125">開始日が終了日よりも大きい場合、各フィールドの時間コンポーネントが異なるため、コピー プロジェクトのテンプレートにエラーが表示される。</span><span class="sxs-lookup"><span data-stu-id="a2555-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="a2555-126">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="a2555-126">**Resource management**</span></span>

<span data-ttu-id="a2555-127">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="a2555-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="a2555-128">リソース利用クエリで不正なパラメータが使用されており、その XML が原因で **リソース利用グリッド** のフィルター結果が不正になる問題が発生する。</span><span class="sxs-lookup"><span data-stu-id="a2555-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="a2555-129">**予約の延長** 確認で、予約の終了日が正しく表示されない。</span><span class="sxs-lookup"><span data-stu-id="a2555-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="a2555-130">**営業**</span><span class="sxs-lookup"><span data-stu-id="a2555-130">**Sales**</span></span>

<span data-ttu-id="a2555-131">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="a2555-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="a2555-132">値がない状態でカテゴリーの価格を作成するとエラーが発生する。</span><span class="sxs-lookup"><span data-stu-id="a2555-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="a2555-133">契約品目のマイルストーンを受注明細なしで作成した場合に、エラーが発生する。</span><span class="sxs-lookup"><span data-stu-id="a2555-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
