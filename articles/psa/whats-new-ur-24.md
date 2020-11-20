---
title: Project Service Automation 更新プログラム リリース 24、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 24、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126579"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="000a2-103">Project Service Automation 更新プログラム リリース 24、V3</span><span class="sxs-lookup"><span data-stu-id="000a2-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="000a2-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="000a2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="000a2-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="000a2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="000a2-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="000a2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="000a2-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="000a2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="000a2-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="000a2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="000a2-109">このトピックには、Project Service Automation V3 更新プログラム 24 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="000a2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="000a2-110">このバージョンのビルド番号は V 3.10.42.43 であり、一般的には 2020 年 10 月の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="000a2-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="000a2-111">更新プログラム 24</span><span class="sxs-lookup"><span data-stu-id="000a2-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="000a2-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="000a2-112">Bug fixes</span></span>

<span data-ttu-id="000a2-113">**営業**</span><span class="sxs-lookup"><span data-stu-id="000a2-113">**Sales**</span></span>

<span data-ttu-id="000a2-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="000a2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="000a2-115">製品の既定の価格表を設定する際の問題。</span><span class="sxs-lookup"><span data-stu-id="000a2-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="000a2-116">価格表とロール価格レコードのコピーが埋め込まれているため、見積もり獲得のパフォーマンスは遅くなります。</span><span class="sxs-lookup"><span data-stu-id="000a2-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="000a2-117">**プロジェクト契約/営業ハブ** > **製品品目/注文明細行の数量** は、最も近い整数に自動的に丸められます。</span><span class="sxs-lookup"><span data-stu-id="000a2-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="000a2-118">価格表の読込み時にシステム特権に引き上げます。</span><span class="sxs-lookup"><span data-stu-id="000a2-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="000a2-119">顧客の住所フィールド **address1_freighttermscode** と **address1_shippingmethodcode** を見積もり/受注にコピーします。</span><span class="sxs-lookup"><span data-stu-id="000a2-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="000a2-120">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="000a2-120">**Time and Expense**</span></span>

<span data-ttu-id="000a2-121">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="000a2-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="000a2-122">**時間エントリ グリッド** は、**日付のみ** の時間動作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="000a2-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="000a2-123">**時間エントリ** は自動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="000a2-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="000a2-124">手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="000a2-124">A manual refresh is required.</span></span>
- <span data-ttu-id="000a2-125">リソースの割り当てにブレーク (0 時間) がある場合、割り当てから時間エントリをインポートできません。</span><span class="sxs-lookup"><span data-stu-id="000a2-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="000a2-126">時間エントリを作成するときは、開始を **msdyn_date** と同じに設定します。</span><span class="sxs-lookup"><span data-stu-id="000a2-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="000a2-127">時間エントリの一括編集を再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="000a2-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="000a2-128">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="000a2-128">**Resource Management**</span></span>

<span data-ttu-id="000a2-129">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="000a2-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="000a2-130">要件なしで日中の予約のステータスを更新しようとすると、null-ref 例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="000a2-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="000a2-131">**調整ビュー** の読み込み中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="000a2-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="000a2-132">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="000a2-132">**Project Management**</span></span>

<span data-ttu-id="000a2-133">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="000a2-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="000a2-134">**プロジェクト スケジュール** で、**手動** から **自動** に変更すると、自動保存が完了しません。</span><span class="sxs-lookup"><span data-stu-id="000a2-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="000a2-135">経費コストは、**プロジェクト追跡グリッド** の差異に対して計算すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="000a2-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="000a2-136">読み込み中と **時間フェーズ** タイプの変更中の **見積もりタグ** 列の動作に一貫性がありません。</span><span class="sxs-lookup"><span data-stu-id="000a2-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="000a2-137">プロジェクトの実際のコストは、**実績** からの合計を反映していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="000a2-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="000a2-138">**概要** タブの **終了予定日** が **WBS スケジュール** に一致しません。</span><span class="sxs-lookup"><span data-stu-id="000a2-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="000a2-139">インデント解除時の **実績時間の更新** が正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="000a2-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="000a2-140">ルート **BU** 外のプロジェクト マネージャーがプロジェクトを作成できません。</span><span class="sxs-lookup"><span data-stu-id="000a2-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="000a2-141">**経費の見積もり** のタスクまたはカテゴリへの変更は、保持されません。</span><span class="sxs-lookup"><span data-stu-id="000a2-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="000a2-142">**契約のコピー** は、請求書スケジュールと実行ステータスをコピーします。</span><span class="sxs-lookup"><span data-stu-id="000a2-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="000a2-143">**実績の更新** ボタンは、誤ってサマリー タスクを計算します。</span><span class="sxs-lookup"><span data-stu-id="000a2-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="000a2-144">Microsoft Project アドイン: チーム メンバーのいずれかに空のリソース単位がある場合、Null 参照エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="000a2-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

