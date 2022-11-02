---
title: セキュリティと承認
description: この記事では、Microsoft Dynamics 365 Project Operations での承認の操作に関するセキュリティ設定について説明します。
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709403"
---
# <a name="security-and-approvals"></a>セキュリティと承認

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_

Microsoft Dynamics 365 Project Operations は、2 つのセキュリティ ロールを使用して、時間、経費、および材料のエントリの承認を可能にします。

- プロジェクト承認者
- プロジェクト承認者管理

## <a name="project-approver"></a>プロジェクト承認者

**プロジェクト承認者** セキュリティ ロールを使用して、プロジェクトの時間、経費、および材料のエントリを承認します。 **プロジェクト** のような関連する関連エンティティへのアクセス権も必要です。 そのアクセス権は、**プロジェクト管理者** ロールを持つ人に割り当てることができます。 さらに、プロジェクトのチーム メンバーであり、承認者としてマークされている必要があります。

非プロジェクト エントリを承認するには、提出者の管理者である必要があります。

## <a name="project-approver-admin"></a>プロジェクト承認者管理

> [!NOTE]
> プロジェクト承認者管理機能を使用する前に、[承認セット](approval-sets.md) 機能を有効にする必要があります。

**プロジェクト承認者管理** セキュリティ ロールを使用すると、ユーザーはポリシーをバイパスし、すべてのプロジェクトでエントリを承認できます。 この役割を割り当てると、チーム メンバーシップと承認者としてのマークが必要な検証ロジックがバイパスされます。 自分に割り当てられたセキュリティ ロールによって、**プロジェクト** などの関連するテーブルにアクセスできる必要があります。

SYSTEM ユーザー コンテキストは、プロジェクト承認者管理セキュリティ ロールと同じ方法で検証をバイパスします。
