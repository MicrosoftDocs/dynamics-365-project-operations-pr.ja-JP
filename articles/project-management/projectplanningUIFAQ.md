---
title: タスク グリッドでの作業のトラブルシューティング
description: このトピックでは、タスク グリッドで作業するときに必要なトラブルシューティング情報を提供します。
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: ee80363cf6f9a65a91be43a84434d37f02511f26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596424"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>タスク グリッドでの作業のトラブルシューティング 


_**適用対象:** リソース/非在庫ベースのシナリオの Project Operations、ライト展開 - 見積もり請求の取引、Project for the Web_

Dynamics 365 Project Operations によって活用されるタスク グリッドは、Microsoft Dataverse 内でホストされている iFrame です。 この使用の結果として、認証と認証が正しく機能していることを確認するには、特定の要件を満たす必要があります。 このトピックは、グリッドをレンダリングしたり、作業分解図 (WBS) でタスクを管理したりする機能に影響を与える可能性のある一般的な問題の概要を示しています。

一般的な問題: 

- タスク グリッド上の **タスク** タブは空です。
- プロジェクトを開くと、プロジェクトが読み込まれず、ユーザー インターフェイス (UI) がスピナーでスタックします。
- **Project for the Web** の特権の管理。
- タスクを作成、更新、または削除しても、変更は保存されません。

## <a name="issue-the-task-tab-is-empty"></a>問題: [タスク] タブが空です

### <a name="mitigation-1-enable-cookies"></a>軽減策 1: Cookie を有効にする

Project Operations では、作業分解図をレンダリングするためにサードパーティの Cookie を有効にする必要があります。 サードパーティの Cookie が有効になっていない場合、**プロジェクト** ページの **タスク** タブを選択するとタスクではなく空白のページが表示されます。

Microsoft Edge または Google Chrome ブラウザの場合、次の手順でブラウザの設定を更新してサードパーティの Cookie を有効にします。

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Edge ブラウザーを開きます。
2. 右上隅で、 **省略記号** (...) を選択してから **設定** を選択します。
3. **Cookie とサイトの許可** の下で、**Cookie とサイト データ** を選択します。
4. **サードパーティの Cookie をブロックする** をオフにします。
5. ブラウザーを最新の情報に更新します。 

#### <a name="google-chrome"></a>Google Chrome

1. Chrome ブラウザーを開きます。
2. 右上の歯車アイコンを選択して、3 つの縦のドットを選択してから **設定** を選択します。
3. **プライバシーとセキュリティ** の下で、**Cookie とその他のサイト データ** を選択します。
4. **すべての Cookie を許可する** を選択します。
5. ブラウザーを最新の情報に更新します。 

> [!NOTE]
> サードパーティの Cookie をブロックすると、そのサイトが例外リストで許可されている場合でも、他のサイトのすべての Cookie とサイト データがブロックされます。

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>軽減策 2: PEX エンドポイントが正しく構成されていることを確認します

Project Operations では、プロジェクト パラメーターが PEX エンドポイントを参照する必要があります。 このエンドポイントは、WBS (作業分解構造) をレンダリングするために使用されるサービスと通信するために必要です。 パラメーターが有効になっていない場合、「プロジェクト パラメーターが無効です」というエラーが表示されます。 PEX エンドポイントを更新するには、それぞれについて次の手順を実行します。

