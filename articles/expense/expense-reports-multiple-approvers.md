---
title: 経費精算書と複数の承認者
description: この記事では、2 人以上の承認を必要とする経費精算書に関する情報を提供します。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f42535e4826d1f618bd542eec3b26a6fde1a97
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914464"
---
# <a name="expense-reports-and-multiple-approvers"></a>経費精算書と複数の承認者

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

組織の経費承認ポリシーによっては、送信された経費レポートを複数の人物による承認が必要となる場合があります。 経費精算書の承認ワークフロー プロセスを設定するときに、1 人以上の経費精算書承認者用のタスクまたはステップを含むワークフロー要素を追加できます。 たとえば、すべての経費精算書について、精算書を提出した従業員の上司と買掛金勘定コーディネーターの 2 人にそれぞれ承認を要求する場合などです。

経費精算書に複数の承認者を設定する場合は、次の方法でワークフロー要素を追加できます。

- 1 つのステップを持つ承認要素を 1 つ追加する。 たとえば、このステップでは、経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50% がこれを承認する必要があると設定することができます。
- 複数のステップを含む承認要素を 1 つ追加する。 たとえば、承認要素には次のステップが含まれる場合があります。

    1. 経費精算書を提出した従業員の上司が精算書を承認する。
    2. 買掛金勘定の事務員が領収書と経費精算書の品目を確認する。
    3. 予算の所有者が経費精算書を承認する。

- それぞれ 1 つのステップを含む複数の承認要素を追加する。 たとえば、次の各ステップに個別の承認要素を追加できます。

    1. 従業員の上司が経費報告書を承認する。
    2. 予算所有者が経費報告書を承認する。


[!INCLUDE[footer-include](../includes/footer-banner.md)]