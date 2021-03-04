---
title: プロジェクトの見積りの確認、更新、送信
description: このトピックでは、顧客に見積りを送信して確認し、フィードバックに基づいて修正し、見積りを再送信する処理について説明します。
author: ruhercul
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f9d76c65cb6732a96cd0bd6c4c36a2a73a65a2b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079406"
---
# <a name="confirm-update-and-send-a-project-quotation"></a>プロジェクトの見積りの確認、更新、送信

[!include [banner](../includes/banner.md)]

プロジェクトの見積りを作成し、顧客に送信した後、見積りのステータスを **送信済み** に更新する前に、顧客から確認を取る必要があります。 顧客から要求された修正は、見積りの中で更新することができます。 見積りの状態を **送信済み** に更新した後は、変更できません。 以下の手順では、確認のために見積りを送信し、フィードバックに基づいて更新を行い、見積りを送信するオプションについて説明します。

## <a name="send-a-project-quotation-confirmation"></a>プロジェクトの見積り確認を送信する  

確認のために、既存のプロジェクトの見積書を電子メールで送信するか、印刷したコピーとして送信することができます。 

1. **プロジェクト管理と会計** > **見積り** > **プロジェクトの見積り** の順に移動します。 
2. **プロジェクトの見積り** ページで、確認のために送信する見積りを選択します。 
3. **フォローアップ** タブの **全般** タブで、 **確認** を選択します。 
4. **見積もりを確認する** ページで、必要なパラメーターを設定します。 たとえば、確認を印刷するには、 **印刷** オプションの配下で、 **印刷を確認する** をオンにして、 **OK** を選択します。
5. **見積りを送信する** ページで、 **オプション** を選択し、 **印刷先の設定** ページで、見積もりを **画面** 、 **Eメール** 、 **ファイル** 、 **アーカイブを印刷する** 、 **プリンター** に送信するかどうかを選択します。その後、見積書をルーティングするために、 **仕様** 領域で必要な調整を行います。
6. **印刷先設定** ページで、 **OK** を選択します。  

## <a name="update-a-project-quotation"></a>プロジェクトの見積を更新する

既存のプロジェクト見積りを変更するには、見積もりの状態が **作成済** になっている必要があります。 次の手順を実行して、既存の見積もりを更新します。 

1. **プロジェクト管理と会計** > **見積もり** > **プロジェクト見積もり** の順に移動します。
2. **プロジェクトの見積もり** ページで、更新する見積もりを選択し、アクションペインで **編集** を選択します。
3. 必要なフィールド情報を更新し、アクションペインで **保存する** を選択します。  

## <a name="send-a-project-quotation-to-a-customer"></a>顧客にプロジェクトの見積もりを送る 

1. **プロジェクト管理と会計** > **見積り** > **プロジェクトの見積り** にアクセスし、送信するプロジェクトの見積もりを選択します。
2. **プロジェクトの見積り** ページの、 **見積もり** タブで、 **処理** グループの **見積りの送信** を選択します。 見積りの状態が **送信済み** に更新されます。

> [!NOTE]
> 状態が **送信済み** に更新された後は、プロジェクトの見積りを変更することはできません。


[!INCLUDE[footer-include](../includes/footer-banner.md)]