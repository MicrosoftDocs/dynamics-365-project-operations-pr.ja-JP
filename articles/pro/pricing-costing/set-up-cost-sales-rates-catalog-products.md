---
title: カタログ製品の原価率と販売率を設定する - Lite
description: このトピックは、製品カタログ内のアイテムのコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176707"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>カタログ製品の原価率と販売率を設定する - Lite

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations での製品カタログ アイテムの価格設定は、Dynamics 365 Sales の場合と同じです。

Project Operations のプロジェクトでは製品を見積もったり使用したりできないため、見積もりや契約のプロジェクト価格表に製品カタログの価格を設定する必要はありません。

製品カタログの価格は、見積もり、契約、またはアカウントの **製品価格** フィールドに設定しなければなりません。 これらのエンティティのプロジェクト価格表に製品カタログ価格を設定しないでください。 プロジェクトの価格表は、Project Operations 専用です。 価格表を見積もりから契約にコピーするアプリケーション固有のビジネス ロジックがあります。 この結果は、契約に固有のプロジェクトの価格表です。 見積もりのプロジェクト価格表が大きくなりすぎると、コピー操作によって見積もりの受注プロセスが遅れる可能性があります。 製品の価格表は、契約のカスタム価格表を作成するためにコピーされません。 これは、製品の価格表が見積もり受注プロセスのパフォーマンスに影響を与えないことを意味します。
