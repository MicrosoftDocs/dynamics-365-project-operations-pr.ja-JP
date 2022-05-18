---
title: 外注に関する重要な概念
description: このトピックは、Microsoft Dynamics 365 Project Operations の外注に適用する重要な概念について説明します。
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578117"
---
# <a name="key-concepts-in-subcontracting"></a>外注に関する重要な概念

[!include [banner](../../includes/dataverse-preview.md)]

_**適用対象:** ライト展開 - 見積もり請求の取引_

このトピックdえは、Microsoft Dynamics 365 Project Operations の外注を機能的に使用する前に把握しておくべき重要な概念を説明します。

## <a name="contracting-unit-on-the-subcontract"></a>外注の契約単位

契約単位は、最終プロジェクトのデリバリーを所有する部門またはプラクティスを表します。 契約単位は、ベンダーと契約関係を結ぶ部門でもあります。

## <a name="purchase-currency"></a>購入通貨

Project Operations では、購入通貨は外注で使用する通貨です。 これは、プロジェクトで下請け業者にかかる費用を記録する通貨でもあります。 購入通貨はプロジェクト通貨とは異なる場合があり、プロジェクト通貨は販売通貨とは異なる場合があります。

## <a name="billing-methods-on-subcontract-lines"></a>外注ラインでの請求方法

プロジェクトの場合、通常、固定手数料と消費ベースの契約モデルがあります。 Project Operations は、販売および購入のコンテキストでこれらの請求方法をサポートします。 購入の場合、請求方法は次のとおりです。

- **時間と材料** – 外注ラインが **時間と材料** 請求方法を使用し、下請け業者がそのプロジェクトに取り組み、時間を記録するときに、時間のコストがプロジェクトに記録されます。 下請け業者からのコスト トランザクションは、ベンダーの請求書の行項目と照合されます。 このモデルでは、Project Operations を使用するプロジェクト マネージャーは、ベンダーの請求書の行を、記録および承認された下請け業者の時間と照合および検証できます。 検証が完了すると、承認後に記録された以前の実際原価が取り消され、ベンダーの請求書に基づく新しい実際原価がプロジェクトに作成されます。
- **固定価格** – この固定料金契約モデルでは、ベンダーの請求書は固定のマイルストーンに基づいています。 ただし、下請け業者のリソースも時間を報告できます。 その後、プロジェクト マネージャーが時間を確認し、承認します。 承認されると、Project Operations はプロジェクトの一時的な実際原価を作成します。 ベンダーがマイルストーンの請求書を送信した後、プロジェクト マネージャーは、以前に記録された実際原価をマイルストーンと照合できます。 検証が完了すると、実際原価が取り消され、マイルストーンベースの原価が記録されます。

## <a name="project-price-lists-on-subcontracts"></a>外注のプロジェクト価格表

プロジェクト価格表は、時間、経費、および他のプロジェクト関連コンポーネントの購入価格を設定するために使用する価格表です。 複数の価格表が存在する可能性があり、Project Operations でそれぞれに独自の有効期限付きの外注を持つことができます。 Project Operations は、外注のプロジェクト価格表で重複する有効日をサポートしていません。

## <a name="transaction-classes-on-subcontracts"></a>外注のトランザクション クラス

Project Operations では、4 種類のトランザクション クラスがサポートされます:

- 時間
- 経費
- 材料
- 料金

購入価格は、**時間**、**経費**、および **材料** のトランザクション クラスでのみ見積り、負担することが可能です。 **手数料** は売上のみのトランザクションクラスであり、購入のコンテンツでは利用できません。

## <a name="purchase-pricing-dimensions"></a>購入価格ディメンション

価格ディメンションを使用すると、購入価格の設定と時間トランザクションの既定設定に使用する属性を決定できます。 購入に関して、Project Operations は、購入価格の設定と既定設定に必要な固定ディメンション セットのみをサポートします。 外注明細行や外注時間トランザクションの購入価格設定および既定設定の場合、属性は **ロール** と **予約可能なリソース** です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
