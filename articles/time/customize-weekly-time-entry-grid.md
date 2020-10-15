---
title: 時間エントリを拡張する
description: このトピックでは、開発者が時間エントリ コントロールを拡張する方法について説明します。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930886"
---
# <a name="extending-time-entries"></a><span data-ttu-id="361f0-103">時間エントリを拡張する</span><span class="sxs-lookup"><span data-stu-id="361f0-103">Extending time entries</span></span>

<span data-ttu-id="361f0-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="361f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="361f0-105">Dynamics 365 Project Operations には、拡張可能な時間エントリ カスタム コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="361f0-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="361f0-106">このコントロールには次の機能が含まれます:</span><span class="sxs-lookup"><span data-stu-id="361f0-106">This control includes the following features:</span></span>

- <span data-ttu-id="361f0-107">1 週間にわたって水平方向に時間を入力する</span><span class="sxs-lookup"><span data-stu-id="361f0-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="361f0-108">日、行、または週ごとを合計する</span><span class="sxs-lookup"><span data-stu-id="361f0-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="361f0-109">行または週をコピーする</span><span class="sxs-lookup"><span data-stu-id="361f0-109">Copy rows or weeks</span></span>
- <span data-ttu-id="361f0-110">HH:mm または HH.hh を使用した時間エントリ (自動的に HH.hh に変換)</span><span class="sxs-lookup"><span data-stu-id="361f0-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="361f0-111">割り当て、予約、または予定からインポートする</span><span class="sxs-lookup"><span data-stu-id="361f0-111">Import from assignments, bookings or appointments</span></span>

<span data-ttu-id="361f0-112">時間エントリの拡張は、次の 2 つの領域で可能です:</span><span class="sxs-lookup"><span data-stu-id="361f0-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="361f0-113">個人で使用するカスタム時間エントリの追加</span><span class="sxs-lookup"><span data-stu-id="361f0-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="361f0-114">週単位の時間エントリ コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="361f0-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="361f0-115">個人で使用するカスタム時間エントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-115">Add custom time entries for your own use.</span></span>

