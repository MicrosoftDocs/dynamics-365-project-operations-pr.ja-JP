---
title: 内部プロジェクトの会計の構成
description: このトピックは、Project Operations で内部プロジェクトの会計処理の設定方法について説明します。
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287604"
---
# <a name="configure-accounting-for-internal-projects"></a>内部プロジェクトの会計の構成

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

内部プロジェクトでは、企業は顧客に請求されていない活動に関連するコストを追跡できます。 内部プロジェクトの例は次のとおりです :

- モバイル アプリなどの製品を開発し、開発に関連するコストの追跡。
- 販売前の時間と費用の管理。 この販売前の内部プロジェクトは、見積もりが獲得された場合、後で請求可能なプロジェクトに変換することができます。

Dynamics 365 Project Operations で契約に関連付けられていないプロジェクトは、内部プロジェクトとして扱われます。 プロジェクト コストと売上のプロファイルは、プロジェクトの会計ルールの決定には使用されていません。 内部プロジェクトの原価は、常に損益原則を使用して転記されます。 転記の元帳勘定は、**台帳転記設定** ページで定義されています。

- 時間取引は、**費用** 勘定を引き落とし、**給与の割り当て** 勘定を入金することで計上されます。
- 経費取引は、**費用** 勘定を引き落とし、**経費の相殺勘定** を入金することで計上されます。

案件に取引が計上された後、案件が案件契約に関連付けられている場合は、累積された取引を全て取り消して、新たに請求可能な取引を作成します。 請求可能な取引は、それぞれのプロジェクトのコストと収益プロファイルに定義された会計ルールに従います。




[!INCLUDE[footer-include](../includes/footer-banner.md)]