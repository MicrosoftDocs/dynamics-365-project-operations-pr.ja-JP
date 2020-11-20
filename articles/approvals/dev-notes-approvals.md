---
title: 承認のための開発者向けノート
description: このトピックでは、承認作業に関する開発者の追加情報を提供します。
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483954"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="7e374-103">承認のための開発者向けノート</span><span class="sxs-lookup"><span data-stu-id="7e374-103">Developer notes for Approvals</span></span>

<span data-ttu-id="7e374-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="7e374-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7e374-105">Dynamics 365 Project Operations には、検証ロジックが含まれており、承認段階での正しいレコードの移行をすることができます。</span><span class="sxs-lookup"><span data-stu-id="7e374-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="7e374-106">正しいレコードの移行により次のことが保証されます :</span><span class="sxs-lookup"><span data-stu-id="7e374-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="7e374-107">すべてのサポート行は、ジャーナルや実績などの関連テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="7e374-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="7e374-108">承認者は、プロジェクトを進める前に **プロジェクト承認者** としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="7e374-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
