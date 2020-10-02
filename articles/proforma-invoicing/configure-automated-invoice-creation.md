---
title: 請求書の自動作成を構成する
description: このトピックでは、請求書を自動的に生成するようにシステムを構成する方法について説明します。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898132"
---
# <a name="configure-automated-invoice-creation"></a>請求書の自動作成を構成する

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

プロジェクト オペレーションで請求書の自動生成の実行を構成するには、以下の手順を実行します。

1. **設定** \> **バッチ ジョブ**に移動します。
2. バッチ ジョブを作成して、 **プロジェクト オペレーション請求書の作成** と名前をつけます。 バッチ ジョブの名前に、「請求書の作成」という語句を含めてください。
3. **ジョブの種類** フィールドで、 **なし** を選択します。 既定で、 **頻度 毎日** および **アクティブ** オプションは **はい** に設定されています。
4. **ワークフローの実行** を選択します。 **レコードの検索** ダイアログ ボックスで、 3 つのワークフローが表示されます:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. **ProcessRunCaller** を選択し、そして **追加** を選択します。
6. 次のダイアログ ボックスで、 **OK** を選択します。 **スリープ** ワークフローの後に、 **プロセス** ワークフローが続きます。

    ステップ 5 で、 **ProcessRunner** を選択することもできます。 **OK** を選択すると、 **プロセス** ワークフロー の後には、 **スリープ** ワークフローが続きます。

**ProcessRunCaller** および **ProcessRunner** ワークフローは、請求書を作成します。 **ProcessRunCaller** は **ProcessRunner** を呼び出します。 **ProcessRunner** は、実際に請求書を作成するワークフローです。 請求書を作成する必要のあるすべての契約品目を調べ、それらの明細の請求書を作成します。 契約書を作成する契約品目を決定するために、ジョブは契約品目の請求書の実行日を参照します。 1 つの契約に属する契約品目の請求書実行日が同じ場合、トランザクションは、 2 つの請求明細行を持つ 1 つの請求書に統合されます。 請求書を作成するトランザクションがない場合、ジョブは請求書の作成をスキップします。

**ProcessRunner** の実行が完了すると、 **ProcessRunCaller** を呼び出して、終了時間が指定されてクローズされます。 **ProcessRunCaller** は、指定された終了時刻から24時間実行するタイマーを開始します。 タイマーが終了すると、 **ProcessRunCaller** が閉じられます。

請求書を作成するバッチ処理ジョブは、定期的なジョブです。 このバッチ処理を何度も実行すると、ジョブの複数のインスタンスが作成され、エラーが発生します。 したがって、バッチ処理は一度だけ実行し、実行が停止した場合のみ、再起動する必要があります。

> [!NOTE]
> バッチ請求は、請求スケジュールで構成されたプロジェクト契約明細に対してのみ実行されます。 固定価格の請求方法の契約品目には、マイルストーンを構成する必要があります。 時間と材料の請求方法を持つプロジェクト契約品目には、日付ベースの請求スケジュールを設定する必要があります。 これは、プロジェクトベースの契約品目でも同じです。     
