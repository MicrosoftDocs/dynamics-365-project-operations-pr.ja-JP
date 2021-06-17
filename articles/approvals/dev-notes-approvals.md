---
title: 承認のための開発者向けノート
description: このトピックでは、承認作業に関する開発者の追加情報を提供します。
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996797"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="afc01-103">承認のための開発者向けノート</span><span class="sxs-lookup"><span data-stu-id="afc01-103">Developer notes for Approvals</span></span>

<span data-ttu-id="afc01-104">_**適用対象 :** リソース/非在庫ベースのシナリオに使用するプロジェクト オペレーション、見積請求に対応する小規模のデプロイ_</span><span class="sxs-lookup"><span data-stu-id="afc01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="afc01-105">Dynamics 365 Project Operations には、承認段階で正しいレコードを確実に移行できる検証ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="afc01-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="afc01-106">正しいレコードの移行により次のことが保証されます :</span><span class="sxs-lookup"><span data-stu-id="afc01-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="afc01-107">すべてのサポート行は、ジャーナルや実績などの関連テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="afc01-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="afc01-108">承認者は、プロジェクトを進める前に **プロジェクト承認者** としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="afc01-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]