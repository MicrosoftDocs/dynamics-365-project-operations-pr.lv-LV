---
title: Valūta
description: Šajā rakstā sniegta informācija par to, kā pievienot un noņemt valūtu veidus programmā Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921541"
---
# <a name="currency"></a>Valūta

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_



No valūtas ir atkarīgas preču katalogā ietverto produktu cenas un darījumu, piemēram, pārdošanas pasūtījumu, izmaksas. Ja jūsu klienti atrodas dažādos ģeogrāfiskajos apgabalos, pievienojiet viņu valūtas savu darījumu pārvaldībai. Pievienojiet jūsu pašreizējām un nākotnes biznesa vajadzībām vispiemērotākās valūtas.  

> [!NOTE]
> Ja vide ir Common Data Service vide, jūs atrodaties Power Platform administrēšanas centrā un atlasāt lapu **Valūtas** (**Vide** > [atlasīt vidi] > **Iestatījumi** > **Biznesa** > **Valūtas**), lapa būs tukša. Tas ir tāpēc, ka Common Data Service vidēs netiek atbalstīta valūtas iestatīšana.

## <a name="add-a-currency"></a>Valūtas pievienošana  
Pirms uzsākat šo procedūru, pārliecinieties, ka jūsu drošības lomā ir iekļautas sistēmas administratora atļaujas 

1. Power Platform administrēšanas centrā atlasiet vidi. 
2. Atlasiet **Iestatījumi** > **Bizness**.
3. Atlasiet **Valūtas**.  
4. Atlasiet **Jauns**.  
5. Aizpildiet nepieciešamo informāciju.  


   |          Lauks          |                                                                                                                                                                                                                                                                                                                                                                            Apraksts                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valūtas veids**    | - **Sistēma** — atlasiet šo iespēju, ja vēlaties izmantot valūtas, kas pieejamas modeļa vadītās programmās risinājumā Dynamics 365. Lai meklētu valūtu, atlasiet **Uzmeklēšana**. Kad atlasāt kādu valūtas kodu, atlasītajai valūtai tiek automātiski pievienots **Valūtas nosaukums** un **Valūtas simbols**.<br />- **Pielāgots** — atlasiet šo iespēju, ja vēlaties pievienot valūtas, kas nav pieejamas modeļa vadītās programmās risinājumā Dynamics 365. Šādā gadījumā jums ir manuāli jāievada vērtības vienumiem **Valūtas kods**, **Valūtas precizitāte**, **Valūtas nosaukums**, **Valūtas simbols** un **Valūtu konvertēšana**. |
   |    **Valūtas kods**    |                                                                                                                                                                                                                                                                                                                                            Valūtas saīsinājums. Piemēram, **USD** atbilst Amerikas Savienoto Valstu dolāram.                                                                                                                                                                                                                                                                                                                                            |
   | **Valūtas precizitāte**  |                                                                                                                                                                                  Ierakstiet, kādu decimāldaļas skaitu vēlaties izmantot šai valūtai.  Varat pievienot vērtību no 0 līdz 4. **Piezīme.**  Ja esat iestatījis precizitātes vērtību dialoglodziņā **Sistēmas iestatījumi**, šeit būs redzama iestatītā vērtība.                                                                                                                                                                                  |
   |    **Valūtas nosaukums**    |                                                                                                                                                                                                                                         Ja atlasījāt valūtas kodu no modeļa vadītās programmās risinājumā Dynamics 365 pieejamo valūtu saraksta, tad šeit tiek rādīts atlasītā koda valūtas nosaukums. Ja atlasījāt **Pielāgots** kā valūtas veidu, ierakstiet valūtas nosaukumu.                                                                                                                                                                                                                                          |
   |   **Valūtas simbols**   |                                                                                                                                                                                                                                                                      Ja atlasījāt valūtas kodu no pieejamo valūtu saraksta, tad šeit tiek rādīts atlasītās valūtas simbols. Ja atlasījāt **Pielāgots** kā valūtas tveidu, ievadiet simbolu jaunajai valūtai.                                                                                                                                                                                                                                                                       |
   | **Valūtu konvertēšana** |                                                                                                                                                                                                                                     Ierakstiet atlasītās valūtas vērtību viena ASV dolāra izteiksmē. Šī ir summa, ar kādu atlasītā valūtā tiek konvertēta uz pamatvalūtu. **Svarīgi!**  Šī vērtība noteikti ir jāatjaunina, cik vien bieži nepieciešams, lai Jūsu darījumos nerastos neprecīzi aprēķini.                                                                                                                                                                                                                                      |


6. Kad tas ir izdarīts, komandjoslā atlasiet **Saglabāt** vai **Saglabāt un aizvērt**.  

   > [!TIP]
   >  Lai rediģētu kādu valūtu, atlasiet attiecīgās valūtas, un pēc tam ievadiet vai atlasiet jaunās vērtības.  

## <a name="delete-a-currency"></a>Dzēst valūtu  

1. Power Platform administrēšanas centrā atlasiet vidi. 
2. Atlasiet **Iestatījumi** > **Bizness**.
3. Atlasiet **Valūtas**.  
4. Parādītajā valūtu sarakstā atlasiet valūtu, ko vēlaties dzēst.  
5. Atlasiet **Dzēst**.  
6. Apstipriniet dzēšanu.  

> [!IMPORTANT]
>  Nevar izdzēst valūtas, kas tiek lietotas citos ierakstos; tās var tikai deaktivizēt. Deaktivizējot valūtas ierakstu, netiek noņemta esošajos ierakstos glabātā informācija par valūtu, piemēram, iespējās vai pasūtījumos. Taču deaktivizētu valūtu Jūs nevarēsiet atlasīt jauniem darījumiem.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]