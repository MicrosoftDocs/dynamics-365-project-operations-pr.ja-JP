---
title: プロジェクト見積もりの管理
description: このトピックでは、プロジェクトの見積もりについて説明します。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272934"
---
# <a name="manage-project-quotes"></a>プロジェクト見積もりの管理

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations では、プロジェクト見積が、プロジェクト作業の提案を構築するのに役立つように設計されています。 Project Operations のプロジェクト見積の構造は、次のコンポーネントを含むプロジェクト提案のために構成されています。

  - 上位レベルのコンポーネントとして表示される作業の個別のコンポーネントを識別する見積明細行。
  - 各上位レベルのコンポーネントまたは見積明細行の作業を識別して見積もる見積明細行の詳細。 作業のスケジュールまたは日付見積、および財務的な側面は、その見積明細行に関連づけられています。
  - 契約モデルと課金可能コンポーネントは、見積明細行ごとに設定されます。 この設定をすることで、各見積品目の収益、費用、利益のスプレッドと見積書全体の見積もりを行うことができます。

## <a name="view-all-project-based-quotes"></a>プロジェクトベースの見積をすべて表示する

すべてのプロジェクトの **見積もり** の一覧は、見積つもり一覧のページから確認できます。 

1. **営業** > **見積もり** に移動します。 システム内のすべてのプロジェクト見積もりの一覧が表示されます。 
2. **ビュー スイッチャー** を使用して、フィルター処理された見積もりを選択します。 カスタム フィルター条件を使用して、独自のビューとナビゲーション オプションを構成できます。

見積もりは、この一覧ページや詳細のページから作成、削除できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]