<span data-ttu-id="361f0-116">時間エントリは、複数のシナリオで使用するように設計されたコア エンティティです。</span><span class="sxs-lookup"><span data-stu-id="361f0-116">Time entries are a core entity that is designed to be used for multiple scenarios.</span></span> <span data-ttu-id="361f0-117">2020 年 4 月のウェーブ 1 で、TESA コア ソリューションが導入され、**設定**エンティティおよび新しい**時間エントリ ユーザー** セキュリティ ロールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="361f0-117">In April Wave 1 2020, the TESA core solution was introduced, which provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="361f0-118">**msdyn_duration** と直接関係がある **msdyn_start** および **msdyn_end** の新しいフィールドも含まれていました。</span><span class="sxs-lookup"><span data-stu-id="361f0-118">The new fields, **msdyn_start** and **msdyn_end** which have a direct relation to **msdyn_duration**, were also included.</span></span> <span data-ttu-id="361f0-119">新しいエンティティ、セキュリティ ロールおよびフィールドにより、複数の製品にわたる時間へのより統一されたアプローチが可能になります。</span><span class="sxs-lookup"><span data-stu-id="361f0-119">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="361f0-120">時間ソース エンティティ</span><span class="sxs-lookup"><span data-stu-id="361f0-120">Time Source Entity</span></span>
| <span data-ttu-id="361f0-121">フィールド</span><span class="sxs-lookup"><span data-stu-id="361f0-121">Field</span></span> | <span data-ttu-id="361f0-122">内容</span><span class="sxs-lookup"><span data-stu-id="361f0-122">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="361f0-123">件名</span><span class="sxs-lookup"><span data-stu-id="361f0-123">Name</span></span>  | <span data-ttu-id="361f0-124">時間エントリの作成時に選択値として使用される時間ソース エントリの名前。</span><span class="sxs-lookup"><span data-stu-id="361f0-124">The name of the Time Source entry used as the selection value during time entry creation.</span></span> |
| <span data-ttu-id="361f0-125">既定の時間ソース [時間ソース: isdefault]</span><span class="sxs-lookup"><span data-stu-id="361f0-125">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="361f0-126">既定では、既定の時間ソースでマークできる時間ソースは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="361f0-126">By default, only one Time Source may be marked at the default time source.</span></span> <span data-ttu-id="361f0-127">この機能によりエントリは、指定されていない場合、既定で時間ソースになります。</span><span class="sxs-lookup"><span data-stu-id="361f0-127">This capability allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="361f0-128">時間ソースの種類 [時間ソース: sourcetype]</span><span class="sxs-lookup"><span data-stu-id="361f0-128">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="361f0-129">ソースの種類は、時間ソースをアプリに関連付けることを可能にするオプション (時間エントリ ソースの種類) です。</span><span class="sxs-lookup"><span data-stu-id="361f0-129">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="361f0-130">追加のアプリケーションが追加されると、このオプション セットにアプリケーション値が追加されます。</span><span class="sxs-lookup"><span data-stu-id="361f0-130">Additional values will be added to this option set as additional applications are added.</span></span> <span data-ttu-id="361f0-131">Microsoft では 190,000,000 を超える値を確保していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="361f0-131">Note that Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="361f0-132">時間エントリおよび時間ソース エンティティ</span><span class="sxs-lookup"><span data-stu-id="361f0-132">Time entries and the Time Source Entity</span></span>
<span data-ttu-id="361f0-133">各時間エントリは、時間ソース レコードに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="361f0-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="361f0-134">このレコードは、どのアプリケーションが時間エントリをどう処理するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="361f0-135">時間エントリは常に、開始、終了、および期間がリンクされた 1 つの継続的な時間ブロックです。</span><span class="sxs-lookup"><span data-stu-id="361f0-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="361f0-136">ロジックでは、次の状況で時間エントリ レコードを自動的に更新します:</span><span class="sxs-lookup"><span data-stu-id="361f0-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="361f0-137">次の 3 つのフィールドのうち 2 つが指定されている場合、3 番目は自動的に計算されます</span><span class="sxs-lookup"><span data-stu-id="361f0-137">If two of the three following fields are provided, the third is calculated automatically</span></span> 

    - <span data-ttu-id="361f0-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="361f0-138">**msdyn_start**</span></span>
    - <span data-ttu-id="361f0-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="361f0-139">**msdyn_end**</span></span>
    - <span data-ttu-id="361f0-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="361f0-140">**msdyn_duration**</span></span>

- <span data-ttu-id="361f0-141">**msdyn_start** および **msdyn_end** のフィールドはタイムゾーンに対応しています。</span><span class="sxs-lookup"><span data-stu-id="361f0-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="361f0-142">**msdyn_date** および **msdyn_duration** のみを指定して作成された時間エントリは深夜に開始され、それに応じて **msdyn_start** および **msdyn_end** が更新されます。</span><span class="sxs-lookup"><span data-stu-id="361f0-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight, and **msdyn_start** and **msdyn_end** will be updated accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="361f0-143">時間エントリの種類</span><span class="sxs-lookup"><span data-stu-id="361f0-143">Time entry types</span></span>

