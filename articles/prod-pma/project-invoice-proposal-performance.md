---
title: プロジェクトの仮発行請求書のパフォーマンス
description: このトピックは、プロジェクトの仮発行請求書のパフォーマンス向上に関する情報を提供します。
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683452"
---
# <a name="project-invoice-proposal-performance"></a>プロジェクトの仮発行請求書のパフォーマンス

[!include [banner](../includes/banner.md)]

新しい仮発行請求書を作成する場合、プロジェクトとサブプロジェクトの数が増えると、パフォーマンスの問題が発生する可能性があります。 パフォーマンスを向上させるために、投稿されたプロジェクト トランザクションの新しい仮発行請求書を作成するために必要な時間を短縮する機能を利用できます。

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>プロジェクトの仮発行請求書拡張機能を有効にする
プロジェクトの仮発行請求書のパフォーマンス拡張機能を有効にするには、次の手順を実行します。

1.  **機能管理** > **すべて** に移動します。 機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。
2.  **今すぐ有効にする** を選択します。
3.  ブラウザを更新してから、新しい仮発行請求書を作成します。

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>プロジェクトの仮発行請求書拡張機能を無効にする
プロジェクトの仮発行請求書のパフォーマンス拡張機能を無効にする手順を実行します。

1.  **機能管理** > **すべて** に移動します。 機能リストで、**プロジェクトの仮発行請求書のパフォーマンス拡張機能** を選択します。
2.  **無効にする** を選択します。
3.  ブラウザーを最新の情報に更新します。

> [!NOTE]
> 請求ルールが有効な場合、請求書の提案パフォーマンスが適用できません。
> 
> 請求書案を作成するバッチ処理では、サブタスクの数は、入力した内容にかかわらず、請求書発行可能な取引のある契約数に応じた最大数にタスクが分割されます。 たとえば、一括で請求書案を作成するサブタスクの数に **3** を入力した場合でも、請求書発行可能な取引がある契約が 2 つしかないと、サブタスクは 2 つしか作成されません。
