---
title: Pārdošanas cenrāžu iestatīšana
description: Šajā tēmā ir sniegta informācija par pārdošanas cenrāžiem projekta cenu noteikšanai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176260"
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
