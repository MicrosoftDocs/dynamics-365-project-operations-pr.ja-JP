---
title: 追加パラメーターの設定を構成する
description: Project Service での追加パラメーター設定の構成方法
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151574"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="6f88c-103">追加パラメーター設定の構成 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6f88c-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6f88c-104">前のトピックで項目を構成してある場合は、プロジェクトで使用する追加のプロジェクト パラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f88c-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="6f88c-105">最初に [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] をインストールしたときは、作業する [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に必要なすべてのレコードを最初に作成するためのパラメーター設定を作成しました。</span><span class="sxs-lookup"><span data-stu-id="6f88c-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="6f88c-106">ここで元に戻り、この設定の追加フィールドを構成します。</span><span class="sxs-lookup"><span data-stu-id="6f88c-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="6f88c-107">次の設定の構成を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f88c-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="6f88c-108">組織単位</span><span class="sxs-lookup"><span data-stu-id="6f88c-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="6f88c-109">請求頻度</span><span class="sxs-lookup"><span data-stu-id="6f88c-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="6f88c-110">作業時間テンプレート</span><span class="sxs-lookup"><span data-stu-id="6f88c-110">Work hours template</span></span>  
  
-   <span data-ttu-id="6f88c-111">価格表</span><span class="sxs-lookup"><span data-stu-id="6f88c-111">Price list</span></span>  
 
<span data-ttu-id="6f88c-112">このステップでは、必要とするリソース割り当てのタイプの指定も行います。</span><span class="sxs-lookup"><span data-stu-id="6f88c-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="6f88c-113">**中央**。</span><span class="sxs-lookup"><span data-stu-id="6f88c-113">**Central**.</span></span> <span data-ttu-id="6f88c-114">リソース管理者のみがプロジェクトにリソースを割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="6f88c-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="6f88c-115">**ハイブリッド**。</span><span class="sxs-lookup"><span data-stu-id="6f88c-115">**Hybrid**.</span></span> <span data-ttu-id="6f88c-116">リソース管理者、プロジェクト管理者、アカウント管理者がプロジェクトにリソースを割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="6f88c-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="6f88c-117">プロジェクト パラメーターの設定方法:</span><span class="sxs-lookup"><span data-stu-id="6f88c-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="6f88c-118">**Project Service > パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f88c-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="6f88c-119">構成するパラメーター設定 ([!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を最初にインストールしたときに作成したもの) をクリックするか、**新規** をクリックして新規作成します。</span><span class="sxs-lookup"><span data-stu-id="6f88c-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="6f88c-120">**全般** 領域で、プロジェクト パラメーターで使用するすべてのオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f88c-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="6f88c-121">**価格表** 領域で、**+** をクリックして価格表を追加して、**プロジェクト パラメーター価格表** ドロップダウン リストで価格表を選択し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f88c-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="6f88c-122">画面の右下隅にある **保存** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f88c-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="6f88c-123">Project Service が正しく機能するには、プロジェクト パラメータ のレコードを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f88c-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="6f88c-124">このレコードを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f88c-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="6f88c-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f88c-125">See Also</span></span>  
 [<span data-ttu-id="6f88c-126">リソースの設定</span><span class="sxs-lookup"><span data-stu-id="6f88c-126">Set up resources</span></span>](../psa/set-up-resources.md)
