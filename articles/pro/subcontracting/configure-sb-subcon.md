---
title: Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi
description: Šajā rakstā ir aprakstīts, kā konfigurēt plānošanas paneli korporācijā Microsoft Dynamics 365 Project Operations, lai parādītu ar apakšuzņēmuma līgumu saistīto resursu noslodzi, nodarbinot projekta resursu prasības.
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

Plānošanas paneli korporācijā Microsoft Dynamics 365 Project Operations var izmantot resursu meklēšanai divos veidos:

- Vispārīga resursu meklēšana bez konteksta, kas saistīts ar konkrētām projekta resursu prasībām.
- Konkrētu resursu meklēšana, kas attiecas uz konkrētām prasībām, kur projekta prasība nodrošinās kontekstu ieteiktajiem resursiem.

Lai paziņotu plānošanas panelim par resursu noslodzes un līgumdarbinieku apakšuzņēmuma līgumiem, jums ir jāveic plānošanas paneļa iestatījumu atjauninājumi. Šie atjauninājumi ietver: 
- Atjauniniet plānošanas paneļa iestatījumus vispārējai resursu meklēšanai.
- Atjauniniet plānošanas paneļa iestatījumus uz prasībām balstītai resursu meklēšanai.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Plānošanas paneļa iestatījumu atjaunināšana vispārīgai resursu meklēšanai
### <a name="update-filters-for-general-resource-search"></a>Atjaunināt filtrus vispārīgai resursu meklēšanai
Meklējot resursu, plānošanas panelī pieejamie filtri ir jāatjaunina, lai varētu meklēt arī ārējos resursus, norādot kādu no šiem elementiem vai to visu:
  - Darba ņēmēja veids, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
  - Kreditoru uzņēmums, kuram vajadzētu piederēt resursam.
  - Resursi, kas pieder konkrētam apakšlīgumam vai apakšlīguma līnijai.
    
### <a name="update-retrieve-resource-query"></a>Resursu vaicājuma izgūšanas atjaunināšana
Meklēšanai izmantotais vaicājums arī ir jāatjaunina, lai izmantotu šos papildu filtra atribūtus. Veiciet tālāk norādītās darbības, lai atjauninātu plānošanas paneļa konfigurāciju vispārīgai resursu meklēšanai.  
1. Atveriet **plānošanas paneļa iestatījumus** konkrētam plānošanas panelim.
2. **Atveriet cilni Vispārīgi iestatījumi** un ritiniet līdz **Citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet filtra izkārtojumu **uz** Noklusējuma filtra izkārtojums **projekta operācijām Lite**.
4. Atjauniniet **resursu izgūšanas vaicājumu** uz **noklusējuma izgūšanas resursu vaicājumu projekta operācijām Lite**.

![Plānošanas paneļa iestatījumu atjaunināšana vispārīgai resursu meklēšanai](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Uz prasībām balstītas resursu meklēšanas plānošanas paneļa iestatījumu atjaunināšana
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atjaunināt filtrus nepieciešamai resursu meklēšanai 
Meklējot resursu, plānošanas panelī pieejamie filtri ir jāatjaunina, lai varētu meklēt arī ārējos resursus, norādot kādu no šiem elementiem vai to visu:
 - Darba ņēmēja veids, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
 - Kreditoru uzņēmums, kuram vajadzētu piederēt resursam.
 - Resursi, kas pieder konkrētam apakšlīgumam vai apakšlīguma līnijai.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Resursu vaicājuma izgūšanas atjaunināšana, lai meklētu resursus, kas saistīti ar konkrētām prasībām 
Meklēšanai izmantotais vaicājums arī ir jāatjaunina, lai izmantotu šos papildu filtra atribūtus. Veiciet tālāk norādītās darbības, lai atjauninātu plānošanas paneļa konfigurāciju uz prasībām balstītu resursu meklēšanai.

1. Atveriet **plānošanas paneļa iestatījumus** konkrētam plānošanas panelim un pēc tam atlasiet **Atvērt noklusējuma iestatījumus**, lai atvērtu iestatījumus nepieciešamajai meklēšanai.
2. **Atveriet cilni Vispārīgi iestatījumi** un ritiniet līdz **Citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet filtra izkārtojumu **uz** Noklusējuma filtra izkārtojums **projekta operācijām Lite**.
4. Atjauniniet **resursu izgūšanas vaicājumu** uz **noklusējuma izgūšanas resursu vaicājumu projekta operācijām Lite**.
5. **Atveriet cilni Grafika veidi** un dodieties uz **Project**.
6. Sadaļā Project iestatījumi **atjauniniet** Schedule Assistant izgūšanas resursu vaicājumu **uz** Noklusējuma izgūšanas resursu vaicājumu projekta operācijām Lite **un atjauniniet** schedule assistant izgūšanas ierobežojumu vaicājumu **uz** noklusējuma izgūšanas ierobežojumu vaicājumu projekta operācijām Lite **.**

![Uz prasībām balstītas resursu meklēšanas plānošanas paneļa iestatījumu atjaunināšana](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
