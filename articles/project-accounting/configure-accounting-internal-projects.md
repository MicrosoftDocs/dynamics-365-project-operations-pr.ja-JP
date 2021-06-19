---
title: 内部プロジェクトの会計の構成
description: このトピックは、Project Operations で内部プロジェクトの会計処理の設定方法について説明します。
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012862"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="6432f-103">内部プロジェクトの会計の構成</span><span class="sxs-lookup"><span data-stu-id="6432f-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="6432f-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6432f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6432f-105">内部プロジェクトでは、企業は顧客に請求されていない活動に関連するコストを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="6432f-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="6432f-106">内部プロジェクトの例には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="6432f-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="6432f-107">モバイル アプリなどの製品の開発。開発に関わる原価を追跡します。</span><span class="sxs-lookup"><span data-stu-id="6432f-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="6432f-108">プリセールスの時間と経費の管理。</span><span class="sxs-lookup"><span data-stu-id="6432f-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="6432f-109">この販売前の内部プロジェクトは、見積もりが獲得された場合、後で請求可能なプロジェクトに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="6432f-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="6432f-110">Dynamics 365 Project Operations で契約に関連付けられていないプロジェクトは、内部プロジェクトとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="6432f-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="6432f-111">プロジェクト コストと売上のプロファイルは、プロジェクトの会計ルールの決定には使用されていません。</span><span class="sxs-lookup"><span data-stu-id="6432f-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="6432f-112">内部プロジェクトの原価は、常に損益の原則を使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="6432f-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="6432f-113">転記の勘定科目は、**元帳転記の設定** ページで定義します。</span><span class="sxs-lookup"><span data-stu-id="6432f-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="6432f-114">時間での取引は、**原価** 勘定を借方に転記し、**給与配賦** 勘定を貸方に転記します。</span><span class="sxs-lookup"><span data-stu-id="6432f-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="6432f-115">経費取引は、**費用** 勘定を引き落とし、**経費の相殺勘定** を入金することで計上されます。</span><span class="sxs-lookup"><span data-stu-id="6432f-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="6432f-116">品目トランザクションは、**原価** 勘定を借方に転記し、**原価 - 品目** 勘定を貸方に転記します。</span><span class="sxs-lookup"><span data-stu-id="6432f-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="6432f-117">取引をプロジェクトに転記すると、プロジェクトがプロジェクト契約に関連付けられている場合は、すべての累計の取引が取り消され、新しく請求可能な取引が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6432f-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="6432f-118">請求可能な取引は、それぞれのプロジェクトの原価および収益プロファイルで定義されている会計ルールに従います。</span><span class="sxs-lookup"><span data-stu-id="6432f-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
