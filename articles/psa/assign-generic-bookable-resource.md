---
title: 一般的な予約可能なリソースをタスクとプロジェクト チームに割り当てる
description: このトピックでは、タスクとプロジェクト チームへの汎用リソースの予約に関する情報を提供します。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079283"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>予約可能な汎用リソースをタスクに割り当て、リソース要件を生成する 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

プロジェクトに名前付きリソースや実リソースを予約して割り当てることに加えて、プロジェクト タスクに汎用リソースを割り当てることができます。 これらのリソースは、プロジェクトに名前付きリソースを配置する準備ができるまで、名前付きリソースのプレースホルダーとして機能します。 

1. Project Service Automation (PSA) で **プロジェクト** ページを開き、 **スケジュール** タブで、スケジュールの **リソース** セルに汎用リソースの位置名を入力します。 または、セルの **リソース** アイコンをクリックしてリソース ピッカーを開き、作成する汎用リソースの名前を入力します。

![汎用チーム メンバーの作成と割り当て](media/RM-how-to-9.png)

これで **簡易作成: プロジェクト チーム メンバー** パネルが開きます。 

2. 汎用リソース チーム メンバーの役割と組織単位を入力して **保存** をクリックします。

![汎用チーム メンバーの簡易作成](media/RM-how-to-10.png)

3. 新しい汎用リソース チーム メンバーを作成が完了すると、タスクに割り当てられます。 タスク スケジュール内の他のタスクに、その汎用リソースを引き続き割り当てることができます。

![既存の汎用チーム メンバーをタスクに割り当てる](media/RM-how-to-11.png)

4. 汎用リソースを割り当てた後、リソース要求を生成して、リソース マネージャーに直接予約または送信してリソース要求を満たすことができます。

![汎用チーム メンバーの要件の生成](media/RM-how-to-12.png)

チーム メンバー グリッドでは、上述したリソース ピッカーを使用できることに加え、汎用リソースを直接追加できます。 リソースは **簡易作成: プロジェクト チーム メンバー** パネルで指定した開始/終了日と割り当て方法に基づいたリソース要件で追加されます。

汎用チーム メンバーを直接追加して、カバーするのに必要な時間よりも多くのタスクを汎用リソースに割り当てると、違いがわかります。 **要件の生成** をクリックして要件を再生成し、必要な時間と割り当てのバランスを取ります。

チーム グリッドの **リソース要件** リンクをクリックして、要件を開き、スキル、優先リソースなどを追加することもできます。

![リソース要件](media/RM-how-to-13.png)
