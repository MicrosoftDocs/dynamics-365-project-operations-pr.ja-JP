---
title: リソース管理の重要な概念
description: このトピックは、Microsoft Dynamics Project Operations でのリソース管理機能に関する情報を提供します。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6362daab7e2e01c7b7b2c2b801fe7e258b21ef16
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000982"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="f8a8d-103">リソース管理の重要な概念</span><span class="sxs-lookup"><span data-stu-id="f8a8d-103">Resource management key concepts</span></span>

<span data-ttu-id="f8a8d-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="f8a8d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8a8d-105">リソースとは、サービス ベース組織の最も重要な資産です。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="f8a8d-106">適切なリソースを必要なな時に検索し、これらのリソースをプロジェクトに予約して、それを利用する機能は、組織が売上目標と顧客満足度目標を達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="f8a8d-107">Dynamics 365 Project Operations のプロジェクト リソース機能を使用すると、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="f8a8d-108">使用可能で適格なリソースでプロジェクト チームを作成する。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="f8a8d-109">汎用チーム メンバ レコードを作成し、そのチームのロールやリソース組織単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="f8a8d-110">汎用チーム メンバーのタスク割り当てから、彼らのリソース要件を生成します。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="f8a8d-111">使用可能なリソース スキルに対してリソース要求で定義されたスキルを識別することでスキルを一致させます。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="f8a8d-112">リソースを代用する。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-112">Substitute resources.</span></span>
- <span data-ttu-id="f8a8d-113">プロジェクト スケジュールの割り当てとリソースの予約を調整する。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="f8a8d-114">予約と割り当ての差異を調整する。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="f8a8d-115">不在状態ステータスに応じてリソース予約を変更する。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="f8a8d-116">プロジェクト マネージャーとリソース マネージャーで共同作業します。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="f8a8d-117">リソースの時間がどのように利用されたかなどの内訳を含む、目標に対してリソースの稼働率の履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="f8a8d-118">スキルと能力リポジトリを維持します。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="f8a8d-119">Project Operations の汎用または名前の付いたリソースでプロジェクトにスタッフを配置できます。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="f8a8d-120">チーム メンバーの追加や割り当て、メンバーの予約や割り当ての管理をおこなうためにさまざまなメソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8a8d-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]