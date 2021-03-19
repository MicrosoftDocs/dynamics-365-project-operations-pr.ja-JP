---
title: 法人ごとに Project Operations 統合を構成する
description: このトピックでは、Project Operations で法人による統合の設定方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276984"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="29068-103">法人ごとに Project Operations 統合を構成する</span><span class="sxs-lookup"><span data-stu-id="29068-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="29068-104">_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_</span><span class="sxs-lookup"><span data-stu-id="29068-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="29068-105">このトピックは、法人ごとに Dynamics 365 Project Operations を構成するのに必要な手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="29068-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="29068-106">Dynamics 365 Finance の機能キーを有効にする</span><span class="sxs-lookup"><span data-stu-id="29068-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="29068-107">必要な機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="29068-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="29068-108">Dynamics 365 Finance では、**機能管理** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="29068-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="29068-109">**機能リスト** に、次の機能を見つけて有効にします。</span><span class="sxs-lookup"><span data-stu-id="29068-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="29068-110">**プロジェクトの複数の契約ラインを有効にする**</span><span class="sxs-lookup"><span data-stu-id="29068-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="29068-111">**Dynamics 365 Customer Engagement 上の Project Operations を有効にする**</span><span class="sxs-lookup"><span data-stu-id="29068-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="29068-112">**機能キー** がリストされていない場合は、Finance バージョンが最小バージョン要件 (すべての品質更新が適用されたアプリケーション バージョン 10.0.13 以上) を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="29068-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="29068-113">**アップデートを確認する** を選択して、機能リストを更新します。</span><span class="sxs-lookup"><span data-stu-id="29068-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="29068-114">法人の Project Operations 展開シナリオを定義する</span><span class="sxs-lookup"><span data-stu-id="29068-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="29068-115">法人レベルで Dynamics 365 Customer Engagement で Project Operations を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="29068-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="29068-116">リソース/在庫のないベースのシナリオに対して Dynamics 365 Customer Engagement の Project Operations を使用して 1 つの法人を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="29068-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="29068-117">同じ環境で、在庫/製造指図シナリオの Project Operations を使用して別の法人を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="29068-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="29068-118">Dynamics 365 Finance で、**プロジェクト管理と会計** > **設定** > **グローバル プロジェクト管理と会計パラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29068-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="29068-119">利用可能な法人のリストで、有効にする Dynamics 365 Customer Engagement 機能で複数の契約ラインと Project Operations が行われているエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="29068-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="29068-120">在庫/製造指図シナリオで Project Operations を使用する法人は選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="29068-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="29068-121">法人は、既存のプロジェクトがない場合にのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="29068-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="29068-122">プロジェクト管理および会計パラメーター ページを構成します。</span><span class="sxs-lookup"><span data-stu-id="29068-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="29068-123">Dynamics 365 Customer Engagement の Project Operations を使用する各法人は、規定パラメータのセットが必要です。</span><span class="sxs-lookup"><span data-stu-id="29068-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="29068-124">これらのパラメータは、**プロジェクト管理と会計パラメータ** ページの **プロジェクト運営** タブで構成します。</span><span class="sxs-lookup"><span data-stu-id="29068-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="29068-125">このパラメーターは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="29068-125">The parameters are:</span></span>

  - <span data-ttu-id="29068-126">**請求タイプのデフォルト**: Project Operations は、明細プロパティ Finance にマップする必要がある請求タイプの既定の固定セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="29068-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="29068-127">請求タイプごとにレコードを作成します: **指定されていない**、**有料**、**非課金**、**無料**、**利用不可**。</span><span class="sxs-lookup"><span data-stu-id="29068-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="29068-128">**プロジェクトカテゴリのデフォルト**: 各トランザクション タイプに使用する規定のプロジェクト カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="29068-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="29068-129">これらの規定は、**Project Operations 統合ジャーナル** とプロジェクト実績のトランザクション カテゴリが指定されていない見積もりで使用されます。</span><span class="sxs-lookup"><span data-stu-id="29068-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="29068-130">**予測**: 時間と費用の見積もりに使用する予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="29068-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]