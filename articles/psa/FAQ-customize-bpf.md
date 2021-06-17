---
title: プロジェクト ストレージ業務プロセス フロー内をカスタマイズする方法を教えてください。
description: プロジェクト ステージ の ビジネス プロセス フロー をカスタマイズする方法
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993152"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="52d4a-103">プロジェクト ストレージ業務プロセス フロー内をカスタマイズする方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="52d4a-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="52d4a-104">プロジェクト ステージ業務プロセス フロー内のステージの名前が、想定される英語の名前 (**Quote**、**Plan**、**Close**) と一致させる必要があるという既知の制限が、Project Service アプリケーションの以前のバージョンにはあります。</span><span class="sxs-lookup"><span data-stu-id="52d4a-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="52d4a-105">それ以外の場合は、英語のステージ名に依存するビジネス ロジックが予想どおりに動作しません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="52d4a-106">このため、プロジェクト フォームで使用できる **プロセスの切り替え** または **プロセスの編集** など使い慣れたアクションが表示されず、ビジネス プロセス フローのカスタマイズが推奨されません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="52d4a-107">この制限は、バージョン 2.4.5.48 以降で対処されています。</span><span class="sxs-lookup"><span data-stu-id="52d4a-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="52d4a-108">この資料では、以前のバージョンの既定の業務プロセス フローをカスタマイズする必要がある場合に推奨される回避策を示します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="52d4a-109">ビジネス ロジックでは、英語のステージ名と完全に一致させる必要があります</span><span class="sxs-lookup"><span data-stu-id="52d4a-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="52d4a-110">プロジェクト ステージ業務プロセス フローには、アプリケーションの動作を制御するビジネス ロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="52d4a-111">プロジェクトが見積もりに関連付けられると、コードによって業務プロセス フローが **Quote** ステージに設定されます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="52d4a-112">プロジェクトが契約に関連付けられると、コードによって業務プロセス フローが **Plan** ステージに設定されます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="52d4a-113">業務プロセス フローが **Close** ステージに進むと、プロジェクト レコードが非アクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="52d4a-114">プロジェクトが非アクティブ化されると、プロジェクト フォームおよび WBS (作業分解構造)が読み取り専用に設定されて、指定されたリソースの予約が解放され、関連する価格表が非アクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="52d4a-115">このビジネス ロジックは、プロジェクト ステージの英語の名前に依存します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="52d4a-116">英語名のこの依存関係は、プロジェクト ステージ業務プロセス フローのカスタマイズが推奨されないことと、プロジェクト エンティティに **プロセスの切り替え** または **プロセスの編集** などの一般的なビジネス プロセス フロー アクションが表示されないことの主な理由です。</span><span class="sxs-lookup"><span data-stu-id="52d4a-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="52d4a-117">英語名がステージ名と一致しない場合はどうなりますか?</span><span class="sxs-lookup"><span data-stu-id="52d4a-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="52d4a-118">8.2 プラットフォームにおける Project Service アプリケーション バージョン 1.x では、ビジネス プロセス フローの英語ステージ名が名前に正確に一致しないと、見積もりまたは契約の適切なステージを設定するビジネス ロジック、またはプロジェクトを閉じるビジネス ロジックがスキップされます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="52d4a-119">エラー メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-119">No error messages are displayed.</span></span> <span data-ttu-id="52d4a-120">したがって、プロジェクト ステージの業務プロセス フローをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="52d4a-121">ただし、見積もり、契約、プロジェクト終了の自動プロセスは何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="52d4a-122">9.0 プラットフォームの Project Service アプリ バージョン 2.4.4.30 以前では、業務プロセス フロー内のアーキテクチャが大幅に変更されたため、業務プロセス フロー ビジネス ロジックを書き直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="52d4a-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="52d4a-123">そのため、プロセスのステージ名が必要な英語の名前に一致しない場合、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="52d4a-124">したがって、プロジェクト エンティティのプロジェクト ステージ業務プロセス フローをカスタマイズするには、現状のまま **Quote**、**Plan**、**Close** ステージを保持しながら、プロジェクト エンティティに対する既定の業務プロセス フローに新しいブランド ステージのみ追加します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="52d4a-125">この制限は、業務プロセス フローで英語名が期待されるビジネス ロジックでエラーが表示されません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="52d4a-126">バージョン 2.4.5.48 以降では、この記事で説明されているビジネス ロジックがプロジェクト エンティティの既定の業務プロセス フローから削除されています。</span><span class="sxs-lookup"><span data-stu-id="52d4a-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="52d4a-127">そのバージョン以降にアップグレードすると、既定の業務プロセス フローをカスタマイズするか、自身のものに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="52d4a-128">以前のバージョンの回避策</span><span class="sxs-lookup"><span data-stu-id="52d4a-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="52d4a-129">アップグレードできない場合、次に示す 2 つの方法のいずれかでプロジェクト エンティティのプロジェクト ステージの業務プロセス フローをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="52d4a-130">**Quote**、**Plan**、**Close** の英語ステージ名を保持したまま、既定の構成に追加ステージを追加します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![既定の構成にステージを追加する方法のスクリーンショット](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="52d4a-132">独自のビジネス プロセス フローを作成し、必要なステージ名にできるプロジェクト エンティティの主な業務プロセス フローを作成します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="52d4a-133">ただし、同じ標準プロジェクト ステージの **Quote**、**Plan**、**Close** を使用する場合、カスタム ステージ名から削除されるいくつかのカスタマイズを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52d4a-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="52d4a-134">複雑なロジックは、プロジェクトの完了にあります。ただし、プロジェクト レコードを非アクティブ化することによってトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF のカスタマイズ](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="52d4a-136">プラットフォーム 9.0 の Project Service アプリ バージョン 2.4.4.30 以前の追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="52d4a-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="52d4a-137">カスタム ビジネス プロセス フローを持つプラットフォーム 9.0 の Project Service 2.4.4.30 以前では、**ステージ別プロジェクト** グラフおよびプロジェクト リスト ビューで使用されるプロジェクト エンティティの **ステージ名** フィールドは、既定のプロジェクト ステージ業務プロセス フローと組み合わされていないため更新されません。</span><span class="sxs-lookup"><span data-stu-id="52d4a-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="52d4a-138">以下の手順に従ってこの問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="52d4a-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="52d4a-139">カスタム ビジネス プロセスをユーザーが進めるときに、更新された現在の業務プロセス フロー ステージを取得するにはユーザー定義フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="52d4a-140">既定の構成ではなく、ユーザー定義フィールドで機能するように **ステージ別プロジェクト** グラフを変更します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="52d4a-141">プロジェクト エンティティ用に独自の業務プロセス フローを作成する手順</span><span class="sxs-lookup"><span data-stu-id="52d4a-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="52d4a-142">プロジェクト エンティティ用に独自の業務プロセス フローを作成するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="52d4a-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="52d4a-143">**設定** > **プロセス センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="52d4a-144">Project Service ビジネス ロジックもコピーされるため、プロジェクト ステージ業務プロセス フローをコピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="52d4a-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![プロセスの作成](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="52d4a-146">プロセス デザイナーを使用して必要なステージ名を作成します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="52d4a-147">**Quote**、**Plan**、**Close** の既定のステージと同じ機能が必要な場合、カスタム業務プロセス フローのステージ名に基づいてこのフォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52d4a-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![BPF をカスタマイズするのに使用されるプロセス デザイナーのスクリーンショット](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="52d4a-149">プロセス デザイナーで、一覧の上部にプロジェクト ステージ業務プロセス フローを移動することで、**受注プロセス フロー** をクリックしてカスタム業務プロセス フローをプロジェクト エンティティの主業務プロセス フローにします。</span><span class="sxs-lookup"><span data-stu-id="52d4a-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="52d4a-150">受注プロセス フローの使用のスクリーンショット</span><span class="sxs-lookup"><span data-stu-id="52d4a-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="52d4a-151">以下のステップは、9.0 プラットフォームの Project Service アプリ 2.4.4.30 以前に適用されます</span><span class="sxs-lookup"><span data-stu-id="52d4a-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="52d4a-152">カスタム業務プロセス フローのカスタム ステージを取得するためにプロジェクト エンティティに新しいユーザー定義フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="52d4a-153">カスタム業務プロセス フローでステージが更新されたときに、このフィールドを更新するようにビジネス ロジック (プラグイン/ワークフロ) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52d4a-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![プロジェクト エンティティのカスタマイズのスクリーンショット](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="52d4a-155">ステージに対して新しいカスタム フィールドを使用するために、**ステージ別プロジェクト** グラフを変更します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![[ステージ別プロジェクト] グラフの使用のスクリーンショット](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="52d4a-157">ステージの新しいカスタム フィールドを含めるにはプロジェクト エンティティのビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="52d4a-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![プロジェクト エンティティでのビューの変更のスクリーンショット](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]