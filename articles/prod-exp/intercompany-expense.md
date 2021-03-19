---
title: 会社間経費
description: このトピックでは、会社間経費を使用して、作業が実行された法人に作業者の経費を割り当てる方法を説明します。
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271539"
---
# <a name="intercompany-expenses"></a>会社間経費

組織内のある法人に雇用されている作業者が、同じ組織内の別の法人で作業を行う場合があります。 会社間経費を使用して、作業が実行された法人に作業者の経費を割り当てることができます。 作業者を雇用する法人は、貸与法人と呼ばれます。 作業者が費用を負担する法人は、借用法人と呼ばれます。 

作業者が会社間経費を作成して提出する前に、会社間経費明細行を有効にする必要があります。 貸付法人では、**経費管理パラメーター** ページで、**会社間経費明細行を許可する** を選択します。 

## <a name="tax-posting-for-intercompany-expenses"></a>会社間費用の税転記

[!include [banner](../includes/banner.md)]

経費精算書で借用法人 (ソース) ではなく貸与法人 (デスティネーション) に関連付けられている税グループを使用できるようになる前に、一般会計の消費税パラメーターのセットアップで機能を有効化する必要があります。 **会社間税転記の法人** パラメーターが **ソース** に設定され、**消費税課税ルールの適用** フィールドが **いいえ** に設定されている場合、貸与法人の税の組み合わせが使用されます。 同じパラメーターが **宛先** に設定されている場合、借用法人の税の組み合わせが使用されます。 米国の法人の場合、パラメーターが **ソース** に設定されている場合、**消費税収入** フィールドも新しい **元帳転記グループ** ページで構成する必要があります。 会計エンジンは、このフィールドの情報を税関連の会計入力に使用します。   
プロジェクトの有無にかかわらず転記された経費明細の動作は一貫しています。  


[!INCLUDE[footer-include](../includes/footer-banner.md)]