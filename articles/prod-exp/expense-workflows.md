---
title: 経費管理のワークフローを設定する
description: ワークフロー プロセスを設定して出張ドキュメントや経費ドキュメントをレビューすることができます。
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97db155a1d8ce77f711ea37bbd537527607f13f212ee59383ea165f5e46b81ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001257"
---
# <a name="set-up-expense-management-workflows"></a>経費管理のワークフローを設定する

ワークフローのプロセスを設定することで、出張ドキュメントや経費ドキュメントをレビューすることができます。 ワークフローを定義できるドキュメントには、経費報告書、出張依頼書、現金前払い依頼書などがあります。

ワークフローは業務プロセスを表します。 これは、ドキュメントのシステム内のフローを定義し、タスクの完了や承認を行う人物を示すものです。 組織でワークフロー システムを使用する利点はいくつか考えられます :

-   **一貫性のあるプロセス** - 購買要求書や経費報告書など、特定のドキュメントの承認プロセスを定義することができます。 ワークフロー システムを使用することで、一貫性のある効率的な方法でドキュメントを処理し、承認することができます。

-   プロセスの可視性 — ワークフロー システムでは、特定のワークフロー インスタンスのステータス、履歴、パフォーマンスの指標を追跡できます。 これにより、効率改善にあたってワークフローに変更を加えるべきかどうかを判断することができます。

-   作業一覧の集中管理 —ユーザーは、集中管理された作業の一覧を表示して、自分に割り当てられたワークフロー タスクや承認を表示します。 

**作成できるワークフローの種類**

次の表は、**経費** で作成できるワークフロー タイプの一覧を表わしています。


|              <strong>型</strong>              |                   <strong>このタイプを次に使用する :</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>経費レポート</strong>         |            経費報告書で使用する承認ワークフローを作成します。             |
|  <strong>経費精算書の自動転記</strong>   |        経費報告書で使用する自動転記ワークフローを作成します。        |
|       <strong>経費の明細品目</strong>        |     経費報告書の明細品目で使用する承認ワークフローを作成します。      |
| <strong>経費明細品目の自動転記</strong> | 経費報告書の明細品目で使用する自動転記ワークフローを作成します。 |
|       <strong>出張費要求</strong>       |          出張申請書の承認ワークフローを作成します。           |
|      <strong>現金前払い申請</strong>      |         現金前払い申請の承認ワークフローを作成します。          |
|        <strong>VAT 過誤納税の還付</strong>        | 付加価値税 (VAT) の還付に使用する承認ワークフローを作成します。  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]