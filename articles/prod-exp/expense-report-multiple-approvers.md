---
title: 経費精算書における複数の承認者
description: この記事では、複数の承認が必要な経費報告書に関する情報を提供します。
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae72ae578455a626c069c01552b3edf60df706a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933958"
---
# <a name="multiple-approvers-on-an-expense-report"></a>経費精算書における複数の承認者

組織の経費承認ポリシーによっては、送信された経費報告書に対して複数の人物による承認が必要となる場合があります。 経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。 たとえば、すべての経費報告書に対して、まず報告書を提出した従業員のマネージャーが承認し、次に買掛金コーディネーターが承認するように要求することができます。

複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:

- 1 つのステップを持つ承認要素を 1 つ追加する。 たとえば、このステップでは、経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50% がこれを承認する必要があると設定することができます。
- 複数のステップを含む承認要素を 1 つ追加する。 たとえば、承認要素には次のステップが含まれる場合があります。

    1. 経費精算書を提出した従業員の上司が精算書を承認する。
    2. 買掛金勘定の事務員が領収書と経費精算書の品目を確認する。
    3. 予算の所有者が経費精算書を承認する。

- それぞれ 1 つのステップを含む複数の承認要素を追加する。 たとえば、次の各ステップに個別の承認要素を追加できます。

    1. 従業員の上司が経費報告書を承認する。
    2. 予算所有者が経費報告書を承認する。


[!INCLUDE[footer-include](../includes/footer-banner.md)]