---
title: Resursa pieprasījuma iesniegšana
description: Šajā tēmā ir sniegta informācija par pieprasījuma iesniegšanu par projekta resursu.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080537"
---
# <a name="submitting-a-resource-request"></a>Resursa pieprasījuma iesniegšana

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu. Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.

1. Programmas Project Service Automation (PSA) lapā **Projekti** noklikšķiniet uz cilnes **Grupa** , lai skatītu rezervējamo resursu sarakstu. 
2. Atlasiet vispārējo resursu, kam sarakstā ir resursa prasība, un pēc tam noklikšķiniet uz **Iesniegt pieprasījumu**.

![Resursa pieprasījuma iesniegšana](media/RM-how-to-18.png)

Vispārēja grupas dalībnieka pieprasījuma statuss mainīsies uz **Iesniegts**.

Pēc tam, kad resursu pārvaldnieks ir izpildījis pieprasījumu, vispārējs resurss tiek aizstāts ar nosauktu resursu, ja resursu pārvaldnieks izpilda pieprasījumu ar nosauktā resursa rezervāciju. Pretējā gadījumā vispārējs resurss paliks komandā, un pieprasījuma statuss mainīsies uz **Jāpārskata** , ja resursu pārvaldnieks ir piedāvājis nosauktu resursu.
