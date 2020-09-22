---
title: Projekta pārdošanas procesā veicamo darbu tāmes nodrošināšana
description: Projekta darba tāmju nodrošināšana pārdošanas procesa laikā programmā Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753543"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Projekta darba tāmju nodrošināšana pārdošanas procesa laikā (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Pārdošanas procesa gaitā var sagatavot pārdošanas tāmi, izmantojot sākotnējā piedāvājuma rindas. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iespējas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] piedāvā zinātniskāku un noteiktāku pārdošanas aplēšu aprēķināšanas metodi, sadalot darbu vienumus un saistot attiecīgos atribūtus, kas atvieglo projekta aplēšu aprēķināšanu darba sadalījuma struktūrā.  
  
 Kad pārdošanas projekts ir apstiprināts, projekta plānā var izmantot saistīto darba sadalījuma struktūru, ko, ja nepieciešams, var pārveidot, lai projekts tiktu sekmīgi pabeigts.  
  
## <a name="link-a-project-to-a-quote-line"></a>Projekta saistīšana ar piedāvājuma rindu  
 Ja tiek izveidota ar projektu saistīta piedāvājuma rinda, to izmantojot, var izveidot jaunu projektu. Pēc tam var izmantot projekta veidnes, kas ir vai nu jūsu organizācijai raksturīgi iepriekš konfigurēti standarta projekta plāni un finanšu aplēses, vai iepriekšējā projekta plāna un aprēķinu kopija. Izveidojot projektu, izvēlētā projekta veidne nodrošina bāzi, kas tiek izmantota projekta plāna, tāmes un ar lomām saistīto prasību precizēšanai. Ja projekts tiek izveidots, izmantojot piedāvājumu, tas automātiski tiek saistīta ar piedāvājuma rindu.  
  
## <a name="project-estimate-components"></a>Projekta tāmes sastāvdaļas  
 Projekta darba sadalījuma struktūra nodrošina iespējas darba sadalīšanai uzdevumos, uzdevumu hierarhijas saglabāšanai un katra uzdevuma izpildei nepieciešamo resursu budžeta iedalīšanai. Lomas var saistīt arī ar uzdevumu, tādējādi norādot uzdevuma un grafika izpildei nepieciešamā resursa tipa budžetu.  
  
 Darba sadalījuma struktūras izmantošana palīdz noteikt darba resursu un grafika budžetu. Pēc noklusējuma projektā tiek izmantoti noklusējuma cenrāži, kas ir definēti iepriekš. Cenrāžos noteikto izmaksu un pārdošanas cenas palīdz aprēķināt projekta darbu sadalījuma tāmes.  
  
 Ja projekts ir saistīts ar piedāvājumu un piedāvājumam pēc noklusējuma ir atšķirīgs cenrādis, piedāvājuma cenrādis tiek izmantots kā tāme.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Tāmes importēšana no projekta uz piedāvājumu  
 Kad projektam ir aprēķināta tāme, šo tāmi var importēt piedāvājuma rindā:  
  
-   Sadaļā **Piedāvājuma rindas dati** noklikšķiniet uz **Importēt no tāmes**. 

-   Atlasiet, vai importēt pēc transakcijas tipa, lomas vai darba sadalījuma struktūras mezgla līmeņa apkopotu projekta tāmi.  
  
### <a name="see-also"></a>Skatiet arī  
 [Projekta vadītāja rokasgrāmata](../project-service/project-manager-guide.md)
