---
title: Project Service Automation から Project Operations へのアップグレード
description: この記事では、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Project Operations へのアップグレードのプロセスの概要について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736672"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation から Project Operations へのアップグレード

Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Project Operations へのアップグレードの 3 つのフェーズのうち、2 番目のフェーズについてお知らせします。 この記事では、このエキサイティングな旅に出ようとしている顧客のみなさんに概要を提供します。 

アップグレード配信プログラムは、3 つのフェーズに分かれています。

| アップグレードの出荷 | フェーズ 1 (2022 年 1 月) | フェーズ 2 (2022 年 11 月) | フェーズ 3 (2023 年 4 月のリリースサイクル)  |
|------------------|------------------------|---------------------------|---------------------------|
| プロジェクトの WBS (Work Breakdown Structure、作業分解構造) に依存しません | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations の現在サポートされている制限内の WBS | | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client のサポートを含む、Project Operations が現在サポートしている範囲外の WBS | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>プロセスのアップグレード機能 

アップグレードプロセスの一環として、サイト マップにアップグレード ログを追加し、管理者がより簡単に不具合を診断できるようにしました。 新しいインターフェースに加えて、アップグレード後のデータの整合性を確保する新しい検証ルールが追加されます。 アップグレードの際に、以下の検証が追加されます。

| 検証 | フェーズ 1 (2022 年 1 月) | フェーズ 2 (2022 年 11 月) | フェーズ 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS は、一般的なデータの整合性違反に対して検証されます (同じ親タスクに関連付けられているが、親プロジェクトが異なるリソースの割り当てなど)。 | | :heavy_check_mark: | :heavy_check_mark: |
| WBS は、[Project for the Web の既知の制限](/project-for-the-web/project-for-the-web-limits-and-boundaries)に対して検証されます。 | | :heavy_check_mark: | :heavy_check_mark: |
| WBS は、Project desktop client の既知の制限に対して検証されます。 | |  | :heavy_check_mark: |
| 予約可能なリソースとプロジェクトのカレンダーは、共通の互換性のないカレンダー ルールの例外に対して評価されます。 | | :heavy_check_mark: | :heavy_check_mark: |

フェーズ2では、Project Operations にアップグレードした顧客は、既存のプロジェクトがプロジェクト計画で使用する読み取り専用のエクスペリエンスにアップグレードされます。 この読み取り専用のエクスペリエンスでは、WBS の全容が追跡グリッドに表示されます。 WBS を編集するには、プロジェクト マネージャーがプロジェクトのメイン ページで [**変換**](/PSA-Upgrade-Project-Conversion.md) を選択します。 その後、バックグラウンド プロセスでプロジェクトが更新され、Project for the Web の新しいプロジェクト スケジュール エクスペリエンスがサポートされます。 このフェーズは、[ Project for the Web の既知の制限](/project-for-the-web/project-for-the-web-limits-and-boundaries) に該当するプロジェクトをご利用の顧客に適しています。

フェーズ 3 では、引き続きプロジェクトの編集を希望される顧客にむけて、Project desktop client のサポートが追加されます。 ただし、既存のプロジェクトが新しい Project for the Web エクスペリエンスに変換された場合は、変換されたプロジェクトごとにアドインへのアクセスが無効になります。

## <a name="prerequisites"></a>前提条件

フェーズ 1 アップグレードの対象となるには、次の基準を満たしている必要があります:

- 対象となる環境には、**msdyn_projecttask** エンティティのレコードが含まれている必要があります。
- 有効な Project Operations ライセンスが、すべてのアクティブ ユーザーに割り当てられている必要があります。 
- 運用環境と整合性のある代表的なデータセットを含む、少なくとも 1 つの非運用環境で、アップグレード プロセスを検証する必要があります。
- 対象となる環境は、Project Service Automation のアプデート リリース 37 (V3.10.58.120) 以降にアップデートする必要があります。

フェーズ 2 アップグレードの対象となるには、次の基準を満たしている必要があります:

- 有効な Project Operations ライセンスが、すべてのアクティブ ユーザーに割り当てられている必要があります。 
- 運用環境と整合性のある代表的なデータセットを含む、少なくとも 1 つの非運用環境で、アップグレード プロセスを検証する必要があります。
- 対象となる環境は、Project Service Automation のアプデート リリース 37 (V3.10.58.120) 以降にアップデートする必要があります。
- タスク (msdyn_projecttask) を含む環境は、プロジェクトあたりのタスクの総数が 500 以下の場合にのみサポートされます。

フェーズ 3 の前提条件は、一般提供日が近づくにつれて更新されます。

## <a name="licensing"></a>ライセンス

