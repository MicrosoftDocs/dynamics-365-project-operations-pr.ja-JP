---
title: カタログ製品の原価率と販売率を設定する - Lite
description: この記事では、製品カタログのアイテムのコストと販売率を設定する方法について説明します。
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917398"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>カタログ製品の原価率と販売率を設定する - Lite

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations で製品カタログ アイテムの価格設定を行う方法は、Dynamics 365 Sales と同じです。

Project Operations では、製品を見積もったりプロジェクトで使用したりすることはできないため、見積もりや契約のために製品カタログの価格をプロジェクトの価格表に設定する必要はありません。

見積もり、契約の **製品価格** フィールドを使うか、製品カタログの価格を設定します。 プロジェクト価格表に製品カタログの価格を設定しないでください。 プロジェクトの価格表は、Project Operations 専用です。 アプリケーション固有のビジネス ロジックは、価格表を見積もりから契約にコピーします。 この結果は、契約に固有のプロジェクトの価格表です。 見積もりのプロジェクト価格表が大きくなりすぎると、コピー操作によって見積もりの受注プロセスが遅れる可能性があります。 製品の価格表は、契約のカスタム価格表を作成するためにコピーされません。 コピーが含まれないため、見積もりプロセスのパフォーマンスに影響はありません。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]