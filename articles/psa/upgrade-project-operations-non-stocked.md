---
title: Project Service Automation から Project Operations へのアップグレード
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Project Operations へのアップグレードのプロセスの概要について説明します。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626718"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation から Project Operations へのアップグレード

今回は、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Project Operations へのアップグレードの 3 つのフェーズのうち、最初のフェーズを発表いたします。 このトピックでは、このエキサイティングな旅に出ようとしている顧客のみなさんに概要を説明します。 今後は、開発者向けの考慮事項や機能拡張の詳細などを紹介する予定です。 Project Operations へのアップグレードの準備に役立つガイダンスを提供するだけでなく、アップグレード後に何が期待できるかについても説明します。

アップグレード配信プログラムは、3 つのフェーズに分かれます。

| アップグレードの出荷 | フェーズ 1 (2022 年 1 月) | フェーズ 2 (2022 年 4 月のリリースサイクル) | フェーズ 3  |
|------------------|------------------------|---------------------------|---------------------------|
| プロジェクトの WBS (Work Breakdown Structure、作業分解構造) に依存しません | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations の現在サポートされている制限内の WBS | | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client のサポートを含む、Project Operations が現在サポートしている範囲外の WBS | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>プロセスのアップグレード機能 

アップグレードプロセスの一環として、サイトマップにアップグレード ログを追加し、管理者がより簡単に不具合を診断できるようになっています。 新しいインターフェースに加えて、アップグレード後のデータの整合性を確保する新しい検証ルールが追加されます。 アップグレードの際に、以下の検証が追加されます。

| 検証 | フェーズ 1 (2022 年 1 月) | フェーズ 2 (2022 年 4 月のリリースサイクル) | フェーズ 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS は、一般的なデータの整合性違反に対して検証されます (同じ親タスクに関連付けられているが、親プロジェクトが異なるリソースの割り当てなど)。 | | :heavy_check_mark: | :heavy_check_mark: |
| WBS は、[Project for the Web の既知の制限](/project-for-the-web/project-for-the-web-limits-and-boundaries)に対して検証されます。 | | :heavy_check_mark: | :heavy_check_mark: |
| WBS は、Project desktop client の既知の制限に対して検証されます。 | |  | :heavy_check_mark: |
| 予約可能なリソースとプロジェクトのカレンダーは、共通の互換性のないカレンダー ルールの例外に対して評価されます。 | | :heavy_check_mark: | :heavy_check_mark: |

フェーズ2では、Project Operations にアップグレードした顧客は、既存のプロジェクトがプロジェクト計画で使用する読み取り専用のエクスペリエンスにアップグレードされます。 この読み取り専用のエクスペリエンスでは、WBS の全容が追跡グリッドに表示されます。 WBS を編集するには、プロジェクトマネージャーはメインの **プロジェクト** ページで **変換** を選択します。 バックグラウンド プロセスでプロジェクトが更新され、Project for the Web の新しいプロジェクト スケジューリング機能がサポートされます。 このフェーズは、[ Project for the Web の既知の制限](/project-for-the-web/project-for-the-web-limits-and-boundaries) に該当するプロジェクトをご利用の顧客に適しています。

フェーズ 3 では、引き続きプロジェクトの編集を希望される顧客にむけて、Project desktop client のサポートが追加されます。 ただし、既存のプロジェクトが新しい Project for the Web エクスペリエンスに変換された場合は、変換されたプロジェクトごとにアドインへのアクセスが無効になります。

## <a name="prerequisites"></a>前提条件

フェーズ 1 アップグレードの対象となるには、顧客は次の基準を満たしている必要があります:

- 対象となる環境には、**msdyn_projecttask** エンティティのレコードが含まれている必要があります。
- 有効な Project Operations ライセンスが、顧客のすべてのアクティブ ユーザーに割り当てられている必要があります。 
- 顧客は、本番データと整合性のある代表的なデータセットがある少なくとも 1 つの非本番環境で、アップグレード プロセスを検証する必要があります。
- 対象となる環境は、Project Service Automation のアプデート リリース 41 (3.10.62.162) 以降にアップデートする必要があります。

フェーズ 2 およびフェーズ 3 の前提条件は、一般公開日が近づくにつれて更新されます。

## <a name="licensing"></a>ライセンス

Project Service Automation のアクティブなライセンスをご利用の場合は、Project Service Automation のすべての機能を備えた Project Operations をインストールして使用することができます。 このようにして、本番環境で Project Service Automation を継続して使い続けながら、Project Operations の機能をテストすることができます。 Project Service Automation のライセンスが終了すると、Project Operations に移行する必要があります。 この移行を計画する際には、Project Operations ライセンスには Project Service Automation ライセンスが含まれていないことを考慮する必要があります。

