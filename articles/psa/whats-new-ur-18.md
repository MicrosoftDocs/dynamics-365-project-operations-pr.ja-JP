---
title: Project Service Automation 更新プログラム リリース 18、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 18、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006652"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="b3880-103">Project Service Automation 更新プログラム リリース 18、V3</span><span class="sxs-lookup"><span data-stu-id="b3880-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b3880-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="b3880-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b3880-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3880-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b3880-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="b3880-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b3880-107">このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="b3880-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="b3880-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3880-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b3880-109">このトピックには、Project Service Automation V3 更新プログラム 18 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="b3880-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="b3880-110">このバージョンのビルド番号は V3.10.8.12 で、通常は 2020 年 4 月の自己更新プログラムを通して使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3880-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="b3880-111">更新プログラム 18</span><span class="sxs-lookup"><span data-stu-id="b3880-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b3880-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="b3880-112">Bug fixes</span></span>

<span data-ttu-id="b3880-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="b3880-113">**Time and Expense**</span></span>

- <span data-ttu-id="b3880-114">修正：**リコール**、 **リクエスト**、 **承認のキャンセル** のフローが不明瞭なエラー メッセージとともに例外をスローする。</span><span class="sxs-lookup"><span data-stu-id="b3880-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="b3880-115">修正：経費に対する **承認のキャンセル** が失敗した際に、関連する例外エラーがスローされない。</span><span class="sxs-lookup"><span data-stu-id="b3880-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="b3880-116">修正：オーストラリアでは、10 月のサマータイム切替え後にも時間エントリのグリッドが、休日を適切に処理しない。</span><span class="sxs-lookup"><span data-stu-id="b3880-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="b3880-117">修正：規定のロジックが不正なために、費用の提出ができない。</span><span class="sxs-lookup"><span data-stu-id="b3880-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="b3880-118">修正：時間エントリの承認が失敗した際に、承認の状態が **保留中** のままとなる。</span><span class="sxs-lookup"><span data-stu-id="b3880-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="b3880-119">修正：一括承認にて SQL エラーが発生する（デッドロック／タイムアウト）。</span><span class="sxs-lookup"><span data-stu-id="b3880-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="b3880-120">修正：時間エントリの承認中にチーム メンバーを更新することで、ユーザー エクスペリエンスにおける重大なパフォーマンスの問題が発生する。</span><span class="sxs-lookup"><span data-stu-id="b3880-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="b3880-121">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="b3880-121">**Project Management**</span></span>

- <span data-ttu-id="b3880-122">修正：タイムゾーンの通知は **調整** ビューから **プロジェクト** メイン フォームに移動しています。</span><span class="sxs-lookup"><span data-stu-id="b3880-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="b3880-123">修正：カレンダーのテンプレートが、新規プロジェクトのフォームを開いた際に規定の設定とならない。</span><span class="sxs-lookup"><span data-stu-id="b3880-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="b3880-124">修正：クロミウム ベースのブラウザでは、先行するタスクを選択して削除することが困難である。</span><span class="sxs-lookup"><span data-stu-id="b3880-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="b3880-125">修正：**空白のテンプレートからプロジェクト** を作成、またはコピーすると関連性のない割り当てがされる。</span><span class="sxs-lookup"><span data-stu-id="b3880-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="b3880-126">修正：特定のエッジ ケースにおいて、タスク グリッドから新規割り当てを作成すると重複するレコードが作成される。</span><span class="sxs-lookup"><span data-stu-id="b3880-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="b3880-127">修正：マニュアル モードで、タスクの開始日を現在日以降に更新できない。</span><span class="sxs-lookup"><span data-stu-id="b3880-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="b3880-128">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="b3880-128">**Resource Management**</span></span>

- <span data-ttu-id="b3880-129">修正：予約の延長後、**調整** ビューの小計列に予約の差異が正確に計算されない。</span><span class="sxs-lookup"><span data-stu-id="b3880-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="b3880-130">修正：予約可能なリソースの日程表とプロジェクトの日程表が合致しない場合、**調整** ビューにリソース管理が正しく表示されない。</span><span class="sxs-lookup"><span data-stu-id="b3880-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="b3880-131">**営業**</span><span class="sxs-lookup"><span data-stu-id="b3880-131">**Sales**</span></span>

- <span data-ttu-id="b3880-132">修正：時間エントリが再承認 （**承認 > キャンセル >** 再度承認）された際に、重複する課金できない実績値が作成される。</span><span class="sxs-lookup"><span data-stu-id="b3880-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]