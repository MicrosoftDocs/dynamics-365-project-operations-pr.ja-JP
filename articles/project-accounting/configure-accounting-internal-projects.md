---
title: 内部プロジェクトの会計の構成
description: このトピックは、Project Operations で内部プロジェクトの会計処理の設定方法について説明します。
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012862"
---
# <a name="configure-accounting-for-internal-projects"></a>内部プロジェクトの会計の構成

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

内部プロジェクトでは、企業は顧客に請求されていない活動に関連するコストを追跡できます。 内部プロジェクトの例には、次のようなものがあります。

- モバイル アプリなどの製品の開発。開発に関わる原価を追跡します。
- プリセールスの時間と経費の管理。 この販売前の内部プロジェクトは、見積もりが獲得された場合、後で請求可能なプロジェクトに変換することができます。

Dynamics 365 Project Operations で契約に関連付けられていないプロジェクトは、内部プロジェクトとして扱われます。 プロジェクト コストと売上のプロファイルは、プロジェクトの会計ルールの決定には使用されていません。 内部プロジェクトの原価は、常に損益の原則を使用して転記されます。 転記の勘定科目は、**元帳転記の設定** ページで定義します。

- 時間での取引は、**原価** 勘定を借方に転記し、**給与配賦** 勘定を貸方に転記します。
- 経費取引は、**費用** 勘定を引き落とし、**経費の相殺勘定** を入金することで計上されます。
- 品目トランザクションは、**原価** 勘定を借方に転記し、**原価 - 品目** 勘定を貸方に転記します。

取引をプロジェクトに転記すると、プロジェクトがプロジェクト契約に関連付けられている場合は、すべての累計の取引が取り消され、新しく請求可能な取引が作成されます。 請求可能な取引は、それぞれのプロジェクトの原価および収益プロファイルで定義されている会計ルールに従います。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
