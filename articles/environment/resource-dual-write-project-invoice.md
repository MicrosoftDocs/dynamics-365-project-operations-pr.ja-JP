---
title: プロジェクト請求書統合
description: このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581244"
---
# <a name="project-invoice-integration"></a>プロジェクト請求書統合

このトピックでは、顧客の請求書作成で使用する Project Operations 二重書き込みの統合についての情報を提供します。

Project Operations では、プロジェクト マネージャーがプロジェクトの請求書のバックログを管理し、Microsoft Dataverse の顧客への仮の請求書を作成します。 仮の請求書に基づいて、売掛金担当者やプロジェクト会計士が顧客向けの請求書を作成します。 二重書き込み統合により、プロフォーマ インボイスの詳細が財務と運用アプリに同期されます。 顧客向けの請求書が転記された後、システムは Dataverse の関連するプロジェクトの実績を会計の詳細に合わせて更新します。 次の図は、この統合の高レベルの概念的概要を示しています。

   ![プロジェクト請求書統合。](./media/DW5Invoicing.png)

プロジェクト マネージャーが Dataverse でプロフォーマ インボイスを確認した後、プロフォーマ インボイス ヘッダー情報は、二重書き込みテーブル マップ、**プロジェクト請求書提案 V2 (請求書)** を使用して財務と運用アプリと同期します。 これは、Dataverse から財務と運用アプリへの一方向の統合です。 財務と運用アプリで直接プロジェクト請求書提案を作成または削除することはサポートされていません。

Dataverse での請求書の確認は、**実績** エンティティに請求書関連のレコードを作成するビジネス ロジックのトリガーにもなります。 これらのレコードは、二重書き込みテーブル マップ **Finance and Operations 統合実績 (msdyn\_actuals)** を使用して財務と運用アプリに同期されます。 詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。 

プロジェクトの請求書提案の明細は、定期的なプロセスである **ステージングからのインポート** によって作成されます。 このプロセスは、**実績のステージング** テーブル の請求済みの売上実績の詳細に基づいて行われます。 詳細については、[プロジェクトの請求書提案を管理する](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)を参照してください。 
