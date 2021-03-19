---
title: Project Service Automation 更新プログラム リリース 16、V3 の新機能と変更点
description: このトピックには、Project Service Automation 更新プログラム リリース 16、V3 で利用可能な機能と修正をリスト化しています。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280899"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation 更新プログラム リリース 16、V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 の Project Service Automation アプリケーションの最新の更新情報をお知らせします。 このリリースには、品質、パフォーマンス、操作性に関するいくつかの重要な改善が含まれています。  このリリースは、Dynamics 365 9.x と互換性があります。 このリリースへと更新をするには、Dynamics 365 オンラインの管理センターにアクセスし、ソリューション ページにアクセスして更新プログラムをインストールしてください。 詳細については [優先ソリューションのインストールと更新](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page) を参照してください。
このトピックには、PSA V3 更新プログラム 16 の新機能または変更された機能と修正をリスト化しています。 このバージョンのビルド番号は V3.10.6.34 であり、一般的には 2020年1月 の自己プログラム更新の処理を通じて入手できます。


## <a name="update-release-16"></a>更新プログラム 16

### <a name="bug-fixes"></a>バグ修正

-   時間と経費

    -   修正済み：承認のために削除された時間と経費の入力を提出しようとすると、関連するエラーメッセージが表示される。

-   プロジェクト管理

    -   修正済み：テンプレートでチームメンバーに定義されているリソースの単位は、テンプレートと共にに新しいプロジェクトに適用されます。

    -   修正済みレコード所有権の再割り当て処理を改善しています。

    -   修正済み：コピー中のプロジェクトは、すべてのコピー操作が完了するまでコピーできません。

-   リソース管理

    -   修正済み：予約の延長にて、短い期間が正しく処理されるようになり、延長予約でゼロ時間が作成されなくなりました。

    -   修正済み：プロジェクトのタイムゾーンが+5：30 GMTで、ユーザーの時間が異なる場合に、調整ビューがレンダリングされるようになりました。

-   Sales

    -   修正済み：契約ラインにマッピングされたプロジェクトが削除され、新しいプロジェクトがマッピングされた場合に、新しいプロジェクトの実際のレコードに対する、契約ラインで定義された請求、価格設定のルールに基づいた再評価がされていませんでした。 この挙動は本リリースで修正されています。 新しくマッピングされたプロジェクトの価格設定と実際のレコードは、契約ラインの価格設定と請求のルールに基づいて取り消され、正しく再作成されます。 マッピングされていないプロジェクトの実際のレコードも、結果として再評価され、再作成されます。

    -   修正済み：見積明細の **金額** フィールドに対する評価が追加され、null 値が保存されないようになりました。

    -   修正済み：プロジェクトで実績が更新されたときに、更新ボタンがプロジェクトのメイン フォームに追加され、ユーザーが実績値を再同期できるようになりました。

    -   修正済み：2.X から 3.X にアップグレードすると、プロジェクト名に NULL 値を持つプロジェクトが許容されます。



[!INCLUDE[footer-include](../includes/footer-banner.md)]