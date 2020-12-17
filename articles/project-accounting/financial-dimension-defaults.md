---
title: 財務分析コードの既定値
description: このトピックは、財務分析コードの規定値を設定する方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642369"
---
# <a name="financial-dimension-defaults"></a>財務分析コードの既定値

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations は Dynamics 365 Finance の [財務分析コード](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) フレームワークを使用して、プロジェクトの補助元帳と総勘定元帳の取引に関する追加的な分析情報を提供しています。

既定の財務分析コードは、顧客、プロジェクトの資金源、マイルストーン、プロジェクトの契約品目、プロジェクトに設定できます。

## <a name="define-default-financial-dimensions-for-a-customer"></a>顧客が使用する既定の財務分析コードを定義する

顧客分析コードの既定は、財務で指定されています。 以下の手順を実行して、分析コードの既定値を設定します。

1. **売掛金勘定** > **顧客** > **すべての顧客** に移動します。
2. **顧客** ページで、**財務分析コード** タブで、特定の顧客の財務分析コード値を設定します。

## <a name="define-default-financial-dimensions-for-project-contracts"></a>プロジェクト契約で使用する既定の財務分析コードを定義する

プロジェクト契約は、 Common Data Service (CDS)で作成・管理されます。 プロジェクト契約の会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>プロジェクトの資金源の財務分析コードを設定する

1. **プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。
2. 更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。
3. **関連情報** を展開し、**資金源** タブを選択します。
4. 財務分析コードの既定値を設定します。 財務分析コードは顧客アカウントから既定に設定されていることに注意してください。

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>プロジェクトの契約品目の財務分析コードを設定する

1. **プロジェクト管理および会計** > **プロジェクト** > **プロジェクト契約** の順に移動します。
2. 更新するレコードを選択し、**プロジェクト契約** タブで、**既定の会計を表示する** を選択します。
3. **関連情報** を展開し、**契約品目** タブを選択します。
4. 財務分析コードの既定値を設定します。 財務分析コードの既定が適用され、固定価格 (マイルストーン) 契約品目でのみ使用できます。

これらの既定は、関連するプロジェクトの当座預金取引および請求書明細で使用されます。

## <a name="define-default-financial-dimensions-for-projects"></a>プロジェクトで使用する既定の財務分析コードを定義する

プロジェクトは、CDS で作成・管理されます。 プロジェクトの会計属性は、財務の **プロジェクト管理と会計** モジュールに設定されています。

1. **プロジェクト管理および会計** > **プロジェクト** > **すべてのプロジェクト** に移動します。
2. 更新するレコードを選択し、**プロジェクト** タブで、**既定の会計を表示する** を選択します。
3. **関連情報** を展開し、**設定** タブを選択します。
4. 財務分析コードの既定値を設定します。 財務分析コードは顧客アカウントから既定に設定されていることに注意してください。 プロジェクトが複数のプロジェクト契約顧客を持つ契約品目に関連付けられている場合、プライマリ顧客は、既定の財務分析コードに使用されます。

プロジェクトの既定の財務分析コードは、**プロジェクト運用統合ジャーナル** の時間、費用、手数料のトランザクションと関連するプロジェクトの請求書明細のジャーナル ラインの既定を設定するために使用されます。
