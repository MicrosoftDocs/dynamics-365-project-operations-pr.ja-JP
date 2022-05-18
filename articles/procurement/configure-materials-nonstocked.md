---
title: 非在庫材料と保留中の仕入先請求書を構成する
description: このトピックでは、在庫のない資材と保留中のベンダーの請求書を有効にする方法を説明しています。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592974"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>非在庫材料と保留中の仕入先請求書を構成する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

## <a name="minimum-version-requirement"></a>バージョンの最小要件

Dynamics 365 Project Operations の在庫のない/リソース ベースのシナリオで、在庫のない材料や保留中のベンダーの請求書を使用するには、以下のバージョンが必要となります:

Dynamics 365 Dataverse の解決策:

- Project Operations – 4.9.0.221 またはそれ以上
- 二重書き込みアプリケーション オーケストレーション ソリューション- 2.2.2.23 またはそれ以上

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) またはそれ以上。 ご利用の Finance 環境が最新であり、すべての品質アップデートが適用されていることを確認し、最小のバージョン要件を満たしていることを確認してください。

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>在庫のない材料とベンダーの請求書統合に二重書き込みマッピングを実行する

このセクションでは、在庫のない材料やベンダーの請求書に必要となる具体的なマッピングについて説明します。 [新しい環境をプロビジョニングする](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps)のトピックに記載されている前提条件のマッピングが環境上で動作していることを確認します。

1. Lifecycle Services (LCS) にアクセスし、LCSプロジェクトに移動トして、**環境の詳細** ページにアクセスします。
2. **Common Data Service環境情報** セクションで、**CDS for Apps へのリンク** を選択します。 リンクを選択すると、マッピングでエンティティのリストにリダイレクトされます。
3. 次のマッピングが実行されていることを確認してください。 これらが実行されていない場合は、実行し、関連するすべてのテーブルマッピングが含まれていることを確認してください。

    - CDSが個別の製品 (products) リリースしている
    - ベンダー v2 (msdyn_vendors)
    - Project Operations テーブルによる材料の見積もり (msdyn_estimatelines)
    - Project Operations 統合プロジェクト ベンダー請求書のエクスポート エンティティ (msdyn_projectvendorinvoices)
    - Project Operations 統合プロジェクト ベンダー請求書明細のエクスポート エンティティ (msdyn_projectvendorinvoicelines)
    - Project Operations の統合実績 (msdyn_actuals)。 マッピング バージョン 1.0.0.14 またはそれ以降を実行していることを確認してください。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 **テーブル マッピングのバージョン** を選択し、選択したバージョンを保存することで、マッピングの新しいバージョンを有効にすることができます。

標準のデモデータを使用している場合は、最初の同期で以下のエンティティマップを停止し、再起動が必要となる場合もあります:
  - 支払い日 CDSV2 (msdyn_paymentdays)
  - 支払いスケジュール (msdyn_paymentschedules)
  - 支払い条件 (msdyn_paymentterms)
  - ベンダー グループ (msdyn_vendorgroups)
  - 単位 (uom)

> [!NOTE]
> ベンダー グループと単位の最初の同期が、既存のデモ データ セットの一部のレコードで失敗する場合がありました。 Project Operations でのデモデータの使用には支障がないため、この失敗は無視してかまいません。

## <a name="configure-prerequisites-in-dataverse"></a>Dataverse で前提条件を構成する

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>ワークフローをアクティブ化して、ベンダーエンティティに基づくアカウントを作成します

二重書き込みのオーケストレーション ソリューションにより、[ベンダーマスター統合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping) が実現します。 この機能を使用する前提として、**アカウント** エンティティにベンダー データが作成されている必要があります。 [ベンダー デザインの切り替え](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch) で解説されているように、**アカウント** テーブルにベンダーを作成するテンプレート ワークフロー プロセスを有効にします。

### <a name="set-products-to-be-created-as-active"></a>作成する製品をアクティブに設定する

在庫のない材料については、Finance で **発売済み商品** として構成する必要があります。 二重書き込みオーケストレーション ソリューションは、既成の[Dataverse 製品カタログへのリリース製品の統合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping)を提供します。 既定では、Finance の製品はドラフト状態で Dataverse に同期されます。 製品をアクティブな状態に同期して、材料使用のドキュメントやベンダーの保留中の請求書に直接使用できるようにするには、**システム** > **管理** > **システム管理** > **システム設定** にアクセスし、**営業** タブで、**アクティブな状態で製品を作成する** を **はい** に設定します。

## <a name="configure-prerequisites-in-finance"></a>Finance で前提条件を構成する

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>保留中のベンダー請求書の機能キーを有効にする

