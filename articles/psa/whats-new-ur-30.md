---
title: Project Service Automation 更新プログラム リリース 30、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 30、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010432"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="ad471-103">Project Service Automation 更新プログラム リリース 30、V3 の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="ad471-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ad471-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="ad471-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ad471-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad471-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ad471-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="ad471-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ad471-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="ad471-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ad471-108">詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad471-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="ad471-109">このトピックには、Project Service Automation V3 更新プログラム 30 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="ad471-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="ad471-110">このバージョンのビルド番号は V3.10.51.61 で、通常は 2021 年 4 月の自己更新プログラムを通して使用できます。</span><span class="sxs-lookup"><span data-stu-id="ad471-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="ad471-111">更新プログラム 30</span><span class="sxs-lookup"><span data-stu-id="ad471-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ad471-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="ad471-112">Bug fixes</span></span>

<span data-ttu-id="ad471-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="ad471-113">**Time and Expense**</span></span>

<span data-ttu-id="ad471-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="ad471-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad471-115">**役割** フィールドが削除された場合、**クイック作成** ページに時間エントリを作成して保存すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ad471-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="ad471-116">時間入力フィルターで、正しくないフィルター演算子が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ad471-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="ad471-117">時間入力制御で **週のコピー** を選択すると、コピーされたタイムシートは自動的に表示されません。</span><span class="sxs-lookup"><span data-stu-id="ad471-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="ad471-118">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="ad471-118">**Resource Management**</span></span>

<span data-ttu-id="ad471-119">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="ad471-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad471-120">予約を延長すると、ハード予約に割り当てられた予約ステータスが正しくなくなります。</span><span class="sxs-lookup"><span data-stu-id="ad471-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="ad471-121">予約の延長は、予約設定メタデータ内で **確定済み** と定義されている予約ステータスを尊重します。</span><span class="sxs-lookup"><span data-stu-id="ad471-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="ad471-122">有効な予約ステータスが指定されていない場合、エラー メッセージが正しくローカライズされません。</span><span class="sxs-lookup"><span data-stu-id="ad471-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="ad471-123">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="ad471-123">**Project Management**</span></span>

<span data-ttu-id="ad471-124">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="ad471-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad471-125">プロジェクトを 1 つの通貨で作成したり、関連するタスクを別の通貨に含めたりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ad471-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="ad471-126">**営業**</span><span class="sxs-lookup"><span data-stu-id="ad471-126">**Sales**</span></span>

<span data-ttu-id="ad471-127">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="ad471-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad471-128">価格表がコピーされても、価格は更新されません。</span><span class="sxs-lookup"><span data-stu-id="ad471-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="ad471-129">コストの詳細に発生元の値がある場合、見積もりを成約としてクローズできません。</span><span class="sxs-lookup"><span data-stu-id="ad471-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="ad471-130">**プロジェクト タスク** エンティティで、**見積もりコスト** が **予定コスト (基本)** に改名されました。</span><span class="sxs-lookup"><span data-stu-id="ad471-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="ad471-131">請求書が作成または削除されると、null 参照例外が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ad471-131">A null reference exception is generated when invoices are created or deleted.</span></span>
