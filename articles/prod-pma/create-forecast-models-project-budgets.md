---
title: プロジェクト予算の予測モデルを作成する
description: このトピックでは、残りの予算の予測モデルの作成方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079404"
---
# <a name="create-forecast-models-for-project-budgets"></a>プロジェクト予算の予測モデルを作成する 

[!include [banner](../includes/banner.md)]

このトピックでは、残りの予算の予測モデルの作成方法について説明します。 予算管理の対象となるプロジェクトでは、元の予算と残りの予算の 2 種類の予算を使用します。 プロジェクト予算を作成する際には、 **予測モデル** ページで作成した元の予算予測モデルと残りの予算予測モデルを指定する必要があります。 指定したモデルに基づくプロジェクト予算は、プロジェクト予算のコミット時に作成されます。

> [!NOTE]
> 予算管理で使用される予測モデルは、サブモデルを持つことも、サブモデルとして使用することもできません。

1. **プロジェクト管理と会計** > **設定** > **予測**  > **予測モデル** を選択します。
2. **新規** を選択して、新しい予測モデルを作成し、新しいモデルのモデル ID 番号と名前を入力します。 
3. **停止** オプションを **はい** に設定して、 予測モデルの予測ラインの変更を防止します。 
4. モデルが関連付けられている予測ラインが総勘定元帳にキャッシュフロー予測を生成する必要がある場合は、、 **キャッシュフロー予測に含める** を **はい** に設定します。 
5. プロジェクトの日付を請求書の日付として使用する場合は、 **予測請求書の日付** を **はい** に設定します。 
6. **計算タイプ** フィールドで、次のいずれかのモデル タイプを選択します :

   - **当初の予算** : 当初の予算が作成され承認された際にコミットされた元の予算額を使用します。
   - **残りの予算** : プロジェクトの存続期間中、残りの予算額を使用します。 この予測モデルの残高は、実際のトランザクションによって減少し、予算の修正によって増減します。
   - **繰り越し** : プロジェクトの繰越予算額を使用します。 繰り越しは、未使用の予算額をある会計年度から別の会計年度に移すために実行できる任意のプロセスです。

7. 必要に応じて次のオプションを設定します :

   - **予測請求日** を有効にして、プロジェクトの日付を請求日として使用します。
   - 仕掛品 (WIP) に基づいて予測する場合は、 **WIP で予測** を有効にし、WIP の種類を選択します。 
   - 既定の **予算タイプ** を **無し** のままにするか、新しいタイプを入力することができます。 レコードを変更しても予算タイプは変更できません。     
    > [!NOTE]
    > 既定の予算タイプを変更すると、他のすべてのオプションが更新できなくなり、この予測モデルを再利用することはできません。 
   


 
