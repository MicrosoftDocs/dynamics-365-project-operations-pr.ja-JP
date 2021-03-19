---
title: 収益認識の概要
description: このトピックでは、Project Operations での売上認識について説明します。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278874"
---
# <a name="revenue-recognition-overview"></a>収益認識の概要

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Dynamics 365 Project Operations で売上認識の原則は、プロジェクトやプロジェクトの一部に対して選択した請求方法によって異なります。 このトピックでは、Project Operations での売上認識について説明します。

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>時間と材料の請求方法で会計処理したトランザクション

- コストと収益の認識は関連しています。 トランザクションのコストと未請求売上は [Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md) を使用して転記されます。
- プロジェクトのコストと売上プロファイルは、未請求の売上トランザクションを一般会計に転記するかどうかを決定します。 **売上計上** を選択する場合、システムは転記中に **仕掛品販売額** と **売上計上の販売額** 勘定を使用します。 この方法の例を以下に示します。  

  | トランザクションの種類 | 借方/貸方 | 金額 |
  | --- | --- | --- |
  | 仕掛品販売額 | 借方 | 100 |
  | 売上計上の販売額 | 貸方 | 100 |

- 収益は請求時に認識されます。 システムは転記時に **請求済売上** 勘定を使用します。 この方法の例を以下に示します。  

  | トランザクションの種類 | 借方/貸方 | 金額 |
  | --- | --- | --- |
  | 顧客残高 | 借方 | 120 |
  | 未払い消費税 | 貸方 | 20 |
  | 請求済み売上 | 貸方 | 100 |

- 未請求売上の転記時に売上を計上した場合、システムは請求時に売上計上を取り消します。

  | トランザクションの種類 | 借方/貸方 | 金額 |
  | --- | --- | --- |
  | 仕掛品販売額 | 貸方 | 100 |
  | 売上計上の販売額 | 借方 | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>固定価格の請求方法で会計処理したトランザクション

- コストと収益の認識は独立しています。 トランザクションのコストは [Project Operations の統合仕訳帳](../project-accounting/project-operations-integration-journal.md) を使用して転記されます。 未請求の売上トランザクションは作成されません。
- プロジェクトのコストと収益プロファイルで **プロジェクト完了計算に使用する原則** を **仕掛品なし** に設定する場合は、請求時に売上を認識できます。 この方法は、短期で単純なプロジェクトにのみ使用します。
- **完了した契約** または **完了割合の売上認識** の方法を使用すると、売上を固定価格の売上見積りを使用して認識できます。

## <a name="additional-resources"></a>その他のリソース
[課金プロジェクトの会計構成に関する記事](../project-accounting/configure-accounting-billable-projects.md)

[固定価格売上見積もりプロジェクト](rev-rec-percentage-completion-method.md)

[売上の見積もりの管理](rev-rec-completed-contract-method.md)

[完了までの原価の計算方法](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]