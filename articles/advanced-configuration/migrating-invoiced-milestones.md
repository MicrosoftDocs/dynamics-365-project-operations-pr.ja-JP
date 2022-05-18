---
title: カットオーバー時に完全に請求された請求マイルストーンを移行する
description: このトピックでは、稼働開始日より前にオープンなプロジェクト契約について顧客に請求された固定価格の請求マイルストーンを移行する方法を説明します。
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576276"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>カットオーバー時に完全に請求された請求マイルストーンを移行する

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

## <a name="scenario"></a>シナリオ

Contoso は、リソース/非在庫シナリオで Microsoft Dynamics 365 Project Operations を稼動させています。 カットオーバー活動の一環として、導入チームは旧システムからオープンなプロジェクト契約を移行する必要があります。 一部のプロジェクト契約には、固定価格請求方式を使用し、すでに部分的に最終顧客に請求されている契約品目が含まれています。 これらの請求マイルストーンは、収益認識上、契約総額に含まれる必要があるため、**顧客請求書の計上** と同時に移行する必要があります。 ただし、売掛金および総勘定元帳の顧客残高は影響を与えないようにする必要があります。

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>前提条件

- Dynamics 365 Finance 10.0.24 以降をインストールする必要があります。
- 移行手順を完了する環境は、メンテナンス モードである必要があります。 マイルストーンの移行中は、他のアクティビティを実行しないでください。
- 移行手順は、ここで説明されているとおりに正確に実行する必要があり、カットオーバー活動のみに使用することができます。 マイクロソフトでは、この機能の他の使用をサポートしていません。

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operations 統合契約品目マイルストーン デュアル ライト マッピングのカットオーバー版の作成 

1. **Project Operations 統合契約品目マイルストーン** エンティティのターゲット マッピングが最新であることを確認する。 

    1. Finance で、**データ管理** \> **データ エンティティ** に移動し、**Project Operations 統合契約品目マイルストーン** エンティティを選択します。 
    2. **ターゲット マッピングの変更** を選択します。 
    3. **ステージングをターゲットにマッピングする** ページで、**マッピングの生成** を選択し、マッピングの生成を確認します。

2. **Project Operations 統合契約品目マイルストーン** (**msdyn\_contractlinescheduleofvalues**)  デュアル ライト マッピングを停止して最新の情報に更新します。 

    1. **データ管理**\>**デュアルライト** に移動し、マップを選択して詳細を開きます。 
    2. **停止** を選択し、システムがマップを停止するまで待機します。 
    3. **テーブルの更新** を選択します。

3. トランザクションの状態のマッピングを追加します。

    1. **マッピングの追加** を選択します。
    2. 新しい行で、**財務と運用アプリ** 列で、**TRANSSTATUS \[TRANSSTATUS\]** フィールドを選択します。
    3. **Microsoft Dataverse** 列で、**msdyn\_ invoicestatus\[請求書のステータス\]** を選択します。
    4. **マップタイプ** 列で、右矢印を選択します (**\>**)。
    5. 表示されるダイアログ ボックスの **同期方向** フィールドで、**Dataverse 財務と運用アプリ** を選択します。
    6. **変換の追加** を選択します。
    7. **変換の種類** フィールドで、 **ValueMap** を選択します。
    8. **値のマッピングの追加** を選択します。
    9. 左のフィールドに、**4** と入力します。 右のフィールドに、**192350001** と入力します。 
    10. **保存** を選択し、ダイアログ ボックスを閉じます。

4. **名前を付けて保存** を選択し、デュアルライト マップのバージョンを保存します。 
5. **テーブルを追加** ペインの、**公開元** フィールドで、**既定の公開元** を選択します。
6. **バージョン** フィールドにバージョンを入力します。
7. **説明** フィールドに、このカットオーバー バージョンのマップに関するメモを入力します。 
8. **保存** を選択します。
9. マップを開始します。

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>請求済みのマイルストーンを Dataverse 環境に移行する

1. Project Operations の Dataverse 環境で、請求書の状態が **請求の準備完了** となっているマイルストーンを作成します。 この時点で、請求されていないマイルストーンは移行しないでください。

    > [!NOTE]
    > 請求マイルストーンを移行する前に、プロジェクト契約品目に関連する財務分析コードが期待どおりに設定されていることを確認してください。 移行が完了した後は、財務分析コードを編集できません。

2. すべてのマイルストーンが移行された後は、次のデュアル ライト マップを停止します。

    - Project Operations 統合契約品目マイルストーン (msdyn\_contractlinescheduleofvalues)
    - Project Operations 統合実績 (msdyn\_actuals)
    - プロジェクトの仮発行請求書 V2 (invoices)

    マップを停止するには、以下の手順を実行します:

    1. Finance で、**データ管理**\>**デュアルライト** に移動し、マップを選択して詳細を開きます。
    2. **停止** を選択し、システムがマップを停止するまで待機します。

3. Project Operations の Dataverse 環境で、請求マイルストーンに応じたプロフォーマ インボイスを作成し、確認します。 

    1. サイトマップで、プロジェクト契約に移動し、契約を選択してから、**請求書の作成** を選択します。
    2. 請求書を作成した後は、 サイトマップの **請求書** メニューから請求書を開き、**確認** を選択します。

    この手順では、Dataverse 環境に必要なレコードを作成します。 ただし、前述のデュアルライト マップが停止されたため、財務および売掛金勘定には影響しません。

4. すべてのプロフォーマ インボイスが確認されたら、すべてのデュアルライト マップを初期状態に戻します。

    1. **Project Operations 統合契約品目マイルストーン** (**msdyn\_contractlinescheduleofvalues**) のデュアル ライト マッピングのバージョンを更新元に戻します。 
    2. マップ リストでデュアル ライトマップを選択し、**テーブル マップ バージョン** を選択します。続いてテーブル マップの元のバージョンを選択します。
    3. **保存** を選択します。
    4. 次のデュアルライト マップを再起動します:

        - Project Operations 統合契約品目マイルストーン (msdyn\_contractlinescheduleofvalues)
        - Project Operations 統合実績 (msdyn\_actuals)
        - プロジェクトの仮発行請求書 V2 (invoices)

以上でマイルストーンの移行が完了し、カットオーバー活動の次のステップに進む準備が整いました。