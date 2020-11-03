---
title: Project Service Automation 更新プログラム リリース 17、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 17、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079224"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="da3df-103">Project Service Automation 更新プログラム リリース 17、V3</span><span class="sxs-lookup"><span data-stu-id="da3df-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="da3df-104">Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。</span><span class="sxs-lookup"><span data-stu-id="da3df-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="da3df-105">このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。</span><span class="sxs-lookup"><span data-stu-id="da3df-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="da3df-106">このリリースは、Dynamics 365 9.x と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="da3df-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="da3df-107">このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="da3df-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="da3df-108">詳細については [優先ソリューションのインストール、更新、または削除](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da3df-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="da3df-109">このトピックには、PSA V3 更新プログラム 17 の新機能または変更された機能と修正をリスト化しています。</span><span class="sxs-lookup"><span data-stu-id="da3df-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="da3df-110">このバージョンのビルド番号は V3.10.6.34 であり、一般的には 2020 年 3 月 の自己プログラム更新の処理を通じて入手できます。</span><span class="sxs-lookup"><span data-stu-id="da3df-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="da3df-111">更新プログラム 17</span><span class="sxs-lookup"><span data-stu-id="da3df-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="da3df-112">バグ修正</span><span class="sxs-lookup"><span data-stu-id="da3df-112">Bug fixes</span></span>

<span data-ttu-id="da3df-113">**一般**</span><span class="sxs-lookup"><span data-stu-id="da3df-113">**General**</span></span>

- <span data-ttu-id="da3df-114">修正済み：Project Service Automation を更新するとチーム メンバー のライセンスが適用されます（プロジェクト リソース ハブにはチーム メンバー サービス プランのメタデータ 3.x が含まれています）</span><span class="sxs-lookup"><span data-stu-id="da3df-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="da3df-115">**時間と経費**</span><span class="sxs-lookup"><span data-stu-id="da3df-115">**Time and Expense**</span></span>

- <span data-ttu-id="da3df-116">修正済み：経費の見積もりをゼロ以外の価格からゼロ（0）に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="da3df-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="da3df-117">この変更は無視されます。</span><span class="sxs-lookup"><span data-stu-id="da3df-117">The change is ignored.</span></span>

<span data-ttu-id="da3df-118">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="da3df-118">**Project Management**</span></span>

- <span data-ttu-id="da3df-119">修正済み：チーム メンバーの役職名に null 値のチェックが追加されました。</span><span class="sxs-lookup"><span data-stu-id="da3df-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="da3df-120">修正済み： **msdyn_resourceassignment** エンティティの **msdyn_userresourceid** フィールドは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="da3df-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="da3df-121">修正済み：2.x から 3.x へのアップグレードでは、タスク割り当てで空のコンターが処理されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="da3df-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="da3df-122">**営業**</span><span class="sxs-lookup"><span data-stu-id="da3df-122">**Sales**</span></span>

- <span data-ttu-id="da3df-123">修正済み： **Invoice.PreValidateInvoiceUpdate** では、レコード所有者の再割り当てのシナリオを適切に処理できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="da3df-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="da3df-124">修正済み：トランザクション クラスが **時間** 、 **UnitGroup** の場合、 **QuoteLineDetails** 、 **JournalLine** 、 **InvoiceLineDetail** 、 **ContractLineDetails** を含むすべてのエンティティで編集できません。</span><span class="sxs-lookup"><span data-stu-id="da3df-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="da3df-125">しかし、 **JournalLine** と **InvoiceLineDetails** の **単位** が編集できません。</span><span class="sxs-lookup"><span data-stu-id="da3df-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


