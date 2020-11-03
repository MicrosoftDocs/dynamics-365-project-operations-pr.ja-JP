---
title: カタログ製品のコストと販売率を設定する
description: このトピックは、製品カタログ内のアイテムのコストと販売率を設定する方法に関する情報を提供します。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079335"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>カタログ製品のコストと販売率を設定する

_**適用対象:** ライト展開 - 見積もり請求の取引_


Dynamics 365 Project Operations での製品カタログ アイテムの価格設定は、Dynamics 365 Sales の場合と同じです。

Project Operations のプロジェクトでは製品を見積もったり使用したりできないため、見積もりや契約のプロジェクト価格表に製品カタログの価格を設定する必要はありません。

製品カタログの価格は、見積もり、契約、またはアカウントの **製品価格** フィールドに設定しなければなりません。 これらのエンティティのプロジェクト価格表に製品カタログ価格を設定しないでください。 プロジェクトの価格表は、Project Operations 専用です。 価格表を見積もりから契約にコピーするアプリケーション固有のビジネス ロジックがあります。 この結果は、契約に固有のプロジェクトの価格表です。 見積もりのプロジェクト価格表が大きくなりすぎると、コピー操作によって見積もりの受注プロセスが遅れる可能性があります。 製品の価格表は、契約のカスタム価格表を作成するためにコピーされません。 これは、製品の価格表が見積もり受注プロセスのパフォーマンスに影響を与えないことを意味します。
