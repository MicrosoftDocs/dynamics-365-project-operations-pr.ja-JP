---
title: 時間エントリを拡張する
description: このトピックでは、開発者が時間エントリ コントロールを拡張する方法について説明します。
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 190ad9e1f9ced690aee953ed992bf7aa2844c3b3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079167"
---
# <a name="extending-time-entries"></a><span data-ttu-id="b1ee6-103">時間エントリを拡張する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-103">Extending time entries</span></span>

<span data-ttu-id="b1ee6-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="b1ee6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b1ee6-105">Dynamics 365 Project Operations には、拡張可能な時間エントリ カスタム コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="b1ee6-106">このコントロールには次の機能が含まれます:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-106">This control includes the following features:</span></span>

- <span data-ttu-id="b1ee6-107">1 週間にわたって水平方向に時間を入力する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="b1ee6-108">日、行、または週ごとを合計する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="b1ee6-109">行または週をコピーする</span><span class="sxs-lookup"><span data-stu-id="b1ee6-109">Copy rows or weeks</span></span>
- <span data-ttu-id="b1ee6-110">HH:mm または HH.hh を使用した時間エントリ (自動的に HH.hh に変換)</span><span class="sxs-lookup"><span data-stu-id="b1ee6-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="b1ee6-111">割り当て、予約、または予定からインポートする</span><span class="sxs-lookup"><span data-stu-id="b1ee6-111">Import from assignments, bookings, or appointments</span></span>

<span data-ttu-id="b1ee6-112">時間エントリの拡張は、次の 2 つの領域で可能です:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="b1ee6-113">個人で使用するカスタム時間エントリの追加</span><span class="sxs-lookup"><span data-stu-id="b1ee6-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="b1ee6-114">週単位の時間エントリ コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="b1ee6-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="b1ee6-115">個人で使用するカスタマイズされた時間エントリを追加します</span><span class="sxs-lookup"><span data-stu-id="b1ee6-115">Add custom time entries for your own use</span></span>

<span data-ttu-id="b1ee6-116">時間エントリは、複数のシナリオで使用されるコア エンティティです。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-116">Time entries are a core entity used in multiple scenarios.</span></span> <span data-ttu-id="b1ee6-117">2020 年 4 月の リリース サイクル 1 では、TESA コア ソリューションが導入されました。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-117">In April Wave 1 2020, the TESA core solution was introduced.</span></span> <span data-ttu-id="b1ee6-118">TESA では **設定** エンティティ、と新しい **時間入力ユーザー** セキュリティ ロールを提供しています。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-118">TESA provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="b1ee6-119">また、 **msdyn_duration** と直接関係のある **msdyn_start** と **msdyn_end** という新しいフィールドも追加されました。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-119">The new fields, **msdyn_start** and **msdyn_end** , which have a direct relation to **msdyn_duration** , were also included.</span></span> <span data-ttu-id="b1ee6-120">新しいエンティティ、セキュリティ ロールおよびフィールドにより、複数の製品にわたる時間へのより統一されたアプローチが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-120">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="b1ee6-121">時間ソース エンティティ</span><span class="sxs-lookup"><span data-stu-id="b1ee6-121">Time source entity</span></span>
| <span data-ttu-id="b1ee6-122">フィールド</span><span class="sxs-lookup"><span data-stu-id="b1ee6-122">Field</span></span> | <span data-ttu-id="b1ee6-123">内容</span><span class="sxs-lookup"><span data-stu-id="b1ee6-123">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="b1ee6-124">件名</span><span class="sxs-lookup"><span data-stu-id="b1ee6-124">Name</span></span>  | <span data-ttu-id="b1ee6-125">時間エントリを作成する際に選択値として使用する時間ソース エントリの名前です。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-125">The name of the Time source entry used as the selection value when creating time entries.</span></span> |
| <span data-ttu-id="b1ee6-126">既定の時間ソース [時間ソース: isdefault]</span><span class="sxs-lookup"><span data-stu-id="b1ee6-126">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="b1ee6-127">既定では、時間ソースは 1 つしかマークできません。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-127">By default, only one Time Source can be marked at the default.</span></span> <span data-ttu-id="b1ee6-128">これは、時間ソースが指定されていない場合に、エントリを既定の時間ソースにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-128">This allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="b1ee6-129">時間ソースの種類 [時間ソース: sourcetype]</span><span class="sxs-lookup"><span data-stu-id="b1ee6-129">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="b1ee6-130">ソースの種類は、時間ソースをアプリに関連付けることを可能にするオプション (時間エントリ ソースの種類) です。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-130">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="b1ee6-131">Microsoft では 190,000,000 超の値を確保していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-131">Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="b1ee6-132">時間エントリと時間ソース エンティティ</span><span class="sxs-lookup"><span data-stu-id="b1ee6-132">Time entries and the Time source entity</span></span>
<span data-ttu-id="b1ee6-133">各時間エントリは、時間ソース レコードに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="b1ee6-134">このレコードは、どのアプリケーションが時間エントリをどう処理するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="b1ee6-135">時間エントリは常に、開始、終了、および期間がリンクされた 1 つの継続的な時間ブロックです。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="b1ee6-136">ロジックでは、次の状況で時間エントリ レコードを自動的に更新します:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="b1ee6-137">次の 3 つのフィールドのうち 2 つが指定されている場合、3 番目のフィールドは自動的に計算されます:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-137">If two of the three following fields are provided, the third is calculated automatically:</span></span> 

    - <span data-ttu-id="b1ee6-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="b1ee6-138">**msdyn_start**</span></span>
    - <span data-ttu-id="b1ee6-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="b1ee6-139">**msdyn_end**</span></span>
    - <span data-ttu-id="b1ee6-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="b1ee6-140">**msdyn_duration**</span></span>