Project Service Automation のアクティブなライセンスをご利用の場合は、Project Service Automation のすべての機能を備えた Project Operations をインストールして使用することができます。 このようにして、本番環境で Project Service Automation を継続して使い続けながら、Project Operations の機能をテストすることができます。 Project Service Automation のライセンスが終了すると、Project Operations に移行する必要があります。 この移行を計画する際には、Project Operations ライセンスには Project Service Automation ライセンスが含まれていないことを考慮する必要があります。 Project Service Automation を展開し、Project Operations への移行を計画している間も、PSA のライセンスを継続して使用または増やす必要があるシナリオをお持ちのお客様は、Project Operations の購入ライセンスに基づいて一時的な PSA ライセンスを要求できます。 1 つの Project Operations ライセンスに対して 1 つの Project Service Automation ライセンスが発行されます。 一時的な PSA ライセンスは、このリンクを使用して要求できます: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>カスタマイズのテストとリファクタリング

まず始めに、すべてのカスタマイズをクリーンな Project Operations (Lite) 環境にインポートし、インポートが正常に行われ、ビジネス オペレーションが期待通りに動作することを確認します。

ここでは、その注意点をご紹介します:

- 依存関係がないため、インポートに失敗することがあります。 つまり、Project Operations で削除されたフィールドやその他のコンポーネントを参照するカスタマイズです。 この場合、開発環境からこれらの依存関係を削除してください。
- アンマネージド ソリューションや管理ソリューションにカスタマイズされていないコンポーネントが含まれている場合は、それらのコンポーネントをソリューションから削除します。 たとえば、カスタマイズする場合 **プロジェクト** エンティティの場合、ソリューションにエンティティ ヘッダーのみを追加します。 すべてのフィールドを追加する必要はありません。 以前にすべてのサブコンポーネントを追加していた場合は、手動で新しいソリューションを作成し、関連するコンポーネントを追加する必要がある場合があります。
- フォームとビューが予期されたようには表示されない場合があります。 状況によっては、初期設定のフォームやビューをカスタマイズした場合、そのカスタマイズによって Project Operations の新しいアップデートが有効にならない場合があります。 これらの問題を確認するためには、Project Operations のクリーン インストールと、カスタマイズした内容を含む Project Operations のインストールを並べて確認することをお勧めします。 ビジネスで最も一般的に使用されているフォームを比較して、フォームのバージョンがまだ意味をなし、フォームのクリーンバージョンから何かが欠落していないことを確認します。 カスタマイズしたビューについても、同じように並べて確認してみましょう。
- ビジネスロジックが実行時に失敗する可能性があります。 プラグインのフィールドへの参照はインポート時に検証されないため、既に存在しないフィールドへの参照が原因でビジネスロジックが失敗し、次のようなエラーメッセージが表示される場合があります:「'Project' entity doesn't contain attribute with Name = 'msdyn_plannedhours' and NameMapping = 'Logical'.」 この場合は、新しいフィールドを使用するようにカスタマイズを修正してください。 プラグインのロジックで自動生成されたプロキシ クラスや強力な型参照を使用している場合は、クリーン インストールからプロキシを再生成することを検討してください。 このようにして、プラグインが非推奨のフィールドに依存しているすべての場所を簡単に特定することができます。

カスタマイズを更新して Project Operations をクリーンにインポートできたら、次のステップに進みます。

## <a name="end-to-end-testing-in-development-environments"></a>開発環境でのエンド ツー エンド テスト

### <a name="initiate-upgrade"></a>アップグレードを開始する 

1. Power Platform で、 管理センターとご利用の環境を選択します。 続いて、アプリケーションで、**Dynamics 365 Project Operations** を見つけて選択します。
2. **インストール** を選択して、アップグレードを開始します。 Power Platform 管理センターは、このインストールを新規インストールとして表示します。 ただし、以前のバージョンの Project Service Automation の存在が検出され、既存のインストールがアップグレードされます。

    アップグレードが完了すると、環境に Project Operations がインストールされており、Project Service Automation がインストールされていないことが表示されます。

    環境のデータ量によっては、アップグレードに数時間かかる場合があります。 アップグレードを管理しているコアチームは、状況に応じて計画を立て、非業務時間中にアップグレードを実行する必要があります。 場合によっては、データ量が多い場合は、週末にアップグレードを実行する必要があります。 スケジュール設定に関する決定は、下位環境でのテスト結果に基づいて実施する必要があります。

