---
title: Project Service Automation 更新プログラム リリース 20、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 20、V3 で利用可能な機能と修正をリスト化しています
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079217"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="02ae3-103">Project Service Automation 更新プログラム リリース 20、V3</span><span class="sxs-lookup"><span data-stu-id="02ae3-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="02ae3-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="02ae3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="02ae3-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02ae3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="02ae3-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="02ae3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="02ae3-107">このリリースに更新するには、Dynamics 365 オンライン ソリューション ページの管理センターにアクセスして、更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="02ae3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="02ae3-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ae3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="02ae3-109">このトピックには、Project Service Automation V3 更新プログラム 20 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="02ae3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="02ae3-110">このバージョンのビルド番号は V 3.10.31.37 であり、2020 年 6 月のセルフ アップデートを通じて一般提供されました。</span><span class="sxs-lookup"><span data-stu-id="02ae3-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="02ae3-111">更新プログラム 20</span><span class="sxs-lookup"><span data-stu-id="02ae3-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="02ae3-112">バグの修正</span><span class="sxs-lookup"><span data-stu-id="02ae3-112">Bug fixes</span></span>

<span data-ttu-id="02ae3-113">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="02ae3-113">**Project Management**</span></span>

<span data-ttu-id="02ae3-114">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="02ae3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="02ae3-115">時間を必要とする割り当て方法でプロジェクト チーム メンバーをインポートすると、指定した時間がゼロの場合に不明確なエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="02ae3-116">プロジェクトタスクの **説明** フィールドに最大文字数を入力すると、ユーザーは誤ったエラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="02ae3-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="02ae3-117">ユーザーの言語設定が日本語に設定されている場合、 **Microsoft Dynamics 365 Project Service Automation アドインのダウンロード** ページは英語のダウンロード ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="02ae3-118">サーバー エラーが発生すると、 **プロジェクト** フォームの **スケジュール** タブに同期ラベルが残ることがあります。</span><span class="sxs-lookup"><span data-stu-id="02ae3-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="02ae3-119">タスクが変更されると、冗長なタスク更新がサーバーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="02ae3-120">**営業**</span><span class="sxs-lookup"><span data-stu-id="02ae3-120">**Sales**</span></span>

<span data-ttu-id="02ae3-121">以下の問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="02ae3-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="02ae3-122">**契約** フォームで、 **請求書の作成** をダブルクリックすると、1 つの実績レコードに対して 2 つの請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="02ae3-123">Internet Explorer 11 では、ユーザーは経費エントリを作成できません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="02ae3-124">原価の取消と未請求売上実績の取消はリンクされていません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="02ae3-125">**プロジェクト** フォームの **実績の更新** ボタンは、 **タスクの実時間数** を更新しません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="02ae3-126">**PreValidateProjectTeamMemberCreate** プラグインは、属性 **msdyn_isgenericresourceprojectscoped** が　 **False** に設定されている場合、重複する予約可能な汎用リソースを作成できます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="02ae3-127">**再計算** は、製品ベースの見積依頼明細行の詳細と契約品目の詳細の請求可能コストをクリアします。</span><span class="sxs-lookup"><span data-stu-id="02ae3-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="02ae3-128">特定のシナリオでは、 **PostEstimateLineUpdate** プラグインが Null 参照の例外エラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="02ae3-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="02ae3-129">**収益性分析チャート** の時間フェーズ期間は、見積の固定価格見積依頼明細行の詳細のコストの期間と一致しません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="02ae3-130">出荷単位および出荷単位一覧の値は、 **契約品目の詳細** と **見積依頼明細行の詳細** フォームの経費カテゴリで正しく既定値設定されません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="02ae3-131">**組織単位原価価格** 一覧には、日付の有効性の重複が許可されています。</span><span class="sxs-lookup"><span data-stu-id="02ae3-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="02ae3-132">受注タイプが作業ベースではない場合、null 参照例外エラーが発生するため、ユーザーは **OrgUnit** を変更できません。</span><span class="sxs-lookup"><span data-stu-id="02ae3-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="02ae3-133">**見積依頼明細行の詳細** フォームから **見積もり** タブに戻って移動しようとすると、フォームが更新され、 **概要** タブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02ae3-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
