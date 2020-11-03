---
title: リソース キャパシティの同期
description: このトピックは、カレンダーとプロジェクト間でリソースの容量を同期する方法に関する情報を提供します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079246"
---
# <a name="synchronize-resource-capacity"></a>リソース キャパシティの同期

[!include [banner](../includes/banner.md)]

リソース同期のプロセスは、カレンダーと基本カレンダーの情報がプロジェクトのリソース スケジュールに流れ込むことを保証するのに役立ちます。 カレンダーが変更された場合、プロセスはプロジェクト リソースのスケジュールに必要な更新を行います。 カレンダーのリソース情報は事前に同期されているため、プロセスはパフォーマンスの向上にも役立ちます。 したがって、リソース スケジュール情報の更新はより迅速に行われます。 プロセスは一度に 1 つではなくバッチとしてスケジュールすることをお勧めします。 それ以外の場合は、情報が最後に同期された包括的な日付をユーザーが忘れるというリスクがあります。 包括的な日付を使用しない場合、日付の同期中にギャップが発生する可能性があります。

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>リソース キャパシティ ロールアップの同期

同期プロセスは、すべてのリソース カレンダー情報を同期するように設計されています。 この情報には、プロジェクトのリソース カレンダーのキャパシティ テーブルへの変更に関する基本カレンダー情報が含まれています。 新しいリソースがプロジェクトに追加された場合、同期は、更新されたカレンダー情報が使用可能であることを保証するのに役立ちます。 この同期はいつでも実行できます。

バッチを使用することをお勧めします。 オプションは、確保済能力の同期中に使用できます。

1. **プロジェクト管理と会計**&gt;**定期的**&gt;**キャパシティの同期**&gt;**リソース キャパシティのロールアップの同期** を選択します。
2. 次の表にオプション設定します。

    | オプション      | 内容 |
    |-------------|-------------|
    | 期間コード | 必要に応じて、総勘定元帳の日付範囲コードを選択して、リソース キャパシティ ロールアップの同期プロセスの開始日と終了日を設定します。 |
    | 開始日  | リソース キャパシティ ロールアップの同期プロセスの開始日を入力します。 |
    | 終了日    | リソース キャパシティ ロールアップの同期プロセスの終了日を入力します。 |

[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
