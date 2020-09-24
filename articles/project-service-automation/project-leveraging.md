---
title: 売上予測とプロジェクト
description: このトピックは、営業プロセスでスケジュールおよび見積もりのメリットを最大限に活用する方法について説明します。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752834"
---
# <a name="sales-estimates-and-projects"></a>売上予測とプロジェクト

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

営業プロセス中には、プロジェクトを販売見積とリンクすることで売上予測を立てることができます。 このようにして、営業プロセス中に明確な予測を立てることができ、プロジェクトのスケジュールと予測能力を最大限に活用することができます。 販売が処理されると、売上予測目的でしようされたスケジュールは、プロジェクト計画のさらなる精密化のベースとして使用することができます。

## <a name="linking-a-project-to-a-quote-line"></a>プロジェクトを見積依頼明細行にリンクする

プロジェクトベースの見積依頼明細行を作成する場合、新規プロジェクトの作成や、**見積依頼明細行**ページの既存のプロジェクトと関連付けることができます。 

> ![見積依頼明細行フォーム](media/project-8.png)
 
見積依頼明細行の詳細で新規プロジェクトを作成する場合、プロジェクト テンプレートを利用できます。 プロジェクト テンプレートは、標準プロジェクト計画と組織内の一般的な会計の予測を表すモデル プロジェクトです。 過去のプロジェクトからのプロジェクト計画や予測のコピーも表すことができます。

> ![見積依頼明細行の詳細](media/project-9.png)
  
見積からプロジェクトを作成する場合、プロジェクトは自動的に見積依頼明細行と関連付けられます。

## <a name="components-of-estimates-in-a-project"></a>プロジェクト内の見積もりのコンポーネント

スケジュールにより、作業のタスクへの分割、タスクの階層維持、タスク完了に必要とされるリソースの決定、タスク完了に必要とされる工数の割り当てができます。

**プロジェクト**ページの**スケジュール**タブのフィールドを使用することで、作業労力とスケジュール予測を定義できます。 価格表がプロジェクトに関連付けられているため、価格表で定義されている原価と売上を使用して、財務見積りが計算されます。

## <a name="importing-estimates-from-a-project-into-a-quote"></a>プロジェクトからの見積もりを見積へインポートする

プロジェクト見積もりを定義した後、これらを見積依頼明細行にインポートできます。 **見積依頼明細行の詳細**ページで、リボン上の**見積もりからのインポート**を選択して、トランザクションの種類、ロール、またはタスク レベルによるプロジェクト見積もりを要約します。