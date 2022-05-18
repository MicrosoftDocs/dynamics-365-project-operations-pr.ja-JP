---
title: Project Service Automation 統合パラメーター
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation を Microsoft Dynamics 365 Finance と統合するときの既定のデータの入力方法を構成する方法について説明します。
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 70dcf44c0948bfb8f17c51e052b6c76e029d35fd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683682"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 統合パラメーター

[!include[banner](../includes/banner.md)]

**Project Service Automation 統合パラメーター** ページで、Dynamics 365 Project Service Automation を Dynamics 365 Finance に統合するときの既定のデータの入力方法を構成できます。 プロジェクトを Project Service Automation から Finance に正常に同期させるには、次のフィールドを設定する必要があります。

**Project Service Automation 統合パラメーター** ページを開き、**プロジェクト管理および会計** \> **セットアップ** \> **Dynamics 365 for Project Service Automation 統合パラメーター** に移動します。 

> [!NOTE]
> - プロジェクト タスクの統合、経費トランザクション カテゴリ、時間の見積もり、経費の見積もり、および機能のロックはバージョン 8.0 で使用可能です。
> - 実績の統合は、バージョン 8.0.1 以降で使用できます。


| Tab                    | フィールド                | 内容 |
|------------------------|----------------------|-------------|
| 全般                | 既定のプロジェクト タイプ | 既定のプロジェクト タイプを選択します。 プロジェクトが Project Service Automation から同期されるときに、統合テンプレートで既定値を指定しなかった場合、この値が使用されます。 新しいプロジェクトの **プロジェクト タイプ** フィールドは同期中に、この値に設定されます。 ただし、Project Service Automation からプロジェクトの契約品目が同期される場合、値が更新される可能性があります。 |
|                        | 時間カテゴリ        | 既定の時間カテゴリを選択します。 この値は、Project Service Automation から時間の見積もりが同期されるときに使用されます。 Project Service Automation から時間の見積もりと時間の実績が同期されると、Finance で、新しいプロジェクト時間の予測の **カテゴリ** フィールドは、この値に設定されます。 |
|                        | 料金カテゴリ         | 既定の料金カテゴリを選択します。 この値は、Project Service Automation から料金の実績が同期されるときに使用されます。 Project Service Automation から料金の実績が同期されると、Finance で、新しい料金のトランザクションの **カテゴリ** フィールドは、この値に設定されます。 |
| プロジェクト グループの既定値 | プロジェクト タイプ         | **新規** をクリックして、既定のプロジェクト グループを設定するためのプロジェクト タイプを選択する行を追加します。 特定のプロジェクト タイプは、構成で一度だけ選択できます。 |
|                        | プロジェクト グループ        | 選択したプロジェクト タイプの既定のプロジェクト グループを選択します。 統合テンプレートで既定値を指定しなかった場合、新しいプロジェクトが Project Service Automation から同期されるときに、**プロジェクト グループ** フィールドはプロジェクト タイプの既定値に設定されます。 |
| 請求の種類の既定値  | 請求の種類         | **新規** をクリックして、既定の明細行プロパティを設定するための請求の種類を選択する行を追加します。 特定の請求の種類は、構成で一度だけ選択できます。 |
|                        | 明細行プロパティ        | 選択した請求の種類のために、既定の明細行プロパティを選択します。 新しい時間の見積もり、新しい経費の見積もり、または新しい実績が Project Service Automation から同期されると、**明細行プロパティ** フィールドは、請求の種類の既定値に設定されます。 |
| 機能のロック  | 適用なし       | Project Service Automation から取得したプロジェクトおよび契約について、Finance で無効にする機能を選択します。 たとえば、契約およびプロジェクトの編集、作業分解構造の作成、および Finance でのタイムシートの入力機能を無効にできます。 会計関連のフィールドは、パラメーター設定で使用不可に設定された場合でも、引き続き有効になります。 既定では、すべての機能が有効になっています。 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]