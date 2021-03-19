---
title: 手動で見積送り状を作成する (ライト)
description: このトピックでは、Project Operations で見積送り状を手動で作成する方法について解説します。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274194"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>手動で見積送り状を作成する (ライト)

_**適用対象:** ライト展開 - 見積もり請求の取引_

Dynamics 365 Project Operations では、必要に応じて見積送り状を手動で作成できます。 **プロジェクト契約** 一覧ページまたは **プロジェクト契約** の詳細ページから、手動で見積送り状を作成することができます。

##  <a name="project-contracts-list-page"></a>プロジェクト契約の価格表

**プロジェクト契約** リストページで、1つ以上のプロジェクト契約を選択し、選択したすべてのレコードの請求書を作成します。

システムは、選択されたプロジェクト契約のうち、今日の日付よりも前の日付の **請求書の発行準備完了** のバックログがあるかどうかをチェックします。 これらの契約から、システムは見積送り状のドラフト版を作成します。 プロジェクト契約に複数の顧客がいる場合、顧客ごとに 1 つの請求書が作成され、プロジェクト契約ごとに複数の請求書が作成される場合があります。

作成されたプロジェクトの請求書はすべて、**営業** エリアの **請求** のセクション内の **請求書** ページに掲載されています。

## <a name="project-contract-details-page"></a>[プロジェクト契約の詳細] ページ

見積送り状は、**プロジェクト契約** 詳細ページからも作成できます。 システムによって、プロジェクト契約に今日の日付より前の日付の **請求準備完了** バックログがあることが確認されます。 それらの契約から、システムによって各契約品目の顧客の数に基づいてドラフトの見積送り状が作成されます。

ひとつの見積送り状が作成されると、**請求書** ページが開きます。 そのプロジェクト契約に対して複数の見積送り状が作成された場合、**請求書** リスト ページが開き、作成されたすべての見積送り状が表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]