1. **PEX エンドポイント** フィールドを **プロジェクト パラメーター** ページに追加します。
2. 使用している製品タイプを特定します。 この値は、PEX エンドポイントが設定されている場合に使用されます。 取得時に、製品タイプは PEX エンドポイントですでに定義されています。 その値を維持します。
3. 以下の値でフィールドを更新する: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`。 次の表に、製品タイプに基づいて使用する必要があるタイプ パラメーターを示します。

      | **製品の種類**                     | **パラメーターの種類** |
      |--------------------------------------|--------------------|
      | 既定の組織の Project for the Web   | タイプ=0             |
      | CDS の Project for the Web が組織の名前を付けました | タイプ=1             |
      | Project Operations                   | タイプ=2             |

4. **プロジェクト パラメーター** ページからフィールドを削除します。

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>軽減策 3: project.microsoft.com にサインインする
Microsoft Edge ブラウザーで新しいタブを開き、project.microsoft.com に移動し、Project Operations へのアクセスに使用しているユーザー ロールを使用してサインインします。

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>問題: プロジェクトが読み込まれず、UI がスピナーで動かなくなる

認証の目的で、タスクグリッドをロードするためにポップアップを有効にする必要があります。 ポップアップが有効になっていない場合、画面は読み込みスピナーでスタックします。 次の図は、アドレスバーにブロックされたポップアップ ラベルが付いたURLを示しています。これにより、スピナーがページを読み込もうとしてスタックします。 

   ![スピナーとポップアップ ブロックが動かなくなった。](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>軽減策 1: ポップアップを有効にする

プロジェクトがスピナーで動かなくなった場合、ポップアップが有効になっていない可能性があります。

#### <a name="microsoft-edge"></a>Microsoft Edge

Edge ブラウザー有効にするでポップアップを有効にする方法は 2 つあります。

1. Edge ブラウザーで、ブラウザーの右上にある通知を選択します。
2. 特定の Dataverse 環境から **ポップアップとリダイレクトを常に許可する** を選択します。
 
     ![ポップアップがウィンドウをブロックしました。](media/enablepopups.png)

または、次の手順を実行することもできます:

1. Edge ブラウザーを開きます。
2. 右上隅で、**省略記号** (...) を選択して、次に **設定** > **サイトのアクセス許可** > **ポップアップとリダイレクト** を選択します。
3. ポップアップをブロックする場合は **ポップアップとリダイレクト** をオフに切り替えるか、デバイスでポップアップを許可する場合はオンに切り替えます。
4. ポップアップを有効にした後、ブラウザを更新します。 

#### <a name="google-chrome"></a>Google Chrome
1. Chrome ブラウザーを開きます。
2. ポップアップがブロックされているページに移動します。
3. アドレスバーで、**ポップアップがブロックされました** を選択します。
4. 表示するポップアップのリンクを選択します。
5. ポップアップを有効にした後、ブラウザを更新します。 

> [!NOTE]
> サイトのポップアップを常に表示するには、**[サイト] からのポップアップとリダイレクトを常に許可する** を選択して次に **完了** を選択します。

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>問題 3: Project for the Web の特権の管理

Project Operations は、外部のスケジューリング サービスに依存しています。 このサービスでは、WBS に関連するエンティティの読み取りと書き込みを可能にするいくつかのロールがユーザーに割り当てられている必要があります。 これらのエンティティには、プロジェクト タスク、リソース割り当て、およびタスク依存関係が含まれます。 ユーザーがに移動したときに WBS をレンダリングできない場合、**タスク** タブに移動します、それはおそらく **Project Operations** の **プロジェクト** が有効になっていません。 ユーザーは、セキュリティ ロール エラー、またはアクセスの拒否に関連するエラーのいずれかを受け取る可能性があります。

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>軽減策 1: アプリケーション ユーザーとエンド ユーザーのセキュリティ ロールを検証する

1. **設定** > **セキュリティ** > **ユーザー** > **アプリケーション ユーザー** に移動します。  

   ![アプリケーション リーダー。](media/applicationuser.jpg)
   
2. アプリケーションのユーザー レコードをダブルクリックして、次のことを確認します。

     - ユーザーにはプロジェクトへのアクセス権があります。 これを行うには、ユーザーが **プロジェクト マネージャー** セキュリティ ロールを持っていることを確認します。
     - Microsoft Project アプリケーション ユーザーが存在し、正しく構成されています。
 
3. このユーザーが存在しない場合は、新しいユーザー レコードを作成します。 
4. **新規ユーザー** を選択して、入力フォームを **アプリケーション ユーザー** に変更して、次に **アプリケーション ID** を追加します。

   ![アプリケーション ユーザー詳細。](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>問題 4: タスクを作成、更新、または削除しても、変更が保存されない

WBS に 1 つ以上の更新を行うと、変更は失敗し、保存されません。 スケジュール グリッドでエラーが発生し、"最近行った変更を保存できませんでした" というメッセージが表示されます。

### <a name="mitigation-1-validate-the-license-assignment"></a>低減策 1: ライセンスの割り当てを検証する

1. ユーザーに正しいライセンスが割り当てられていること、およびライセンスのサービス プラン詳細でサービスが有効になっていることを確認してください。  
2. ユーザーが **project.microsoft.com** を開けれることを確認します。
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>低減策 2: プロジェクト アプリケーション ユーザーの検証構成
1. プロジェクト アプリケーション ユーザーが作成されていることを確認します。
2. 次のセキュリティ ロールをユーザーに適用します。
  
  - Dataverse ユーザーまたは Base ユーザー
  - Project Operations システム
  - プロジェクト システム
  - Project Operations の二重書き込みシステム。 この役割は、リソース/非在庫ベースの Project Operations の展開向けに必要です。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