<span data-ttu-id="361f0-144">時間エントリ レコードには、関連アプリケーションの送信フローで動作を定義する関連付けられた種類があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-144">Time entry records have an associated type that defines behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="361f0-145">ラベル</span><span class="sxs-lookup"><span data-stu-id="361f0-145">Label</span></span> | <span data-ttu-id="361f0-146">値</span><span class="sxs-lookup"><span data-stu-id="361f0-146">Value</span></span>|
|-----|-----|
|<span data-ttu-id="361f0-147">休憩中</span><span class="sxs-lookup"><span data-stu-id="361f0-147">On break</span></span>   |<span data-ttu-id="361f0-148">192,355,000</span><span class="sxs-lookup"><span data-stu-id="361f0-148">192,355,000</span></span>|
|<span data-ttu-id="361f0-149">移動</span><span class="sxs-lookup"><span data-stu-id="361f0-149">Travel</span></span> | <span data-ttu-id="361f0-150">192,355,001</span><span class="sxs-lookup"><span data-stu-id="361f0-150">192,355,001</span></span>|
|<span data-ttu-id="361f0-151">残業</span><span class="sxs-lookup"><span data-stu-id="361f0-151">Overtime</span></span>   | <span data-ttu-id="361f0-152">192,354,320</span><span class="sxs-lookup"><span data-stu-id="361f0-152">192,354,320</span></span>|
|<span data-ttu-id="361f0-153">作業</span><span class="sxs-lookup"><span data-stu-id="361f0-153">Work</span></span>   | <span data-ttu-id="361f0-154">192,350,000</span><span class="sxs-lookup"><span data-stu-id="361f0-154">192,350,000</span></span>|
|<span data-ttu-id="361f0-155">不在</span><span class="sxs-lookup"><span data-stu-id="361f0-155">Absence</span></span>    | <span data-ttu-id="361f0-156">192,350,001</span><span class="sxs-lookup"><span data-stu-id="361f0-156">192,350,001</span></span>|
|<span data-ttu-id="361f0-157">休暇</span><span class="sxs-lookup"><span data-stu-id="361f0-157">Vacation</span></span>   | <span data-ttu-id="361f0-158">192,350,002</span><span class="sxs-lookup"><span data-stu-id="361f0-158">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="361f0-159">週単位の時間エントリ コントロールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="361f0-159">Customize the weekly Time Entry control</span></span>
<span data-ttu-id="361f0-160">開発者は、他のエンティティに追加のフィールドと検索を追加し、ビジネス シナリオをサポートするユーザー定義のビジネス ルールを実装できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-160">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="361f0-161">他のエンティティに検索付きのカスタム フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="361f0-161">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="361f0-162">毎週の時間エントリのグリッドにカスタム フィールドを追加する場合、3 つの重要な手順があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-162">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

- <span data-ttu-id="361f0-163">カスタム フィールドを簡易作成ダイアログ ボックスに追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-163">Add the custom field to the quick create dialog box.</span></span>
- <span data-ttu-id="361f0-164">グリッドを構成し、カスタム フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="361f0-164">Configure the grid to show the custom field.</span></span>
- <span data-ttu-id="361f0-165">カスタムフィールドを行編集タスク フローまたはセル編集タスク フローのいずれかに追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-165">Add the custom field to either the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="361f0-166">また、行またはセルの編集タスク フローでは、新しいフィールドの検証が必須であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-166">You must also make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="361f0-167">この手順の一部として、時間エントリ状態に基づいてフィールドをロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-167">As part of this step, you must lock the field based on the time entry status.</span></span>

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="361f0-168">カスタム フィールドを簡易作成ダイアログ ボックスに追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-168">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="361f0-169">**時間エントリ簡易作成**ダイアログ ボックスにカスタム フィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-169">You must add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="361f0-170">次に、ユーザーは**新規**を選択して時間エントリを追加するときに値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-170">Users can then enter a value when they add time entries by selecting **New**.</span></span>

#### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="361f0-171">グリッドを構成し、カスタム フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="361f0-171">Configure the grid to show the custom field</span></span>
<span data-ttu-id="361f0-172">週単位の時間エントリのグリッドにカスタム フィールドを追加する 2 つの手順があります:</span><span class="sxs-lookup"><span data-stu-id="361f0-172">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="361f0-173">ビューをカスタマイズし、カスタム フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="361f0-173">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="361f0-174">既定の新しいカスタム時間エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="361f0-174">Create a new default custom time entry</span></span> 


<span data-ttu-id="361f0-175">**ビューをカスタマイズし、カスタム フィールドを追加する**</span><span class="sxs-lookup"><span data-stu-id="361f0-175">**Customize a view and add a custom field**</span></span>

<span data-ttu-id="361f0-176">**週単位の自分の時間エントリ** ビューをカスタマイズして、そこにカスタム フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-176">You can customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="361f0-177">ビューでこれらのプロパティを編集することによって、グリッドのカスタム フィールドの場所とサイズを選択できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-177">You can choose the position and size of the custom field in the grid by editing those properties in the view.</span></span>

<span data-ttu-id="361f0-178">**既定の新しいカスタム時間エントリを作成する**</span><span class="sxs-lookup"><span data-stu-id="361f0-178">**Create a new default custom time entry**</span></span> 

