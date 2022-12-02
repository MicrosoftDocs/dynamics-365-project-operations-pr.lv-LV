---
title: Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi
description: Šajā rakstā ir aprakstīts, kā konfigurēt plānošanas paneli programmā Microsoft Dynamics 365 Project Operations, lai, nodrošinot darbiniekus projekta resursu prasībām, tiktu rādīta apakšuzņēmēja līgumā iekļauto resursu noslodze.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262226"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi 

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Plānošanas panelis programmā Microsoft Dynamics 365 Project Operations var tikt izmantots resursu meklēšanai divos veidos:

- vispārīga resursu meklēšana bez konkrētu projekta resursu prasību konteksta;
- prasību noteikta resursu meklēšana, kad projekta prasība nodrošina ieteikto resursu kontekstu.

Lai informētu plānošanas paneli par apakšuzņēmēja līgumā iekļauto resursu noslodzi un līguma darbiniekiem, ir jāveic plānošanas paneļa iestatījumu atjauninājumi. Šie atjauninājumi ietver: 
- plānošanas paneļa iestatījumu atjaunināšanu vispārējai resursu meklēšanai;
- plānošanas paneļa iestatījumu atjaunināšanu prasību noteiktai resursu meklēšanai;

## <a name="update-schedule-board-settings-for-general-resource-search"></a>plānošanas paneļa iestatījumu atjaunināšanu vispārīgai resursu meklēšanai;
### <a name="update-filters-for-general-resource-search"></a>filtru atjaunināšanu vispārīgai resursu meklēšanai.
Meklējot resursu, plānošanas panelī ir jāatjaunina pieejamie filtri, lai varētu meklēt arī ārējus resursus, norādot vienu vai visus šos datus:
  - darbinieka tips, vai parādītajiem resursiem jābūt līguma darbiniekiem vai darbiniekiem;
  - piegādātāja uzņēmums, kam pieder resurss;
  - resursi, kas pieder noteiktam apakšlīgumam vai apakšlīguma rindai.
    
### <a name="update-retrieve-resource-query"></a>Resursu vaicājumu izgūšanas atjaunināšana
Ir jāatjaunina arī meklēšanā izmantotais vaicājums, lai izmantotu šos papildu filtra atribūtus. Lai atjauninātu plānošanas paneļa konfigurāciju vispārīgai resursu meklēšanai, veiciet tālāk norādītās darbības.  
1. Atveriet sadaļu **Plānošanas paneļa iestatījumi** noteiktam plānošanas panelim.
2. Atveriet cilni **Vispārīgi iestatījumi** un ritiniet līdz **Citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet **filtra izkārtojumu** uz **Project Operations Lite paredzēts noklusējuma filtru izkārtojums**.
4. Atjauniniet **Izgūt resursu vaicājumu** uz **Project Operations Lite paredzēts noklusējuma izgūšanas resursu vaicājums**.

![plānošanas paneļa iestatījumu atjaunināšanu vispārīgai resursu meklēšanai;](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Plānošanas paneļa iestatījumu atjaunināšana prasību noteiktai resursu meklēšanai
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filtru atjaunināšana prasību noteiktai resursu meklēšanai 
Meklējot resursu, plānošanas panelī ir jāatjaunina pieejamie filtri, lai varētu meklēt arī ārējus resursus, norādot vienu vai visus šos datus:
 - darbinieka tips, vai parādītajiem resursiem jābūt līguma darbiniekiem vai darbiniekiem;
 - piegādātāja uzņēmums, kam pieder resurss;
 - resursi, kas pieder noteiktam apakšlīgumam vai apakšlīguma rindai.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Resursa vaicājuma izgūšanas atjaunināšana prasību noteiktai resursu meklēšanai 
Ir jāatjaunina arī meklēšanā izmantotais vaicājums, lai izmantotu šos papildu filtra atribūtus. Lai atjauninātu plānošanas paneļa konfigurāciju prasību noteiktai resursu meklēšanai, veiciet tālāk norādītās darbības.

1. Atveriet sadaļu **Plānošanas paneļa iestatījumi** noteiktam plānošanas panelim un pēc tam atlasiet **Atvērt noklusējuma iestatījumus**, lai atvērtu prasību noteiktas meklēšanas iestatījumus.
2. Atveriet cilni **Vispārīgi iestatījumi** un ritiniet līdz **Citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet **filtra izkārtojumu** uz **Project Operations Lite paredzēts noklusējuma filtru izkārtojums**.
4. Atjauniniet **Izgūt resursu vaicājumu** uz **Project Operations Lite paredzēts noklusējuma izgūšanas resursu vaicājums**.
5. Atveriet cilni **Plānošanas tipi** un pārejiet uz **Projekts**.
6. Sadaļas **Projekts** iestatījumos atjauniniet **Plānošanas palīga resursu izgūšanas vaicājums** uz **Project Operations Lite paredzēts noklusējuma izgūšanas resursu vaicājums** un atjauniniet **Plānošanas palīga ierobežojumu izgūšanas vaicājums** uz **Project Operations Lite paredzēts noklusējuma izgūšanas ierobežojumu vaicājums**.

![Plānošanas paneļa iestatījumu atjaunināšana prasību noteiktai resursu meklēšanai](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
