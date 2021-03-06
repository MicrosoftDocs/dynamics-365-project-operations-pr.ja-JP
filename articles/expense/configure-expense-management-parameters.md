---
title: 経費管理パラメーターの構成
description: このトピックでは、経費管理の一般的な動作を制御するパラメーターについて説明します。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897277"
---
# <a name="configure-expense-management-parameters"></a>経費管理パラメーターの構成

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

このトピックでは、経費管理の一般的な動作を制御するパラメーターについて説明します。

## <a name="general"></a>全般

| フィールド                                                    | 内容 |
|----------------------------------------------------------|-------------|
| マイレージの標準レート                                 | マイレージ経費の払い戻し率を入力します。 このレートに経費として入力されたマイレージを乗算して、出張費の払い戻し額を計算します。 |
| 経費目的の検証                                 | このオプションをオンにすると、ユーザーが経費報告書を作成する際に、**経費報告書の目的**フィールドで構成される既存の一連の値に制限されます。 |
| 支払い者の個人経費                                | 個人として分類されたクレジットカード取引金額の支払いの責任を負う担当者を選択します。 |
| ドリルバックに関する経費報告書全体を表示する               | このオプションを選択すると、経費報告書の転記時に生成された特定の伝票の元のドキュメントの詳細が表示されたときに、経費報告書のすべての経費が表示されます。 |
| 旅行の事前承認が必須である                 | このオプションを選択すると、従業員が経費報告書を提出する前に、出張申請書の提出と承認が必要になります。 |
| 転記前に配分の編集を許可する            | 経費報告書の配布を転記前に編集できるかどうかを選択します。 |
| 経費管理ポリシーを評価する                     | 経費を評価する時期を選択して、経費ポリシーに違反しているかどうかを判断します。 経費は、経費エントリが入力されて保存される際、または経費の承認のために提出される際に、違反に関して評価されます。 必要な領収書のポリシー ルールは、経費明細の保存時に評価されます。 |
| 会社間の経費明細を許可する                         | 他の法人の経費を経費報告書に入力できるかどうかを選択します。 |
| クレジット カード経費の為替レートの編集を許可する | このオプションを選択すると、ユーザーがインポートされたクレジット カード経費の為替レートを編集できるようになります。 |
| 表示する複数レベルの階層フィールド                  | ワークフロー割り当ての種類が階層に設定され、**階層**の選択が承認階層、経費の複数レベル承認を使用するよう設定されている場合に表示される承認者フィールドを選択します。 複数レベルの承認階層がワークフローに使用される場合、選択されたフィールドは経費報告書に表示され、編集することができます。 |
| 従業員のクレジット カード番号を入力する                        | 従業員の**クレジット カード** ページの**カード ID** フィールドで、15 文字または 16 文字の番号を入力して保存できるかどうかを選択します。 |
| 出張申請書の目的を検証する                      | このオプションをオンにすると、ユーザーが出張申請書を作成する際に、**経費報告書の目的**フィールドで構成される既存の一連の値に制限されます。 |

## <a name="financial"></a>金融業

| フィールド                                                                                    | 内容 |
|------------------------------------------------------------------------------------------|-------------|
| 元帳日次仕訳帳名                                                                | 承認された経費報告書が転記される元帳仕訳帳の名前を選択します。 |
| 経費からの税還付を可能にする                                                        | 対象となる経費の経費税の還付を有効にするには、このオプションを選択します。 米国の消費税と使用税ルールが有効になっている場合、このオプションは選択できません。 |
| 現金前払いを直ちに転記する                                                           | 支払いと送金プロセスの完了時に、承認された現金前払いを転記するには、このオプションを選択します。 このオプションが選択されていない場合、支払いと送金プロセスにより、未転記の一般仕訳帳が生成されます。 |
| 転記中に会計日を修正する                                                   | 現在の期間が保留中または終了している場合に、経費が転記される会計日を更新するには、このオプションを選択します。 会計日は次のオープン期間に設定されます。 |
| 支払い方法で指定された相殺勘定に基づいてトランザクションのグループ化を許可する       | 経費の支払い方法で指定された相殺勘定に基づいて、経費報告書の経費トランザクションを要約するには、このオプションを選択します。 |
| 税込み                                                                             | 既定で経費金額に消費税を含めるには、このオプションを選択します。 |
| 出張申請書の決算に関する債務を解除する                                      | 承認された出張申請書の決算時に、債務のある資金を解放するには、このオプションを選択します。 |
| 予算登録およびプロジェクト予算の予算超過時に出張申請書の提出を許可する | 予算登録に設定されている許容予算またはプロジェクトの許容予算のいずれかを超えている場合でも、従業員が承認用の出張申請書を送信できるようにするには、このオプションを選択します。 |
| 予算登録およびプロジェクト予算の予算超過時に経費報告書の提出を許可する     | 予算登録に設定されている許容予算またはプロジェクトの許容予算のいずれかを超えている場合でも、従業員が承認用の経費報告書を送信できるようにするには、このオプションを選択します。 |
| 予算登録のみの予算超過時に経費報告書の承認を許可する                 | このオプションを選択すると、承認者は、予算登録に設定されている許可予算を超える経費報告書を承認できます。 |

