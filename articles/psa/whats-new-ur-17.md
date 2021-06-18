---
title: Project Service Automation 更新プログラム リリース 17、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 17、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006697"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation 更新プログラム リリース 17、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。  このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストール、更新、または削除](/power-platform/admin/install-remove-preferred-solution) を参照してください。

このトピックには、PSA V3 更新プログラム 17 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.6.34 であり、一般的には 2020 年 3 月 の自己プログラム更新の処理を通じて入手できます。


## <a name="update-release-17"></a>更新プログラム 17

### <a name="bug-fixes"></a>バグ修正

**一般**

- 修正済み：Project Service Automation を更新するとチーム メンバー のライセンスが適用されます（プロジェクト リソース ハブにはチーム メンバー サービス プランのメタデータ 3.x が含まれています）
 
**時間と経費**

- 修正済み：経費の見積もりをゼロ以外の価格からゼロ（0）に変更することはできません。 この変更は無視されます。

**プロジェクト管理**

- 修正済み：チーム メンバーの役職名に null 値のチェックが追加されました。
- 修正済み：**msdyn_resourceassignment** エンティティの **msdyn_userresourceid** フィールドは廃止されました。
- 修正済み：2.x から 3.x へのアップグレードでは、タスク割り当てで空のコンターが処理されるようになりました。

**営業**

- 修正済み：**Invoice.PreValidateInvoiceUpdate** では、レコード所有者の再割り当てのシナリオを適切に処理できるようになっています。
- 修正済み：トランザクション クラスが **時間**、**UnitGroup** の場合、**QuoteLineDetails**、**JournalLine**、**InvoiceLineDetail**、**ContractLineDetails** を含むすべてのエンティティで編集できません。 しかし、**JournalLine** と **InvoiceLineDetails** の **単位** が編集できません。




[!INCLUDE[footer-include](../includes/footer-banner.md)]