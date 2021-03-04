---
title: Project Service Automation 更新プログラム リリース 21、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 21、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147029"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="2b53b-103">Project Service Automation 更新プログラム リリース 21、V3</span><span class="sxs-lookup"><span data-stu-id="2b53b-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2b53b-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="2b53b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2b53b-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b53b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2b53b-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="2b53b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2b53b-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="2b53b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2b53b-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b53b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2b53b-109">このトピックには、Project Service Automation V3 更新プログラム 21 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="2b53b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="2b53b-110">このバージョンのビルド番号は V 3.10.32.50 であり、2020 年 6 月のセルフ アップデートを通じて一般提供されました。</span><span class="sxs-lookup"><span data-stu-id="2b53b-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="2b53b-111">更新プログラム 21</span><span class="sxs-lookup"><span data-stu-id="2b53b-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2b53b-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="2b53b-112">Bug fixes</span></span>

<span data-ttu-id="2b53b-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="2b53b-113">**Time and Expense**</span></span>

<span data-ttu-id="2b53b-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="2b53b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b53b-115">ダッシュボードで **時間エントリ グリッド コントロール** をホストする場合、グリッドはダッシュボード グリッド コンテナーの幅全体を利用しません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="2b53b-116">特定のタイム ゾーンでは、**時間エントリ** グリッド コントロールはレコードを表示しません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="2b53b-117">午後 9 時より後の時間エントリは、誤った日付に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b53b-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="2b53b-118">ユーザーは、経費カテゴリ **経費の領収書が必要** に値がない場合、経費を送信できません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="2b53b-119">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="2b53b-119">**Resource Management**</span></span>

<span data-ttu-id="2b53b-120">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="2b53b-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b53b-121">非アクティブな予約は、**調整** ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b53b-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="2b53b-122">汎用リソースフルフィルメントには、有効な予約状態が存在することを確認する検証がありませんでした。</span><span class="sxs-lookup"><span data-stu-id="2b53b-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="2b53b-123">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="2b53b-123">**Project Management**</span></span>

<span data-ttu-id="2b53b-124">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="2b53b-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b53b-125">**プロジェクト** フォーム グリッド (**リソース割り当て**、**タスク**、**調整** ビュー、**経費の見積もり**) は、プロジェクトがアクティブでない場合でも編集可能です。</span><span class="sxs-lookup"><span data-stu-id="2b53b-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="2b53b-126">重複する顧客は、確認済みのプロジェクト契約にリンクされている顧客とマージすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="2b53b-127">有効なカレンダーを持たないリソースが追加された場合、システムはユーザー フレンドリーなエラー メッセージを返しません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="2b53b-128">タスク グリッドの **タスクの追加** ボタンは、プロジェクトが **Microsoft Project アドイン** にリンクされている場合に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2b53b-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="2b53b-129">カテゴリのあるタスクが、原価価格が定義されているロールを持つリソースに割り当てられると、工数が制御不能に増加します。</span><span class="sxs-lookup"><span data-stu-id="2b53b-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="2b53b-130">**営業**</span><span class="sxs-lookup"><span data-stu-id="2b53b-130">**Sales**</span></span>

<span data-ttu-id="2b53b-131">次の機能強化が行われました:</span><span class="sxs-lookup"><span data-stu-id="2b53b-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="2b53b-132">**請求頻度** と **請求開始** は **請求書スケジュール** タブに移動されました。</span><span class="sxs-lookup"><span data-stu-id="2b53b-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="2b53b-133">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="2b53b-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b53b-134">**ロール** の合計販売価格がゼロではない場合でも、**カテゴリー** の **合計販売価格** は ゼロ (0) です。</span><span class="sxs-lookup"><span data-stu-id="2b53b-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="2b53b-135">別のカスタマイズ プロセスが追加フィールドを更新している場合、顧客は **請求書の状況** フィールドの値を **請求準備完了** に変更できません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="2b53b-136">**請求明細行の更新** ボタンを繰り返し選択すると、複数の重複する明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2b53b-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="2b53b-137">**価格の更新** ボタンが、**簡易表示** フォームの **ロール価格** サブグリッドで機能しません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="2b53b-138">**販売価格表の解決** ロジックがタイムゾーンを不適切に処理するため、価格表の選択が正しく行われません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="2b53b-139">プロジェクトの **実際の合計コスト** は、1 回の時間エントリが承認された後、端数でオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2b53b-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="2b53b-140">**価格解決** ロジックでは、**取得した RolePrice** が **'標準出荷単位'** と **'標準出荷単位の価格'** フィールドに値を持たない場合、ユーザー フレンドリなエラー メッセージを提供しません。</span><span class="sxs-lookup"><span data-stu-id="2b53b-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
