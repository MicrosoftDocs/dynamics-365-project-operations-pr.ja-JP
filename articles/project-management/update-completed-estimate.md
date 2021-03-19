---
title: 完了時予測の更新
description: このトピックでは、プロジェクトの作業量予測の更新に関する説明をします。
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286434"
---
# <a name="update-estimate-at-completion"></a>完了時予測の更新

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

プロジェクト マネージャーが、タスクの最初の予測を変更することはよくあります。 プロジェクトの再プロジェクションは、プロジェクトの現在の状態による、プロジェクト マネージャーの予測の認識です。 ただし、プロジェクトのベースラインは、プロジェクトのスケジュールおよびコスト見積もりに関する公表済みの真実のソースを表しており、これはプロジェクトの全利害関係者が既に合意しているため、プロジェクト マネージャーがベースライン値を変更することは推奨されません。

プロジェクト マネージャーがタスクの工数を再プロジェクトするには 2 つの方法があります:

- 規定の完了見込み (ETC) をタスクの実際の残り工数の新たな見積もりで上書きします。 
- 規定の進捗率をタスクの実際の残り工数の新しい見込みで上書きします。

これらのアプローチではそれぞれ、タスクの ETC、完了時予測 (EAC)、進捗率の再計算やタスクの予測工数差異を発生させます。 サマリー タスクの EAC、ETC、進捗率が再計算され、新たな工数分散の予測が作成されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]