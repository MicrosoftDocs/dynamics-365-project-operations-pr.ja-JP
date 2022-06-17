---
title: ホーム ページのレポート作成
description: この記事では、 Dynamics 365 Project Service Automation でのレポート作成に関する情報へのリンクを提供します。
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cf55495cc435d929bd305c9fea270aeb2d62a3da
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921676"
---
# <a name="reporting-home-page"></a>ホーム ページのレポート作成

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation を使うことで、プロジェクトベースの組織は事業の運営を効率的に管理することができます。 どのプロジェクトでも、チーム メンバーは、営業案件、見積もり、および作業の計画の管理、プロジェクトのリソース、計画に従った作業の管理、作業の請求書、そしてプロジェクトを完了するために作業を実行する必要があります。 操作でレポート機能は、組織の正常性を判断し、必要な修正措置を講じるための重要な鍵となります。 PSA はすべてのレポート作成で、Microsoft Dynamics 365 のレポート作成メソッドと技術を使用しています。 レポートのオプションの詳細については、[Dynamics 365 Customer Engagement (on-premises)のレポート作成ガイド、バージョン9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365)を参照してください。

## <a name="report-wizard"></a>レポート ウィザード

レポート ウィザードでは、開発者以外の人が簡単なレポートを作成できます。 アプリが既存のプラットフォーム上に構築されていることから、この体験は、[レポート ウィザードを使用したレポートの作成、または編集](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard)で文書化された体験と同じです。 ただし、Project Service Automation 固有のエンティティを使用します。

## <a name="custom-sql-server-reporting-services-reports"></a>カスタム SQL Server Reporting Service のレポート

あなたのビジネスがレポート ウィザードを使用して作成することができない特定のレポートを必要とする場合は、カスタム レポートを作成できます。 Microsoft Visual Studio と、適切な Microsoft SQL Server Data Tools と Report Authoring Extension がインストールされている必要があります。 ツール、およびバージョンの詳細については、[SQL Server Data Tools を使用したレポート作成環境](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools) を参照してください。 カスタム レポートの作成方法に関しては、[SQL Server Data Tools を使用して新規レポートを作成する](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)を参照してください。

## <a name="power-bi-insights-apps"></a>Power BI インサイト アプリケーション

Microsoft Power BI と Dynamics 365 が組み合わさって、インサイト アプリの形式でデータを処理するパワフルな方法を提供します。 インサイト アプリの可用性については、[Power BI インサイト アプリ ページ](https://powerbi.microsoft.com/power-bi-insights-apps/)を参照してください。


## <a name="additional-resources"></a>その他のリソース
PSA でのレポート作成については、次の記事を参照してください。

- [Project Service のデータ モデルでの作業](reports-working-project-service-data-model.md)
- [ダッシュボード](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
