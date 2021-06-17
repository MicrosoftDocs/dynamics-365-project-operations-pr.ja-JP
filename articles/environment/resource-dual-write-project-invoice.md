---
title: プロジェクト請求書統合
description: このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996572"
---
# <a name="project-invoice-integration"></a>プロジェクト請求書統合

このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。

Project Operations では、プロジェクト マネージャーがプロジェクトの請求書のバックログを管理し、Microsoft Dataverse の顧客への仮の請求書を作成します。 仮の請求書に基づいて、売掛金担当者やプロジェクト会計士が顧客向けの請求書を作成します。 二重書き込みの統合により、仮の請求書の詳細が Finance and Operations アプリに同期されます。 顧客向けの請求書が転記された後、システムは Dataverse の関連するプロジェクトの実績を会計の詳細に合わせて更新します。 次の図は、この統合の高レベルの概念的概要を示しています。

   ![プロジェクト請求書統合](./media/DW5Invoicing.png)

プロジェクト マネージャーが Dataverse で仮の請求書を確認した後、仮の請求書のヘッダー情報は、二重書き込みテーブル マッピング **ロジェクト請求書提案 V2 (invoices)** を使って Finance and Operations アプリに同期されます。 これは Dataverse アプリから Finance and Operations アプリへの一方通行の統合です。 Finance and Operations アプリで直接プロジェクトの請求書案を作成や削除はサポートされていません。

Dataverse での請求書の確認は、**実績** エンティティに請求書関連のレコードを作成するビジネス ロジックのトリガーにもなります。 これらのレコードは、二重書き込みテーブルマッピングの **Project Operations 統合実績 (msdyn\_actuals)** を使って Finance and Operations に同期されます。 詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。 

プロジェクトの請求書提案の明細は、定期的なプロセスである **ステージングからのインポート** によって作成されます。 このプロセスは、**実績のステージング** テーブル の請求済みの売上実績の詳細に基づいて行われます。 詳細については、[プロジェクトの請求書提案を管理する](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)を参照してください。 
