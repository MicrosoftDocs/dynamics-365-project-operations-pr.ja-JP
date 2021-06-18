---
title: プロジェクト ステージのタイプ
description: このトピックでは、プロジェクト ステージについて説明します。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008992"
---
# <a name="project-stage-types"></a>プロジェクト ステージのタイプ 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

プロジェクト ステージは、プロジェクトの進み具合の状態を反映するように設計されます。 カスタマイズを使用して、ビジネス プロセス フロー、Power Automate、またはプラグイン拡張機能でステージを自動的に更新できます。

次のステージは既定 BPF で定義されています。

- 新規​​
- 見積もり
- 計画
- 実行
- 完了
- [閉じる] 

## <a name="new"></a>新規

プロジェクトを作成する場合、プロジェクト ステージは **新規** に設定されます。 プロジェクトがテンプレートから作成された場合は、それにはスケジュール、予測、チーム データがある場合もあります。 さもなければ、これはプロジェクトの概説であり、残りのコンポーネントを入力する必要があります。

## <a name="quote"></a>見積もり

プロジェクトを見積もりに関連付けたり、見積もりからプロジェクトを作成する場合、このプロジェクト ステージは **見積もり** に設定され、予想される開始日と終了日も更新されます。 プロジェクトが **見積もり** ステージの場合、**プロジェクト エンティティ** ページにある **営業** タブは見積もりの詳細を表示します。

## <a name="plan"></a>計画

プロジェクトに関連付けられた見積もりが達成された場合、プロジェクトは **契約** フェーズに移動され、プロジェクト ステージは **計画** へと更新されます。 プロジェクトが **計画** ステージの場合、**プロジェクト エンティティ** ページは契約の詳細を表示します。

## <a name="deliver"></a>実行

プロジェクト計画が完了し、プロジェクトを開始する準備ができたら、プロジェクト管理者は、プロジェクト ステージを **実行** へと更新し、プロジェクトが開始したことを示す必要があります。

## <a name="complete"></a>完了 

プロジェクトの作業が完了したら、プロジェクト管理者はステージを **完了** に更新できます。 プロジェクト ステージを **完了** に更新することで、プロジェクト管理者は、作業は 100 パーセント完了しているが、保留中の時間や経費項目が記録できるようにプロジェクトは開いたままになっていることを示します。

## <a name="close"></a>[閉じる]

プロジェクトのすべてのトランザクションが記録されたら、プロジェクト管理者はステージを **閉じる** に更新できます。 この時点で、トランザクションの記録はできなくなり、プロジェクトは読み取り専用に設定されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]