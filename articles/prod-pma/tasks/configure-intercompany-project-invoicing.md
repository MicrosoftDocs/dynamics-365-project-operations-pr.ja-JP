---
title: 会社間プロジェクト請求を構成する
description: このトピックでは、組織内の 2 つの会社間でプロジェクト請求を設定する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079327"
---
# <a name="configure-intercompany-project-invoicing"></a>会社間プロジェクト請求を構成する

[!include [banner](../../includes/banner.md)]

このトピックでは、組織内の 2 つの会社間でプロジェクト請求を設定する方法について説明します。 このタスクでは、USSI データセットを使用します。

1. ナビゲーション ウィンドウで、 **モジュール > 買掛金勘定 > ベンダー > すべてのベンダー** に移動します。
2. **すべてのベンダー** リストで、目的のレコードを見つけて選択します。
3. アクション ウィンドウで、 **全般** を選択します。
4. **会社間** を選択します。
5. **アクティブ** を **はい** に設定し、会社間取引を有効にします。
6. **顧客の会社** フィールドに値を入力するか選択します。
7. **自分のアカウント** フィールドで、値を入力または選択します。
8. **保存** を選択します。
9. ページを閉じてホーム ページに戻ります。
10. ナビゲーション ウィンドウで、 **モジュール > プロジェクト管理および会計 > 設定 > プロジェクト管理および会計パラメーター** に移動します。
11. **会社間** タブを選択します。
12. スライダーを **はい** に移動させ、会社間リソース スケジュールとタイムシートを有効にします。
13. 一覧で、選択された行をマークします。
14. **新規** をクリックします。
15. **借入法人** フィールドで、値を入力するか選択します。
16. **売上の計上** チェック ボックスをオンにします。
17. **既定のタイムシート カテゴリ** フィールドで、値を入力または選択します。
18. **既定の経費カテゴリ** フィールドで、値を入力または選択します。
19. **保存** を選択します。
20. ページを閉じます。
21. ナビゲーション ウィンドウで、 **モジュール > プロジェクト管理および会計 > 設定 > 転記 > 元帳転記の設定** に移動します。
22. **勘定科目の種類** フィールドでオプションを選択します。
23. **新規** をクリックします。
24. 新しい行の **主勘定** フィールドで、必要な値を指定します。
25. **保存** を選択します。
26. ページを閉じます。
27. ナビゲーション ウィンドウで、 **モジュール > プロジェクト管理および会計 > 設定 > 価格 > 移転価格** に移動します。
28. **新規** をクリックします。
29. **有効日** フィールドに日付を入力します。
30. **借入法人** フィールドで、値を入力するか選択します。
31. **移転価格モデル** フィールドでオプションを選択します。
32. **価格** フィールドに数値を入力します。
33. **保存** を選択します。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]