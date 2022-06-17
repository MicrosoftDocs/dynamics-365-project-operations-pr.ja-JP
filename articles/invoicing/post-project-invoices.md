---
title: 請求書プロセスの概要
description: この記事では、Project Operations におけるリソース/非在庫ベースのシナリオの請求書発行のプロセス概要を説明します。
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923102"
---
# <a name="invoicing-process-overview"></a>請求書プロセスの概要

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

リソース/非在庫ベースのシナリオ向けの Project Operations は、プロジェクト マネージャーと売掛金担当者/プロジェクト経理担当の両方のニーズに合うように調整された包括的な機能を提供します。 請求プロセスでは、プロジェクト マネージャーがプロジェクトの請求バックログを管理し、売掛金担当者/プロジェクト経理担当が準拠した正確な顧客向けの請求書ドキュメントを作成します。

![請求書のフロー図。](./media/invoicing-flow.png)

プロジェクト契約品目により、関連するプロジェクト トランザクションの請求方法が定義されます。 プロジェクト マネージャーが時間/経費トランザクションを承認すると、システムによりトランザクションが **Project Actuals** エンティティに記録され、その情報が Dynamics 365 Finance の **プロジェクト管理および会計** モジュールに送信されます。 次に、プロジェクト経理担当は、[Project Operations 統合仕訳帳](../project-accounting/project-operations-integration-journal.md)を使用してレコードを確認および転記します。 この仕訳帳には、請求、消費税グループ、請求項目消費税グループ、財務ディメンションなど、プロジェクト実績の重要な会計詳細が含まれています。

プロジェクト マネージャーは、[時間と材料の請求バックログ](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)および固定価格請求[固定価格のマイルストーン](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)の時間と材料の請求方法を使用して、未請求の販売トランザクションを確認できます。 これらのビューを使用すると、次の請求サイクルに含める必要があるトランザクションをフィルター処理して選択し、**請求準備完了** としてマークできます。

[見積送り状は手動で作成する](../proforma-invoicing/create-manual-proforma-invoice.md)か、[定期的なプロセス](../proforma-invoicing/configure-automated-invoice-creation.md)を使用できます。 プロジェクトマネージャーは必要に応じて[ドラフト見積送り状を調整](../proforma-invoicing/manage-proforma-invoice.md)して、確認することができます。

確認済みの見積送り状は Finance の **プロジェクト管理および会計** モジュールに送信されます。 プロジェクト経理担当は、プロジェクト仮発行請求書をフォーマットして更新してから、ドキュメントを転記して印刷します。 転記されたプロジェクト請求書は、総勘定元帳に加えて、顧客とプロジェクトの補助元帳に記録されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]