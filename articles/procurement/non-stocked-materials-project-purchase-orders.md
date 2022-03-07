---
title: プロジェクトの発注書を使用してプロジェクトの非在庫材料を注文する
description: このトピックでは、プロジェクトの発注書を使用してプロジェクトの非在庫材料を注文できます。
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563028"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>プロジェクトの発注書を使用してプロジェクトの非在庫材料を注文する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

商品やサービスの注文を追跡するために、組織の調達部門が [発注書](/dynamics365/supply-chain/procurement/purchase-order-overview) を使用する場合もあります。 非在庫材料の発注書はプロジェクトに帰属させることができます。 これらの発注書に請求すると、プロジェクトに対するコストが記録されます。

## <a name="prerequisites"></a>前提条件
プロジェクトの発注書機能を有効にするには、次の手順を実行します。

1. Dynamics 365 Finance では、**機能管理** ワークスペースに移動します。
2. 機能リストで、機能を見つけて選択し、**リソースベース/非在庫シナリオの Project Operations でプロジェクト発注書を有効にします**。
3. **有効にする** を選択します。
4. 非在庫材料と保留中のベンダーの請求書を、[非在庫材料や保留中のベンダー請求書を構成する](configure-materials-nonstocked.md) の説明に従って構成します。

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>プロジェクト発注書リストからプロジェクト発注書を作成する

1. Finance では、**プロジェクト管理と会計** > **プロジェクト** > **すべてのプロジェクト** に移動して、プロジェクトを選択します。
2. アクション ペインの **管理** タブの **新規** グループで、**項目タスク** > **発注書** を選択します。
3. **発注書を作成する** ページで、発注をしたいベンダーを選択し、必要に応じて他の情報を入力してから **OK** を選択します。
4. **発注書** ページの **発注書明細行** グリッドで、**明細行の追加** を選択します。
5. 必要に応じて、品目番号、数量、単位、単価、およびその他の情報を入力します。

    > [!NOTE]
    > プロジェクトの発注書で使用できるのは、非在庫の品目とサービスのみです。 在庫品と調達カテゴリはサポートされていません。

6. 必要に応じてアイテムを追加し続け、発注書を確認します。

    商品とサービスの領収書は、商品の領収書を作成して転記することで記録できます。

    > [!NOTE]
    > 製品の領収書は、Microsoft Dataverse ではプロジェクトの実績に記録されず、プロジェクトの補助元帳に影響を与えません。

    ベンダーが発注書の品目とサービスの請求書を送信した後、調達部門はアクション ペインの **請求書** > **生成** > **請求書** に移動することで、発注書の請求書を生成できます。 保留中のベンダー請求書の詳細については、[保留中のベンダー請求書を使用して、在庫のない資材を購入する](pending-vendor-invoices.md) を参照してください。