---
title: Pārdošanas cenrāžu iestatīšana
description: Šajā rakstā ir sniegta informācija par projektu izcenojumu pārdošanas cenrāžiem.
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
ms.openlocfilehash: 1892607ac121e23a05cd45bc05d4e23ea84690b4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923059"
---
# <a name="set-up-a-sales-price-list"></a>Pārdošanas cenrāžu iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Attiecībā uz projektu piedāvājumiem un līgumiem projekta cenrādim ir no preču cenrāža atšķirīgs cenas pārlabošanas modelis. Preču kataloga piedāvājuma rindā varat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā, jo katra piedāvājuma rinda norāda uz vienu kataloga vienumu. Taču projekta piedāvājuma rindā nevarat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā. Varat izmantot projekta cenrādi, lai strādātu ar divām atšķirīgām, pārlabotām sistēmām.

> [!NOTE]
> Ieteicams projekta resursiem un kataloga vienumiem izmantot atsevišķus cenrāžus, jo starp abiem pastāv uzvedības atšķirības, kad pārlabojat cenas.

Katrai no tālāk minētajām entītijām var būt viens vai vairāki piesaistītie pārdošanas cenrāži projekta izcenojumam.

- Klients (uzņēmums) 
- Iespēja 
- Piedāvājums 
- Projekta līgums

Šo entītiju saistību ar cenrādi norāda projekta cenrāži. Varat saistīt vienu vai vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līguma pārdošana.

Noklusējuma projekta cenrādis netiek automātiski ievadīts klienta ierakstā. Tomēr varat manuāli pievienot projekta cenrādi klienta ierakstam. Taču projekta cenrādi drīkst manuāli pievienot tikai tad, ja jums ir pielāgots izcenojuma līgums ar klientu. 

Kad pārdošanas entītijai tiek pievienots projekta cenrādis, tiek pārbaudīta šāda informācija:

- Cenrādim ir entītijas **Pārdošana** konteksts. 
- Cenrāža valūta atbilst klienta valūtai. 

Projekta līgumā izmanto tālāk norādīto prioritāšu secību, lai automātiski iestatītu saistītos projekta cenrāžus.

1. Piedāvājums
2. Iespēja
3. Klients 
4. Globālie iestatījumi 

Kad projekta cenrādis tiek ievadīts pēc noklusējuma, sistēma pārbauda, vai šī valūta atbilst klienta valūtai un vai ievadītajiem noklusējuma cenrāžiem ir entītijas **Pārdošana** konteksts.

Varat saistīt vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līgums. Šī iespēja atbalsta datumam specifiskas noklusējuma cenas ilgstošam projekta līgumam, kam var būt nepieciešams vairāk nekā viens cenrādis, lai uzskaitītu cenas atjauninājumus, kas rodas inflācijas dēļ. Tomēr, ja cenrāžos, ko saistāt ar entītiju Klients, Iespēja, Piedāvājums vai Projekta līgums, pārklājas spēkā stāšanās datumi, noklusējuma cenas var būt nepareizas. Tāpēc ir jāpārliecinās, vai projekta cenrāži, kam pārklājas spēkā esošie datumi, netiek saistīti ar šīm entītijām.


[!INCLUDE[footer-include](../includes/footer-banner.md)]