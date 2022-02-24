---
title: 経費管理のワークフロー
description: このトピックは、Microsoft Dynamics 365 Finance のワークフロー システムを使用して、経費管理で経費報告書のレビュープロセスを設定する方法について解説します。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271674"
---
# <a name="expense-management-workflow"></a>経費管理のワークフロー

このトピックは、経費管理で経費報告書のレビュープロセスを設定する方法について解説します。 次の基準を使用して、経費報告書の承認者を決定するワークフローを設定することができます :

- 従業員のレポート階層と事前定義された承認制限
- 暫定承認者と最終承認者をサポートする複数レベルの承認
- 財務的側面とプロジェクトの責任
- 特定のユーザー、またはユーザー グループへの割り当て

ワークフローの承認は、経費報告書、出張の要求、仮払金、付加価値税 (VAT) の精算に使用できます。

**例**

次のプロセスは、経費報告書の経費管理ワークフローの例です。

1. 従業員が経費報告書を作成して保存します。
2. 従業員の経費報告書を提出して承認を待機します。 承認者は、ワークフローの設定時に定義されたルールに基づいて識別されます。
3. 承認者は、経費報告書の承認準備が整った旨の通知を受け取ります。 承認者は経費報告書を確認し、次の条件が満たされていることを確認します :

    - 経費は経費方針に違反していないこと。 経費が本心に違反している場合、承認者は経費レポートに正当な業務上の理由が含まれていることを確認します。
    - 経費報告書には電子領収書が添付されています。

4. 承認者が経費報告書を承認します。
5. 経費報告書は、買掛金コーディネーターに割り当てられて転記されます。
6. 自動転記の構成に応じて、次のいずれかの手順が発生します :

    - 自動転記が設定されている場合、経費報告書支払い処理が行われ、経費報告書のステータスが更新されます。
    - 自動転記が構成されていない場合、買掛金コーディネーターは、すべての領収書の原本が提出されているかどうか、領収書が経費報告書の経費と一致しているかどうかを確認します。 経費報告書に入力されているすべての税コードが正しいことを確認する必要があります。

これらの要件を確認後、経費報告書が転記されます。

経費報告書が転記された後、経費報告書の支払いが承認され、従業員に精算されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]