保留中のベンダーの請求書行にプロジェクトの詳細を追加する機能を有効にするには、次の手順を実行してください。

1. Finance で、**機能管理** ワークスペースに移動します。
2. 機能のリストで、**リソースベース/在庫のないシナリオの Project Operations で保留中のベンダー請求書を有効にする** 機能を選択し、**有効にする** を選択します。

### <a name="define-category-groups-and-project-categories-for-items"></a>項目のカテゴリ グループとプロジェクト カテゴリを定義する

**項目** トランザクション タイプに少なくとも 1 つのカテゴリー グループを設定し、このグループを使用して少なくとも 1 つのプロジェクト カテゴリーを設定します。 詳細については、[プロジェクト　カテゴリの構成](../project-accounting/configure-project-categories.md#category-groups) を参照してください。

プロジェクトのコストと収益のプロファイルを確認し、項目のトランザクションの元帳転記設定を行います。 詳細については、[請求可能なプロジェクトの会計を構成する](../project-accounting/configure-accounting-billable-projects.md) を参照してください。

### <a name="set-up-a-write-in-product"></a>書き込み式の製品を設定する

Project Operations では、リリースされた製品カタログに設定されているカタログ製品や、書き込み式の製品について、材料の見積もりや使用量を記録することができます。 書き込み式の製品を使用するには、この目的のために Finance で構成された単一のリリース済みの製品が必要です。 書き込み式の製品を構成するには、次の手順を実行します。 リソース/在庫のないシナリオで Project Operations を使用している各法人で、これらの手順を繰り返します。

1. Finance で、**製品情報管理** > **製品** > **リリース済製品** に移動し、**新規** を選択します。
2. **製品タイプ** フィールドで、**項目** を選択し、**製品のサブタイプ** フィールドで、**製品** を選択します。
3. 製品番号 (WRITEIN) と製品名 (書き込み式の製品) を入力します。
4. 項目のモデル グループを選択します。 選択した項目モデルのグループで、**在庫ポリシーの「在庫あり」製品** フィールドが **False** に設定されていることを確認してください。
5. **項目グループ**、**ストレージ ディメンション グループ**、**ディメンショングループの追跡** フィールドの値を選択します。 **ストレージ ディメンション** は **サイト** にのみ使用します。**トラッキング ディメンション** フィールドには、**無し** を選択します。
6. **在庫単位**、**購入ユニット**、**販売単位** フィールドの値を選択し、変更を保存します。
7. **予定** タブで、既定の順序設定を行い、**在庫** タブで、既定のサイトとウェアハウスを設定します。
8. **プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメータ** に移動し、**Dynamics 365 Dataverse の Project Operations** を開きます。 
9. **材料** タブ、**書き込み式の製品** フィールドで、作成した製品を選択します。
10. ご利用の Dataverse 環境のサイトマップで、**製品** エンティティを開き、書き込み式製品レコードを見つけます。 
11. レコードの詳細を開き、製品の状態を **引退** に設定します。 この製品の状態は、誤ってこのレコードを材料の見積もりや使用率の文書に直接使用することを防ぎます。

### <a name="set-up-a-procurement-integration-account"></a>調達の統合勘定を設定する

調達統合勘定は、プロジェクトに帰属する明細を含む保留中のベンダー請求書を転記する際の決済勘定として使用されます。

保留中のベンダーの請求書をシステムが転記をする際、この勘定がプロジェクトの原価額に使用されます。 ベンダーの請求書の詳細は Dataverse で処理されます、そして対応するプロジェクト実績が作成されます。 プロジェクトの実績からの情報は、Project Operations の統合仕訳帳に追加されます。 統合仕訳帳を転記すると、調達統合勘定から金額が消去され、プロジェクト原価に計上されます。

1. 調達統合勘定を設定するには、**プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメータ** に移動し、**Dynamics 365 Dataverse の Project Operations** を開きます。 
2. **材料** タブを選択し、**調達統合アカウント** フィールドで値を選択します。

#### <a name="set-up-project-category-defaults-for-an-item"></a>品目のプロジェクト カテゴリの既定を設定する

1. Finance で、**プロジェクト管理と会計** > **設定** > **プロジェクト管理と会計パラメータ** に移動し、**Dynamics 365 Dataverse の Project Operations** を開きます。 
2. **プロジェクト カテゴリの既定** タブの、**項目** フィールドで、値を選択します。 このプロジェクトカテゴリは、プロジェクト実績レコードにプロジェクトカテゴリが設定されていない場合に、材料のトランザクションに使用されます。
