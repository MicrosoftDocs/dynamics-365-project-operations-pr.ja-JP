---
title: Microsoft Project で作業を計画するための Project Service アドインの使用 | MicrosoftDocs
description: このトピックは、Microsoft Project Service の Microsoft Project アドインを追加、構成、使用する方法について説明します。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129684"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Microsoft Project で作業を計画するための Project Service Automation アドインの使用

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用することで、より簡単に見積もりを含んだプロジェクト計画を実行できるようになります。 最終提案を堤出するために費用、行動および販売額が明確になるように作業を定義できます。  

 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] をインストールして、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の使い慣れた環境で計画している作業を実行することができるようになりました。 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の強力な計画および管理機能を使用して、Project Service Automation のプロジェクト計画を更新します。  

> [!IMPORTANT]
> - SharePoint のドキュメント管理機能を使用して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルを保存するには、 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] の管理者がドキュメント管理を有効にする必要があります。 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] は [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition とのみ互換性があります。  

## <a name="download-and-install-the-add-in"></a>アドインのダウンロードおよびインストール  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のサインイン情報を準備します。 この情報は、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] から [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に接続するために必要です。  

1.  ダウンロード センターからご利用の環境に対応している Project Service のバージョン [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) または [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) のアドインをダウンロードできます。  

2.  ダウンロード リンクをクリックします。  

3.  ダウンロードが完了したら、**はい** をクリックしてアドインをインストールします。  

## <a name="configure-the-add-in"></a>アドインの構成  

1. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を開いて **Project Service** タブをクリックします。  

2. **接続** をクリックします。  

3. サインイン情報を入力して、**サインイン** をクリックします。  

   これで、アドインを使用できるようになります。  

## <a name="read-from-a-template"></a>テンプレートからの読み取り  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作成して [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] にコピーしたテンプレートから読み取り、プロジェクト計画を開始します。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [プロジェクトのテンプレートの作成 (Project Service Automation)](../psa/create-project-template.md)  

1.  **Project Service** タブから、**読み取り** > **Project Service Automation プロジェクト テンプレート** の順にクリックします。  

2.  リストからプロジェクト テンプレートを選択して、**開く** をクリックします。  

    > [!NOTE]
    >  既定では、テンプレートからプロジェクトにコピーされるタスクは、手動で予定するように設定されます。  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>プロジェクトのリソースに [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] のロールを割り当てる  

1.  プロジェクトを開いて、**タスク** リボンをクリックします。  

2.  **ガント チャート** メニューをクリックして、**リソース シート** を選択します。  

3.  リソース シートで、**Project Service のリソース ロール** ドロップダウン メニューをクリックして、Project Service Automation のロールを選択します。  

## <a name="staff-your-project-with-resources"></a>プロジェクトへのリソースの設定  

1.  [Project Service] タブから、行を選択して **リソースの検索** をクリックします。  

2.  **リソースの予約** 画面で、プロジェクトに使用したいリソースを選択します。  

3.  **予約** をクリックし、**OK** をクリックします。  

## <a name="publish-your-project"></a>プロジェクトの公開  
プロジェクト計画が完了した場合、次のステップはプロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートして公開することです。  

プロジェクトを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートします。 価格設定およびチーム生成プロセスが適用されます。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクトを開いて、チーム、プロジェクトの予測および作業分解構造が生成されていることを確認します。 次の表は結果が表示される場所を示します。


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **ガント チャート**   | [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **WBS (作業分解構造)** 画面にインポートします。 |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **シート リソース** |   [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト チーム メンバー** 画面にインポートします。   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **使用状況を使用**    |    [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **プロジェクト見積** 画面にインポートします。     |

**プロジェクトをインポートして公開する**  
1. **Project Service** タブから、**公開** > **新しい Project Service Automation プロジェクト** の順にクリックします。  

2. **Project Service の新しいプロジェクトへの公開** ダイアログ ボックスで、**プロジェクト名** を入力して **顧客** を選択します。  

3. オプションで、**プロジェクト計画を Project Service Automation にリンクする** を選択すると、Project Service Automation に計画プロジェクト ファイルをリンクできます。  

4. **発行** をクリックします。  

   プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で作業分解構造を読み取り専用に設定できます。  プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。  

## <a name="edit-a-project-thats-been-imported"></a>インポートするプロジェクトの編集  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にインポートするプロジェクト計画に変更を加えるには、2 つのオプションがあります。  

- マスター ファイルを開いて [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集します。  

- ファイルをリンク解除して、Project Service で直接編集します。 デフォルトで、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] からアップロードされたプロジェクトはロックされ、プロジェクトでのみ編集することができます。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でファイルを編集するには、ファイルのリンクを解除する必要があります。  

### <a name="edit-in-pn_microsoft_project"></a>[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で編集する  

1. メイン メニューから、**Project Service** > **プロジェクト** の順にクリックします。  

2. プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。  

3. リボンの **MS Project で開く** をクリックします。 これで、リンクされたファイルが [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開きます。  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>ファイルのリンクを切り、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] サービスで編集します。  

1. メイン メニューから、**Project Service** > **プロジェクト** の順にクリックします。  

2. プロジェクトのリストから、[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成したものをオープンします。  

3. リボンの **MS Project からリンク解除する** をクリックします。  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>プロジェクトファイルを SharePoint や Office グループにアップロードする  
 プロジェクト ファイルを SharePoint にアップロードすることが可能で、それは [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクトの [関連ドキュメント] の下に保存されます。  管理者に要請をして SharePoint のドキュメント管理を構成し、プロジェクト エンティティで使用できるように有効化する必要があります。 

 また、Office グループをセットアップ済みの場合は、プロジェクト ファイルを [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] にアップロードすることができます。

### <a name="upload-a-file-for-sharepoint"></a>SharePoint にファイルをアップロードする  

1. メイン メニューから、**Project Service** > **アップロード** の順にクリックします。  

2. **Project Service Automation プロジェクト ドキュメントへ** を選択します。  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開くことを有効にする** ダイアログで、 **はい** または **いいえ** を選択します。  

   - **はい** をクリックすると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** ボタンを選択した際に [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動して SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。  

   - **いいえ** をクリックすると、 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** ボタン のリンクは機能しなくなります。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の **ドキュメント** の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。  

### <a name="upload-a-file-for-office-groups"></a>Office グループ用のファイルのアップロード  

1. メイン メニューから、**Project Service** > **アップロード** の順にクリックします。  

2. **Project Service Automation プロジェクト ドキュメントへ** を選択します。  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開くことを有効にする** ダイアログで、 **はい** または **いいえ** を選択します。  

   - **はい** をクリックすると、Project Service Automation の **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で開く** ボタンを選択した際に [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] を起動して SharePoint ドキュメント ライブラリからプロジェクト ファイルを読み込むことができます。  

   - **いいえ** をクリックすると、 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]で開く** ボタン のリンクは機能しなくなります。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ファイルは、特定の [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] プロジェクト用の **ドキュメント** の下にある [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で見つけることができます。  

## <a name="publish--your-project-as-a-template"></a>テンプレートとしてのプロジェクトの公開  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] でプロジェクト テンプレートとして保存することで、プロジェクトを保存して再使用できます。  プロジェクト テンプレートは、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] で再使用可能なプロジェクト計画です。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [プロジェクトのテンプレートの作成 (Project Service Automation)](../psa/create-project-template.md)  

1. **Project Service** タブから、**公開** > **新しい Project Service Automation プロジェクト テンプレート** の順にクリックします。  

2. **Project Service テンプレートの新しいプロジェクトへの公開** ダイアログ ボックスで、**プロジェクト テンプレート名** を入力します。  

3. また任意で、**プロジェクト 計画を Project Service Automation にリンクする** を選択すると、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にプロジェクト ファイルをリンクします。  

4. **発行** をクリックします。  

プロジェクト ファイルを [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] にリンクすると、プロジェクト ファイルをマスターにして、[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] テンプレートで作業分解構造を読み取り専用に設定できます。  プロジェクト計画への変更を行うためには、それを [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] で作成して [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に更新として公開する必要があります。

### <a name="see-also"></a>関連項目  
 [プロジェクト管理者ガイド](../psa/project-manager-guide.md)
