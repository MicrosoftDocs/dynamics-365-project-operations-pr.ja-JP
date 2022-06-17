---
title: 承認のための開発者向けノート
description: この記事では、承認作業に関する開発者向けの追加情報を提供します。
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924758"
---
# <a name="developer-notes-for-approvals"></a>承認のための開発者向けノート

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Dynamics 365 Project Operations には、承認段階で正しいレコードを確実に移行できる検証ロジックが含まれています。 正しいレコードの移行により次のことが保証されます : 

  - すべてのサポート行は、ジャーナルや実績などの関連テーブルに作成されます。
  - 承認者は、プロジェクトを進める前に **プロジェクト承認者** としてマークされます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]