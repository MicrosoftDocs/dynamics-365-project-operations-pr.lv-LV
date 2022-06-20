---
title: Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi
description: Šajā rakstā ir aprakstīts, kā konfigurēt schedule board programmā Microsoft Dynamics 365 Project Operations, lai rādītu apakšuzņēmēju resursu noslodzi, kad tiek pieprasīts personāls projekta resursiem.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919839"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi 

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Schedule Board in Microsoft Dynamics 365 Project Operations var izmantot resursu meklēšanai divos veidos:

- Vispārēja resursu meklēšana bez konteksta, kas saistīta ar noteiktām uz projektiem balstītām resursu vajadzībām.
- Vajadzības resursu meklēšana, kur projekta vajadzības nodrošinās piedāvāto resursu kontekstu.

Lai paziņotu grafika panelim par apakšuzņēmēju resursu noslodzi un līgumdarbiniekiem, ir jāatjaunina grafika dēļa iestatījumi. Šie atjauninājumi ietver: 
- Atjaunināt grafika dēļa iestatījumus vispārējai resursu meklēšanai.
- Atjaunināt grafika dēļa iestatījumus uz vajadzībām balstītai resursu meklēšanai.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atjaunināt grafika dēļa iestatījumus vispārējai resursu meklēšanai
### <a name="update-filters-for-general-resource-search"></a>Atjaunināt filtrus vispārējai resursu meklēšanai
Meklējot resursu, ir jāatjaunina grafika panelī pieejamie filtri, lai varētu meklēt arī ārējos resursus, norādot kādu no šīm darbībām vai visas no šīm darbībām:
  - Darbinieka tips, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
  - Kreditora uzņēmums, kuram pieder resurss.
  - Resursi, kas pieder noteiktai apakšuzņēmuma vai apakšuzņēmuma rindai.
    
### <a name="update-retrieve-resource-query"></a>Atjaunināt izgūt resursu vaicājumu
Lai izmantotu šos papildu filtra atribūtus, ir jāatjaunina arī meklēšanai izmantotais vaicājums. Lai atjauninātu grafika dēļa konfigurāciju vispārējai resursu meklēšanai, veiciet šādas darbības:  
1. Atveriet **grafika dēļa iestatījumus** noteiktam grafika dēlim.
2. **Atveriet cilni Vispārīgie iestatījumi** un ritiniet līdz **citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet filtra izkārtojumu **uz** projekta operāciju **Lite noklusējuma filtra izkārtojumu**.
4. Atjaunināt **izgūt resursu vaicājumu** uz **Project Operations Lite noklusējuma izgūšanas resursu vaicājumu**.

![Atjaunināt grafika dēļa iestatījumus vispārējai resursu meklēšanai](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atjaunināt grafika dēļa iestatījumus uz vajadzībām balstītai resursu meklēšanai
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atjaunināt filtrus resursu meklēšanai, kas attiecas uz prasībām 
Meklējot resursu, ir jāatjaunina grafika panelī pieejamie filtri, lai varētu meklēt arī ārējos resursus, norādot kādu no šīm darbībām vai visas no šīm darbībām:
 - Darbinieka tips, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
 - Kreditora uzņēmums, kuram pieder resurss.
 - Resursi, kas pieder noteiktai apakšuzņēmuma vai apakšuzņēmuma rindai.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atjaunināt izgūt resursu vaicājumu vajadzībai specifisku resursu meklēšanai 
Lai izmantotu šos papildu filtra atribūtus, ir jāatjaunina arī meklēšanai izmantotais vaicājums. Lai atjauninātu grafika dēļa konfigurāciju uz vajadzībām balstītai resursu meklēšanai, veiciet tālāk norādītās darbības.

1. Atveriet **grafika dēļa iestatījumus** noteiktam grafika dēlim un pēc tam atlasiet **Atvērt noklusējuma iestatījumus**, lai atvērtu iestatījumus konkrētai vajadzībai paredzētai meklēšanai.
2. **Atveriet cilni Vispārīgie iestatījumi** un ritiniet līdz **citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet filtra izkārtojumu **uz** projekta operāciju **Lite noklusējuma filtra izkārtojumu**.
4. Atjaunināt **izgūt resursu vaicājumu** uz **Project Operations Lite noklusējuma izgūšanas resursu vaicājumu**.
5. Atveriet cilni **Grafika tipi** un dodieties uz **Project**.
6. Sadaļā Project iestatījumi **atjauniniet** Schedule Assistant Retrieve Resources Query to Default Retrieve Resources Query **for** Default Retrieve Resources Query for Project Operations Lite **un atjauniniet** Schedule Assistant Izgūt ierobežojumus Vaicājums **noklusējuma** izgūšanas ierobežojumu vaicājumam projekta operācijām Lite **.**

![Atjaunināt grafika dēļa iestatījumus uz vajadzībām balstītai resursu meklēšanai](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
