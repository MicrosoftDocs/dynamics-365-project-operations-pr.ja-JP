---
title: 仮予約の要件
description: このトピックでは、仮予約の要件について説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ba5e2e01c1280f5c5a1af284f1ca9c49c8b1fe27
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598862"
---
# <a name="soft-book-requirements"></a>仮予約の要件

[!include [banner](../includes/psa-now-project-operations.md)]

リソース要件は本予約できます。 本予約では、リソースの容量を使用する提案を作成できます。 提案が承認のために要求者に返されます。 仮予約でプロジェクト チームに一時的にリソースが追加され、スケジュール ボードに別の状態が示されますが、リソースの容量は消費されません。 スケジュール ボードの仮予約リソースに対して、**予約の状態** フィールドを **仮予約** に設定します。

![[仮予約] に設定された予約の状態。](media/Resource-Management-image77.png)

**チーム** タブが **名前付きチーム メンバー** ビューにある場合は、リソースは常にそこに表示されます。 仮予約された時間は **仮予約時間** 列に報告されます。

![[名前付きチーム メンバー] ビューの仮予約時間。](media/Resource-Management-image78.png)

仮予約済みのチーム メンバーはタスクに割り当てることができます。

![タスクに割り当てられた仮予約済みのチーム メンバー。](media/Resource-Management-image79.png)

**調整** タブについて、**調整** タブは本予約のみを対象とするため、仮予約リソースについては表示されません。

![[調整] タブの、仮予約済みで予約なしのリソース。](media/Resource-Management-image80.png)

> [!NOTE]
> 汎用チーム メンバーから生成される要件内のリソースは仮予約できません。

スケジュール ボードで、別のカラリングは、リソースの仮予約のために使用されます。

![スケジュール ボードで仮予約。](media/Resource-Management-image81.png)

仮予約を本予約に変換するには、スケジュール ボードで [仮予約] を右クリックし、**状態を変更する**\> **本予約**\>**本予約** を選択します。

![予約の状態を [本予約] に変更する。](media/Resource-Management-image82.png)

予約が変更され、状態はスケジュール ボードで変更されます。 現在の予約の状態が **本予約** である場合は、リソースが予約済みであることを示しています。また、容量と可用性が調整されます。

スケジュール ボードから本予約または仮予約を取り消す場合、同じ方法を使用できます。

プロジェクトの **チーム** タブで仮予約済みのリソースを本予約済みに変換するには、リソースを選び、**確認する** を選択します。

![コマンドを確認する。](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
