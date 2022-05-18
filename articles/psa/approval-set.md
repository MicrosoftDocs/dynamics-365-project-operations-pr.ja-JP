---
title: Project Service Automation の承認セット
description: このトピックでは、承認セット、要求、およびそれらの操作のサブセットについて説明します。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583314"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation の承認セット

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

承認セットは、承認要求を操作のより小さなサブセットにグループ化します。 このグループ化により、承認はプロジェクトごとに順番に処理され、再試行と順序付けが可能になります。 グループ化により、大量の承認に対する承認処理の信頼性と追跡可能性が向上します。

承認セットは、関連するレコードの全体的な処理状態を示します。 承認セットを使用して承認レコードが処理されると、レコードは **提出済み** から **承認済** になり、承認セットからリンク解除されます。 承認のために提出されたときにレコードが失敗した場合、レコードの状態は **提出済み** のままで、承認セットは失敗としてマークされます。 承認セットには、失敗のエラー メッセージが記録されます。

## <a name="processing-approvals-and-approval-sets"></a>処理中の承認と承認セット
処理待ちの承認は、**処理中の承認** ビューに表示されます。 システムは、すべてのエントリを非同期で複数回処理しようとしますが、これには以前の試みが失敗した場合の承認の再試行も含まれます。

**承認セットの有効期間** フィールドには、セットが失敗としてマークされるまでに残された処理の試行回数が記録されます。

## <a name="failed-approvals-and-approval-sets"></a>失敗した承認と承認セット
**失敗した承認** ビューには、ユーザーの介入が必要なすべての承認が一覧表示されます。 関連する承認セットのログを開いて、失敗の原因を特定します。
**再試行** を選択すると、承認セットの有効期間カウントが追加され、承認セット状態が **処理中** に戻り、残りのレコードの処理を試みます。

## <a name="configure-approval-sets"></a>承認セットの構成

###  <a name="enable-the-approval-sets-feature"></a>承認セット機能を有効にする
承認セット機能を有効にする前に、現在処理中の承認がないことを確認してください。

- **プロジェクト パラメーター** ページに移動し、**機能コントロール** > **最新の承認を有効にする** を選択します。

### <a name="turn-off-the-approval-sets-feature"></a>承認セット機能を無効にする
承認セット機能を無効にする前に、現在処理中の承認がないことを確認してください。

- **プロジェクト パラメーター** ページに移動し、**機能コントロール** > **最新の承認を無効にする** を選択します。

### <a name="configuring-the-asynchronous-threshold"></a>非同期しきい値を構成する 
承認セットを作成すると、承認のために選択したレコード数が指定されたしきい値を超えると、処理はバックグラウンドに移動します。 **非同期しきい値** フィールドを使用して、承認処理を同期または非同期で実行する時期を構成します。
有効な値は:

  - ゼロ: すべての要求は非同期に処理されます。 
  - 0 より大きい数値: 承認は、提出された承認の数がこの値を超えた場合にのみ非同期に処理されます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
