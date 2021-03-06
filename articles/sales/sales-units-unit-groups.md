---
title: 出荷単位および出荷単位一覧
description: このトピックでは、Dynamics 365 プロジェクト オペレーションでユニットとユニット グループを作成する方法について説明します。
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898762"
---
# <a name="units-and-unit-groups"></a>出荷単位および出荷単位一覧

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

出荷単位とは、製品やサービスを販売する際の数量や単位です。 たとえば、園芸用品を販売する場合、種をパケット、箱、およびパレットの単位で販売することがあります。 出荷単位一覧は、このようにさまざまな出荷単位のコレクションです。

このトピックの手順を完了するには、システム管理者、または Sales Professional マネージャーの役割が割り当てられているか、同等の権限を持っていることを確認してください。

## <a name="create-a-unit-group"></a>出荷単位一覧の作成

1. サイトマップにて **単位**を選択します。
2. **新規**を選択し、**出荷単位一覧の作成**ダイアログ ボックスに、単位の名称を入力します。
3. **標準出荷単位**フィールドで、製品を販売する際の、共通測定単位の最小値を入力します。 たとえば、「個」または「オンス」と入力します。
4. **OK** を選択します。

## <a name="add-units-to-a-unit-group"></a>出荷単位一覧に単位を追加する

1. 出荷単位一覧を開き、**関連**タブの、**単位**を選択します。 標準出荷単位が既に追加されていることが確認できます。
2. **新しい単位を追加**を選択し、**クイック作成 : 単位**ページで、**名前**フィールドに、単位の名前を入力します。
3. **数量**フィールドに、その単位が含有する数量を入力します。 例えば、ひと箱あたりに2個収まるのであれば、「2」と入力します。 
4. **基本単位**フィールドで、基本単位を選択し、単位の最小測定単位を設定します。 たとえば、「個」を選択します。
5. **保存**を選択します :
