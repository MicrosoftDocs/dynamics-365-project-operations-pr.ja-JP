---
title: 法人ごとに Project Operations 統合を構成する
description: このトピックでは、Project Operations で法人による統合の設定方法について説明します。
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999412"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>法人ごとに Project Operations 統合を構成する 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックは、法人ごとに Dynamics 365 Project Operations を構成するのに必要な手順を説明します。

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dynamics 365 Finance の機能キーを有効にする

必要な機能を有効にするには、次の手順を実行します。

1. Dynamics 365 Finance では、**機能管理** ワークスペースに移動します。
2. **機能リスト** に、次の機能を見つけて有効にします。
  
    - **プロジェクトの複数の契約ラインを有効にする**
    - **Dynamics 365 Customer Engagement 上の Project Operations を有効にする**

> [!NOTE]
> **機能キー** がリストされていない場合は、Finance バージョンが最小バージョン要件 (すべての品質更新が適用されたアプリケーション バージョン 10.0.13 以上) を満たしていることを確認します。 **アップデートを確認する** を選択して、機能リストを更新します。

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>法人の Project Operations 展開シナリオを定義する

法人レベルで Dynamics 365 Customer Engagement で Project Operations を有効にできます。 リソース/在庫のないベースのシナリオに対して Dynamics 365 Customer Engagement の Project Operations を使用して 1 つの法人を持つことができます。 同じ環境で、在庫/製造指図シナリオの Project Operations を使用して別の法人を持つことができます。

1. Dynamics 365 Finance で、**プロジェクト管理と会計** > **設定** > **グローバル プロジェクト管理と会計パラメータ** の順に移動します。
2. 利用可能な法人のリストで、有効にする Dynamics 365 Customer Engagement 機能で複数の契約ラインと Project Operations が行われているエンティティを選択します。 在庫/製造指図シナリオで Project Operations を使用する法人は選択しないでください。

> [!NOTE]
> 法人は、既存のプロジェクトがない場合にのみ選択できます。

## <a name="configure-project-management-and-accounting-parameters"></a>プロジェクト管理および会計パラメーター ページを構成します。

Dynamics 365 Customer Engagement の Project Operations を使用する各法人は、規定パラメータのセットが必要です。 これらのパラメータは、**プロジェクト管理と会計パラメータ** ページの **プロジェクト運営** タブで構成します。 このパラメーターは、次のとおりです。

  - **請求タイプのデフォルト**: Project Operations は、明細プロパティ Finance にマップする必要がある請求タイプの既定の固定セットを使用します。 請求タイプごとにレコードを作成します: **指定されていない**、**有料**、**非課金**、**無料**、**利用不可**。
  - **プロジェクトカテゴリのデフォルト**: 各トランザクション タイプに使用する規定のプロジェクト カテゴリを選択します。 これらの規定は、**Project Operations 統合ジャーナル** とプロジェクト実績のトランザクション カテゴリが指定されていない見積もりで使用されます。
  - **予測**: 時間と費用の見積もりに使用する予測モデルを選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]