<span data-ttu-id="361f0-179">このビューでは、グリッド内の目的の列に加えて、さらに**説明** および **外部コメント** フィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-179">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="361f0-180">ビューでこれらのプロパティを編集することによって、グリッドの場所、サイズ、既定の並べ替え順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="361f0-180">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="361f0-181">**時間エントリ グリッド** コントロールになるように、このビューのカスタム コントロールを構成します。</span><span class="sxs-lookup"><span data-stu-id="361f0-181">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="361f0-182">このコントロールをビューに追加して、Web、携帯電話、タブレットを選択します。</span><span class="sxs-lookup"><span data-stu-id="361f0-182">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="361f0-183">週単位の時間エントリ グリッドのパラメーターを構成します。</span><span class="sxs-lookup"><span data-stu-id="361f0-183">Configure the parameters for the weekly time entry grid.</span></span> <span data-ttu-id="361f0-184">**開始日** フィールドを **msdyn_date**に設定し、**期間** フィールドを **msdyn_duration**に設定し、**msdyn_entrystatus**に **状態** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-184">Set the **Start Date** field to **msdyn_date**, set the **Duration** field to **msdyn_duration**, and set the **Status** field to **msdyn_entrystatus**.</span></span> 
5. <span data-ttu-id="361f0-185">既定のビューで、**読み取り専用状態のリスト** フィールドを **192350002、192350003、192350004** に設定し、**行によるタスク フローの編集** フィールドを **msdyn_timeentryrowedit** に設定し、**セルによるタスク フローの編集** フィールドを **msdyn_timeentryedit** に設定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-185">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**, the **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**, and the **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
6. <span data-ttu-id="361f0-186">これらのフィールドをカスタマイズして、読み取り専用の状態を追加あるいは削除したり、行またはセルの編集用に別のタスク ベーのエクスペリエンス (TBX) を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="361f0-186">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="361f0-187">これらのフィールドは静的な値に対して限界があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-187">These fields should be bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="361f0-188">これら 2 つのオプションは両方とも、**プロジェクト**および**プロジェクト タスク** エンティテイの標準フィルターを削除して、エンティティのすべての検索ビューを表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="361f0-188">Both options will remove some out-of-box filtering on **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="361f0-189">標準ボックスで、関連する検索ビューのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="361f0-189">Out-of-the-box, only the relevant lookup views are visible.</span></span>
<span data-ttu-id="361f0-190">カスタム フィールド向けの適切なタスク フローを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-190">You must determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="361f0-191">ほとんどの場合、フィールドをグリッドに追加すると、行編集タスク フローに移動します。これは、時間エントリ行全体に適用するフィールドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="361f0-191">Most likely, if you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="361f0-192">カスタム フィールドでは、毎日、**終了時刻**のカスタム フィールドのように一意の値が生成され、一意の値は [セル編集タスク フロー] に移動します。</span><span class="sxs-lookup"><span data-stu-id="361f0-192">If the custom field has a unique value every day, such as a custom field for **End time**, it should go in the cell edit task flow.</span></span>

