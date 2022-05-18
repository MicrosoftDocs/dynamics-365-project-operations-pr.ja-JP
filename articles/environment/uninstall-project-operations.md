---
title: Dynamics 365 Project Operations をアンインストールする
description: このトピックでは、Dynamics 365 Project Operations のアンインストール方法について説明します。
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575862"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dynamics 365 Project Operations をアンインストールする 

_**適用対象:** リソース/非在庫ベースのシナリオ向け Project Operations_

Dynamics 365 Project Operations をアンインストールするには、管理者の役割を割り当てる必要があります。

1. **設定** > **ソリューション** に移動します。

    ![設定ページ。](./media/uninstall-proj-ops-solutions.png)
  
2. 次の表に記載されている順番通りに、ソリューションを削除します。 

    | Step | ソリューション名                                    | メモ                                                                                          |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 6 | msdyn_ProjectServiceUpgrade_managed.cab            | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 2 | ProjectOperations_Anchor                           | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 5 | ProjectService                                     | 追加のメモはありません。                                                                         |
    | 6 | ProjectServiceCore_Patch                           | 追加のメモはありません。                                                                         |
    | 7 | ProjectServiceCore                                 | 追加のメモはありません。                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 9 | FieldServiceCommon                                 | Dynamics 365 Finance または Dynamics 365 Supply Chain Management でのに二重書き込みに必要です。   |
    | 10 | msdyn_AssetCommon                                  | Dynamics 365 Finance または Dynamics 365 Supply Chain Management でのに二重書き込みに必要です。   |
    | 11 | msdyn_TESA_Anchor                                  | Dynamics 365 Field Service に必要となります。                                                     |
    | 12 | msdyn_TESA_Patch                                   | Dynamics 365 Field Service に必要となります。                                                     |
    | 13 | msdyn_TESA                                         | Dynamics 365 Field Service に必要となります。                                                     |
    | 14 | ResourceSchedulingControls                         | Dynamics 365 Field Service に必要となります。                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Dynamics 365 Field Service に必要となります。                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Dynamics 365 Field Service に必要となります。                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Dynamics 365 Field Service に必要となります。                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 19 | Dynamics365Notes                                   | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 21 | DualWriteCore                                      | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 22 | Dynamics365AssetManagementApp                      | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 23 | Dynamics365AssetManagement                         | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 25 | Dynamics365FinanceExtended                         | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 26 | HCMCommon                                          | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 28 | 関係者                                              | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 29 | Dynamics365Company                                 | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 30 | CurrencyExchangeRates                              | 見つからない場合は、このソリューションをスキップしてください。                                                            |
    | 31 | AssetCommon                                        | 見つからない場合は、このソリューションをスキップしてください。                                                            |
