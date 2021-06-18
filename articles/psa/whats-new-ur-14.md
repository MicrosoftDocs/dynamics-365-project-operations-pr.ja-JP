---
title: Project Service Automation 更新プログラム リリース 14、V3 の新機能と変更点
description: このトピックでは、Project Service Automation バージョン 14、V3 の新機能と変更点について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006877"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="de68e-103">Project Service Automation 更新プログラム リリース 14、V3</span><span class="sxs-lookup"><span data-stu-id="de68e-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="de68e-104">Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="de68e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="de68e-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de68e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="de68e-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="de68e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="de68e-107">このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="de68e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="de68e-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de68e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="de68e-109">このトピックには、PSA V3 更新プログラム 14 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="de68e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="de68e-110">このバージョンのビルド番号は V3.10.4.21 であり、次のスケジュールで入手できます:</span><span class="sxs-lookup"><span data-stu-id="de68e-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="de68e-111">**一般的な入手（自己プログラム アップデート）：** 2020年1月</span><span class="sxs-lookup"><span data-stu-id="de68e-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="de68e-112">**自動更新：** 2020年2月</span><span class="sxs-lookup"><span data-stu-id="de68e-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="de68e-113">更新プログラム 14</span><span class="sxs-lookup"><span data-stu-id="de68e-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="de68e-114">拡張機能</span><span class="sxs-lookup"><span data-stu-id="de68e-114">Enhancements</span></span>

- <span data-ttu-id="de68e-115">Sales</span><span class="sxs-lookup"><span data-stu-id="de68e-115">Sales</span></span>

     - <span data-ttu-id="de68e-116">見積が **商談成立としてクローズ** として更新された際に、 **見積明細の詳細** のカスタムフィールド値が、 **プロジェクト契約ラインの詳細** にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="de68e-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="de68e-117">確認済みのプロジェクトは **失注としてクローズ** となります。</span><span class="sxs-lookup"><span data-stu-id="de68e-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="de68e-118">リソース管理</span><span class="sxs-lookup"><span data-stu-id="de68e-118">Resource Management</span></span>

     - <span data-ttu-id="de68e-119">予約を延長すると、予約結果を要約し、予約の管理 へのリンクを案内する確認のダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de68e-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="de68e-120">バグ修正</span><span class="sxs-lookup"><span data-stu-id="de68e-120">Bug fixes</span></span>

- <span data-ttu-id="de68e-121">時間と経費</span><span class="sxs-lookup"><span data-stu-id="de68e-121">Time and Expense</span></span>

     - <span data-ttu-id="de68e-122">修正：修正する入力内容をユーザーが選択していない場合のユーザー エクスペリエンスが改善されました。</span><span class="sxs-lookup"><span data-stu-id="de68e-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="de68e-123">リソース管理</span><span class="sxs-lookup"><span data-stu-id="de68e-123">Resource Management</span></span>

     - <span data-ttu-id="de68e-124">修正：リソースを複数回予約すると、予約可能なリソースの名前が桁あふれする。</span><span class="sxs-lookup"><span data-stu-id="de68e-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="de68e-125">Sales</span><span class="sxs-lookup"><span data-stu-id="de68e-125">Sales</span></span>

     - <span data-ttu-id="de68e-126">修正済み：ユーザーがプロジェクトの費用の見積もり原価価格を入力するまで総販売価格が計算されない。</span><span class="sxs-lookup"><span data-stu-id="de68e-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="de68e-127">修正：見積もりに関連付けられているプロジェクトの契約が **下書き** 状態の場合、この見積を **成約** としてクローズことができない。</span><span class="sxs-lookup"><span data-stu-id="de68e-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]