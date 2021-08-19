---
title: 請求書プロセスの概要
description: このトピックでは、リソース/非在庫ベースのシナリオのため、Project Operations における請求書のプロセス概要を説明します。
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 804d42f7e8bfd103b9143dc0f5c7ddecdee9e66e6072c3e7bf76b2a8c549cf55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003777"
---
# <a name="invoicing-process-overview"></a>請求書プロセスの概要

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

リソース/非在庫ベースのシナリオ向けの Project Operations は、プロジェクト マネージャーと売掛金担当者/プロジェクト経理担当の両方のニーズに合うように調整された包括的な機能を提供します。 請求プロセスでは、プロジェクト マネージャーがプロジェクトの請求バックログを管理し、売掛金担当者/プロジェクト経理担当が準拠した正確な顧客向けの請求書ドキュメントを作成します。

![請求書のフロー図。](./media/invoicing-flow.png)

プロジェクト契約品目により、関連するプロジェクト トランザクションの請求方法が定義されます。 プロジェクト マネージャーが時間と費用のトランザクションを承認すると、システムはトランザクションを **プロジェクト実績** エンティティに記録し、情報をDynamics 365 Finance の **プロジェクト管理および会計** モジュールに送信します。 次に、プロジェクト経理担当は、[Project Operations 統合仕訳帳](../project-accounting/project-operations-integration-journal.md)を使用してレコードを確認および転記します。 この仕訳帳には、請求、消費税グループ、請求項目消費税グループ、財務ディメンションなど、プロジェクト実績の重要な会計詳細が含まれています。

プロジェクト マネージャーは、[時間と材料の請求バックログ](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)および固定価格請求[固定価格のマイルストーン](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)の時間と材料の請求方法を使用して、未請求の販売トランザクションを確認できます。 これらのビューを使用すると、次の請求サイクルに含める必要があるトランザクションをフィルター処理して選択し、**請求準備完了** としてマークできます。

[見積送り状は手動で作成する](../proforma-invoicing/create-manual-proforma-invoice.md)か、[定期的なプロセス](../proforma-invoicing/configure-automated-invoice-creation.md)を使用できます。 プロジェクトマネージャーは必要に応じて[ドラフト見積送り状を調整](../proforma-invoicing/manage-proforma-invoice.md)して、確認することができます。

確認済みの見積送り状は Finance の **プロジェクト管理および会計** モジュールに送信されます。 プロジェクト経理担当は、プロジェクト仮発行請求書をフォーマットして更新してから、ドキュメントを転記して印刷します。 転記されたプロジェクト請求書は、総勘定元帳に加えて、顧客とプロジェクトの補助元帳に記録されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]