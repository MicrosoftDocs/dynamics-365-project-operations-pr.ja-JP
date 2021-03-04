---
title: 経費精算書における複数の承認者
description: このトピックでは、複数の人物による承認を行う経費報告書について説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960613"
---
# <a name="multiple-approvers-on-an-expense-report"></a>経費精算書における複数の承認者

組織の経費承認ポリシーによっては、送信された経費報告書に対して複数の人物による承認が必要となる場合があります。 経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。 たとえば、すべての経費報告書に対して、まず報告書を提出した従業員のマネージャーが承認し、次に買掛金コーディネーターが承認するように要求することができます。

複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:

- 1 つの承認段階を持つ、 1 つの承認要素を追加します。 たとえば、このステップでは、経費報告書をユーザー グループに割り当て、ユーザー グループのメンバーの 50％ の承認を必要とする場合があります。
- 複数の承認段階を持つ 1 つの承認要素を追加します。 たとえば、承認要素には次のステップがあります :

    1. 経費報告書を提出した従業員の上司が承認する。
    2. 買掛金担当者が領収書と経費精算書を確認する。
    3. 予算所有者が経費報告書を承認する。

- それぞれが 1 つの承認段階を持つ複数の承認要素を追加します。 たとえば、次の手順ごとに個別の承認要素を追加することができます :

    1. 従業員の上司が経費報告書を承認する。
    2. 予算所有者が経費報告書を承認する。