- <span data-ttu-id="b1ee6-141">**msdyn_start** および **msdyn_end** のフィールドはタイムゾーンに対応しています。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="b1ee6-142">**msdyn_date** と **msdyn_duration** のみを指定して作成された時間項目は、深夜から開始されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight.</span></span> <span data-ttu-id="b1ee6-143">**msdyn_start** と **msdyn_end** のフィールドはタイムゾーンに応じて更新されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-143">The **msdyn_start** and **msdyn_end** fields will update accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="b1ee6-144">時間エントリの種類</span><span class="sxs-lookup"><span data-stu-id="b1ee6-144">Time entry types</span></span>

<span data-ttu-id="b1ee6-145">時間エントリ レコードには、関連するアプリケーションの送信フローでの動作を定義する関連するタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-145">Time entry records have an associated type that defines the behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="b1ee6-146">ラベル</span><span class="sxs-lookup"><span data-stu-id="b1ee6-146">Label</span></span> | <span data-ttu-id="b1ee6-147">値</span><span class="sxs-lookup"><span data-stu-id="b1ee6-147">Value</span></span>|
|-----|-----|
|<span data-ttu-id="b1ee6-148">休憩中</span><span class="sxs-lookup"><span data-stu-id="b1ee6-148">On break</span></span>   |<span data-ttu-id="b1ee6-149">192,355,000</span><span class="sxs-lookup"><span data-stu-id="b1ee6-149">192,355,000</span></span>|
|<span data-ttu-id="b1ee6-150">移動</span><span class="sxs-lookup"><span data-stu-id="b1ee6-150">Travel</span></span> | <span data-ttu-id="b1ee6-151">192,355,001</span><span class="sxs-lookup"><span data-stu-id="b1ee6-151">192,355,001</span></span>|
|<span data-ttu-id="b1ee6-152">残業</span><span class="sxs-lookup"><span data-stu-id="b1ee6-152">Overtime</span></span>   | <span data-ttu-id="b1ee6-153">192,354,320</span><span class="sxs-lookup"><span data-stu-id="b1ee6-153">192,354,320</span></span>|
|<span data-ttu-id="b1ee6-154">作業</span><span class="sxs-lookup"><span data-stu-id="b1ee6-154">Work</span></span>   | <span data-ttu-id="b1ee6-155">192,350,000</span><span class="sxs-lookup"><span data-stu-id="b1ee6-155">192,350,000</span></span>|
|<span data-ttu-id="b1ee6-156">不在</span><span class="sxs-lookup"><span data-stu-id="b1ee6-156">Absence</span></span>    | <span data-ttu-id="b1ee6-157">192,350,001</span><span class="sxs-lookup"><span data-stu-id="b1ee6-157">192,350,001</span></span>|
|<span data-ttu-id="b1ee6-158">休暇</span><span class="sxs-lookup"><span data-stu-id="b1ee6-158">Vacation</span></span>   | <span data-ttu-id="b1ee6-159">192,350,002</span><span class="sxs-lookup"><span data-stu-id="b1ee6-159">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="b1ee6-160">週単位の時間エントリ コントロールをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="b1ee6-160">Customize the weekly Time entry control</span></span>
<span data-ttu-id="b1ee6-161">開発者は、他のエンティティに追加のフィールドと検索を追加し、ビジネス シナリオをサポートするユーザー定義のビジネス ルールを実装できます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-161">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="b1ee6-162">他のエンティティに検索付きのカスタム フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-162">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="b1ee6-163">毎週の時間エントリのグリッドにカスタム フィールドを追加する場合、3 つの重要な手順があります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-163">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

