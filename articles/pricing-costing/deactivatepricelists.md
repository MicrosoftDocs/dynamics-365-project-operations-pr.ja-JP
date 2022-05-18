---
title: 価格表を非アクティブ化する
description: このトピックは、使用していないか古い価格表を非アクティブ化または削除する方法を説明しています。
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ab790764f7a99118fd42bc76934105389173ff88
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596889"
---
# <a name="deactivate-price-lists"></a>価格表を非アクティブ化する 

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations から古いまたは使用していない価格表を削除するために実行するステップが 2 つあります。 

1. 特定のページから価格表を除去または削除します。
2. **価格表** ページで、アクティブな価格リストから価格リストを非アクティブ化または削除します。

>[!IMPORTANT]
> 価格表を完全に削除するには、両方の手順を実行する必要があります。 [アクティブな価格リスト] ビューから価格リストを直接削除または非アクティブ化するステップ 2 を実行するだけでは不十分です。 また、ステップ 1 で説明したすべての場所から、この価格表の関連付けを削除する必要があります。

## <a name="delete-the-price-list-from-specific-pages"></a>特定のページから価格表を削除します
1. Project Operations から価格表を削除するには、次のページに移動します。  

      - **プロジェクト パラメーター** ページ > **価格表** タブ
      - **組織単位** ページ > **価格表** グリッド
      - **アカウント** ページ > **プロジェクト価格表** グリッド
      - **プロジェクトの見積もり** ページ > **プロジェクト価格表** グリッド: これは、すべてのアクティブなプロジェクト見積もりに適用されます。
      - **プロジェクト契約** ページ > **プロジェクト価格表** グリッド: これは、すべてのアクティブなプロジェクト契約に適用されます。

 2. ページごとに、削除する価格表を選択してから、**削除** を選択する必要があります。 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>[価格表] ページで、価格リストを削除または非アクティブ化します
 
1. アクティブ価格表から価格表を削除するには、**販売** > **顧客** > **価格表** に移動します。 
2. 削除する価格表を選択し、それから **削除** を選択します。 価格表が既存のトランザクションで参照されている場合、それを削除することはできません。 これが発生した場合は、価格表を非アクティブ化して、どのビューにも表示されないようにすることができます。 
3. 価格表を非アクティブ化するには、価格表をもう一度選択してから、**非アクティブ化** を選択します。   
