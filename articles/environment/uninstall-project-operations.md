---
title: Dynamics 365 Project Operations atinstalēšana
description: Šajā tēmā ir sniegta informācija par to, kā atinstalēt Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783652"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dynamics 365 Project Operations atinstalēšana 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai atinstalētu Dynamics 365 Project Operations, ir jāpiešķir administratora loma.

1. Dodieties uz **Iestatījumi** > **Risinājumi**.

    ![Iestatījumu lapa.](./media/uninstall-proj-ops-solutions.png)
  
2. Noņemiet risinājumus tādā secībā, kā norādīts tālāk sniegtajā tabulā. 

    | Solis | Risinājuma nosaukums                                    | Piezīme                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 2 | ProjectOperations_Anchor                           | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 5 | ProjectService                                     | Nav papildu piezīmju.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Nav papildu piezīmju.                                                                         |
    | 7 | ProjectServiceCore                                 | Nav papildu piezīmju.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 9 | FieldServiceCommon                                 | Obligāts, lai rakstītu ar Dynamics 365 Financevai Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Obligāts, lai rakstītu ar Dynamics 365 Financevai Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Obligāts ar Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 19 | Dynamics365Notes                                   | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 21 | DualWriteCore                                      | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 23 | Dynamics365AssetManagement                         | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 26 | HCMCommon                                          | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 28 | Iesaistītā puse                                              | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 29 | Dynamics365Company                                 | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 30 | CurrencyExchangeRates                              | Ja risinājums nav atrasts, izlaidiet to.                                                            |
    | 31 | AssetCommon                                        | Ja risinājums nav atrasts, izlaidiet to.                                                            |