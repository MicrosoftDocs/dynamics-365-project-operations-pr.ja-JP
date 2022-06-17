---
title: 出荷単位および出荷単位一覧
description: この記事では、Dynamics 365 Project Operations で出荷単位と出荷単位一覧を作成する方法について説明します。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a46b7d182d3d7fc77c1275c108f5dc569ffebff1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921446"
---
# <a name="units-and-unit-groups"></a>出荷単位および出荷単位一覧

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

出荷単位とは、製品やサービスを販売する際の数量や単位です。 たとえば、園芸用品を販売する場合、種をパケット、箱、およびパレットの単位で販売することがあります。 出荷単位一覧は、このようにさまざまな出荷単位のコレクションです。

この記事の手順を完了するには、システム管理者または営業担当マネージャーの役割が割り当てられているか、同等の権限を持っていることを確認してください。

## <a name="create-a-unit-group"></a>出荷単位一覧の作成

1. サイトマップにて **単位** を選択します。
2. **新規** を選択し、**出荷単位一覧の作成** ダイアログ ボックスに、単位の名称を入力します。
3. **標準出荷単位** フィールドで、製品を販売する際の、共通測定単位の最小値を入力します。 たとえば、「個」または「オンス」と入力します。
4. **OK** を選択します。

## <a name="add-units-to-a-unit-group"></a>出荷単位一覧に単位を追加する

1. 出荷単位一覧を開き、**関連** タブの、**単位** を選択します。 標準出荷単位が既に追加されていることが確認できます。
2. **新しい単位を追加** を選択し、**クイック作成 : 単位** ページで、**名前** フィールドに、単位の名前を入力します。
3. **数量** フィールドに、その単位が含有する数量を入力します。 例えば、ひと箱あたりに2個収まるのであれば、「2」と入力します。 
4. **基本単位** フィールドで、基本単位を選択し、単位の最小測定単位を設定します。 たとえば、「個」を選択します。
5. **保存** を選択します :


[!INCLUDE[footer-include](../includes/footer-banner.md)]