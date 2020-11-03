---
title: 組織単位
description: このトピックでは Dynamics 365 Project Service Automation の組織単位に関する情報を提供します。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 454d9a4c4d139f493adf4604f8ba40a0211f0eec
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079380"
---
# <a name="organizational-units"></a><span data-ttu-id="f60b1-103">組織単位</span><span class="sxs-lookup"><span data-stu-id="f60b1-103">Organizational units</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f60b1-104">Dynamics 365 Project Service Automation における組織単位は、コスト率を持つ請求可能リソースを使用するプロフェッショナル サービス企業の個別のグループまたは部門です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-104">Dynamics 365 Project Service Automation, an organizational unit is a distinct group or division in a professional services company that employs billable resources that have cost rates.</span></span>

<span data-ttu-id="f60b1-105">さまざまな実践分野や事業分野で技術リソースを採用するプロフェッショナルサービス企業の場合、役割を遂行するコストは実践分野や業務分野によって場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-105">For professional services companies that employ technical resources in various practice areas or business lines, the cost to fill a role in one practice area or business line might differ from the cost to fill a role in another practice area or business line.</span></span> <span data-ttu-id="f60b1-106">組織単位の概念は、これらの役割に明確なコスト構造を持つ企業の部門で請求可能な役割のセットをグループ化する方法を提供することにより、このシナリオで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-106">The concept  organizational units helps in this scenario by providing a way to group a set of billable roles in a division of a company that has a distinct cost structure for these roles.</span></span>

## <a name="key-attributes-and-associations-of-organizational-units"></a><span data-ttu-id="f60b1-107">組織単位の重要な属性と関連付け</span><span class="sxs-lookup"><span data-stu-id="f60b1-107">Key attributes and associations of organizational units</span></span>

<span data-ttu-id="f60b1-108">PSA で、PSA の組織単位は特定の通貨と特定の原価価格リストを持ちます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-108">In PSA, an organizational unit in PSA has a specific currency and specific cost price lists.</span></span>

<span data-ttu-id="f60b1-109">組織単位の通貨は、コストの追跡に使用される主要通貨です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-109">The currency of an organizational unit is the primary currency that is used to track costs.</span></span>

<span data-ttu-id="f60b1-110">それぞれの組織単位に 1 つ以上の原価価格リストを添付できます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-110">One or more cost price lists can be attached to each organizational unit.</span></span> <span data-ttu-id="f60b1-111">PSA で組織単位に添付できる価格表には次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-111">PSA puts the following limitations on the price lists that can be attached to an organizational unit:</span></span>

- <span data-ttu-id="f60b1-112">組織単位の通貨での価格表である必要があります</span><span class="sxs-lookup"><span data-stu-id="f60b1-112">Price lists must be in the currency of the organizational unit</span></span>
- <span data-ttu-id="f60b1-113">価格表は原価価格表である必要があります</span><span class="sxs-lookup"><span data-stu-id="f60b1-113">Price lists must be of cost price lists</span></span>

<span data-ttu-id="f60b1-114">さらに、リソース エンティティに組織単位の属性があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-114">In addition, there is an attribute for the organizational unit on the Resource entity.</span></span> <span data-ttu-id="f60b1-115">それぞれのリソースを 1 つの組織単位に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-115">Each resource can be assigned to one organizational unit.</span></span>

## <a name="roles-of-organizational-units"></a><span data-ttu-id="f60b1-116">組織単位の役割</span><span class="sxs-lookup"><span data-stu-id="f60b1-116">Roles of organizational units</span></span>

<span data-ttu-id="f60b1-117">組織単位は PSA で 2 つの役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="f60b1-117">The organizational unit plays two roles in PSA:</span></span>

