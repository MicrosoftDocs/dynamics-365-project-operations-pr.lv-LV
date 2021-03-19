---
title: Resursu saskaņošanas pārskats
description: Šajā tēmā ir sniegta informācija, kas palīdzēs nodrošināt, ka projektu resursu rezervācijas un projektu piešķire ir saskaņoti.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0416e93944e7b6686a0e4da1d633188dd51e590b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279372"
---
# <a name="resource-reconciliation-overview"></a>Resursu saskaņošanas pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Darba grupas dalībniekiem rezervācijas un piešķires ir brīvi savienotas. Citiem vārdiem sakot — resursiem var būt piešķires un var nebūt rezervāciju, vai arī tiem var būt rezervācijas un var nebūt piešķiru. Ideālā gadījumā rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze uzdevumu piešķiru izpildīšanai. Taču rezervācijas var būt balstītas uz pieejamību, un projekta gaitā uzdevumu laiki var mainīties. Tādēļ rezervāciju un piešķiru brīvais savienojums nodrošina elastību.

**Projektu** lapā ir cilne **Saskaņošana**, kas ļauj projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un viņu piešķires projektu darba grupās.

Cilnē **Saskaņošana** rezervācijas un piešķires katram darba grupas dalībniekam ir parādītas līdz atsevišķa uzdevuma piešķires līmenim. Stundas tiek rādītas šūnās, kas var apzīmēt periodus no mēnešiem līdz dienām. Šajā cilnē ir redzama arī projekta vispārējā neto kopsumma kopā ar **Kopsummas** kolonnu.

Katram resursam **Saskaņošanas** cilne aprēķina atšķirību starp darba grupas dalībnieka rezervācijām un darba grupas dalībnieka uzdevumu piešķiru apkopojumu. Ideālā gadījumā šai atšķirībai vajadzētu būt 0 (nulle). Citiem vārdiem sakot — starp rezervācijām un piešķirēm nevajadzētu būt nekādai starpībai. Atšķirības tiek iekrāsotas un ieēnotas, lai pievērstu uzmanību diviem tālāk aprakstītajiem apstākļiem.

- **Rezervācijas deficīts** — rezervācijas deficīts rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var vēlēties izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību.
- **Rezervāciju pārsniegšana** — rezervāciju pārsniegšana rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem. Šis apstāklis var būt pieņemams gadījumos, kad resurss projektam tika rezervēts vēl pirms tam, kad radās uzdevuma piešķire. Taču citos gadījumos, ja nav plāna piešķirt resursu uzdevumiem, projekta vadītājam vajadzētu apsvērt resursa rezervāciju atcelšanu. Tādējādi noslodzi var izmantot citā projektā.

Reizēm, kad laiku skatāt augstākā līmenī nekā dienas līmenis (piemēram, mēneša līmenī), varat pamanīt, ka neto starpība resursam ir nulle (citiem vārdiem sakot, rezervācijas ir tas pats, kas piešķires). Taču, ja laiku skatāt nedēļas līmenī, varat redzēt, ka pirmajā nedēļā piešķires ir nulle stundu un rezervācijas ir 40 stundas, bet otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir nulle stundu. Kopumā rezervācijas un piešķires ir saskaņotas, bet katrai nedēļai tās atšķiras.

Kad laiku skatāties augstākos līmeņos, šūnām cilnē **Saskaņošana** ir indikators, lai informētu jūs, ka pastāv atšķirības zemākos līmeņos. Divreiz pieskaroties vai veicot dubultklikšķi uz šūnas, varat tuvināt, lai apskatītu atšķirību. Pēc tam varat atlasīt un turēt (vai nospiest peles labo pogu), lai tālinātu. Atlasot kādu resursu un pēc tam režģa rīkjoslā izmantojot vadīklu **Nākamā atšķirība**, varat pāriet uz nākamo atšķirību starp šī resursa rezervācijām un piešķirēm. Pēc tam varat izmantot vadīklu **Iepriekšējā atšķirība**, lai dotos atpakaļ. Varat arī izslēgt atšķirību indikatoru un navigācijas uzvedību sadaļā **Iestatījumi**.

Ja jums ir uzdevumu piešķires kādam resursam, bet nav nevienas rezervācijas, lapā **Projekti**, cilnē **Saskaņošana** atlasiet rezervāciju deficītu un pēc tam atlasiet vienumu **Paplašināt rezervāciju**. Tiek parādīts dialoglodziņš **Paplašināt rezervāciju**, un tajā ir redzama rezervācija, kura ir nepieciešama, lai novērstu šo resursu deficītu. Dialoglodziņā redzamas arī resursu esošās rezervācijas visos projektos vai citos plānojamos elementos. Ja atlasāt **Labi**, lai izveidotu rezervāciju attiecīgajam resursam neatkarīgi no šī resursa pieejamības, varat izraisīt virsrezervāciju.

Rezervācijas, kuras tiek izveidotas, izmantojot darbību **Izvērst rezervāciju**, tiek saistītas ar primāro projekta prasību. Kad paplašināšana tiek sākta, nevar noteikt konkrēto prasību, kura jāpaplašina, jo resurss var būt saistīts ar vairāk nekā vienu projekta prasību.

Pēc tam projekta vadītājs vai resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu visas situācijas, kur resursa rezervācija pārsniedz tā noslodzi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]