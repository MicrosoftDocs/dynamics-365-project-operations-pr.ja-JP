---
title: Project Service Automation 更新プログラム リリース 22、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 22、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079216"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="b5e6f-103">Project Service Automation 更新プログラム リリース 22、V3</span><span class="sxs-lookup"><span data-stu-id="b5e6f-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="b5e6f-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b5e6f-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b5e6f-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b5e6f-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b5e6f-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b5e6f-109">このトピックには、Project Service Automation V3 更新プログラム 22 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="b5e6f-110">このバージョンのビルド番号は V 3.10.33.48 であり、2020 年 6 月のセルフ アップデートを通じて一般提供されました。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="b5e6f-111">更新プログラム 22</span><span class="sxs-lookup"><span data-stu-id="b5e6f-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b5e6f-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="b5e6f-112">Bug fixes</span></span>



<span data-ttu-id="b5e6f-113">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="b5e6f-113">**Time and Expense**</span></span>

<span data-ttu-id="b5e6f-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="b5e6f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5e6f-115">**時間エントリ** は、インポート後、時間エントリ スケジュールに自動的に追加されません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="b5e6f-116">**時間エントリ** グリッドの日付ピッカーは、ユーザーの地域設定を認識しません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="b5e6f-117">**リソース管理**</span><span class="sxs-lookup"><span data-stu-id="b5e6f-117">**Resource Management**</span></span>

<span data-ttu-id="b5e6f-118">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="b5e6f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5e6f-119">手動モードでは、 **リソース要件** の生成時に **リソース割り当て** 輪郭は認識されません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="b5e6f-120">**リソース要求** はカスタム リクエスト ステータスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="b5e6f-121">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="b5e6f-121">**Project Management**</span></span>

<span data-ttu-id="b5e6f-122">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="b5e6f-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5e6f-123">EstimateGridControl をダブルクリックすると、オランダ語形式の数値は正しく解析されません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="b5e6f-124">Microsoft Project デスクトップ クライアント アドインを使用して割り当てを変更すると、割り当てられた時間は正しく更新されません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="b5e6f-125">契約通貨が顧客の通貨と異なり、組織が通貨記号の代わりに通貨コードを表示するように構成されている場合、プロジェクトの追跡と見積もりグリッドに誤った販売通貨コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="b5e6f-126">勤務時間のスケジュールが 1 日 24 時間の場合、チーム メンバーの終了日は 1 日追加されます。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="b5e6f-127">プロジェクト スケジュールで、トランザクション カテゴリをタスクに追加しても、自動保存はトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="b5e6f-128">チーム メンバーをプロジェクト テンプレート: "リソース要件をプロジェクト テンプレートに関連付けることはできません" に追加すると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="b5e6f-129">リボン ルール スクリプト "msdyn.Approval.CanApproveOrReject"がタイムアウトエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="b5e6f-130">**営業**</span><span class="sxs-lookup"><span data-stu-id="b5e6f-130">**Sales**</span></span>

<span data-ttu-id="b5e6f-131">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="b5e6f-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5e6f-132">'新規見積もりプロジェクト価格表' フォーム/エンティティの価格表検索ダイアログで原価価格表が選択されていると、検証エラーメッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="b5e6f-133">見積もりに添付された BPF が最終段階にある場合、見積もりを受注としてクローズしても作成された契約に移動しません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="b5e6f-134">**未請求売上** の戻し処理は、時間エントリが取り消されると、元のコストにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="b5e6f-135">**確認** ボタンを選択した後、請求書の状態は請求書が更新されない限り、 **確認済み** に変わりません。</span><span class="sxs-lookup"><span data-stu-id="b5e6f-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
