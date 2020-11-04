---
title: Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana
description: Šajā tēmā ir sniegta informācija par to, kā izveidot projekta veidnes, izmantojot pielāgoto darbību Projekta kopēšana.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080384"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations atbalsta iespēju kopēt projektu un atjaunot visu uzdevumu vispārējos resursus, kas norāda lomu. Klienti var izmantot šo funkcionalitāti, lai veidotu vienkāršas projektu veidnes.

Atlasot **Projekta kopēšana** , tiek atjaunināts mērķa projekta statuss. Izmantojiet **Statusa iemesls** , lai noteiktu, kad kopēšanas darbība ir pabeigta. Atlasot **Projekta kopēšana** , tiek atjaunināts arī projekta sākuma datums uz pašreizējo sākuma datumu, ja mērķa projekta entītijā nav noteikts mērķa datums.

## <a name="copy-project-custom-action"></a>Pielāgotā darbība Projekta kopēšana 

### <a name="name"></a>Nosaukums/vārds, uzvārds 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Ievades parametri
Ir trīs ievades parametri.

| Parametrs          | Veidi   | Vērtības                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** vai **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entītijas atsauce | Avota projekts |
| Mērķis             | Entītijas atsauce | Mērķa projekts |


- **{"clearTeamsAndAssignments":true}** : Noklusējuma darbība Project tīmeklim, un tiks noņemti visi piešķīrumi un darba grupas dalībnieki.
- **{"removeNamedResources":true}** Project Operations noklusējuma darbība, un tiks atjaunoti vispārīgie resursi.

Vairāk darbību noklusējuma vērtību skatiet sadaļā [Web API darbību izmantošana](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Kopējamo lauku norādīšana 
Kad tiek izsaukta darbība, darbība **Projekta kopēšana** apskatīs projekta skatu **Projekta kolonnu kopēšana** , lai noteiktu, kuri lauki jākopē, pārkopējot projektu.
