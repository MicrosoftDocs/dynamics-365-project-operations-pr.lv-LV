---
title: Konfigurēt plānošanas dēli, lai parādītu līgumdarbiniekus un apakšuzņēmēju noslodzi
description: Šajā tēmā ir aprakstīts, kā konfigurēt Schedule Board programmā Dynamics 365 Project Operations Microsoft, lai parādītu apakšuzņēmēju resursu noslodzi, strādājot ar projekta resursu vajadzībām.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903710"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurēt plānošanas dēli, lai parādītu līgumdarbiniekus un apakšuzņēmēju noslodzi 

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Schedule Board programmā Microsoft Dynamics 365 Project Operations var izmantot resursu meklēšanai divos veidos:

- Vispārējā resursu meklēšana bez konteksta, kas saistīta ar īpašām uz projektiem balstītām resursu vajadzībām.
- Prasībai raksturīga resursu meklēšana, kur projekta vajadzība nodrošinās ieteikto resursu kontekstu.

Lai paziņotu grafika padomei par apakšuzņēmēju resursu ietilpību un līgumdarbiniekiem, ir jāveic grafika padomes iestatījumu atjauninājumi. Šie atjauninājumi ietver: 
- Atjaunināt Schedule Board iestatījumus vispārējai resursu meklēšanai.
- Atjaunināt Schedule Board iestatījumus uz prasībām balstītai resursu meklēšanai.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atjaunināt grafika dēļa iestatījumus vispārējai resursu meklēšanai
### <a name="update-filters-for-general-resource-search"></a>Atjaunināt filtrus vispārējai resursu meklēšanai
Meklējot resursu, plānošanas panelī pieejamie filtri ir jāatjaunina, lai varētu meklēt arī ārējos resursus, norādot kādu vai visas no šīm darbībām:
  - Darbinieka tips, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
  - Kreditora uzņēmums, kuram pieder resursam.
  - Resursi, kas pieder noteiktam apakšuzņēmuma vai apakšuzņēmuma rindu.
    
### <a name="update-retrieve-resource-query"></a>Atjaunināt resursu izgūšanas vaicājumu
Meklēšanā izmantotais vaicājums arī jāatjaunina, lai izmantotu šos papildu filtra atribūtus. Veiciet tālāk norādītās darbības, lai atjauninātu Schedule Board konfigurāciju vispārējai resursu meklēšanai:  
1. Atveriet **Schedule Board iestatījumus** noteiktam schedule board.
2. Atveriet **cilni Vispārīgie iestatījumi** un ritiniet līdz **citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet **filtra izkārtojumu** uz Noklusējuma filtra izkārtojumu **projekta operācijām Lite**.
4. Atjaunināt **resursu izgūšanas** vaicājumu, lai noklusējuma **izgūtu resursu vaicājumu projekta operācijām Lite**.

![Atjaunināt grafika dēļa iestatījumus vispārējai resursu meklēšanai](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atjaunināt schedule board iestatījumus uz prasībām balstītai resursu meklēšanai
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atjaunināt filtrus prasībām specifisku resursu meklēšanai 
Meklējot resursu, plānošanas panelī pieejamie filtri ir jāatjaunina, lai varētu meklēt arī ārējos resursus, norādot kādu vai visas no šīm darbībām:
 - Darbinieka tips, neatkarīgi no tā, vai norādītajiem resursiem jābūt līgumdarbiniekiem vai darbiniekiem.
 - Kreditora uzņēmums, kuram pieder resursam.
 - Resursi, kas pieder noteiktam apakšuzņēmuma vai apakšuzņēmuma rindu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atjaunināt resursu izgūšanas vaicājumu prasībām specifisku resursu meklēšanai 
Meklēšanā izmantotais vaicājums arī jāatjaunina, lai izmantotu šos papildu filtra atribūtus. Veiciet tālāk norādītās darbības, lai atjauninātu Schedule Board konfigurāciju uz vajadzībām balstītai resursu meklēšanai:

1. Atveriet **Schedule Board settings for a specific Schedule Board un pēc tam** atlasiet Atvērt noklusējuma **iestatījumus**, lai atvērtu iestatījumus meklēšanai, kas saistīta ar prasībām.
2. Atveriet **cilni Vispārīgie iestatījumi** un ritiniet līdz **citi iestatījumi**.
3. Šīs sadaļas iestatījumu sarakstā atjauniniet **filtra izkārtojumu** uz Noklusējuma filtra izkārtojumu **projekta operācijām Lite**.
4. Atjaunināt **resursu izgūšanas** vaicājumu, lai noklusējuma **izgūtu resursu vaicājumu projekta operācijām Lite**.
5. Atveriet **cilni Grafika tipi** un dodieties uz **Project**.
6. Projekta iestatījumos **atjauniniet** **Schedule Assistant Retrieve Resources Query to Default Retrieve Resources Query for Project Operations** **Lite un update Schedule Assistant Retrieve Constraints** Query to Default Retrieve Constraints Query for Project **Operations** **Lite**.

![Atjaunināt schedule board iestatījumus uz prasībām balstītai resursu meklēšanai](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