3. 必要に応じてカスタム ソリューションをアップグレードします。 この時点では、この記事の [カスタマイズのテストとリファクタリング](#testing-and-refactoring-customizations) セクションでカスタマイズした内容を展開します。
4. **make.powerapps.com** に移動し、ポータルの右上にあるドロップ ダウンから環境を選択し、左側のメニューから **ソリューション** を選択し、**Project Operations 非推奨のコンポーネント** ソリューションと **アンインストール** を選択します。

    このソリューションは、アップグレード時に存在する既存のデータ モデルとコンポーネントを保持する一時的なソリューションです。 このソリューションを削除することで、使用されなくなったフィールドやコンポーネントをすべて削除します。 そうすることで、インターフェースを簡素化し、統合や拡張を容易にすることができます。
    
### <a name="upgrade-to-project-operations-lite"></a>Project Operations Lite へのアップグレード

次の手順では、アップグレード プロセスと関連するエラー ログについて説明します:

1. **PSA バージョン チェック:** Project Operations をインストールするには、V3.10.58.120 以上が必要です。
1. **事前検証:** 管理者がアップグレードを開始すると、システムは Project Operations ソリューションの中核である各エンティティに対して事前検証操作を実行します。 このステップでは、すべてのエンティティ参照が有効であることを確認し、WBS に関連するデータが Project for the Web の公開された制限内にあることを確認します。
1. **メタデータのアップグレード:** 事前検証が成功すると、システムはスキーマへの変更を開始し、非推奨のコンポーネント ソリューションを作成します。 必要なカスタマイズのリファクタリングがすべて完了したら、この非推奨のソリューションを削除できます。 このステップは、アップグレード プロセスの中で最も時間がかかり、完了するまでに最大 4 時間かかる場合があります。
1. **データのアップグレード:** メタデータのアップグレード ステップで必要なすべてのスキーマ変更が完了すると、データが新しいスキーマに移行され、必要なデフォルト設定と再計算が行われます。
1. **プロジェクト スケジュール エンジンの更新:** データのアップグレードが成功すると、メイン ページの **スケジュール** タブのラベルが **タスク** に変更されます。 アップグレード後にユーザーがこのタブを選択すると、追跡グリッドに移動して WBS の読み取り専用バージョンを表示するように指示されます。 WBS を編集するには、スケジュール [変換プロセス](/PSA-Upgrade-Project-Conversion.md) を開始する必要があります。 既存の WBS を持たないすべてのプロジェクトは、変換せずに新しいスケジュール エクスペリエンスを直接使用できます。
 
### <a name="validate-common-scenarios"></a>一般的なシナリオの検証

特定のカスタマイズを検証するときは、アプリケーション全体でサポートされているビジネス プロセスも確認することをお勧めします。 これらのビジネス プロセスには、見積もりや契約などの販売エンティティの作成、WBS と実績の承認を含むプロジェクトの作成が含まれますが、これらに限定されません。

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation と Project Operations の主な違い

このセクションでは、Project Service Automation と Project Operations の間での主な変更点をまとめています。

### <a name="project-planning"></a>プロジェクト計画

Project Operations のプロジェクト計画機能は、クライアント サイドのロジックとサーバー サイドのロジックの組み合わせに依存しなくなりました。 その代わり、Project Operations では Project for the Web をスケジューリング エンジンとして使用しています。 このスケジュール機能の変更により、ボード ビューやガント ビュー、リソース主導の計画、[タスク チェックリスト項目](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)、プロジェクト スケジューリング モードなどの新機能が追加されました。 また、新しいスケジューリング機能は、豊富な[アプリケーション プログラミング インターフェース (API)](../project-management/schedule-api-preview.md) でサポートされています。 これらの API は、WBS のエンティティを作成、更新、または削除するプログラム操作が、スケジュールの計算フィールドを破壊しないようにすることを目的としています。

### <a name="billing-and-pricing"></a>請求および価格設定

Project Operations への継続的な投資の一環として、請求と価格にいくつかの新機能が追加されました。 次に例をいくつか示します。

- [プロジェクトやプロジェクトのタスクにおける資材の使用状況の記録](../material/material-usage-log.md)
- [外注管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [前払いおよび着手金ベースの契約](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [上限と検証へのコンタクト](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- タスクベースの請求

### <a name="resource-management"></a>リソース管理

Project Operations は、Universal Resource Scheduling (URS) ボードとスケジュール アシスタントのオプション サポートを提供します。 この新しいエクスペリエンスは、2023 年 4 月サイクルで必須になります。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>現在、アップグレードがサポートされている展開の種類は何ですか？

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite の展開                        | サポート対象               |
| Dynamics 365 Finance プロジェクト管理および会計 | Project Operations Lite の展開                        | 現在のサポートされていません |
| ファイナンス プロジェクト マネジメントと会計              | リソース/非在庫のシナリオ向け Project Operations     | 現在のサポートされていません |
| Project Service Automation 3.x                         | リソース/非在庫のシナリオ向け Project Operations     | 現在のサポートされていません |
| Project for the Web (専用環境)            | Project Operations Lite の展開                        | 現在のサポートされていません |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>アップグレードツールが利用可能になる前に Project Operations をインストールするにはどうすればよいですか？

アップグレードツールが利用可能になる前に Project Operations をインストールするには、2つのオプションがあります:

- 新しい環境をプロビジョニングする。
- Project Service Automation が導入されていない営業組織には、Project Operations を別途導入します。

組織に Project Service Automation がインストールされていても、使用されていない場合は、アンインストールできます。 Project Service Automation を完全に削除すると、同じ組織に Project Operations をインストールできるようになります。
