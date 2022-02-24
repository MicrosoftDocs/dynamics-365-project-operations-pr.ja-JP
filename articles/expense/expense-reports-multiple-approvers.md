---
title: 経費精算書と複数の承認者
description: このトピックでは、複数の人物による承認を必要とする経費報告書について説明します。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120999"
---
# <a name="expense-reports-and-multiple-approvers"></a>経費精算書と複数の承認者

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

組織の経費承認ポリシーによっては、送信された経費レポートを複数の人物による承認が必要となる場合があります。 経費報告書承認のワークフロー プロセスを設定する場合、1 つ以上の経費報告書承認者のタスク、またはステップを含むワークフロー要素を追加できます。 たとえば、すべての経費報告書に対して、報告書を提出した従業員の上司と買掛金コーディネーターの 2 人の別々の人物による承認が必要となる要件を設定するとします。

複数の経費報告書承認者を必要とする場合は、以下のいずれかの方法でワークフロー要素を追加できます:

- 1 つの承認段階を持つ、 1 つの承認要素を追加します。 たとえば、このステップでは、経費報告書をユーザー グループに割り当て、ユーザー グループのメンバーの 50％ の承認を必要とする場合があります。
- 複数の承認段階を持つ 1 つの承認要素を追加します。 たとえば、承認要素には次のステップがあります :

    1. 経費報告書を提出した従業員の上司が承認する。
    2. 買掛金担当者が領収書と経費精算書を確認する。
    3. 予算所有者が経費報告書を承認する。

- それぞれが 1 つの承認段階を持つ複数の承認要素を追加します。 たとえば、次の手順ごとに個別の承認要素を追加することができます :

    1. 従業員の上司が経費報告書を承認する。
    2. 予算所有者が経費報告書を承認する。