## <a name="testing-and-refactoring-customizations"></a>カスタマイズのテストとリファクタリング

まず始めに、すべてのカスタマイズをクリーンな Project Operations (lite) 環境にインポートし、インポートが成功し、ビジネスオペレーションが期待通りに動作することを確認します。

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

    > [!NOTE]
    > 環境のデータ量によっては、アップグレードに数時間かかる場合があります。 アップグレードを管理しているコアチームは、状況に応じて計画を立て、非業務時間中にアップグレードを実行する必要があります。 場合によっては、データ量が多い場合は、週末にアップグレードを実行する必要があります。 スケジュール設定に関する決定は、下位環境でのテスト結果に基づいて実施する必要があります。

3. 必要に応じてカスタム ソリューションをアップグレードします。 この時点で、このトピックの[カスタマイズのテストとリファクタリング](#testing-and-refactoring-customizations) セクションでカスタマイズした内容を展開します。
4. **設定**\>**ソリューション** にアクセスし、**Project Operations の非推奨コンポーネント** ソリューションを選択してアンインストールします。

    このソリューションは、アップグレード時に存在する既存のデータ モデルとコンポーネントを保持する一時的なソリューションです。 このソリューションを削除することで、使用されなくなったフィールドやコンポーネントをすべて削除します。 そうすることで、インターフェースを簡素化し、統合や拡張を容易にすることができます。
    
### <a name="validate-common-scenarios"></a>一般的なシナリオの検証

特定のカスタマイズを検証するときは、アプリケーション全体でサポートされているビジネス プロセスも確認することをお勧めします。 これらのビジネス プロセスには、見積もりや契約などの販売エンティティの作成、WBS と実績の承認を含むプロジェクトの作成が含まれますが、これらに限定されません。

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation と Project Operations の主な違い

このセクションでは、Project Service Automation と Project Operations の間での主な変更点をまとめています。

### <a name="project-planning"></a>プロジェクト計画

Project Operations のプロジェクト計画機能は、クライアント サイドのロジックとサーバー サイドのロジックの組み合わせに依存しなくなりました。 その代わり、Project Operations では Project for the Web をスケジューリング エンジンとして使用しています。 このスケジュール機能の変更により、ボード ビューやガント ビュー、リソース主導の計画、[タスク チェックリスト項目](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)、プロジェクト スケジューリング モードなどの新機能が追加されました。 また、新しいスケジューリング機能は、豊富な[アプリケーション プログラミング インターフェース (API)](../project-management/schedule-api-preview.md) でサポートされています。 これらの API は、WBS のエンティティを作成、更新、または削除するプログラム操作が、スケジュールの計算フィールドを破壊しないようにすることを目的としています。

## <a name="billing-and-pricing"></a>請求および価格設定

Project Operations への継続的な投資の一環として、請求と価格にいくつかの新機能が追加されました。 次に例をいくつか示します。

- [プロジェクトやプロジェクトのタスクにおける資材の使用状況の記録](../material/material-usage-log.md)
- [外注管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [前払いおよび着手金ベースの契約](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [上限と検証へのコンタクト](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- タスクベースの請求

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>現在、アップグレードがサポートされている展開の種類は何ですか？

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite の展開                        | サポート対象               |
| Dynamics 365 Finance プロジェクト管理および会計 | Project Operations Lite の展開                        | 現在のサポートされていません |
| ファイナンス プロジェクト マネジメントと会計              | リソース/非在庫のシナリオ向け Project Operations     | 現在のサポートされていません |
| ファイナンス プロジェクト マネジメントと会計              | 在庫/製造指示のシナリオ向け Project Operations | 現在のサポートされていません |
| Project Service Automation 3.x                         | リソース/非在庫のシナリオ向け Project Operations     | 現在のサポートされていません |
| Project for the Web (専用環境)            | Project Operations Lite の展開                        | 現在のサポートされていません |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>アップグレードツールが利用可能になる前に Project Operations をインストールするにはどうすればよいですか？

アップグレードツールが利用可能になる前に Project Operations をインストールするには、2つのオプションがあります:

- 新しい環境をプロビジョニングする。
- Project Service Automation が導入されていない営業組織には、Project Operations を別途導入します。

> [!NOTE]
> 組織に Project Service Automation がインストールされていても、使用されていない場合は、アンインストールできます。 Project Service Automation を完全に削除すると、同じ組織に Project Operations をインストールできるようになります。
