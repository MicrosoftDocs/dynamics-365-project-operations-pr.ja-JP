---
title: 時間エントリ の UI の動作
description: このトピックでは、時間エントリの UI の動作について説明します。
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961721"
---
# <a name="time-entry-ui-behavior"></a>時間エントリ の UI の動作

_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_


**週単位の時間エントリ** グリッドは、2 つのメイン セクション、**ディメンション**および**期間**を持つ カスタム コントロールです。

## <a name="dimensions"></a>ディメンション
**ディメンション** セクションには、時間を入力できるディメンションが表示されます。 次のディメンションは、標準でサポートされています。

  - Project
  - プロジェクト タスク
  - ロール
  - 型
  - 入力の状態

**ディメンション** セクションではインライン編集はできません。 このセクションは、カスタム フィールドを毎週の時間エントリ グリッドに追加できるように、ビューにより支えられています。

## <a name="duration"></a>時間
期間セクションには、列見出しとしてその週の曜日が示されます。 このセクションはインライン編集が可能です。 適切なディメンションで時間エントリ行が作成された後、ユーザーはそれらのディメンションで使用した時間数をすばやく入力できます。

## <a name="create-a-new-time-entry"></a>新しい時間エントリを作成します

1. 時間エントリ グリッドで、**新規**を選択します。 
2. **時間入力簡易作成フォーム** ダイアログ ボックスで、時間エントリ日付を選択します。
3. **プロジェクト**のデータ、**プロジェクトのタスク**、**ロール**、および**期間**のディメンションを入力します。 この情報は、数値と共に **h**、**m**、または **d** を入力して、分、時、または日単位で追加される必要があります。 
4. エントリの説明および時間エントリに関連して外部に共有できるコメントを入力します。 

エントリを保存した場合、入力した値は**ディメンション** セクションに表示されます。 **期間**フィールドに入力した情報は、時間エントリの作成対象の日付に表示されます。

検索フィールドはシステム ビューに支えられています。 たとえば、ユーザーがプロジェクトを入力すると、**プロジェクト タスク** フィールドは、**コピー** ビューに既定で設定されます。 ユーザーに割り当てられていないタスクの時間エントリを作成するには、検索ダイアログ ボックスの **ビューの変更** を選択し、**すべてのアクティブなプロジェクト タスク** ビューを選択します。

## <a name="edit-a-time-entry"></a>時間エントリの編集 
時間エントリ ページでの一部のフィールドの詳細、**説明** と **外部コメント**などは、週単位の時間エントリ グリッドに表示されません。 代わりに、小さな三角の指標が、詳細情報がある**期間**のセルに表示されます。 

1. 時間エントリを編集するには、時間エントリで更新するセルを選択します。
2. **詳細の編集**を選択し、**時間エントリ メイン フォーム** ウィンドウでデータを更新します。 

## <a name="copy-a-time-entry-row"></a>時間エントリ行のコピー
行が作成された後、行全体を新しい行にコピーする場合は、**行のコピー**を選択します。 行がこのようにコピーされると、ディメンション、期間もコピーされます。 **行の編集**を選択して、**期間**セクションのディメンション値と期間を更新することもできます。

## <a name="open-a-time-entry-behavior"></a>時間エントリを開くの動作
最も目立つフィールドに最適かつ迅速に入力できるようにするために、週単位の時間エントリ グリッドには、選択済みのディメンションと期間のサブセットが表示されます。 単一の時間エントリのすべての情報を **エントリの編集** で表示するには、**開く**を選択します。

## <a name="submit-a-time-entry"></a>時間エントリを送信する
セルのブロックまたは時間エントリ行全体を選択した後、**送信**を選択して、単一の時間エントリまたは時間エントリの単一のグループを送信できます。 送信された時間エントリは、承認者の **承認** ページで承認が保留になっているエントリとして表示されます。 時間エントリが正常に送信されると、編集できなくなります。

## <a name="recall-a-time-entry"></a>時間エントリの取り消し
送信済みの時間エントリを取り消すことができます。 単一の時間エントリ、時間エントリの単一のブロック、または時間エントリ行全体を取り消すことができます。 取り消した時間エントリは編集できます。

## <a name="time-entry-status"></a>時間エントリの状態

- **下書き**: 新しい時間エントリには、**下書き**状態が自動的に割り当てられます。 **下書き** の状態の時間エントリしか削除できません。
- **送信済み**: 時間エントリを送信すると、その状態が**送信済み**に更新されます。 
- **承認済み**: 送信した時間エントリが承認されると、その状態が**承認済み**に更新されます。 
- **差し戻し済み**: 時間エントリが拒否されると、その状態が**差し戻し済み**に更新され、エントリは収集および再送信の対象となります。 

## <a name="view-rejection-comments"></a>拒否のコメントを表示する
時間エントリが承認者に拒否された場合、承認者は、リソースが拒否の理由を理解しやすいように、コメントを付けることができます。 時間エントリの拒否のコメントを表示するには、**エントリを開く** を選択します。 拒否のコメントはタイムラインに表示されます。 ユーザーは、エントリを再送信する前に、拒否のコメントに応答できます。

## <a name="copy-week"></a>週のコピー
いくつかの時間エントリが作成された後、ユーザーは同時に複数の時間エントリを作成することができます。

1. **時間エントリ** フォームで、**週のコピー**を選択して、追加の時間エントリを一括作成できます。 
2. **コピー** ダイアログ ボックスの**期間開始**セクションで、**開始日**および**終了日**フィールドを使用して、時間エントリをコピーする場合のコピー元の日付範囲を定義します。 
3. フィールド **終了期間** セクションあるいは**開始日** フィールドで、時間エントリを作成する日付を指定します。 
4. **コピー**を選択します。 **終了期間**で作成済みの日付に対し、**開始期間**の対象の週の、対応する曜日の時間エントリのコピーが作成されます。 たとえば、先週の月曜日の時間エントリは、**終了期間**として指定された週の月曜日にコピーされます。

## <a name="import"></a>インポート
同一の基本プロセスが、予約、割り当て、および交換からインポートして使用されます。 予約のインポート元の日付範囲を指定し、時間エントリの下書きにコピーされる予約を明示的に選択することができます。 
