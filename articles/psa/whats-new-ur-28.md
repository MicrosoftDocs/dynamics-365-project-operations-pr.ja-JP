---
title: Project Service Automation 更新プログラム リリース 28、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 28、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948694"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="1ad47-103">Project Service Automation 更新プログラム リリース 28、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="1ad47-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1ad47-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="1ad47-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1ad47-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ad47-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1ad47-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="1ad47-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1ad47-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="1ad47-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1ad47-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ad47-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1ad47-109">このトピックでは、Project Service Automation V3、更新プログラム リリース 28 で新規または変更された機能と修正の一覧を示します。このバージョンのビルド番号は V3.10.46.32 で、2021 年 1 月に自己更新で一般提供されます。</span><span class="sxs-lookup"><span data-stu-id="1ad47-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="1ad47-110">更新プログラム 28</span><span class="sxs-lookup"><span data-stu-id="1ad47-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1ad47-111">バグの修正</span><span class="sxs-lookup"><span data-stu-id="1ad47-111">Bug fixes</span></span>

<span data-ttu-id="1ad47-112">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="1ad47-112">**Time and Expense**</span></span>

<span data-ttu-id="1ad47-113">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="1ad47-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="1ad47-114">ユーザーは **一括編集** を使って、承認および送信済みの時間エントリを更新できます。</span><span class="sxs-lookup"><span data-stu-id="1ad47-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="1ad47-115">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="1ad47-115">**Project Management**</span></span>

<span data-ttu-id="1ad47-116">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="1ad47-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="1ad47-117">タスク GUID が数値として解釈される場合、**WBS (作業分解構造)** ページのリボンに表示された **タスクの編集** を使用して編集するためにタスクを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="1ad47-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="1ad47-118">**営業**</span><span class="sxs-lookup"><span data-stu-id="1ad47-118">**Sales**</span></span>

<span data-ttu-id="1ad47-119">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="1ad47-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="1ad47-120">**GetEstimatesForProject** プラグインが呼び出されると、null 参照例外が生成されます。</span><span class="sxs-lookup"><span data-stu-id="1ad47-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="1ad47-121">マイルストーン グリッドの **請求準備完了としてマーク** は、**InvoiceStatus** 属性 (更新済み) 以外の属性を部分的にのみ更新します。</span><span class="sxs-lookup"><span data-stu-id="1ad47-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]