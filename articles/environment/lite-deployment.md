---
title: Project Operations の展開 - ライト
description: この記事では、Project Operations lite の展開 (見積もり請求の取引) をインストールする方法に関する情報を提供します。
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810984"
---
# <a name="deploy-project-operations-lite"></a>Project Operations の展開 - ライト

_**適用対象:** ライト展開 - 見積もり請求の取引_



Project Operations は、複数の展開モデルをサポートしています。 最適な展開モデルを決定するには、[展開の種類](determine-deployment-type.md) を参照してください。


> [!IMPORTANT]
> この展開、ライト展開 – 見積もり請求に対処すると、**Dataverse - Project Operations の展開のみ** となります。

- [Project Operations を新しい Dataverse 環境にインストールする](#new)
- [既存の Dataverse 環境にインストールする](#existing)
- [既存の Dataverse 二重書き込みコンポーネントを持つ環境にインストール](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Lite を新しい Dataverse 環境にインストールする

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、[PowerPlatform 管理センター](https://admin.powerplatform.com) で新しい Dataverse 環境を作成します。 **この環境用のデータベースの作成** と **Dynamics 365 アプリ** が有効になっていることを確認します。 詳細については、[Power Platform 管理センターで環境を作成および管理する](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) を参照してください。
1. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** を選択します。


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Lite を既存の Dataverse 環境にインストールする 
1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。
1. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** をインストールします。 詳細については、[Dynamics 365 アプリを管理する](/power-platform/admin/manage-apps) 参照してください。

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>二重書き込みソリューションが既に存在する既存の Dataverse 環境にProject Operations Lite をインストールします

Project Operations をライト展開モードで引き続き実行する場合は、以下の手順を実行する必要があります:

1. Project Operations ライセンスの[グローバルまたは Power Platform 管理者](/power-platform/admin/global-service-administrators-can-administer-without-license) として、Project Operations をインストールする [PowerPlatform 管理センター](https://admin.powerplatform.com) で環境を見つけます。
1. Dynamics 365 アプリの展開リストから **Microsoft Dynamics 365 Project Operations** をインストールします。 詳細については、[Dynamics 365 アプリを管理する](/power-platform/admin/manage-apps) 参照してください。
1. ご利用の環境には、財務と運用アプリへの統合を支援する二重書き込みコンポーネントがインストールされているため、Project Operations のインストールでは、Project 関連データを財務と運用アプリに統合するために必要な機能や拡張機能もインストールされます。 ライト展開で Project Operations を実行する必要があるため、これらの統合コンポーネントはライト展開シナリオの制限とオーバーヘッドを作成するため、削除する必要があります。 ソリューション **Dynamics 365 Project Operations 二重書き込み** および **Dynamics 365 Project Operations 二重書き込みエンティティ マップ** を手動でアンインストールして、これらのコンポーネントを削除します。
1. **Project Operations -> 設定 -> パラメーター** に移動します。 **プロジェクト パラメーター** の詳細ページを開き、 **ソリューション アップグレード動作** フィールドを **ライトのみ** に設定します。 これにより、その後の Project Operations のアップグレードで、統合コンポーネントが Project Operations に戻されなくなります。  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
