---
title: Project Service Automation 更新プログラム リリース 17.5、ホットフィックス、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 17.5、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: cd4142176258820f4718f457ca8610f19f584a32
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143732"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="0ae8c-103">Project Service Automation 更新プログラム リリース 17.5、V3</span><span class="sxs-lookup"><span data-stu-id="0ae8c-103">Project Service Automation Update Release 17.5, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0ae8c-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0ae8c-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="0ae8c-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0ae8c-107">このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="0ae8c-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0ae8c-109">このトピックには、更新プログラム リリース 17.5、V3 の新規追加または変更された機能と修正点をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="0ae8c-110">このバージョンのビルド番号は V3.10.7.32 であり、一般的には 2020 年 3 月 の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="0ae8c-111">更新プログラム 17.5</span><span class="sxs-lookup"><span data-stu-id="0ae8c-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0ae8c-112">バグ修正</span><span class="sxs-lookup"><span data-stu-id="0ae8c-112">Bug fixes</span></span>


<span data-ttu-id="0ae8c-113">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="0ae8c-113">**Project Management**</span></span>

- <span data-ttu-id="0ae8c-114">修正済み：長時間のタスクで発生するサーバー側同期の問題に対処しました。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="0ae8c-115">修正済み：24 時間勤務のテンプレートに対応し、タスクに誤って 1 日分を追加する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="0ae8c-116">修正済み：+13 GMT の勤務時間テンプレートに対応し、タスクが 1 日先にずれる問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0ae8c-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

