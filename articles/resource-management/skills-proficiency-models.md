---
title: スキルおよび認定資格
description: このトピックでは、リソースへのスキルと認定資格の特性の追加について説明します。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4c814754e68b3a1a8bf8784434d45010bf8d0123
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079185"
---
# <a name="skills-and-certifications"></a><span data-ttu-id="1dd23-103">スキルおよび認定資格</span><span class="sxs-lookup"><span data-stu-id="1dd23-103">Skills and certifications</span></span>
<span data-ttu-id="1dd23-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="1dd23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1dd23-105">特性は、リソースの能力を説明するために使用される属性に関する情報を追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-105">Characteristics are used to enrich the attributes used to describe the abilities of a resource.</span></span> <span data-ttu-id="1dd23-106">リソースの各特性は、 **スキル** または **認定資格** として説明されます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-106">Each characteristic of a resource can be described as a **Skill** or a **Certification**.</span></span>

<span data-ttu-id="1dd23-107">リソース要件に特性を追加することにより、リソースがプロジェクトのタスクを完了するのに必要な情報または専門知識を文書化することができます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-107">Adding characteristics to resource requirements lets you document the knowledge or expertise needed by a resource to complete tasks on a project.</span></span> <span data-ttu-id="1dd23-108">特性を使用すると、リソース要件をスケジュールするときに、必要な特性を持つリソースに対して使用可能なリソースの一覧をフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-108">Characteristics let you filter the list of available resources to those resources that have the required characteristics when scheduling the resource requirement.</span></span>

## <a name="add-characteristics"></a><span data-ttu-id="1dd23-109">特性の追加</span><span class="sxs-lookup"><span data-stu-id="1dd23-109">Add characteristics</span></span>

1. <span data-ttu-id="1dd23-110">メイン メニューから **リソース** を開き、 **リソース** セクションで **スキル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-110">From the main menu, open **Resources** and in the **Resources** section, select **Skills**.</span></span>
2. <span data-ttu-id="1dd23-111">**新規** を選択し、特性を追加します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-111">Select **New** to add characteristics.</span></span>
3. <span data-ttu-id="1dd23-112">必要なフィールドに入力し、 **特性の種類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-112">Fill in the required fields and select the **Characteristic Type**.</span></span>

## <a name="assign-characteristics-to-resources"></a><span data-ttu-id="1dd23-113">リソースへの特性の割り当て</span><span class="sxs-lookup"><span data-stu-id="1dd23-113">Assign characteristics to resources</span></span>

1. <span data-ttu-id="1dd23-114">メイン メニューから、 **リソース** >  **予約可能リソース** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-114">From the main menu, select **Resources** > **Bookable Resources**.</span></span> <span data-ttu-id="1dd23-115">**アクティブな予約可能リソース** ページが開き、システムで使用可能なすべてのリソースの一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-115">The **Active Bookable Resources** page opens and you can view a list of all available resources in the system.</span></span>
2. <span data-ttu-id="1dd23-116">一覧から、予約可能リソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-116">From the list, select the name of a bookable resource.</span></span>
3. <span data-ttu-id="1dd23-117">**Project Service** セクションで、 **+予約可能なリソースの特性レコードの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-117">In the **Project Service** section, select **+Add Bookable Resource Characteristics record**.</span></span>
4. <span data-ttu-id="1dd23-118">開いたポップアップ ウィンドウで必要な特性を検索および選択して、リソースの **評価値** を追加できます。</span><span class="sxs-lookup"><span data-stu-id="1dd23-118">In the pop-up window that opens, find and select the required characteristics, and add a **Rating Value** for the resource.</span></span>
5. <span data-ttu-id="1dd23-119">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-119">Select **Save & Close**.</span></span>

## <a name="assign-characteristics-to-resource-requirements"></a><span data-ttu-id="1dd23-120">リソース要件への特性の割り当て</span><span class="sxs-lookup"><span data-stu-id="1dd23-120">Assign characteristics to resource requirements</span></span>

1. <span data-ttu-id="1dd23-121">チーム メンバー グリッドで、更新が必要な特性を持つ汎用チーム メンバーを検索し、ダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dd23-121">In the team member grid, find and double-click the generic team member with the characteristics that need to be updated.</span></span>
2. <span data-ttu-id="1dd23-122">**プロジェクト チーム メンバーの詳細** で、 **リソース要件** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-122">In the **Project Team member Detail** , select the **Resource Requirement** tab.</span></span>
3. <span data-ttu-id="1dd23-123">**スキル** サブグリッドで、 **+新しい要件特性コマンドを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-123">In the **Skills** subgrid, select **+Add new Requirement Characteristic.**</span></span>
4. <span data-ttu-id="1dd23-124">簡易作成ウィンドウで、必要な特性を検索して選択し、 **評価値** を追加します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-124">In the quick create pane, find and select the required characteristics and add a **Rating Value**.</span></span>
5. <span data-ttu-id="1dd23-125">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dd23-125">Select **Save & Close**.</span></span>