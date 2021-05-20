---
title: Project Service Automation 更新プログラム リリース 31、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 31、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945541"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="89444-103">Project Service Automation 更新プログラム リリース 31、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="89444-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="89444-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="89444-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="89444-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="89444-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="89444-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="89444-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="89444-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="89444-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="89444-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89444-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="89444-109">このトピックには、Project Service Automation V3 更新プログラム 31 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="89444-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="89444-110">このバージョンのビルド番号は V3.10.52.77 であり、2021 年 5 月のセルフ アップデートを通じて一般提供されました。</span><span class="sxs-lookup"><span data-stu-id="89444-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="89444-111">更新プログラム 31</span><span class="sxs-lookup"><span data-stu-id="89444-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="89444-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="89444-112">Bug fixes</span></span>

<span data-ttu-id="89444-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="89444-113">**Time and Expense**</span></span>

<span data-ttu-id="89444-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="89444-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="89444-115">**予約可能なリソース** ページのの時間入力制御コマンドボタンがわかりにくい。</span><span class="sxs-lookup"><span data-stu-id="89444-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="89444-116">時間入力を承認する際に、**Project.SetTrackingFields** で null 値参照の例外が発生する。</span><span class="sxs-lookup"><span data-stu-id="89444-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="89444-117">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="89444-117">**Resource Management**</span></span>

<span data-ttu-id="89444-118">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="89444-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="89444-119">**チーム メンバーを作成する** 予約設定メタデータの **既定の予約コミット状態** が正しく表示されませんでした。</span><span class="sxs-lookup"><span data-stu-id="89444-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="89444-120">PSA 1.X から 3.X にアップグレードする際に、**UpgradeResourceRequirements** でアップグレード処理が失敗する問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="89444-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="89444-121">**営業**</span><span class="sxs-lookup"><span data-stu-id="89444-121">**Sales**</span></span>

<span data-ttu-id="89444-122">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="89444-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="89444-123">実際の収益が、追跡グリッドで金額をプロジェクトの通貨に変換される。</span><span class="sxs-lookup"><span data-stu-id="89444-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="89444-124">組織の基本通貨とプロジェクトの通貨が異なる場合に、仕訳明細、見積明細、契約明細を作成すると、既定の通貨のが不明瞭になる。</span><span class="sxs-lookup"><span data-stu-id="89444-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="89444-125">**修正ジャーナルの検証を保留中** クエリがプロジェクトでフィルター処理されない。</span><span class="sxs-lookup"><span data-stu-id="89444-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="89444-126">プロジェクトで残りの売上が正しく計算されない。</span><span class="sxs-lookup"><span data-stu-id="89444-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="89444-127">価格表を作成せずに、連絡先担当者を元に見積書を作成すると失敗する。</span><span class="sxs-lookup"><span data-stu-id="89444-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="89444-128">**請求書の確認** を選択しても、処理スピナーが表示されない。</span><span class="sxs-lookup"><span data-stu-id="89444-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="89444-129">**請求書の作成** を選択しても、処理スピナーが表示されない。</span><span class="sxs-lookup"><span data-stu-id="89444-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="89444-130">見積書を失注としてクローズしても、予約をキャンセルできない。</span><span class="sxs-lookup"><span data-stu-id="89444-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







