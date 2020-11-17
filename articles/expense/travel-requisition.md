---
title: 出張申請書
description: このトピックでは、出張申請書について説明します。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079137"
---
# <a name="travel-requisitions"></a>出張申請書

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

出張申請書には、出張目的のために発生する費用が一覧表示されています。 出張申請書はレビューのために送信され、経費の承認に使用することができます。

組織に請求される経費が発生する前に、出張申請書を提出する必要がある場合があります。 この要件は、会社のクレジット カードに経費が請求されるか、現金前払いから受け取った現金を使うか、または組織によって払い戻される自己負担の経費が発生するかに関係なく適用されます。

出張申請書とポリシーは、組織の経費管理に役立ちます。 たとえば、組織が出張を必要とする固定価格プロジェクトの作業を行っている場合、プロジェクト チーム メンバーの出張費はプロジェクトの予算内に収まる必要があります。 出張費が発生する前に承認を要求することにより、組織はプロジェクトが予算内に収まるようにすることができます。

## <a name="configuration"></a>構成 

経費管理パラメーターで「出張の事前承認が必須である」パラメーターを有効にすることにより、出張申請書を「必須」として設定することができます。 

## <a name="create-and-submit-a-travel-requisition"></a>出張申請書の作成および送信

1. **自分の経費: 出張申請書** に移動し、 **新しい出張申請書** を選択します。
2. 申請書に目的と出張先を入力します。
3. **出張の説明** フィールドに、追加情報を入力します。 
4. フライト、食事、レンタカーなどの各予定経費について、経費明細行品目を作成します。 各経費について、予定日、見積もり金額、および通貨を含めます。 
5. 予想される経費の追加が完了したら、 **保存** を選択します。
6. 出張申請書を送信する準備ができたら、 **ワークフロー** > **送信** を選択します。

**自分の経費: 出張申請書** の下で承認された出張申請書を確認できます。 

## <a name="view-available-travel-requisitions"></a>利用可能な出張申請書の表示

**自分の経費: 出張申請書** の下ですべての出張申請書を確認できます。

## <a name="approve-travel-requisitions"></a>承認された出張申請書

承認する出張申請書を選択し、 **ワークフロー** > **承認** を選択します。  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>承認された出張申請書を使用して経費報告書を送信する

1. 新しい経費報告書を作成し、経費報告書ヘッダーで、承認された出張申請書の一覧から **出張申請書へのマップ** を選択します。
2. 経費報告書ヘッダーの **出張申請書金額** フィールドは自動的に更新されます。
3. 出張で発生した各経費を追加します。 **事前承認済み** フィールドが有効になっていると、特定の経費カテゴリの調整された金額と承認された金額が更新されます。

> [!NOTE]
> 経費報告書を承認された出張申請書にマップする場合、取引金額は承認された金額を超えることはできません。 