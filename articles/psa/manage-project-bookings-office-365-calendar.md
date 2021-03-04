---
title: Office 365 カレンダーでプロジェクトおよび予約を管理する
description: Office 365 カレンダーでプロジェクトおよび予約を管理する方法
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c575bd3deba5bcde2526ccfc598327917bf91642
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144464"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>カレンダーでプロジェクトおよび予約を管理する (Project Service)

> [!Note]
> 廃止: この機能は廃止され、使用できなくなりました。

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーを使用して個人的な予定、プロジェクト ワークの予約、および Field Service の作業指示書の割り当てを表示します。  
  
 1 つの場所にすべてがあるので、1 日の管理が容易です。 あなたの会議、予定、予約およびタスクはすべて [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーで利用できます。  
  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を使用している場合、Project Service の時間エントリ ビュー内で個人的な予定も入力できます。 これにより、プロジェクトおよびリソースの管理者は、プロジェクトにあなたが参加可能かどうかを知ることができます。 これにより、個人の予定を 2 回入力する必要がないために、時間を節約できます。 カレンダーから Project Service の時間エントリ ビューに個人の予定をインポートするだけです。  
  
 カレンダーは今日から次の 4 週間のプロジェクトと作業指示書の予約を同期します。 この設定は変更できません。  
  
 同期は、PSA から [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーへの 1 方向のみがサポートされています。 逆の順序での同期ができます。 
  
 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーの使用方法に関する詳細は、「[ビジネス用 Outlook on the web カレンダー](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)」を参照してください。  
  
## <a name="setup"></a>セットアップ  
 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーで予約の表示および管理をする前に、いくつかの事柄を設定する必要があります。  
  
- [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] のグローバル管理者、またはシステム管理者の資格情報が必要です。  
  
- 管理者は、電子メール サーバー のプロファイルを設定する必要があります。また各ユーザーは各自のメールボックスを構成する必要があります。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [サーバー側の同期による電子メールの処理のセットアップ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>自分の組織の同期を有効にする (管理者のタスク)  
  
1.  メイン メニューから **設定** >  **管理** の順にクリックします。  
  
2.  **システムの設定** をクリックします。  
  
3.  **同期** タブをクリックします。  
  
4.  **リソース予約の同期を、何と有効にするかどうかを選択する** で、**リソース予約を Outlook と同期する** をクリックします。  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>ユーザー プロファイルに対する同期を有効にする (ユーザー タスク)  
  
1.  画面の右上にある **設定** ボタンをクリックします。  
  
2.  **オプション** をクリックします。  
  
3.  **同期** タブをクリックします。  
  
4.  **リソース予約を Outlook と同期する** で、**Outlook とリソース予約の同期** をクリックします。  
  
## <a name="import-your-personal-appointments-user-task"></a>個人の予定をインポートする (ユーザー タスク)  
 カレンダーから Project Service Automation の時間エントリ ビューに個人の予定をインポートします。  
  
1. [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] カレンダーを開き、**データのインポート** をクリックします。  
  
2. フィルター画面で、**Exchange の予定** を選択し、次に **適用** をクリックします。  
  
3. システムは、現在の週から推奨されたエントリとして、時間エントリ ビューから予定を取得します。 別の週のためのエントリを追加するには、**前へ** または **次へ** をクリックします。  
  
4. Project Service Automation の時間エントリ ビューに加える予定を選択して下さい。  
  
5. **時間入力** ポップアップ ボックスで、適切なオプションを選択して、Project Service Automation の時間エントリ ビューに予定を変換します。  
  
6. **保存** をクリックします。  
  
### <a name="see-also"></a>関連項目  
 [時間、経費、および共同作業ガイド](../psa/time-expense-collaboration-guide.md)