1. <span data-ttu-id="b1ee6-164">カスタム フィールドを簡易作成ダイアログ ボックスに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-164">Add the custom field to the quick create dialog box.</span></span>
2. <span data-ttu-id="b1ee6-165">グリッドを構成し、カスタム フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-165">Configure the grid to show the custom field.</span></span>
3. <span data-ttu-id="b1ee6-166">行編集タスク フローまたはセル編集タスク フローにカスタムフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-166">Add the custom field to the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="b1ee6-167">新しいフィールドが、行やセル編集タスク フローで必要な検証がされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-167">Make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="b1ee6-168">この手順の一部として、時間の入力状態に基づいてフィールドをロックします。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-168">As part of this step, lock the field based on the time entry status.</span></span>

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="b1ee6-169">カスタム フィールドを簡易作成ダイアログ ボックスに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-169">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="b1ee6-170">**時間エントリの簡易作成** ダイアログ ボックスにカスタム フィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-170">Add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="b1ee6-171">時間エントリが追加されたときに、 **新規** を選択することで、値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-171">Then, when time entries are added, a value can be entered by selecting **New**.</span></span>

### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="b1ee6-172">グリッドを構成し、カスタム フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-172">Configure the grid to show the custom field</span></span>
<span data-ttu-id="b1ee6-173">週単位の時間エントリのグリッドにカスタム フィールドを追加する 2 つの手順があります:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-173">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="b1ee6-174">ビューをカスタマイズし、カスタム フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-174">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="b1ee6-175">既定の新しいカスタム時間エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-175">Create a new default custom time entry</span></span> 


#### <a name="customize-a-view-and-add-a-custom-field"></a><span data-ttu-id="b1ee6-176">ビューをカスタマイズし、カスタム フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-176">Customize a view and add a custom field</span></span>

<span data-ttu-id="b1ee6-177">**週単位の自分の時間エントリ** ビューをカスタマイズし、カスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-177">Customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="b1ee6-178">ビューのプロパティを編集することで、グリッド内のカスタム フィールドの位置とサイズを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-178">You can choose the position and size of the custom field in the grid by editing the properties in the view.</span></span>

#### <a name="create-a-new-default-custom-time-entry"></a><span data-ttu-id="b1ee6-179">既定の新しいカスタム時間エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-179">Create a new default custom time entry</span></span>

