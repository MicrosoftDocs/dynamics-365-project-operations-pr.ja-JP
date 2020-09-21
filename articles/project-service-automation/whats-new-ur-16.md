---
title: Project Service Automation バージョン 16、V3 更新プログラム の最新情報
description: このトピックには、Project Service Automation 更新プログラム リリース 16、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752852"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="6952c-103">Project Service Automation V3 、更新プログラム 16 の最新情報</span><span class="sxs-lookup"><span data-stu-id="6952c-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="6952c-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="6952c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6952c-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6952c-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="6952c-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="6952c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6952c-107">このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="6952c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="6952c-108">詳細については [優先ソリューションのインストールと更新](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6952c-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="6952c-109">このトピックには、PSA V3 更新プログラム 16 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="6952c-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="6952c-110">このバージョンのビルド番号は V3.10.6.34 であり、一般的には 2020 年 1 月の自己プログラム更新の処理を通じて入手できます</span><span class="sxs-lookup"><span data-stu-id="6952c-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="6952c-111">更新プログラム 16</span><span class="sxs-lookup"><span data-stu-id="6952c-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6952c-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="6952c-112">Bug fixes</span></span>

-   <span data-ttu-id="6952c-113">時間と経費</span><span class="sxs-lookup"><span data-stu-id="6952c-113">Time and Expense</span></span>

    -   <span data-ttu-id="6952c-114">修正済み：承認のために削除された時間と経費の入力を提出しようとすると、関連するエラーメッセージが表示される。</span><span class="sxs-lookup"><span data-stu-id="6952c-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="6952c-115">プロジェクト管理</span><span class="sxs-lookup"><span data-stu-id="6952c-115">Project Management</span></span>

    -   <span data-ttu-id="6952c-116">修正済み：テンプレートでチームメンバーに定義されているリソースの単位は、テンプレートと共にに新しいプロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6952c-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="6952c-117">修正済みレコード所有権の再割り当て処理を改善しています。</span><span class="sxs-lookup"><span data-stu-id="6952c-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="6952c-118">修正済み：コピー中のプロジェクトは、すべてのコピー操作が完了するまでコピーできません。</span><span class="sxs-lookup"><span data-stu-id="6952c-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="6952c-119">リソース管理</span><span class="sxs-lookup"><span data-stu-id="6952c-119">Resource Management</span></span>

    -   <span data-ttu-id="6952c-120">修正済み：予約の延長にて、短い期間が正しく処理されるようになり、延長予約でゼロ時間が作成されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6952c-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="6952c-121">修正済み：プロジェクトのタイムゾーンが+5：30 GMTで、ユーザーの時間が異なる場合に、調整ビューがレンダリングされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6952c-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="6952c-122">Sales</span><span class="sxs-lookup"><span data-stu-id="6952c-122">Sales</span></span>

    -   <span data-ttu-id="6952c-123">修正済み：契約ラインにマッピングされたプロジェクトが削除され、新しいプロジェクトがマッピングされた場合に、新しいプロジェクトの実際のレコードに対する、契約ラインで定義された請求、価格設定のルールに基づいた再評価がされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="6952c-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="6952c-124">この挙動は本リリースで修正されています。</span><span class="sxs-lookup"><span data-stu-id="6952c-124">This has been fixed in this release.</span></span> <span data-ttu-id="6952c-125">新しくマッピングされたプロジェクトの価格設定と実際のレコードは、契約ラインの価格設定と請求のルールに基づいて取り消され、正しく再作成されます。</span><span class="sxs-lookup"><span data-stu-id="6952c-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="6952c-126">マッピングされていないプロジェクトの実際のレコードも、結果として再評価され、再作成されます。</span><span class="sxs-lookup"><span data-stu-id="6952c-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="6952c-127">修正済み：見積明細の **金額** フィールドに対する評価が追加され、null 値が保存されないようになりました。</span><span class="sxs-lookup"><span data-stu-id="6952c-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="6952c-128">修正済み：プロジェクトで実績が更新されたときに、更新ボタンがプロジェクトのメイン フォームに追加され、ユーザーが実績値を再同期できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6952c-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="6952c-129">修正済み：2.X から 3.X にアップグレードすると、プロジェクト名に NULL 値を持つプロジェクトが許容されます。</span><span class="sxs-lookup"><span data-stu-id="6952c-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