## <a name="per-diem"></a>日当

| フィールド                                 | 内容 |
|---------------------------------------|-------------|
| 日当の最小時間            | 従業員が出張関連費の日当を受け取る資格を得るため、1 日に働かなければならない既定の最小時間数を入力します。 この値は、日当レート階層に対する**最小時間**フィールドの既定値としてのみ使用されます。 |
| 食事の割合                          | **食事の減額を計算**フィールドが **1 日あたりの食事の種類**または **1 日あたりの食事回数**のいずれかに設定されている場合、出張関連費の最初と最後の日に使用される食事の日当の既定割合を入力します。 最初と最後の日の作業日は、標準の作業日よりも短い場合があります。 そのため、それらの日の日当は標準額と異なる場合があります。 割合が **0**(ゼロ) に設定されている場合、最初と最後の日の控除額は 0.00 になります。 |
| ホテルの割合                         | 出張関連費の最初と最後の日に使用されるホテルの日当の既定割合を入力します。 最初と最後の日の作業日は、標準の作業日よりも短い場合があります。 そのため、それらの日の日当は標準額と異なる場合があります。 割合が **0**(ゼロ) に設定されている場合、最初と最後の日の控除額は 0.00 になります。 |
| その他の割合                         | 出張関連費の最初と最後の日に使用されるその他の経費の日当の既定割合を入力します。 最初と最後の日の作業日は、標準の作業日よりも短い場合があります。 そのため、それらの日の日当は標準額と異なる場合があります。 割合が **0**(ゼロ) に設定されている場合、最初と最後の日の控除額は 0.00 になります。 |
| 朝食の割合の減少 | 朝食の日当を減らす量を入力します。 たとえば、従業員が無料の朝食を受け取った場合、日当の量を 10％ 減らすことができます。 |
| 昼食の割合の減少     | 昼食の日当を減らす量を入力します。 たとえば、従業員が無料の昼食を受け取った場合、日当の量を 15％ 減らすことができます。 |
| 夕食の割合の減少    | 夕食の日当を減らす量を入力します。 たとえば、従業員が無料の夕食を受け取った場合、日当の量を 25％ 減らすことができます。 |
| 食事の減額を計算する           | 減額が 1 回の出張または 1 日あたりの食事の種類に基づくのか、1 日あたりに許可される食事の回数に基づくのかを選択して、システムが日当の食事の減額を計算する方法を指定します。 |
| 日当の丸め                     | 日当経費に使用する丸めの種類を選択します。 通常の丸めを選択すると、金額が 0.50 の日当経費は 1.00 に切り上げられ、金額が 0.50 未満の日当経費は 0.00 に切り下げられます。 |
| 日当の計算の基準          | 日当金額が暦日または 24 時間に基づくかを選択します。 |

## <a name="fax-cover-pages"></a>FAX の送付状

| フィールド                          | 内容 |
|--------------------------------|-------------|
| 方法                   | 経費報告書に関連する領収書の送信に使用する FAX の送付状を作成するときに、従業員が実行する手順を入力します。 ユーザーの言語に基づいて、表示される言語固有のテキストを入力するには、**翻訳**を選択します。 |
| ユーザー ID(バーコード情報) | FAX の送付状に使用されるバーコードに従業員の一意識別子を保存するには、このオプションを選択します。 |
| バーコード                       | FAX の送付状に使用されるバーコードを選択します。 バーコード 39 および 128 は、経費管理でサポートされています。 |

## <a name="anti-corruption"></a>汚職防止

| フィールド                                 | 内容 |
|---------------------------------------|-------------|
| 汚職防止証明書を表示する   | 経費報告書の作成時に汚職防止テキストを表示するには、このオプションを選択します。 次に、経費報告書で汚職防止証明書を選択する必要がある特定の経費カテゴリを有効にすることができます。 たとえば、政府関係者の経費に関連するギフト カテゴリでは、その経費が政府関係者に関連する会社方針を満たしていることを従業員が確認する必要があります。 |
| 提出者への汚職防止メッセージ | 経費報告書を作成している従業員に表示される必要のあるテキストを入力します。 ユーザーの言語に基づいて、表示される言語固有のテキストを入力するには、**翻訳**を選択します。 |
| 承認者への汚職防止メッセージ  | 経費報告書の作成時に、承認者に表示される必要のあるテキストを入力します。 ユーザーの言語に基づいて、表示される言語固有のテキストを入力するには、**翻訳**を選択します。 |
