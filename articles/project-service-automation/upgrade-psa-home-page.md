---
title: ホーム ページのアップグレード
description: このトピックでは、Dynamics 365 Project Service Automation の新しい、変更された機能に関する重要な情報の見つけ方、および最新バージョンへのアップグレードの手順を説明します。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752891"
---
# <a name="upgrade-home-page"></a>ホーム ページのアップグレード

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>PSA バージョン 2.x または 1.x からバージョン 3.x へのアップグレード

### <a name="new-instances"></a>新しいインスタンス

2019 年 5 月 17 日から、新しいインスタンスの Project Service Automation が選択されている場合、バージョン 3.x が既定でインストールされます。

### <a name="existing-instances"></a>既存のインスタンス

以前は、 PSA バージョン 2.x のインスタンスを使用していて、PSA の統一顧客インターフェイス ベース（UCI）のバージョンである PSA バージョン 3.x. にアップグレードする必要がある場合は、バージョン 3.x. へのアップグレードを目的としてインスタンスを有効にできるように、Microsoft サポートに連絡して顧客のインスタンスの詳細情報を提供する必要があります。 2020 年 3 月 1 日以降は、PSA バージョン 2.x のインスタンスを使用していて、バージョン 3.x にアップグレードする必要があるユーザーは、Microsoft サポートに連絡することなく、管理ポータルから直接インスタンスをアップグレードできます。  

> [!NOTE]
> PSA バージョン 3.x には大きな変更が含まれます。 これは、ユーザー エクスペリエンスを高める際に役立つように、統一インターフェイス フレームワークで構築されています。 再設計済みのアプリケーションでは、一貫性のある統一ユーザー インターフェイス (UI) を提供しています。また、画面のサイズまたはデバイスを使用して最適に表示するためにレスポンシブ デザインの原則を採用しています。 アプリケーション全体で他にも変更を行っています。 変更された領域の一部には、価格、予約、およびリソースの割り当て、時間、経費、承認が含まれています。

アップグレード プロセスを開始する前に、以下のタスクを完了することをお勧めします。

- Dynamics 365 Field Service および Project Service Automation の両方が、指定したインスタンスにインストールされているかどうかを確認してください。 双方のソリューションがインストールされている場合は、定期的なインスタンスの使用を再開する前に両方ともアップグレードするプランを立ててください。
- 次のトピックをよく確認してください。 バージョン間での変更に関して認知および解釈しておくと、アップグレード プロセスで役立ちます。 このトピックでは、PSA での大きな変更に関する情報とともに、3.x バージョンにアップグレードするプランを立てる場合のお勧めの方法を提供します。

    - [Project Service Automation バージョン 3 の最新情報または変更事項](whats-new-changed-v3.md)
    - [アップグレードの考慮事項 - Project Service Automation バージョン 2.x または 1.x から バージョン 3 へ](upgrade-v3.md)

- サンドボックス インスタンスをアップグレードしてから実装の変更について評価し、実稼働インスタンスをアップグレードします。

先ほど説明したトピックを確認し、PSA バージョン 3.x または UCI ベース バージョンへのアップグレードの準備が完了したら、管理センターのアップグレードを有効にするように Microsoft サポートに要求を送信します。 要求する際には、ユーザーのインスタンスについての詳細を提供します。

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>新しく作成したインスタンスの PSA (PSA バージョン 2.x) の古いバージョン

2019 年 5 月 17 日から、すべての新規インスタンスには、既定のクライアントとして UCI が含まれるようになります。 この変更を使用して配置する場合は、 PSA version 3.x および Field Service バージョン 8.x が規定でプロビジョニングされるようになります。これらが UCI クライアントで機能するように設計されているためです。

2020 年 3 月 1 日以降、Dynamics PSA のユーザーは、PSA の古いバージョン（PSA バージョン 2.x 以下など）で新しい環境を作成できなくなります。 新しい環境では、PSA のバージョン 3.x のみを取得することになります。

> [!NOTE]
> 旧バージョンの Field Service および PSA アプリケーションを使用する場合の一番のエクスペリエンスとしては **システム設定** ページに移動し、フィールドの場合は **新しい統一インターフェイスのみ (推奨) を使用する** フィールドに移動して、**いいえ** を選択します。これらのバージョンが UCI で現在ロードできるように設計されていないためです。 UCI を停止後に、古い Web クライアントを使用することによって、Field Service や PSA のバージョンを開いて実行できます。 UCI クライアントを停止する方法については、[統一インターフェイスのみを有効にする](../admin/enable-unified-interface-only.md)を参照してください。