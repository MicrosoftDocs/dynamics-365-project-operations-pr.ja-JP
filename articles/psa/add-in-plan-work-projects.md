---
title: Project Service アドインを使って Microsoft Project で作業を計画する
description: このトピックは、Microsoft Project Service の Microsoft Project アドインを使用する方法について説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014572"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Project Service アドインを使って Microsoft Project で作業を計画する

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用することで、より簡単に見積もりを含んだプロジェクト計画を実行できるようになります。 最終提案を堤出するために費用、行動および販売額が明確になるように作業を定義できます。  

[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] をインストールして、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の使い慣れた環境で計画作業を実行することができます。 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の強力な計画および管理機能を使用して、Project Service Automation のプロジェクト計画を更新します。  

> [!IMPORTANT]
> - SharePoint のドキュメント管理機能を使用して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルを保存するには、 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の管理者がドキュメント管理を有効にする必要があります。 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] は [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition とのみ互換性があります。  

## <a name="download-and-install-the-add-in"></a>アドインのダウンロードおよびインストール  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のサインイン情報を準備します。 この情報は、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] から [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に接続するために必要です。  

1.  ダウンロード センターからご利用の環境に対応している Project Service のバージョン [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) または [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) のアドインをダウンロードできます。  

2.  選択してリンクをダウンロードします。  

3.  ダウンロードが完了したら、**はい** を選択してアドインをインストールします。  

## <a name="configure-the-add-in"></a>アドインの構成  

1. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を開いて **Project Service** タブを選択します。  

2. **接続** を選択します。  

3. サインイン情報を入力して、**サインイン** を選択します。  

   これで、アドインを使用できるようになります。  

## <a name="read-from-a-template"></a>テンプレートからの読み取り  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作成して [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] にコピーしたテンプレートから読み取り、プロジェクト計画を開始します。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [プロジェクトのテンプレートの作成 (Project Service Automation)](../psa/create-project-template.md)  

1.  **Project Service** タブから、**読み取り** > **Project Service Automation プロジェクト テンプレート** の順に選択します。  

2.  リストからプロジェクト テンプレートを選択して、**開く** を選択します。  

    > [!NOTE]
    >  既定では、テンプレートからプロジェクトにコピーされるタスクは、手動で予定するように設定されます。  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>プロジェクトのリソースに [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のロールを割り当てる  

1.  プロジェクトを開いて、**タスク** リボンを選択します。  

2. **ガント チャート** メニューを選択して、**リソース シート** を選択します。  

3. リソース シートで、**Project Service のリソース ロール** ドロップダウン メニューを選択して、Project Service Automation のロールを選択します。  

## <a name="staff-your-project-with-resources"></a>プロジェクトへのリソースの設定  

1.  [Project Service] タブから、行を選択して **リソースの検索** を選択します。  

2.  **リソースの予約** 画面で、プロジェクトに使用したいリソースを選択します。  

3.  **予約** を選び、**OK** を選択します。  

## <a name="publish-your-project"></a>プロジェクトの公開  
プロジェクト計画が完了した場合、次のステップはプロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートして公開することです。  

プロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートします。 価格設定およびチーム生成プロセスが適用されます。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクトを開いて、チーム、プロジェクトの見積もり、作業分解構造が生成済みなことを確認します。 次の表は結果が表示される場所を示します。


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **ガント チャート**   | [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **WBS (作業分解構造)** 画面にインポートします。 |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **シート リソース** |   [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト チーム メンバー** 画面にインポートします。   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **使用状況を使用**    |    [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト見積** 画面にインポートします。     |

**プロジェクトをインポートして公開する**  
1. **Project Service** タブで、**公開** > **新しい Project Service Automation プロジェクト** に移動します。  

2. **Project Service の新しいプロジェクトへの公開** ダイアログ ボックスで、**プロジェクト名** を入力して **顧客** を選択します。  

3. オプションで、**プロジェクト計画を Project Service Automation にリンクする** を選択して、Project Service Automation に計画プロジェクト ファイルをリンクします。  

4. **公開** を選択します。  

   プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作業分解構造を読み取り専用に設定できます。  プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。  

## <a name="edit-a-project-thats-been-imported"></a>インポートするプロジェクトの編集  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートするプロジェクト計画に変更を加えるには、2 つのオプションがあります。  

- マスター ファイルを開いて [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集します。  

- ファイルをリンク解除して、Project Service で直接編集します。 デフォルトで、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] からアップロードされたプロジェクトはロックされ、プロジェクトでのみ編集することができます。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でファイルを編集するには、ファイルのリンクを解除する必要があります。  

### <a name="edit-in-pn_microsoft_project"></a>[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集する  

1. メイン メニューで、**Project Service** > **プロジェクト** に移動します。  

2. プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。  

3. リボンの **MS Project で開く** を選択します。 これで、リンクされたファイルが [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開きます。  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>ファイルのリンクを切り、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] サービスで編集します。  

1. メイン メニューで、**Project Service** > **プロジェクト** に移動します。  

2. プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。  

3. リボンの **MS Project からリンク解除する** を選択します。  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>プロジェクトファイルを SharePoint や Office グループにアップロードする  
 プロジェクト ファイルを SharePoint にアップロードすることが可能で、それは [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [関連ドキュメント] の下に保存されます。  管理者に要請をして SharePoint のドキュメント管理を構成し、プロジェクト エンティティで使用できるように有効化する必要があります。 

 また、Office グループをセットアップ済みの場合は、プロジェクト ファイルを [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] にアップロードすることができます。

### <a name="upload-a-file-for-sharepoint"></a>SharePoint にファイルをアップロードする  

1. メイン メニューで、**Project Service** > **アップロード** に移動します。  

2. **Project Service Automation プロジェクト ドキュメントへ** を選択します。  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開くことを有効にする** ダイアログ ボックスで、**はい** または **いいえ** を選択します。  

   - **はい** を選択すると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** を選択して、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動し、SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。  

   - **いいえ** を選択した場合、**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** のリンクは機能しません。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の **ドキュメント** の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。  

### <a name="upload-a-file-for-office-groups"></a>Office グループ用のファイルのアップロード  

1. メイン メニューで、**Project Service** > **アップロード** に移動します。  

2. **Project Service Automation プロジェクト ドキュメントへ** を選択します。  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開くことを有効にする** ダイアログ ボックスで、**はい** または **いいえ** を選択します。  

   - **はい** を選択すると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** を選択して、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動し、SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。  

   - **いいえ** を選択した場合、**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** のリンクは機能しません。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の **ドキュメント** の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。  

## <a name="publish--your-project-as-a-template"></a>テンプレートとしてのプロジェクトの公開  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクト テンプレートとして保存することで、プロジェクトを保存して再使用できます。 プロジェクト テンプレートは、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で再使用可能なプロジェクト計画です。 詳細については、[プロジェクト テンプレートの作成 (Project Service Automation)](../psa/create-project-template.md) を参照してください。 

1. **Project Service** タブで、**公開** > **新しい Project Service Automation プロジェクト テンプレート** に移動します。  

2. **Project Service テンプレートの新しいプロジェクトへの公開** ダイアログ ボックスで、**プロジェクト テンプレート名** を入力します。  

3. オプションで、**プロジェクト計画を Project Service Automation にリンクする** を選択すると、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にプロジェクト ファイルをリンクできます。  

4. **公開** を選択します。  

プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] テンプレートで作業分解構造を読み取り専用に設定できます。  プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。

## <a name="read-a-resource-loaded-schedule"></a>リソースをロードしたスケジュールを読む

Project Service Automation のプロジェクトを読み取る際に、リソースのカレンダーをデスクトップ クライアントに同期しません。 タスクの期間、労力、終了に違いがある場合、リソースとデスクトップ クライアントで、同じ勤務時間テンプレート カレンダーをプロジェクトに適用していないことが原因である可能性があります。


## <a name="data-synchronization"></a>データの同期
このセクションのテーブルは、Project Service Automation と Microsoft Project デスクトップ アドイン間のエンティティデータの同期に関する情報を提供します。

### <a name="project-task-entity-table"></a>プロジェクト タスク エンティティ テーブル
次のテーブルは、Project Service Automation と Microsoft Project デスクトップ アドインの間で Project Task エンティティ データを同期する方法の概要を示します。

| **エンティティ** | **フィールド** | **Microsoft Project から Project Service Automation へ** | **Project Service Automation から Microsoft Project へ** |
| --- | --- | --- | --- |
| プロジェクト タスク | 期日 | 同期 | 非同期 |
| プロジェクト タスク | 推定工数 | 同期 | 非同期 |
| プロジェクト タスク | MS Project クライアント ID | 同期 | 非同期 |
| プロジェクト タスク | 親タスク | 同期 | 非同期 |
| プロジェクト タスク | Project | 同期 | 非同期 |
| プロジェクト タスク | プロジェクト タスク | 同期 | 非同期 |
| プロジェクト タスク | プロジェクト タスク名 | 同期 | 非同期 |
| プロジェクト タスク | リソース単位 (v3.0 で廃止) | 同期 | 非同期 |
| プロジェクト タスク | スケジュールされた期間 | 同期 | 非同期 |
| プロジェクト タスク | 開始日 | 同期 | 非同期 |
| プロジェクト タスク | WBS ID | 同期 | 非同期 |

### <a name="team-member-entity-table"></a>チーム メンバー エンティティ テーブル
次の表は、Project Service Automation と Micro の間でチーム メンバー エンティティ データを同期する方法の概要を示します。

| **エンティティ** | **フィールド** | **Microsoft Project から Project Service Automation へ** | **Project Service Automation から Microsoft Project へ** |
| --- | --- | --- | --- |
| チーム メンバー | MS Project クライアント ID | 同期 | 非同期 |
| チーム メンバー | ポジション名 | 同期 | 非同期 |
| チーム メンバー | プロジェクト | 同期 | 同期 |
| チーム メンバー | プロジェクト チームです | 同期 | 同期 |
| チーム メンバー | リソース単位 | 非同期 | 同期 |
| チーム メンバー | ロール | 非同期 | 同期 |
| チーム メンバー | 作業時間 | 非同期 | 非同期 |

### <a name="resource-assignment-entity-table"></a>リソース割り当てエンティティ テーブル
次の表は、Project Service Automation と Micro の間でリソース割当エンティティ データを同期する方法の概要を示します。

| **エンティティ** | **フィールド** | **Microsoft Project から Project Service Automation へ** | **Project Service Automation から Microsoft Project へ** |
| --- | --- | --- | --- |
| リソース割り当て | 開始日 | 同期 | 非同期 |
| リソース割り当て | 時間 | 同期 | 非同期 |
| リソース割り当て | MS Project クライアント ID | 同期 | 非同期 |
| リソース割り当て | 予定作業 | 同期 | 非同期 |
| リソース割り当て | Project | 同期 | 非同期 |
| リソース割り当て | プロジェクト チームです | 同期 | 非同期 |
| リソース割り当て | リソース割り当て | 同期 | 非同期 |
| リソース割り当て | タスク​ | 同期 | 非同期 |
| リソース割り当て | 終了日 | 同期 | 非同期 |

### <a name="project-task-dependencies-entity-table"></a>プロジェクト タスク依存関係エンティティ テーブル
次の表は、Project Service Automation と Micro の間でプロジェクト タスク依存関係エンティティ データを同期する方法の概要を示します。

| **エンティティ** | **フィールド** | **Microsoft Project から Project Service Automation へ** | **Project Service Automation から Microsoft Project へ** |
| --- | --- | --- | --- |
| プロジェクト タスクの依存関係 | プロジェクト タスクの依存関係 | 同期 | 非同期 |
| プロジェクト タスクの依存関係 | リンクの種類 | 同期 | 非同期 |
| プロジェクト タスクの依存関係 | 前任のタスク | 同期 | 非同期 |
| プロジェクト タスクの依存関係 | Project | 同期 | 非同期 |
| プロジェクト タスクの依存関係 | 後継のタスク | 同期 | 非同期 |

### <a name="additional-resources"></a>その他のリソース
 [プロジェクト管理者ガイド](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]