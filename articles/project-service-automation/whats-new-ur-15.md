---
title: Project Service Automation バージョン 15、V3 更新プログラム の最新情報
description: このトピックでは、Project Service Automation バージョン 15、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752853"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="a99fb-103">Project Service Automation V3 、更新プログラム 15 の最新情報</span><span class="sxs-lookup"><span data-stu-id="a99fb-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="a99fb-104">Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="a99fb-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a99fb-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a99fb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a99fb-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="a99fb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a99fb-107">このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="a99fb-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a99fb-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a99fb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a99fb-109">このトピックには、PSA V3 更新プログラム 15 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="a99fb-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="a99fb-110">このバージョンのビルド番号は V3.10.5.28 であり、一般的には 2020年1月 の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="a99fb-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="a99fb-111">更新プログラム 15</span><span class="sxs-lookup"><span data-stu-id="a99fb-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="a99fb-112">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a99fb-112">Enhancements</span></span>

- <span data-ttu-id="a99fb-113">プロジェクト管理</span><span class="sxs-lookup"><span data-stu-id="a99fb-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a99fb-114">バグ修正</span><span class="sxs-lookup"><span data-stu-id="a99fb-114">Bug fixes</span></span>

- <span data-ttu-id="a99fb-115">時間と経費</span><span class="sxs-lookup"><span data-stu-id="a99fb-115">Time and Expense</span></span>

  - <span data-ttu-id="a99fb-116">修正：調整ビューにオンロード エラー処理を追加。</span><span class="sxs-lookup"><span data-stu-id="a99fb-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="a99fb-117">修正：プロジェクト リソース ハブ：**数量** を変更してあいまいさを回避します。</span><span class="sxs-lookup"><span data-stu-id="a99fb-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="a99fb-118">修正：**時間入力列のコピー** のビューを調整して種別をを含めます。</span><span class="sxs-lookup"><span data-stu-id="a99fb-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="a99fb-119">修正：小数を使用してグリッドビューで時間入力期間を編集すると、一部の数値で不明なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a99fb-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="a99fb-120">プロジェクト管理</span><span class="sxs-lookup"><span data-stu-id="a99fb-120">Project Management</span></span>

  - <span data-ttu-id="a99fb-121">修正：**トラッキング ビューで使用する** のドロップダウンメニューが、オプションの幅に基づいて展開できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="a99fb-122">修正：+13 のタイムゾーンでプロジェクトを管理する場合、タスクの計算において不正確な結果が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a99fb-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="a99fb-123">修繕：24時間 カレンダーを使用する場合の **チームメンバーの終了時間** が修正されました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="a99fb-124">修正：**msdyn_project** メインフォームの **BPF** を再アクティブ化しています。</span><span class="sxs-lookup"><span data-stu-id="a99fb-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="a99fb-125">修正：割り当ての計算で1日の期間が対象とならない事象が解消されています。</span><span class="sxs-lookup"><span data-stu-id="a99fb-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="a99fb-126">修正：ユーザーとプロジェクトでタイムゾーンが異なる場合に、新しい通知バナーがプロジェクトフォームに追加されました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="a99fb-127">Sales</span><span class="sxs-lookup"><span data-stu-id="a99fb-127">Sales</span></span>

  - <span data-ttu-id="a99fb-128">修正：費用見積カテゴリの参照を使用して重複のフィルター処理ができます。</span><span class="sxs-lookup"><span data-stu-id="a99fb-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="a99fb-129">修正： **PluginDomain.ExecuteInTryCatchBlock(..)** のコードが例外の発生元を非表示にしなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="a99fb-130">修正：1000 以上のプロジェクトがある場合に、 **見積行** フォームの **プロジェクト検索** のエラーメッセージが表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="a99fb-131">修正：労働と経費の **見積り** グリッドに正しい通貨記号が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="a99fb-132">修正：PSA を 更新プログラム 14 から 更新プログラム 15に更新後、**プロジェクト** フォームの **スケジュール** タブが空白で表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a99fb-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
