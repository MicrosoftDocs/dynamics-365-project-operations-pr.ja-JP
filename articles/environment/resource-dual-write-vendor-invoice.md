---
title: 仕入先請求書統合
description: この記事では、Project Operations でのベンダー請求書統合について説明します。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912062"
---
# <a name="vendor-invoice-integration"></a>仕入先請求書統合

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Dynamics 365 Project Operations でのプロジェクト関連の調達は、**買掛金勘定** > **請求書** > **保留中のベンダーの請求書** にアクセスして保留中のベンダー請求書を使って記録することができます。 詳細については、[保留中のベンダーの請求書を使って非在庫の材料を購入する](../procurement/pending-vendor-invoices.md)を参照してください。

> [!IMPORTANT]
> この記事で説明されている機能を使用する前に、必要な構成を確認して適用してください。 詳細については、[在庫のない資材と保留中のベンダーの請求書を有効にします](../procurement/configure-materials-nonstocked.md)を参照してください。

Project Operations では、プロジェクト関連のベンダーの請求書は、特別な転記ルールを使用して転記されます。

- プロジェクト関連のコスト (回収不能な税金を含む) は、総勘定元帳のプロジェクトのコスト勘定にすぐには計上されません。 代わりに、コストは **調達の統合アカウント** に転記されます。 この勘定は、**プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメーター**、**Dynamics 365 Customer engagement の Project Operations** タブで構成されています。
- 二重書き込みは、以下のテーブル マッピングを使用して、ベンダーの請求書明細を Microsoft Dataverse に同期します。

     - **Project Operations 統合プロジェクトベンダーの請求書エクスポート エンティティ (msdyn_projectvendorinvoices)**: このテーブル マッピングは、ベンダーの請求書ヘッダー情報を同期します。 プロジェクト ID を含む行がひとつ以上あるベンダーの請求書だけが  Dataverse に同期されます。
     - **Project Operations 統合プロジェクト ベンダーの請求書エクスポート明細のエンティティ (msdyn_projectvendorinvoicelines)**: このテーブル マッピングは、ベンダーの請求書明細の情報を同期します。 プロジェクト ID を含む行のみが Dataverse に同期されます。

     > [!NOTE]
     > Dataverse 内のベンダーの請求書の詳細は編集できません。

税補助元帳、ベンダー補助元帳、その他の財務転記は、ベンダーの請求書が転記されるときに、Dynamics 365 Finance に該当するものとして記録されます。

![ベンダー請求書統合。](media/DW7VendorInvoice.png)

Dataverse の **ベンダーの請求書** エンティティに記録が書き込まれると、記録の自動承認プロセスが始まります。 必要に応じて、次にアクセスすることで、Dataverse の自動承認プロセスの状態を確認できます : **高度な設定** > **システム** > **システム ジョブ**。 承認が完了すると、システムは **実績** エンティティに材料トランザクション クラスのレコードを作成します。

材料関連の実績は、二重書き込みテーブル マッピングの  **Project Operations 統合実績 (msdyn_actuals)** を使って処理されます。 詳細については、[プロジェクトの見積もりと実績](resource-dual-write-estimates-actuals.md) を参照してください。

定期的なプロセスである **ステージング テーブルからのインポート** では、ベンダーの請求書に関連する Project Operations 統合仕訳を作成します。 オフセット勘定は、既定で調達統合アカウントになります。 統合仕訳が転記されると、ベンダーの請求書取引の勘定残高がクリアされ、明細の額がプロジェクト費用勘定に移動します。 また、ダウンストリームの請求書作成や収益認識のために、プロジェクト サブリーダーのトランザクションも作成されます。
