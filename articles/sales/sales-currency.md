---
title: 通貨
description: このトピックは、プロジェクト オペレーションで通貨タイプの追加や削除をする方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: d53bae2f64e7b427f762161ff08917598217bb5a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898357"
---
# <a name="currency"></a>通貨

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

通貨は、製品カタログ内の製品の価格、および受注などの取引のコストを決定します。 顧客が地理的に散在している場合、トランザクションを管理するために、顧客の通貨を追加します。 現在および将来のビジネス ニーズに最適な通貨を追加します。  

> [!NOTE]
> ご利用の環境が Common Data Service 環境 の場合、Power Platform 管理センターにて、**通貨** ページ (**環境** > 環境の選択 > **設定** > **ビジネス** > **通貨**) を選択した場合、ページは空白になります。 これは、Common Data Service 環境では通貨の設定がサポートされていないためです。

## <a name="add-a-currency"></a>通貨の追加  
この手順を開始する前に、セキュリティ ロールにシステム管理者権限が含まれていることを確認してください。 

1. Power Platform 管理センターで、環境を選択します。 
2. **設定** > **ビジネス**を選択します。
3. **通貨** を選択します。  
4. **新規**を選択します。  
5. 必要に応じて、情報を入力します。  


   |          フィールド          |                                                                                                                                                                                                                                                                                                                                                                            説明                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **通貨の種類**    | - **システム** - Dynamics 365 のモデル駆動アプリで利用可能な通貨を使用する場合、このオプションを選択します。 通貨を検索するには、**検索**を選択します。 通貨コードを選択すると、選択した通貨の**通貨名**と**通貨記号**が自動で入力されます。<br />- **カスタム** - Dynamics 365 のモデル駆動アプリで利用可能ではない通貨を追加する場合、このオプションを選択します。 この場合、**通貨コード**、**通貨の精度**、**通貨名**、**通貨記号**、および**為替換算**に対して値を手動で入力する必要があります。 |
   |    **通貨コード**    |                                                                                                                                                                                                                                                                                                                                            通貨の短い形式です。 例えば、米ドルは **USD** となります。                                                                                                                                                                                                                                                                                                                                            |
   | **通貨の有効桁数**  |                                                                                                                                                                                  通貨に使用する小数点以下の桁数を入力します。  0 から 4 までの値を追加できます。 **注意:** もし **システム設定** ダイアログ ボックス に精密な値を設定する場合、その値はここに表示されます。                                                                                                                                                                                  |
   |    **通貨名**    |                                                                                                                                                                                                                                         Dynamics 365 のモデル駆動型アプリで利用可能な通貨の一覧から通貨コードを選択した場合は、その選択した通貨コードの通貨名がここに表示されます。 [通貨の種類] に**カスタム**を選択した場合は、通貨の名前を入力します。                                                                                                                                                                                                                                          |
   |   **通貨記号**   |                                                                                                                                                                                                                                                                      利用可能な通貨の一覧から通貨コードを選択した場合は、その選択した通貨の記号がここに表示されます。 [通貨の種類] に**カスタム**を選択した場合は、追加する通貨の記号を入力します。                                                                                                                                                                                                                                                                       |
   | **為替換算** |                                                                                                                                                                                                                                     選択した通貨の 1 米ドルに相当する金額を入力します。 これは指定通貨を基本通貨に換算した金額です。 **重要:** 取引で不正確な計算を回避するために、この値を必要に応じて頻繁に更新してください。                                                                                                                                                                                                                                      |


6. 変更を終了したら、コマンド バーで、**保存** または **保存して閉じる** を選択します。  

   > [!TIP]
   >  通貨を編集するには、その通貨を選択し、新しい値を入力または選択します。  

## <a name="delete-a-currency"></a>通貨の削除  

1. Power Platform 管理センターで、環境を選択します。 
2. **設定** > **ビジネス**を選択します。
3. **通貨** を選択します。  
4. 表示される通貨の一覧から削除する通貨を選択します。  
5. **削除**を選択します。  
6. 削除を確認します。  

> [!IMPORTANT]
>  他のレコードで使用されている通貨を削除することはできず、非アクティブ化するすることしかできません。 通貨レコードを非アクティブ化した場合でも、営業案件や受注など、既存のレコードに保存されている通貨情報は削除されません。 ただし、新規取引においては、非アクティブ化された通貨は選択できなくなります。  
