---
title: 2021 年 12 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations
description: この記事は、リソース/非在庫ベースのシナリオの Project Operations の 2021 年 12 月リリースで利用可能な品質更新について説明します。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 79ae9f49a4291d162a8a9bb6eb9a22d615773f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910866"
---
# <a name="whats-new-december-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 12 月の新機能 - リソース/非在庫ベースのシナリオ向け Project Operations

*適用対象: リソース/非在庫ベースのシナリオ向け Project Operations*

この記事は、Microsoft Dynamics 365 Project Operations の次のコンポーネントとバージョンに適用されます。

- Dataverse 環境のバージョン 4.27.0.195、4.27.0.242、4.27.0.244 の Project Operations
- Dynamics 365 Finance 環境バージョン 10.0.23 でのプロジェクト管理と会計

## <a name="features-included-in-this-release"></a>このリリースが含む機能

- システム管理者向けトラブルシューティングを改善しました。 ユーザーがプロジェクトを開くことができない場合、管理者は Project for the Web が生成する[プロジェクト スケジュール ログ](../project-management/schedule-api-logs.md)の関連エラーで確認することができます。
- [Microsoft Project for the Web のタスク チェック リストを使用する](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)。 Microsoft Project for the Webでは、タスクにチェックリストを追加して、特定の項目を追跡できます。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations の二重書き込みのマッピングの更新

今回のリリースでは、Project Operations の二重書き込みマッピングの更新はありません。 Project Operations の二重書き込みマッピングの最新のリストとバージョンについては、[Project Operations 二重書き込みマッピングのバージョン](../environment/resource-dual-write-maps.md)を参照してください。

常に最新バージョンのマッピングを環境で実行し、Project Operations Dataverse ソリューションや Finance ソリューションのバージョンを更新する際に、関連するすべてのテーブル マッピングを有効にします。 マップの最新バージョンが有効になっていない場合、一部の機能が正しく機能しない可能性があります。 マッピングのアクティブなバージョンは、**二重書き込み** ページの **バージョン** の列で確認できます。 新しいバージョンのマッピングをアクティブ化するには、**テーブル マッピングのバージョン** を選択し、最新バージョンを選択した後で、選択したバージョンを保存します。 すぐに使用できるテーブル マップをカスタマイズした場合は、変更を再適用します。 詳しくは、[アプリケーションのライフサイクル管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) を参照してください。

マップの開始時に問題が発生した場合は、二重書き込みトラブルシューティング ガイドの [マップでのテーブル列の欠落の問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) セクションにある指示に従ってください。

## <a name="quality-updates"></a>品質更新プログラム

### <a name="project-operations-on-dataverse"></a>Dataverse の Project Operations

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| 計画と追跡 | 2392596 | スケジュールAPIで、 **残りの作業**、**完了した作業**、**% 完了** の各フィールドを更新できるようになりました。 |
| 計画と追跡 | 2478497 | スケジュール API の **アクティビティ番号** と **タスク ID** のフィールドは、システムが自動採番で入力するため、入力時に空白にすることができます。|
| 時間と経費 | 2468135 | 承認の再試行回数が 5 回から 3 回に減りました。 |
| 時間と経費 | 2468188 | **注釈** エンティティの **notetext** 属性で、ログテキストが最大長を超える問題を修正しました。 |
| 請求と価格 | 2488698 | 環境設定に Finance から入力された元帳エンティティ レコードがない場合に発生するエラー メッセージを更新しました。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance でのプロジェクト管理および会計の概要

