---
title: Project Service Automation 更新プログラム リリース 27.6 ホットフィックス、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム 27.6 ホットフィックス、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481278"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="3f17f-103">Project Service Automation 更新プログラム リリース 27.6、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="3f17f-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="3f17f-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="3f17f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3f17f-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f17f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3f17f-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="3f17f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3f17f-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="3f17f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3f17f-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f17f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3f17f-109">このトピックには、Project Service Automation V3 更新プログラム 27.6 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="3f17f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="3f17f-110">このバージョンのビルド番号は V3.10.45.120 であり、一般的には 2021 年 1 月の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="3f17f-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="3f17f-111">更新プログラム 27.6</span><span class="sxs-lookup"><span data-stu-id="3f17f-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3f17f-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="3f17f-112">Bug fixes</span></span>


<span data-ttu-id="3f17f-113">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="3f17f-113">**Resource Management**</span></span>

<span data-ttu-id="3f17f-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="3f17f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f17f-115">リソースの可用性を見つける際、**ExpandCalendar** がカレンダー ルールが適用されていないリソースごとに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3f17f-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