<span data-ttu-id="b1ee6-180">このビューでは、グリッド内の目的の列に加えて、さらに **説明** および **外部コメント** フィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-180">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="b1ee6-181">ビューでこれらのプロパティを編集することによって、グリッドの場所、サイズ、既定の並べ替え順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-181">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="b1ee6-182">**時間エントリ グリッド** コントロールになるように、このビューのカスタム コントロールを構成します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-182">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="b1ee6-183">このコントロールをビューに追加して、Web、携帯電話、タブレットを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-183">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="b1ee6-184">週単位の時間エントリ グリッドのパラメーターを構成します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-184">Configure the parameters for the weekly time entry grid.</span></span> 
5. <span data-ttu-id="b1ee6-185">**開始日** フィールドを **msdyn_date** に設定し、 **期間** フィールドを **msdyn_duration** に設定し、 **msdyn_entrystatus** に **状態** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-185">Set the **Start Date** field to **msdyn_date** , set the **Duration** field to **msdyn_duration** , and set the **Status** field to **msdyn_entrystatus**.</span></span> 
6. <span data-ttu-id="b1ee6-186">既定のビューの場合、 **読み取り専用の状態リスト** フィールドは **192350002,192350003,192350004** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-186">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**.</span></span> <span data-ttu-id="b1ee6-187">**行編集タスク フロー** フィールドは **msdyn_timeentryrowedit** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-187">The **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**.</span></span> <span data-ttu-id="b1ee6-188">**セル編集タスク フロー** フィールドは **msdyn_timeentryedit** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-188">The **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
7. <span data-ttu-id="b1ee6-189">これらのフィールドをカスタマイズして、読み取り専用の状態を追加あるいは削除したり、行またはセルの編集用に別のタスク ベーのエクスペリエンス (TBX) を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-189">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="b1ee6-190">これらのフィールドは静的な値にバインドされます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-190">These fields are now bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="b1ee6-191">どちらのオプションも、 **プロジェクト** と **プロジェクト タスク** のエンティティのフィルタリングを削除して、エンティティのすべてのルックアップビューが表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-191">Both options will remove some out-of-box filtering on the **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="b1ee6-192">標準ボックスで、関連する検索ビューのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-192">Out-of-the-box, only the relevant lookup views are visible.</span></span>

<span data-ttu-id="b1ee6-193">カスタム フィールドで使用する適切なタスクフローを決定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-193">Determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="b1ee6-194">グリッドにフィールドを追加した場合、そのフィールドは、時間エントリの行全体に適用されるフィールドに使用される行編集タスクフローに入ります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-194">If you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="b1ee6-195">カスタム フィールドでは、毎日、 **終了時刻** のカスタム フィールドのように一意の値が生成され、一意の値は [セル編集タスク フロー] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-195">If the custom field has a unique value every day, such as a custom field for **End time** , it should go in the cell edit task flow.</span></span>

