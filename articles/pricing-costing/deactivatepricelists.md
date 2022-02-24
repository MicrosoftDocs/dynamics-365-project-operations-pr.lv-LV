---
title: Cenrāžu deaktivēšana
description: Šajā tēmā izskaidrots, kā deaktivizēt vai noņemt nelietotus vai vecus cenrāžus.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701952"
---
# <a name="deactivate-price-lists"></a>Cenrāžu deaktivēšana 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Lai noņemtu vecos vai neizmantotos cenrāžus no Dynamics 365 Project Operations, ir jāveic divas darbības. 

1. Noņemiet vai dzēsiet cenrādi no noteiktām lapām.
2. Deaktivizējiet vai izdzēsiet cenrādi no cenrāža lapas **Cenrāži** aktīvajiem cenrāžiem.

>[!IMPORTANT]
> Lai pilnībā noņemtu cenrādi, ir jāveic abas darbības. Nepietiek tikai ar 2. darbību, ar kuru tiek tieši dzēsts vai deaktivizēts cenrādis skatā Aktīvie cenrāži. Jums ir arī jāizdzēš šī cenrāža saistība no visām 1. darbībā minētajām vietām.

## <a name="delete-the-price-list-from-specific-pages"></a>Cenrāža dzēšana konkrētās lapās
1. Lai programmā Project Operations dzēstu cenrādi, atveriet tākāk minētās lapas.  

      - Lapa **Projekta parametri** > cilne **Cenrāži**
      - Lapa **Organizācijas vienība** > režģis **Cenrāži**
      - Lapa **Konts** > režģis **Projekta cenrāži**
      - Lapa **Projekta piedāvājumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta piedāvājumiem.
      - Lapa **Projekta līgumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta līgumiem.

 2. Katrai lapai ir jāatlasa cenrādis, ko vēlaties dzēst, un pēc tam jāatlasa **Dzēst**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Cenrāža dzēšana vai deaktivizēšana lapā Cenrāži
 
1. Lai dzēstu cenrādi no aktīvajiem cenrāžiem, atveriet **Pārdošana** > **Klienti** > **Cenrāži**. 
2. Atlasiet cenrādi, kuru vēlaties dzēst, un pēc tam atlasiet **Dzēst**. Ja uz cenrādi ir atsauce uz esošām transakcijām, to nevarēs dzēst. Šādā gadījumā cenrādi var deaktivizēt tā, lai tas nebūtu redzams skatos. 
3. Lai deaktivizētu cenrādi, vēlreiz atlasiet cenrādi un pēc tam atlasiet **Deaktivizēt**.   
