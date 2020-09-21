---
title: プロジェクトのリソースをスケジュールする
description: Project Service でのプロジェクトのリソースをスケジュールする方法
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752929"
---
# <a name="schedule-resources-for-a-project-project-service"></a>プロジェクトのリソースをスケジュールする (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

リソースの空き時間をチェックして、リソースの予約状況の全体のビューを取得できます。または、ビューをスキル、チーム、場所、およびその他のオプションでフィルターすることができます。  
  
スケジュール ボードにはリソースと可用性が一覧表示されます。 ビュー モードを選択し、**時間**、**日**、**週**、または **月** 別に可用性を表示します。  
  
スケジュール ボードを使用する前に、それをセットすることは重要です。 詳細については、 [スケジュール ボードの構成 (Field Service または Project Service Automation)](../field-service/configure-schedule-board.md) を参照してください。
  
リソースの可用性の目的で、古いバージョンを使用している場合は、[ビュー リソースの可用性](../project-service/view-resource-availability.md) を参照してください。  

> [!IMPORTANT]
>  スケジュール ボード予約機能、ジオコード化、および位置サービスを使用するには、マップを有効にする必要があります。  
> 
> 1. メイン メニューから、**リソース スケジュール** > **管理** を選択します。  
> 2. **スケジュール パラメーター**をクリックします。  
> 3. レコードを開き、**Resource Scheduling Optimization** セクションへと下にスクロールします。  
> 4. **マップに接続する**フィールドで、**はい**を選択します。  
> 5. サブスクリプション利用条件に同意し、レコードを保存します。  
> 6. メイン メニューで、**プロジェクト サービス** > **スケジュール ボード** を選択します。 ここでは、予約条件を手動でスケジュールするには複数の方法があります。 都合のよい方法を選択します。
  
## <a name="find-available-resources"></a>利用可能なリソースをみつける

1.  **予約の条件**リストから、スケジュールが完了していない予約を右クリックし、次のいずれかを選びます:  
  
- **使用可能の検索 - 現在のリソース** を選択して、スケジュール ボードのリストから使用可能なリソースを検索します。  
- **使用可能の検索 - 全てのリソース** を選択して、システムのリソースから使用可能なリソースを検索します。  
   > [!NOTE]
   >  この操作を行う場合、フィルターは選択された予約要件のオプションを表示します。  
  
2. 利用可能な時間帯が表示されたら、スケジュール ボードの時間帯を右クリックし、**ここを予約する** を選択します。 または、使用可能な時間スロットに予約の条件をドラッグ・アンド・ドロップします。  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>日単位を使用してリソースを予約し、誰の名前で予約されているかを検索する
  
1.  スケジュール ボードで、**モードの表示** を選択し **日** を選択します。  
  
    これではリソースが 1 日あたりに何時間予約されるかおよび何日が空いているかのグリッド ビューが表示されます。  
  
2.  予約するリソース名をクリックし、**予約** を選択します。  
  
3.  **リソースの予約 (作成)** ダイアログ ボックスで、予約方法と開始時間や終了時間と共に、リソースを予約するプロジェクトを選びます。  
  
4.  完了したら、**予約** を選択します。  
  
## <a name="view-to-the-schedule-board"></a>スケジュール ボードの表示
  
1.  下部の一覧からスケジュールが完了していない予約要件を選択します。  
  
2.  その予約要件をスケジュール ボード上の使用可能なリソース/時間帯にドラッグします。  
  
3.  完了したら、**予約** を選択します。  
  
### <a name="additional-resources"></a>その他のリソース  
 [リソース マネージャー ガイド](../project-service/resource-manager-guide.md)
