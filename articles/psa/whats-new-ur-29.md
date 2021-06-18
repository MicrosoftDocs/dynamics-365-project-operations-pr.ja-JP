---
title: Project Service Automation 更新プログラム リリース 29、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 29、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010477"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="36848-103">Project Service Automation 更新プログラム リリース 29、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="36848-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="36848-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="36848-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="36848-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="36848-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="36848-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="36848-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="36848-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="36848-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="36848-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36848-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="36848-109">このトピックには、Project Service Automation V3 更新プログラム 29 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="36848-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="36848-110">このバージョンのビルド番号は V3.10.47.7 で、2021 年 2 月のセルフアップデートで一般提供されます。</span><span class="sxs-lookup"><span data-stu-id="36848-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="36848-111">更新プログラム 29</span><span class="sxs-lookup"><span data-stu-id="36848-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="36848-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="36848-112">Bug fixes</span></span>

<span data-ttu-id="36848-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="36848-113">**Time and Expense**</span></span>

<span data-ttu-id="36848-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="36848-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="36848-115">ユーザーは、時間入力グリッドで非稼働日に記録された作業時間を表示できません。</span><span class="sxs-lookup"><span data-stu-id="36848-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="36848-116">承認された経費エントリは、グリッド上で編集できます。</span><span class="sxs-lookup"><span data-stu-id="36848-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="36848-117">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="36848-117">**Project Management**</span></span>

<span data-ttu-id="36848-118">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="36848-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="36848-119">リソース割り当ての作業時間を確保するための検証ロジックが欠落していても、マイナスになることはありません。</span><span class="sxs-lookup"><span data-stu-id="36848-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="36848-120">**AssignResourcesForTask** カスタムアクションは、変更されたフィールドだけでなく、すべてのフィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="36848-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="36848-121">**CreateProject** イベントにプラグインまたはワークフローが登録されている環境でプロジェクトをコピーする場合、**CopyWBSToProject** が失敗すると、**msdyn_bulkgenerationstatus** 属性が更新されません。</span><span class="sxs-lookup"><span data-stu-id="36848-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="36848-122">プロジェクト カレンダーを展開すると、稼働日日が昇順で並べ替えられないため、一部のプロジェクト タスクの更新が失敗します。</span><span class="sxs-lookup"><span data-stu-id="36848-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="36848-123">既存のプロジェクトでプロジェクト マネージャーを変更すると、組織単位が既定となるロジックがトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="36848-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="36848-124">**営業**</span><span class="sxs-lookup"><span data-stu-id="36848-124">**Sales**</span></span>

<span data-ttu-id="36848-125">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="36848-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="36848-126">契約行がない場合、**契約** ページの **契約履行** タブが初期化中にサイレントに失敗します。</span><span class="sxs-lookup"><span data-stu-id="36848-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>