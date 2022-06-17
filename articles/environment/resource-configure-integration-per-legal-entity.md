---
title: 法人ごとに Project Operations 統合を構成する
description: この記事では、Project Operations で法人が構成データをセットアップして適用する方法について説明します。
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914684"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>法人ごとに Project Operations 統合を構成する 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

この記事では、法人ごとに Dynamics 365 Project Operations を構成するために必要な手順について説明します。

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dynamics 365 Finance の機能キーを有効にする

必要な機能を有効にするには、次の手順を実行します。

1. Dynamics 365 Finance で、**機能管理** ワークスペースに移動します。
2. **機能リスト** に、次の機能を見つけて有効にします。
  
    - **プロジェクトの複数の契約ラインを有効にする**
    - **Dynamics 365 Customer Engagement で Project Operations を有効にする**

> [!NOTE]
> **機能キー** がリストされていない場合は、Finance バージョンが最小バージョン要件 (すべての品質更新が適用されたアプリケーション バージョン 10.0.13 以上) を満たしていることを確認します。 **アップデートを確認する** を選択して、機能リストを更新します。

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>法人の Project Operations 展開シナリオを定義する

法人レベルで Dynamics 365 Customer Engagement の Project Operations を有効にできます。 リソース/非在庫ベースのシナリオで Dynamics 365 Customer Engagement の Project Operations を使用する 1 つの法人を持つことができます。 同じ環境で、在庫/製造指図シナリオの Project Operations を使用して別の法人を持つことができます。

1. Dynamics 365 Finance で、**プロジェクト管理と会計** > **設定** > **グローバル プロジェクト管理および会計パラメータ** に移動します。
2. 使用可能な法人のリストで、複数の契約品目と Dynamics 365 Customer Engagement 機能の Project Operations が有効になるエンティティを選択します。 在庫/製造指図シナリオで Project Operations を使用する法人は選択しないでください。

> [!NOTE]
> 法人は、既存のプロジェクトがない場合にのみ選択できます。

## <a name="configure-project-management-and-accounting-parameters"></a>プロジェクト管理および会計パラメーター ページを構成します。

Dynamics 365 Customer Engagement で Project Operations を使用する各法人には、一連の既定のパラメーターが必要です。 これらのパラメータは、**プロジェクト管理と会計パラメータ** ページの **プロジェクト運営** タブで構成します。 このパラメーターは、次のとおりです。

  - **請求タイプのデフォルト**: Project Operations は、明細プロパティ Finance にマップする必要がある請求タイプの既定の固定セットを使用します。 請求タイプごとにレコードを作成します: **指定されていない**、**有料**、**非課金**、**無料**、**利用不可**。
  - **プロジェクトカテゴリのデフォルト**: 各トランザクション タイプに使用する規定のプロジェクト カテゴリを選択します。 これらの規定は、**Project Operations 統合ジャーナル** とプロジェクト実績のトランザクション カテゴリが指定されていない見積もりで使用されます。
  - **予測**: 時間と費用の見積もりに使用する予測モデルを選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]