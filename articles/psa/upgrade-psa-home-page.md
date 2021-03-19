---
title: ホーム ページのアップグレード
description: このトピックでは、Dynamics 365 Project Service Automation の新しい、変更された機能に関する重要な情報の見つけ方、および最新バージョンへのアップグレードの手順を説明します。
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.openlocfilehash: 838eecb1229ea20106c7d5487dc37a81e8df501b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281709"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="7d0c8-103">ホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="7d0c8-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="7d0c8-104">PSA バージョン 2.x または 1.x からバージョン 3.x へのアップグレード</span><span class="sxs-lookup"><span data-stu-id="7d0c8-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="7d0c8-105">新しいインスタンス</span><span class="sxs-lookup"><span data-stu-id="7d0c8-105">New instances</span></span>

<span data-ttu-id="7d0c8-106">2019 年 5 月 17 日から、新しいインスタンスの Project Service Automation が選択されている場合、バージョン 3.x が既定でインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="7d0c8-107">既存のインスタンス</span><span class="sxs-lookup"><span data-stu-id="7d0c8-107">Existing instances</span></span>

<span data-ttu-id="7d0c8-108">以前、顧客が 2.x のインスタンスを持っているが、PSA の統一顧客インターフェイス ベース (UCI) のバージョンである PSA バージョン 3.x. にアップグレードする必要がある場合は、サポートがバージョン 3.x. へのアップグレードできるように、Microsoft サポートに連絡して顧客のインスタンスの詳細情報を提供する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="7d0c8-109">2020 年 3 月 1 日の時点で、PSA バージョン 2.x のインスタンスを持っておりバージョン 3.x にアップグレードする必要がある顧客は、Microsoft サポートに連絡することなく、管理ポータルから直接インスタンスをアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d0c8-110">PSA バージョン 3.x には大きな変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="7d0c8-111">これは、ユーザー エクスペリエンスを高める際に役立つように、統一インターフェイス フレームワークで構築されています。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="7d0c8-112">再設計済みのアプリケーションでは、一貫性のある統一ユーザー インターフェイス (UI) を提供しています。また、画面のサイズまたはデバイスを使用して最適に表示するためにレスポンシブ デザインの原則を採用しています。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="7d0c8-113">アプリケーション全体で他にも変更を行っています。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="7d0c8-114">変更された領域の一部には、価格、予約、およびリソースの割り当て、時間、経費、承認が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="7d0c8-115">アップグレード プロセスを開始する前に、以下のタスクを完了することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="7d0c8-116">Dynamics 365 Field Service および Project Service Automation の両方が、指定したインスタンスにインストールされているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="7d0c8-117">双方のソリューションがインストールされている場合は、定期的なインスタンスの使用を再開する前に両方ともアップグレードするプランを立ててください。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="7d0c8-118">次のトピックをよく確認してください。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-118">Carefully review the following topics.</span></span> <span data-ttu-id="7d0c8-119">バージョン間での変更に関して認知および解釈しておくと、アップグレード プロセスで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="7d0c8-120">このトピックでは、PSA での大きな変更に関する情報とともに、3.x バージョンにアップグレードするプランを立てる場合のお勧めの方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="7d0c8-121">Project Service Automation バージョン 3 の最新情報または変更事項</span><span class="sxs-lookup"><span data-stu-id="7d0c8-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="7d0c8-122">アップグレードの考慮事項 - Project Service Automation バージョン 2.x または 1.x から バージョン 3 へ</span><span class="sxs-lookup"><span data-stu-id="7d0c8-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="7d0c8-123">サンドボックス インスタンスをアップグレードしてから実装の変更について評価し、実稼働インスタンスをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="7d0c8-124">先ほど説明したトピックを確認し、PSA バージョン 3.x または UCI ベース バージョンへのアップグレードの準備が完了したら、管理センターのアップグレードを有効にするように Microsoft サポートに要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="7d0c8-125">要求する際には、ユーザーのインスタンスについての詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="7d0c8-126">新しく作成したインスタンスの PSA (PSA バージョン 2.x) の古いバージョン</span><span class="sxs-lookup"><span data-stu-id="7d0c8-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="7d0c8-127">2019 年 5 月 17 日から、すべての新規インスタンスには、既定のクライアントとして UCI が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="7d0c8-128">この変更を使用して配置する場合は、 PSA version 3.x および Field Service バージョン 8.x が規定でプロビジョニングされるようになります。これらが UCI クライアントで機能するように設計されているためです。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="7d0c8-129">2020 年 3 月 1 日以降、Dynamics PSA の顧客は、PSA バージョン 2.x 以下などの古いバージョンの PSA で新しい環境を作成できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="7d0c8-130">新しい環境では、PSA のバージョン 3.x のみを取得することになります。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="7d0c8-131">旧バージョンの Field Service および PSA アプリケーションを使用する場合の一番のエクスペリエンスとしては **システム設定** ページに移動し、フィールドの場合は **新しい統一インターフェイスのみ (推奨) を使用する** フィールドに移動して、**いいえ** を選択します。これらのバージョンが UCI で現在ロードできるように設計されていないためです。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="7d0c8-132">UCI を停止後に、古い Web クライアントを使用することによって、Field Service や PSA のバージョンを開いて実行できます。</span><span class="sxs-lookup"><span data-stu-id="7d0c8-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]