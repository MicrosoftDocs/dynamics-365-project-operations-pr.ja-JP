---
title: 会社間経費
description: 組織内のある法人に雇用されている作業者は、同じ組織内の別の法人のために仕事をする場合があります。 この状況では、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079419"
---
# <a name="intercompany-expenses"></a>会社間経費

[!include [banner](../includes/banner.md)]

組織内のある法人に雇用されている作業者は、同じ組織内の別の法人のために仕事をする場合があります。 この状況では、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。 作業者を雇用する法人は、貸与法人と呼ばれます。 作業者が費用を負担する法人は、借用法人と呼ばれます。 

作業者が別の法人のために行われる作業の費用を作成して提出できるようにするには、貸与法人の **経費管理パラメーター** ページで、 **会社間経費明細の許可** オプションを選択します。 

## <a name="tax-posting-for-intercompany-expenses"></a>会社間費用の税転記

[!include [banner](../includes/banner.md)]

経費報告書で借用 (宛先) 法人の代わりに貸与 (ソース) 法人に関連付けられている税グループを使用する場合は、一般会計の消費税設定でこれを構成する必要があります。 一般会計パラメーター、 **会社間税転記の法人** が **ソース** に設定され、 **消費税課税ルールの適用** が **いいえ** に設定されている場合、貸与法人の税の組み合わせが使用されます。 同じパラメーターが **宛先** に設定されている場合、借用法人の税の組み合わせが使用されます。 米国の法人の場合、パラメーターが **ソース** に設定されている場合、 **消費税収入** フィールドも新しい **元帳転記グループ** ページで構成する必要があります。 会計エンジンは、このフィールドの情報を税関連の会計入力に使用します。   
プロジェクトの有無にかかわらず転記された経費明細の動作は一貫しています。  
