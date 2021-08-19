---
title: 経費精算書と複数の承認者
description: このトピックでは、複数の人物による承認を必要とする経費報告書について説明します。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2acae2d518a02539f01d5498450236999fe609d1e8f26b5f90e18b986b83cab1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988432"
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