| **機能** | **照合番号** | **品質更新プログラム** |
| --- | --- | --- |
| プロジェクト管理および会計 | [587187](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D587187&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225501421%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=qpKECMgKZe9sHGVZUhBxs%2F4ou3fXIiFFg2amMTJ6t9U%3D&amp;reserved=0) | 会社間収益勘定はは、消費税グループが含まれていない **すべて - すべての明細行** のみを考慮しています。 |
| プロジェクト管理および会計 | [599568](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599568&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225600986%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=IudfEjWmkNeiTsWmR%2Fu2oR0CnnCkffAshvqZJuF76q8%3D&amp;reserved=0) | 定額の推定値が正しく計算されていません。 |
| プロジェクト管理および会計 | [602728](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227094434%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Q2%2BveFHlGrzg4QHtqcgeqjyZSQkmpr%2Fku7oObKHMB9g%3D&amp;reserved=0) | 適用されたリテーナーのケースでプロジェクトの請求書による収益を計上すると、伝票上の取引のバランスが正しく取れないという問題がありました。 |
| プロジェクト管理および会計 | [610906](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610906&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=xDBnz10T71GmOZt78ooFK3SYvmTLoC5fj1OftYNYDpY%3D&amp;reserved=0) | Project Operations の実績と統合するためのパフォーマンスの改善。 |
| プロジェクト管理および会計 | [618670](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D618670&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227203949%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PqvHsTGLcQ3bYbUlzYABYhl7J9v2zbnjcOgm%2FTvXB20%3D&amp;reserved=0) | 時間コストの取引が **元帳を使用しない** または **元帳がない** で計上されている場合、ユーザーは請求書を発行できません。 |
| プロジェクト管理および会計 | [623818](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D623818&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227303517%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=LAfdEiuKG8DoGk8O48MRLuaKYDINhCyMAtrlpGvVAw0%3D&amp;reserved=0) | バッチジョブは、1 つの仕訳の転記が失敗し、残りの仕訳が処理されないと失敗します。  |
| 出張と経費 | [575378](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575378&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225451644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3tW0ngQqcz8pdNFY8FVuFlsgv3l73HMgeQTLbzIAAOg%3D&amp;reserved=0) | 添付されていない経費の承認状況が変更できるようになりました。 |
| 出張と経費 | [592997](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D592997&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225521336%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=0leQsokHcl2NLqePFXC6%2BuH1V5UNRWUIPx0wTUaB4vg%3D&amp;reserved=0) | ワークフローに登録された経費報告書では、新しい経費項目を作成することができます。 |
| 出張と経費 | [594853](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D594853&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225541248%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=5PINC45EBeV8PC0Cvtt0QPPJn0VYQ%2FRCjBmlEsZJCq4%3D&amp;reserved=0) | 経費精算書の未転記の経費明細をリセットできます。 |
| 出張と経費 | [599821](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599821&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225610944%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=eb2CAb8L9IUDxDoukDcZQxNyI3TNQtFO%2FcjycucNj44%3D&amp;reserved=0) | 経費の所有者が従業員である未接続の支出がある場合、経費のキャッシング機能を有効にすることはできません。 |
| 出張と経費 | [601446](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601446&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225650767%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Z4CBMqrmYtlIEBWxzMEBf%2BXu5dlst7NnKcQ62yoV%2BWM%3D&amp;reserved=0) | 出張リクエストが null に設定されている場合、**IsPreAuthorized** を経費ヘッダーで有効にしないでください。 |
| 出張と経費 | [601753](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601753&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225660718%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PVwbDhH5uqGJJZTNLddsHYlHsCknK%2FC%2FY%2Btg6fu8heo%3D&amp;reserved=0) | **経費管理** の **Billable** フィールド経費が保存されるとクリアされます。 |
| 出張と経費 | [602009](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602009&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225680636%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=t3m29Vkxx8g96CvaDz%2FRzuciP2doP2xejomPl440wNs%3D&amp;reserved=0) | サブカテゴリーに **課税から除外する** が選択されている項目を削除すると、その経費報告書では **税込み** のスライダーが **いいえ** に移動します。 |
| 出張と経費 | [607516](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D607516&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225849894%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2BceTskfUl1kTe2XHk6QSYu9UN%2FE%2F9nP2gv20kVweURA%3D&amp;reserved=0) |会計イベントが空で、会計の状態が正しくありません。 |
| 出張と経費 | [617801](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617801&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919226337756%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=L69x65xY6LQDS1u2sUbVX5QKEYgbDh6lld2Pm%2BSsUyI%3D&amp;reserved=0) | クレジットカード取引で経費が分割された場合、ワークフローが経費レポートを正しく評価しません。 |
| 出張と経費 | [575295](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575295&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227074518%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=FyrzO1Yx%2BWLfw5arIrFiW07QZC%2F%2BpUk3ekx3g66X8bE%3D&amp;reserved=0) | ベンダーの銀行取引の不適切な報告通貨額が、経費報告書から閉鎖された期間に計上されてしまう。 |
| 出張と経費 | [610910](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610910&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=P6wVchjx9GcH7nZ07yg3%2FuEFht6Df7Ew5Z4hSL%2BQ8oY%3D&amp;reserved=0) | 経費レポートの再構築機能では、経費の作成時に支払い方法を変更した場合でも、既定の支払い方法が支出行に入力される。 |
| 出張と経費 | [617146](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617146&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227193996%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=134C%2BXGuzA8GmM7ZjWYaiYQfNqnV9a1mEKuzrh0hzpw%3D&amp;reserved=0) | 領収書ポリシーが有効になっている場合、経費報告書を提出できない。 |
| 出張と経費 | [619783](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D619783&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227243778%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=pV1rLgOniDy3hXMHAtXeD9o4ZPTmyhZHd7O7zCUpLLs%3D&amp;reserved=0) | 経費報告書を提出すると、次のエラーが発生します: **スタック トレース: 会社が存在しません**。 |
| 出張と経費 | [620773](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D620773&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227253737%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2B5ZZAsXV%2FM29%2Byg6JoGzwJFRa1Fi4NDj4BB38ZeYTH0%3D&amp;reserved=0) | 会社間取引の経費項目では、添付されていない取引が経費報告書に再追加されても、分配で法人が更新されない。 |
| 出張と経費 | [621967](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D621967&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227273644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=RdiupzmL8Dp8nqQIHu9rGMTdJ%2FVVhqN5EIP5uFYS2W4%3D&amp;reserved=0) | プロジェクトに関連し、インポートされたクレジットカード取引を使用して外貨建てで作成された経費報告書で、ベンダー取引の報告通貨での販売価格と金額が正しく計算されない。 |