- <span data-ttu-id="f60b1-118">**契約単位** – 営業の獲得、納品、顧客サービスの提供の管理を主に担当する企業グループや部門を表す組織単位。</span><span class="sxs-lookup"><span data-stu-id="f60b1-118">**Contracting unit** – The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> <span data-ttu-id="f60b1-119">契約単位は **営業案件** 、 **見積もり** 、 **プロジェクト契約** 、 **プロジェクト** の各ページのヘッダーセクションの **契約単位** フィールドによって識別されます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-119">The contracting unit is identified by the **Contracting Unit** field in the header section of the **Opportunity** , **Quote** , **Project Contract** , and **Project** pages.</span></span>
- <span data-ttu-id="f60b1-120">**リソース単位** – リソースが属するまたは割り当てられている組織単位。</span><span class="sxs-lookup"><span data-stu-id="f60b1-120">**Resourcing unit** – The organizational unit that a resource belongs to or is assigned to.</span></span> <span data-ttu-id="f60b1-121">この組織単位は、所有する作業指示書 (SOW) とプロジェクトのいくつかの役割にリソースを提供できます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-121">This organizational unit can provide its resources for some roles on statements of work (SOWs) and projects that are owned by the contracting unit.</span></span>

> ![契約単位とリソース単位](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a><span data-ttu-id="f60b1-123">組織単位に関するよくある質問</span><span class="sxs-lookup"><span data-stu-id="f60b1-123">Organizational unit FAQs</span></span>

<span data-ttu-id="f60b1-124">ここで組織部門に関するよくある質問をいくつか紹介します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-124">Here are some of the most frequently asked questions about organizational units.</span></span>

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a><span data-ttu-id="f60b1-125">PSA の組織単位エンティティは、Dynamics 365 に既に存在する組織エンティティとどのように関連しますか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-125">How is the Organizational Unit entity in PSA related to the Organization entity that already exists in Dynamics 365?</span></span>

<span data-ttu-id="f60b1-126">Microsoft Dynamics 365 の組織エンティティは、グローバルな Dynamics 365 インスタンスの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-126">The Organization entity in Microsoft Dynamics 365 represents the name of a global Dynamics 365 instance.</span></span> <span data-ttu-id="f60b1-127">この名前は通常、グローバル企業の名前です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-127">This name is usually the name of the global enterprise.</span></span>

<span data-ttu-id="f60b1-128">組織単位エンティティは、グローバル企業のグループや部門を表します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-128">The Organizational Unit entity represents a group or division in the global enterprise.</span></span> <span data-ttu-id="f60b1-129">このグループや部門にはロールのセットとロールのコスト価格リストがあり、それらのロールと価格リストは企業内の他のグループや部門のロールと価格リストとは異なります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-129">This group or division has a set of roles and a cost price list for those roles, and those roles and price list differ from the roles and price list of other groups or divisions in the enterprise.</span></span>

<span data-ttu-id="f60b1-130">PSA がインストールされると、組織に基づいて既定の組織単位が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-130">When PSA is installed, a default organizational unit is created based on the organization.</span></span> <span data-ttu-id="f60b1-131">既存のリソースはすべて既定の組織単位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-131">All existing resources are assigned to the default organizational unit.</span></span> <span data-ttu-id="f60b1-132">新しい Active Directory ユーザーやリソースが Dynamics 365 にインポートされた場合、ユーザー インポート プロセスは PSA の既定の組織単位にそれらを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-132">If any new Active Directory users or resources are imported into Dynamics 365, the user import process assigns them to the default organizational unit in PSA.</span></span>
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a><span data-ttu-id="f60b1-133">組織単位エンティティと部署エンティティの違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-133">How does the organizational unit entity differ from the business unit entity?</span></span>

<span data-ttu-id="f60b1-134">Dynamics 365 で部署エンティティはセキュリティ構造です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-134">In Dynamics 365, the Business Unit entity is a security construct.</span></span> <span data-ttu-id="f60b1-135">ユーザーと部署の関連付けにより、ユーザーがアクセスできるエンティティとエンティティ レコードが決まります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-135">The association of a user with a business unit determines the entities and entity records that the user has access to.</span></span> <span data-ttu-id="f60b1-136">また、これらのエンティティ レコードに対するユーザーのアクセス許可 (作成、読み取り、書き込み、削除、追加、任意の場所に追加、割り当て、共有) も決定します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-136">It also determines the permissions (Create, Read, Write, Delete, Append, Append To, Assign, or Share) that the user has for those entity records.</span></span>

<span data-ttu-id="f60b1-137">組織単位エンティティは、割り当てられた従業員のコスト率が異なる企業グループや部門を表します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-137">The Organizational Unit entity represents a company group or division that has distinct cost rates for employees that are assigned to it.</span></span> <span data-ttu-id="f60b1-138">リソースと組織単位との関連付けにより、プロジェクト エンゲージメントに対するリソースのコストが決まります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-138">The association of a resource with an organizational unit determines the resource's cost to a project engagement.</span></span>

<span data-ttu-id="f60b1-139">Dynamics 365 の実装時に、部署の階層のセキュリティ承認と、部署へのユーザーの割り当てを最適化します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-139">When you implement Dynamics 365, optimize security authorization for the hierarchy of business units and the assignment of users to business units.</span></span> <span data-ttu-id="f60b1-140">通常、同じレコード セットにアクセスするすべてのユーザーを同じ部署に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-140">Assign all users who must typically access the same set of records to the same business unit.</span></span> <span data-ttu-id="f60b1-141">組織単位は、セキュリティ承認やアクセスに影響しません。</span><span class="sxs-lookup"><span data-stu-id="f60b1-141">The organizational unit has no effect on security authorization or access.</span></span>

#### <a name="example-of-organizational-units-and-business-units"></a><span data-ttu-id="f60b1-142">組織単位と部署の例</span><span class="sxs-lookup"><span data-stu-id="f60b1-142">Example of organizational units and business units</span></span>

<span data-ttu-id="f60b1-143">Contoso, Ltd. 社は積極的に Microsoft のテクノロジを実践しています。</span><span class="sxs-lookup"><span data-stu-id="f60b1-143">Contoso, Ltd. has a thriving Microsoft technology practice.</span></span> <span data-ttu-id="f60b1-144">直樹と綾乃はどちらも C\# 開発者ですが、綾乃は米国に、直樹はインドにいます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-144">Prakash and Tricia are both C\# developers, but Tricia is in the United States, whereas Prakash is in India.</span></span> <span data-ttu-id="f60b1-145">プロジェクトへの取り組みのほとんどは、Contoso India と Contoso US のリソースを必要とし、直樹と綾乃はこの実践領域のプロジェクトで同じレベルのセキュリティ アクセスを必要とします。</span><span class="sxs-lookup"><span data-stu-id="f60b1-145">Most of the project engagements require resources from Contoso India and Contoso US, and Prakash and Tricia require the same level of security access to projects in this practice area.</span></span> <span data-ttu-id="f60b1-146">ところが、Contoso India の開発者のコストは、Contoso US の開発者のコストと大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-146">However, the cost of developers from Contoso India differs significantly from the cost of developers from Contoso US.</span></span>

<span data-ttu-id="f60b1-147">Dynamics 365 と PSA を使用して、このシナリオを設計する最適な方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-147">Here is an optimal way to design for this scenario by using Dynamics 365 and PSA.</span></span>

1. <span data-ttu-id="f60b1-148">Microsoft のテクノロジ プラクティスを部署として作成し、そこに直樹と綾乃を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-148">Create the Microsoft technology practice as a business unit, and associate Prakash and Tricia with it.</span></span> <span data-ttu-id="f60b1-149">この方法により、両方の従業員がその実践分野のプロジェクトに対して、同じレベルのセキュリティ アクセスを持つことを保証します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-149">In this way, you help guarantee that both employees have the same level of security access to any projects in that practice area.</span></span> <span data-ttu-id="f60b1-150">どちらも進捗を確認し、時間、経費、タスクの更新を報告できます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-150">They both will be able to check progress and report time, expenses, and task updates.</span></span> 
2. <span data-ttu-id="f60b1-151">2 つの組織単位を作成して、プロジェクトのコストが正しく反映されるようにします。</span><span class="sxs-lookup"><span data-stu-id="f60b1-151">Create two organizational units to hel guarantee that the cost to the project is correctly reflected.</span></span> 
3. <span data-ttu-id="f60b1-152">綾乃を Contoso US に関連付け、直樹を Contoso India に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-152">Associate Tricia wtih Contoso US and associate Prakash with Contoso India.</span></span>
4. <span data-ttu-id="f60b1-153">適切な原価価格表を両方の組織単位に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-153">Assign appropriate cost price lists to both organizational units.</span></span> <span data-ttu-id="f60b1-154">このようにして、プロジェクトに記録された綾乃と直樹のコストが、Contoso US と Contoso India のコストの差を正確に反映することを保証できます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-154">TIn this way, you help guarantee that the costs that are recorded on the project for Prakash and Tricia accurately reflect the difference in costs between Contoso US and Contoso India.</span></span>

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a><span data-ttu-id="f60b1-155">組織単位は Dynamics 365 の販売地域に関連していますか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-155">Are organizational units related to sales territories in Dynamics 365?</span></span>

<span data-ttu-id="f60b1-156">販売地域と組織単位との間に関連付けや関係はありません。</span><span class="sxs-lookup"><span data-stu-id="f60b1-156">There is no association or relationship between sales territories and organizational units.</span></span> <span data-ttu-id="f60b1-157">販売地域は通常、販売が行われる地理的領域です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-157">A sales territory is typically a geographical area where sales occur.</span></span> <span data-ttu-id="f60b1-158">販売価格表は、それぞれの販売地域に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-158">A sales price list can be associated with each sales territory.</span></span>

<span data-ttu-id="f60b1-159">組織単位は、会社の内部グループや部門であり、他の部門や外部の顧客に販売する一連の役割のコストを追跡します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-159">An organizational unit is an internal group or division in the company that tracks costs for a set of roles that it sells to other divisions or to external customers.</span></span>

#### <a name="example-of-organizational-units-and-sales-territories"></a><span data-ttu-id="f60b1-160">組織単位と販売地域の例</span><span class="sxs-lookup"><span data-stu-id="f60b1-160">Example of organizational units and sales territories</span></span>

<span data-ttu-id="f60b1-161">Contoso, Ltd. 社には Contoso US と Contoso India の 2 つの開発センターがあります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-161">Contoso, Ltd. has two development centers: Contoso US and Contoso India.</span></span> <span data-ttu-id="f60b1-162">これらの 2 つの開発センターでは、リソースのコストが大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-162">Costs of resources differ greatly between these two development centers.</span></span>

<span data-ttu-id="f60b1-163">Contoso 社は、ラテン アメリカ、北米、アジア太平洋、西ヨーロッパ、中東など、多くの国際市場で IT サービスを販売しています。</span><span class="sxs-lookup"><span data-stu-id="f60b1-163">Contoso sells its IT services in many international markets, such as Latin America, North America, Asia-Pacific, Western Europe, and the Middle East.</span></span> <span data-ttu-id="f60b1-164">同じプロジェクトの役割の請求レートは、これらの市場ごとに大きく異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-164">Bill rates for the same project roles can vary widely across these markets.</span></span>

<span data-ttu-id="f60b1-165">Contoso US と Contoso India を組織単位として設定し、それぞれの組織単位に独自の原価価格表を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-165">Contoso US and Contoso India should be set up as organizational units, and each organizational unit should have its own cost price list.</span></span> <span data-ttu-id="f60b1-166">アジア太平洋、ラテン アメリカ、北米、西ヨーロッパ、中東を販売地域として設定し、それぞれの販売地域に独自の販売価格表を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-166">Asia-Pacific, Latin America, North America, Western Europe, and the Middle East should be set up as sales territories, and each sales territory should have its own sales price list.</span></span>

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a><span data-ttu-id="f60b1-167">組織単位と価格表の関連付けに制限があるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-167">Why is there a restriction on the association of price lists with organizational units?</span></span> 

<span data-ttu-id="f60b1-168">通常、販売価格はサービスが販売される地理的領域や市場に固有です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-168">Sales pricing is usually unique to the geographical areas or markets where services are sold.</span></span> <span data-ttu-id="f60b1-169">会社の内部部門は、同じタイプのサービスに対して通常は独自の販売価格を設定しません。</span><span class="sxs-lookup"><span data-stu-id="f60b1-169">Internal divisions of a company don't usually have their own sales pricing for the same type of services.</span></span> <span data-ttu-id="f60b1-170">ただし、内部部門では雇用する従業員のスキルと事業を展開する地域の労働条件に応じて、売却済商品の原価 (COGS) が異なります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-170">However, internal divisions have a different cost of goods sold (COGS), depending on the skills of the people that they employ and the labor conditions of the region where they operate.</span></span> <span data-ttu-id="f60b1-171">組織単位は会社の内部部門としてモデル化されるため、原価価格表のみを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-171">Because organizational units are modeled as internal divisions of a company, they can have only cost price lists.</span></span>

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a><span data-ttu-id="f60b1-172">販売価格表を組織単位に関連付けることができないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-172">Why can’t we associate sales price lists to organizational units?</span></span>

<span data-ttu-id="f60b1-173">PSA では販売価格表を顧客と販売地域に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-173">In PSA, sales price lists can be associated with customers and sales territories.</span></span> <span data-ttu-id="f60b1-174">営業案件、プロジェクト契約、プロジェクトのようなトランザクション エンティティは、顧客アカウントや販売地域に添付される販売価格表を使用して、プロジェクト エンゲージメントの請求レートと潜在的な収益を決定します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-174">Transactional entities like Opportunity, Quote, Project Contract, and Project use sales price lists that are attached to the customer account or the sales territory to determine bill rates and potential revenue on the project engagement.</span></span>

<span data-ttu-id="f60b1-175">原価価格表は組織単位に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-175">Cost price lists are associated with organizational units.</span></span> <span data-ttu-id="f60b1-176">営業案件、プロジェクト契約、プロジェクトのようなトランザクション エンティティは、契約単位に添付される原価価格表を使用して、プロジェクト契約のコストを決定します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-176">Transactional entities like Opportunity, Quote, Project Contract, and Project use cost price lists that are attached to the contracting unit to determine costs to a project engagement.</span></span>

### <a name="are-organizational-units-hierarchical-in-psa"></a><span data-ttu-id="f60b1-177">PSA の組織単位は階層的ですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-177">Are organizational units hierarchical in PSA?</span></span>

<span data-ttu-id="f60b1-178">番号</span><span class="sxs-lookup"><span data-stu-id="f60b1-178">No.</span></span> <span data-ttu-id="f60b1-179">PSA の現在のリリースでは組織単位は階層的ではありません。</span><span class="sxs-lookup"><span data-stu-id="f60b1-179">In the current release of PSA, organizational units are not hierarchical.</span></span> <span data-ttu-id="f60b1-180">これは次のことができないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-180">This means that you can’t:</span></span>

- <span data-ttu-id="f60b1-181">階層横断的な既定の原価価格のパターン構成</span><span class="sxs-lookup"><span data-stu-id="f60b1-181">Configure a pattern for defaulting cost prices that traverses up a hierarchy.</span></span> 
- <span data-ttu-id="f60b1-182">組織単位の階層についてさまざまなレベルでロールアップした収益やコストの報告。</span><span class="sxs-lookup"><span data-stu-id="f60b1-182">Report revenue or cost rolled up at different levels of the organizational unit hierarchy.</span></span>

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a><span data-ttu-id="f60b1-183">私たちはコスト センター、部門、請求オフィスの複雑で多層な階層を持つ大規模な多国籍企業です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-183">We're a big multinational firm with a complex, multilevel hierarchy of cost centers, divisions, and billing offices.</span></span> <span data-ttu-id="f60b1-184">このバージョンの Project Service アプリで、組織単位の概念を最大限に活用するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-184">How can we make the best use of the organizational unit concept in this version of the Project Service app?</span></span>

<span data-ttu-id="f60b1-185">コスト センター、部門、請求オフィスなどの複雑な階層がある場合、その階層のリーフ ノードを個別の組織単位として設定します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-185">When you have a complex hierarchy of cost centers, divisions, billing offices, etc., set up the leaf nodes of that hierarchy as distinct organizational units.</span></span>
<span data-ttu-id="f60b1-186">典型的な階層を次の例で示します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-186">The following example shows a typical hierarchy:</span></span>

<span data-ttu-id="f60b1-187">**Contoso India**</span><span class="sxs-lookup"><span data-stu-id="f60b1-187">**Contoso India**</span></span>

  - <span data-ttu-id="f60b1-188">SAP の実践</span><span class="sxs-lookup"><span data-stu-id="f60b1-188">SAP Practice</span></span> 

    - <span data-ttu-id="f60b1-189">技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-189">Technical Consultants</span></span> 
    - <span data-ttu-id="f60b1-190">機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-190">Functional Consultants</span></span> 
    
  - <span data-ttu-id="f60b1-191">Microsoftテクノロジの実践</span><span class="sxs-lookup"><span data-stu-id="f60b1-191">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="f60b1-192">技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-192">Technical Consultants</span></span>
    - <span data-ttu-id="f60b1-193">機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-193">Functional Consultants</span></span> 
    
<span data-ttu-id="f60b1-194">**Contoso US**</span><span class="sxs-lookup"><span data-stu-id="f60b1-194">**Contoso US**</span></span>

 - <span data-ttu-id="f60b1-195">SAP の実践</span><span class="sxs-lookup"><span data-stu-id="f60b1-195">SAP Practice</span></span> 

    - <span data-ttu-id="f60b1-196">技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-196">Technical Consultants</span></span> 
    - <span data-ttu-id="f60b1-197">機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-197">Functional Consultants</span></span> 
    
 - <span data-ttu-id="f60b1-198">Microsoftテクノロジの実践</span><span class="sxs-lookup"><span data-stu-id="f60b1-198">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="f60b1-199">技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-199">Technical Consultants</span></span> 
    - <span data-ttu-id="f60b1-200">機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-200">Functional Consultants</span></span> 
 
<span data-ttu-id="f60b1-201">階層が類似している場合、以下に示すようにフラット リストとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-201">If your hierarchy is similar, you must set it up as a flat list, as shown here:</span></span>
- <span data-ttu-id="f60b1-202">Contoso India - SAP の実践 - 技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-202">Contoso India - SAP Practice - Technical Consultants</span></span> 
- <span data-ttu-id="f60b1-203">Contoso India - SAP の実践 - 機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-203">Contoso India - SAP Practice - Functional Consultants</span></span>       
- <span data-ttu-id="f60b1-204">Contoso India - Microsoft テクノロジの実践、機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-204">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="f60b1-205">Contoso India - Microsoft テクノロジの実践、機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-205">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="f60b1-206">Contoso US - SAP の実践 - 技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-206">Contoso US - SAP Practice - Technical Consultants</span></span>  
- <span data-ttu-id="f60b1-207">Contoso US - SAP の実践 - 機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-207">Contoso US - SAP Practice - Functional Consultants</span></span>  
- <span data-ttu-id="f60b1-208">Contoso US - Microsoft テクノロジの実践 - 技術コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-208">Contoso US - Microsoft Technology Practice - Technical Consultants</span></span> 
- <span data-ttu-id="f60b1-209">Contoso US - Microsoft テクノロジの実践 - 機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="f60b1-209">Contoso US - Microsoft Technology Practice - Functional Consultants</span></span>

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a><span data-ttu-id="f60b1-210">私たちは、1 つの部門として運営している小さな専門サービス企業です。</span><span class="sxs-lookup"><span data-stu-id="f60b1-210">We're a small professional services company that operates as only one division.</span></span> <span data-ttu-id="f60b1-211">現在のバージョンの PSA で組織単位の概念をどのように最適に利用できますか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-211">How can we best use the organizational unit concept in the current version of PSA?</span></span>

<span data-ttu-id="f60b1-212">会社を 1 つの原価価格表を持つ 1 つの単位として運営している場合、組織単位を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f60b1-212">If your company operates as one unit that has one cost price list, you don't have to set up any organizational units.</span></span> <span data-ttu-id="f60b1-213">PSA のインストール中に Dynamics 365 は組織と同じ名前を持つ既定の組織単位を 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="f60b1-213">During PSA installation, Dynamics 365 creates one default organizational unit that has the same name as the organization.</span></span> <span data-ttu-id="f60b1-214">すべてのユーザーがこの組織単位に既定で割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-214">By default, all users are assigned to this organizational unit.</span></span> <span data-ttu-id="f60b1-215">システムが組織単位の選択を必要とする場合、常にこの組織単位が既定で選択されます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-215">Whenever the system requires that an organizational unit be selected, this organizational unit is selected by default.</span></span>

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a><span data-ttu-id="f60b1-216">見積もりやプロジェクト契約品目からプロジェクトが作成される場合、既定の契約単位は見積もりやプロジェクト契約から取得されます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-216">When a project is created from a quote or project contract line, the default contracting unit comes from the quote or project contract.</span></span> <span data-ttu-id="f60b1-217">見積もりやプロジェクト契約などの販売エンティティの前にプロジェクトを作成する場合、既定の契約単位は何ですか。</span><span class="sxs-lookup"><span data-stu-id="f60b1-217">If a project is created before sales entities such as quote or project contract, what is the default contracting unit?</span></span>

<span data-ttu-id="f60b1-218">プロジェクトを独自に作成する場合、プロジェクトの既定の契約単位は、プロジェクトを作成したユーザーに基づきます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-218">When a project is created on its own, the default contracting unit of the project is based on the user who creates it.</span></span> <span data-ttu-id="f60b1-219">そのユーザーは既定のプロジェクト マネージャーでもあります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-219">That user is also the default project manager.</span></span> <span data-ttu-id="f60b1-220">プロジェクトが見積もりやプロジェクト契約などの販売エンティティにマップされる場合、プロジェクトの契約単位は代わりに販売エンティティに基づきます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-220">If the project is mapped to a sales entity such as a quote or project contract, the contracting unit on the project is based on the sales entity instead.</span></span> <span data-ttu-id="f60b1-221">この場合には、契約単位が変更された場合のコスト見積もり変更の計算に原価価格表が使用されるため、プロジェクトの見積もりが再計算される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60b1-221">In this case, project estimates might be recalculated, because the cost price list is used to calculate the cost estimate changes if the contracting unit is changed.</span></span> <span data-ttu-id="f60b1-222">販売価格表は、見積もりのプロジェクト価格表と同期するように変更される販売見積もりの計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-222">The sales price list is used to calculate the sales estimates that will be changed so that they are in sync with the project price list on the quote.</span></span>

<span data-ttu-id="f60b1-223">プロジェクトがマップされる販売エンティティ (見積もりやプロジェクト契約) の値と同期する必要があるため、プロジェクトの **契約単位** フィールドと **通貨** フィールドは編集がロックされます。</span><span class="sxs-lookup"><span data-stu-id="f60b1-223">The **Contracting Unit** and **Currency** fields on the project are locked for editing, because they must be in sync with the values on the sales entity (quote or project contract) that the project is mapped to.</span></span>