<span data-ttu-id="361f0-193">タスク フローにカスタム フィールドを追加するには、**フィールド**要素をページの適切な場所にドラッグしてから、フィールド プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-193">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="361f0-194">**ソース** プロパティを **時間エントリ**に設定して、カスタム フィールドに **データ フィールド** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-194">Set the **Source** property to **Time Entry**, and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="361f0-195">**フィールド** プロパティでは、TBX ページに表示名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-195">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="361f0-196">**適用**を選択してフィールドへの変更を保存してから、**更新**を選択してページへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="361f0-196">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="361f0-197">新しいユーザー定義の TBX ページを使用するには、新しいプロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="361f0-197">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="361f0-198">カテゴリを **ビジネス プロセス フロー**に設定し、エンティティを **時間エントリ**に設定し、ビジネス プロセスの種類を **タスク フローとしてプロセスを実行する** に設定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-198">Set the category to **Business Process Flow**, set the entity to **Time Entry**, and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="361f0-199">**プロパティ**で、**ページ名** プロパティは、そのページの表示名に設定されています。</span><span class="sxs-lookup"><span data-stu-id="361f0-199">Under **Properties**, the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="361f0-200">TBX のページに、すべての関連フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-200">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="361f0-201">プロセスを保存してアクティブ化し、関連タスク フローのカスタム コントロール プロパティを、プロセスの **名前** の値に更新します。</span><span class="sxs-lookup"><span data-stu-id="361f0-201">Save and activate the process, and then update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="361f0-202">新しいオプション セット値を追加する</span><span class="sxs-lookup"><span data-stu-id="361f0-202">Add new option set values</span></span>
<span data-ttu-id="361f0-203">オプション セットの値を標準フィールドに追加するには、[フィールドの編集] ページを開き、**種類**で、オプション セットの横にある **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="361f0-203">To add option set values to an out-of-box field, open the editing page for the field, and then, under **Type**, select **Edit** next to the option set.</span></span> <span data-ttu-id="361f0-204">次に、ユーザー定義のラベルと色を持つ新しいオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-204">Next, add a new option that has a custom label and color.</span></span> <span data-ttu-id="361f0-205">新しい時間エントリ状態を追加する場合は、標準フィールドは、**エントリ状態**であり、**状態**ではありません。</span><span class="sxs-lookup"><span data-stu-id="361f0-205">If you want to add a new time entry status, the out-of-box field is named **Entry Status**, not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="361f0-206">読み取り専用として、新しい時間エントリ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="361f0-206">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="361f0-207">読み取り専用として新しい時間エントリ条件を指定するには、**読み取り専用状態のリスト** プロパティに新しい時間エントリ値を追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-207">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="361f0-208">時間エントリ グリッドの編集可能な部分は、新規の状態になっている行にロックされます。</span><span class="sxs-lookup"><span data-stu-id="361f0-208">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="361f0-209">次に、**時間エントリ行を編集する** および **時間エントリ編集** の TBX のページで、すべてのフィールドをロックするビジネス ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="361f0-209">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="361f0-210">ページのビジネス プロセス フロー エディターを開いて **ビジネス ルール** を選択すると、これらのページに関するビジネス ルールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="361f0-210">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="361f0-211">既存のビジネス ルールの状況で新しい状態を追加できます。または、新規の状態用に新しいビジネス ルールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-211">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="361f0-212">カスタム検証ルールを追加する</span><span class="sxs-lookup"><span data-stu-id="361f0-212">Add custom validation rules</span></span>
<span data-ttu-id="361f0-213">週単位の時間エントリ グリッド エクスペリエンスに追加できる検証ルールには、次の 2 種類があります:</span><span class="sxs-lookup"><span data-stu-id="361f0-213">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="361f0-214">簡易作成ダイアログ ボックスおよび TBX ページで機能するクライアント側のビジネス ルール。</span><span class="sxs-lookup"><span data-stu-id="361f0-214">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="361f0-215">すべての時間エントリの更新に適用されるサーバー側のプラグイン検証。</span><span class="sxs-lookup"><span data-stu-id="361f0-215">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="361f0-216">ビジネス ルール</span><span class="sxs-lookup"><span data-stu-id="361f0-216">Business rules</span></span>
<span data-ttu-id="361f0-217">ビジネス ルールを使用して、フィールドのロックおよびロック解除を行い、既定値をフィールドに入力し、現在の時間エントリ レコードからの情報のみを必要とする検証を定義します。</span><span class="sxs-lookup"><span data-stu-id="361f0-217">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="361f0-218">TBX ページのビジネス ルールにアクセスするには、ページのビジネス プロセス フロー エディターを開き、 **ビジネス ルール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="361f0-218">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="361f0-219">これで、既存のビジネス ルールの編集または新しいビジネス ルールの追加ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="361f0-219">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="361f0-220">さらにカスタマイズされた検証では、JavaScript を実行するビジネス ルールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="361f0-220">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="361f0-221">プラグインの検証</span><span class="sxs-lookup"><span data-stu-id="361f0-221">Plug-in validations</span></span>
<span data-ttu-id="361f0-222">単一の時間エントリ レコードで使用する場合よりも多くのコンテキストを必要とする検証の場合、またはグリッド内のインライン更新で実行する検証の場合は、プラグイン検証を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="361f0-222">You should use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="361f0-223">検証を完了するには、**時間エントリ** のエンティティに対してカスタム プラグインを作成します。</span><span class="sxs-lookup"><span data-stu-id="361f0-223">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>
