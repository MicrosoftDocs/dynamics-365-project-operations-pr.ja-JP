---
title: Project Service Automation 更新プログラム リリース 12、V3 の新機能と変更点
description: このトピックでは、Project Service Automation バージョン 12、V3 の新機能と変更点について説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143834"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="16750-103">Project Service Automation 更新プログラム リリース 12、V3</span><span class="sxs-lookup"><span data-stu-id="16750-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="16750-104">Dynamics 365 Project Service Automation (PSA) アプリケーションの最新のアップデートをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="16750-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="16750-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="16750-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="16750-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="16750-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="16750-107">このリリースへと更新をするには、Dynamics 365 のオンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="16750-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="16750-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16750-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="16750-109">このトピックには、Project Service Automation V3 更新プログラム 12 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="16750-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="16750-110">このバージョンのビルド番号は V3.10.2.34 であり、一般的には 2019年10月 の自己更新処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="16750-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="16750-111">更新プログラム 12</span><span class="sxs-lookup"><span data-stu-id="16750-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="16750-112">バグ修正</span><span class="sxs-lookup"><span data-stu-id="16750-112">Bug fixes</span></span>

- <span data-ttu-id="16750-113">時間と経費</span><span class="sxs-lookup"><span data-stu-id="16750-113">Time and Expense</span></span>

    - <span data-ttu-id="16750-114">修正：時間の入力でのエラーメッセージが更新され、より関連性の高いコンテキストが追加されました。</span><span class="sxs-lookup"><span data-stu-id="16750-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="16750-115">修正：時間入力のグリッドとスケジュールが、必要に応じて垂直方向のスクロールバーを正しく表示します。</span><span class="sxs-lookup"><span data-stu-id="16750-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="16750-116">修正：送信済みの経費と時間入力を承認することができます。</span><span class="sxs-lookup"><span data-stu-id="16750-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="16750-117">修正：承認キャンセル時の確認ダイアログ メッセージが修正され、 **承認済み** から **提出済み** へと変更された際の承認ステータスが反映されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16750-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="16750-118">修正： **価格**、 **単位**、 **数量** フィールドが、承認後に経費レコード上でロックされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16750-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="16750-119">プロジェクト管理</span><span class="sxs-lookup"><span data-stu-id="16750-119">Project Management</span></span>

    - <span data-ttu-id="16750-120">修正：メイン フォームの **チームメンバー** 上の **新規** アクション が削除されました。</span><span class="sxs-lookup"><span data-stu-id="16750-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="16750-121">修正：タスクの終了日がずれる原因となる端数処理のエラーが不正確なため、リソースの割り当てが変更されました。</span><span class="sxs-lookup"><span data-stu-id="16750-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="16750-122">修正：タスク グリッドで、関連するサーバー側のエラーがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="16750-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="16750-123">修正：役職名の代わりにチームメンバーの名前がタスクのユーザー ピッカーで表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16750-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="16750-124">リソース管理</span><span class="sxs-lookup"><span data-stu-id="16750-124">Resource Management</span></span>

    - <span data-ttu-id="16750-125">修正：テンプレートから作成されたプロジェクトのリソース要件の詳細で、プロジェクトカレンダーが使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16750-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="16750-126">修正：スキルとコンピテンシーが、ロール マスターデータから、そのロールに対して作成されたリソースの要件に既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="16750-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="16750-127">Sales</span><span class="sxs-lookup"><span data-stu-id="16750-127">Sales</span></span>

    - <span data-ttu-id="16750-128">修正：**契約のメイン** フォームで重複するオブジェクトIDが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="16750-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="16750-129">修正： **見積もり分析** タブが表示されるようにロジックが更新され、タブのメタデータ設定が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16750-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="16750-130">修正：実績レコードの計上日は、承認された日ではなく、時間/経費の入力日となります。</span><span class="sxs-lookup"><span data-stu-id="16750-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
