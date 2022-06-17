---
title: 追加パラメーターの設定を構成する
description: Project Service での追加パラメーター設定の構成方法
author: JohnPBurrows
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
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 75fe0aab8ea8bf41fcb98f4318380c93ac52fef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919238"
---
# <a name="configure-additional-parameter-settings-project-service"></a>追加パラメーター設定の構成 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

前述の記事で項目を構成してある場合は、プロジェクトで使用する追加のプロジェクト パラメーターを設定する必要があります。 最初に [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] をインストールしたときは、作業する [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] に必要なすべてのレコードを最初に作成するためのパラメーター設定を作成しました。 ここで元に戻り、この設定の追加フィールドを構成します。  
  
 次の設定の構成を完了する必要があります。  
  
-   組織単位  
  
-   請求頻度  
  
-   作業時間テンプレート  
  
-   価格表  
 
このステップでは、必要とするリソース割り当てのタイプの指定も行います。  
  
- **中央**。 リソース管理者のみがプロジェクトにリソースを割り当てできます。  
  
- **ハイブリッド**。 リソース管理者、プロジェクト管理者、アカウント管理者がプロジェクトにリソースを割り当てできます。  
  
 
プロジェクト パラメーターの設定方法:  
  
1. **Project Service > パラメーター** に移動します。  
  
2. 構成するパラメーター設定 ([!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] を最初にインストールしたときに作成したもの) をクリックするか、**新規** をクリックして新規作成します。  
  
3. **全般** 領域で、プロジェクト パラメーターで使用するすべてのオプションを設定します。  
  
4. **価格表** 領域で、**+** をクリックして価格表を追加して、**プロジェクト パラメーター価格表** ドロップダウン リストで価格表を選択し、**保存** をクリックします。  
  
5. 画面の右下隅にある **保存** ボタンをクリックします。  

> [!NOTE]
> Project Service が正しく機能するには、プロジェクト パラメータ のレコードを管理する必要があります。 このレコードを削除することはできません。

### <a name="see-also"></a>関連項目  
 [リソースの設定](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