<span data-ttu-id="b1ee6-196">タスク フローにカスタム フィールドを追加するには、 **フィールド** 要素をページの適切な場所にドラッグしてから、フィールド プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-196">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="b1ee6-197">**ソース** プロパティを **時間エントリ** に設定して、カスタム フィールドに **データ フィールド** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-197">Set the **Source** property to **Time Entry** , and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="b1ee6-198">**フィールド** プロパティでは、TBX ページに表示名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-198">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="b1ee6-199">**適用** を選択してフィールドへの変更を保存してから、 **更新** を選択してページへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-199">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="b1ee6-200">新しいユーザー定義の TBX ページを使用するには、新しいプロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-200">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="b1ee6-201">カテゴリを **ビジネス プロセス フロー** に設定し、エンティティを **時間エントリ** に設定し、ビジネス プロセスの種類を **タスク フローとしてプロセスを実行する** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-201">Set the category to **Business Process Flow** , set the entity to **Time Entry** , and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="b1ee6-202">**プロパティ** で、 **ページ名** プロパティは、そのページの表示名に設定されています。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-202">Under **Properties** , the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="b1ee6-203">TBX のページに、すべての関連フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-203">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="b1ee6-204">保存してプロセスをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-204">Save and activate the process.</span></span> <span data-ttu-id="b1ee6-205">関連するタスクフローのカスタム コントロール プロパティをプロセス上の **名前** の値に更新します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-205">Update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="b1ee6-206">新しいオプション セット値を追加する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-206">Add new option set values</span></span>
<span data-ttu-id="b1ee6-207">オプション セットの値を既成のフィールドに追加するには、フィールドの編集ページを開き、、 **種類** の下のオプショ ンセットの横にある **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-207">To add option set values to an out-of-the-box field, open the editing page for the field, and under **Type** , select **Edit** next to the option set.</span></span> <span data-ttu-id="b1ee6-208">カスタム ラベルとカラーを持つ新しいオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-208">Add a new option that has a custom label and color.</span></span> <span data-ttu-id="b1ee6-209">新しい時間エントリの状態を追加する場合、既成のフィールドは、 **状態** ではなく、 **入力の状態** という名前になります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-209">If you want to add a new time entry status, the out-of-the-box field is named **Entry Status** , not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="b1ee6-210">読み取り専用として、新しい時間エントリ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-210">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="b1ee6-211">読み取り専用として新しい時間エントリ条件を指定するには、 **読み取り専用状態のリスト** プロパティに新しい時間エントリ値を追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-211">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="b1ee6-212">時間エントリ グリッドの編集可能な部分は、新規の状態になっている行にロックされます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-212">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="b1ee6-213">次に、 **時間エントリ行を編集する** および **時間エントリ編集** の TBX のページで、すべてのフィールドをロックするビジネス ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-213">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="b1ee6-214">ページのビジネス プロセス フロー エディターを開いて **ビジネス ルール** を選択すると、これらのページに関するビジネス ルールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-214">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="b1ee6-215">既存のビジネス ルールの状況で新しい状態を追加できます。または、新規の状態用に新しいビジネス ルールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-215">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="b1ee6-216">カスタム検証ルールを追加する</span><span class="sxs-lookup"><span data-stu-id="b1ee6-216">Add custom validation rules</span></span>
<span data-ttu-id="b1ee6-217">週単位の時間エントリ グリッド エクスペリエンスに追加できる検証ルールには、次の 2 種類があります:</span><span class="sxs-lookup"><span data-stu-id="b1ee6-217">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="b1ee6-218">簡易作成ダイアログ ボックスおよび TBX ページで機能するクライアント側のビジネス ルール。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-218">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="b1ee6-219">すべての時間エントリの更新に適用されるサーバー側のプラグイン検証。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-219">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="b1ee6-220">ビジネス ルール</span><span class="sxs-lookup"><span data-stu-id="b1ee6-220">Business rules</span></span>
<span data-ttu-id="b1ee6-221">ビジネス ルールを使用して、フィールドのロックおよびロック解除を行い、既定値をフィールドに入力し、現在の時間エントリ レコードからの情報のみを必要とする検証を定義します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-221">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="b1ee6-222">TBX ページのビジネス ルールにアクセスするには、ページのビジネス プロセス フロー エディターを開き、 **ビジネス ルール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-222">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="b1ee6-223">これで、既存のビジネス ルールの編集または新しいビジネス ルールの追加ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-223">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="b1ee6-224">さらにカスタマイズされた検証では、JavaScript を実行するビジネス ルールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-224">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="b1ee6-225">プラグインの検証</span><span class="sxs-lookup"><span data-stu-id="b1ee6-225">Plug-in validations</span></span>
<span data-ttu-id="b1ee6-226">ひとつの時間エントリ レコードで利用可能なコンテクストよりも多くのコンテクストを必要とする検証や、グリッドのインライン更新で実行する検証には、プラグイン検証を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-226">Use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="b1ee6-227">検証を完了するには、 **時間エントリ** のエンティティに対してカスタム プラグインを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-227">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>

### <a name="copying-time-entries"></a><span data-ttu-id="b1ee6-228">時間エントリのコピー</span><span class="sxs-lookup"><span data-stu-id="b1ee6-228">Copying time entries</span></span>
<span data-ttu-id="b1ee6-229">時間入力中にコピーするフィールドのリストを定義するには、 **時間エントリ列のコピー** ビューを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-229">Use the view **Copy Time Entry Columns** to define the list of fields to copy during time entry.</span></span> <span data-ttu-id="b1ee6-230">**日付** と **期間** は必須フィールドのため、ビューから削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="b1ee6-230">**Date** and **Duration** are required fields and shouldn't be removed from the view.</span></span>
