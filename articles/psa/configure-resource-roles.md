---
title: リソース ロールの構成
description: Project Service でのリソース ロールの構成方法
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 59c66aa7bd6c481f8db3088bede71c1ab81a203f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999317"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="daa7c-103">リソース ロールの構成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="daa7c-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="daa7c-104">ロールは、プロジェクトの計画でプロジェクトのリソースの要件またはコストを決定するとき、重要な役割を果します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="daa7c-105">プロジェクトが必要とするロールごとに、リソース ロールを作成し、そのロールにスキルと能力を関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="daa7c-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="daa7c-106">たとえば、開発者、プロジェクト管理者、またはゲーム テスターのロールを作成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="daa7c-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="daa7c-107">また、ロールに必要とされるスキルと能力レベルも設定します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="daa7c-108">組織にとって有効なプロジェクトの見積もりを確保するように、リソースのロールを構成します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="daa7c-109">また、請求の種類の設定が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="daa7c-110">請求不可の請求の種類に設定されている品目は、契約または見積もりの明細行に表示されません。</span><span class="sxs-lookup"><span data-stu-id="daa7c-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="daa7c-111">リソースのロールを設定すると、コストと販売価格を価格表を使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="daa7c-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="daa7c-112">追加するロールごとに、以下の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="daa7c-113">**Project Service > リソース ロール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="daa7c-114">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="daa7c-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="daa7c-115">**全般** 領域で、ロールの名前を **名前** に入力してから、必要に応じて他のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="daa7c-116">**保存** をクリックしてレコードを作成します。これにより、そのレコードの編集を継続できます。</span><span class="sxs-lookup"><span data-stu-id="daa7c-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="daa7c-117">**スキル** 領域で、**+** をクリックしてスキルを追加します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="daa7c-118">**ロールのコンピテンシー要件** ウィンドウで、**スキル** フィールドをクリックし、**検索** ボタンをクリックしてから、スキルを選択します。</span><span class="sxs-lookup"><span data-stu-id="daa7c-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="daa7c-119">このスキルの能力を選択し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="daa7c-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="daa7c-120">必要に応じて、スキルの追加を続けます。</span><span class="sxs-lookup"><span data-stu-id="daa7c-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="daa7c-121">完了したら、画面の右下隅の **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="daa7c-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="daa7c-122">このリソース ロールを使用するプロジェクトが使用可能にするためには、**アクティブ化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="daa7c-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="daa7c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="daa7c-123">See Also</span></span>  
 [<span data-ttu-id="daa7c-124">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="daa7c-124">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]