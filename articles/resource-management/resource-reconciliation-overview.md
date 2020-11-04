---
title: Resursu saskaņošanas pārskats
description: Šajā tēmā sniegta informācija par to, kā nodrošināt, ka resursu rezervācijas un projektu piešķiršana ir saskaņota.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080386"
---
# <a name="resource-reconciliation-overview"></a>Resursu saskaņošanas pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Darba grupas dalībniekiem rezervācijas un piešķires ir brīvi savienotas. Citiem vārdiem sakot — resursiem var būt piešķires, bet var nebūt rezervāciju, vai arī tiem var būt rezervācijas, bet var nebūt piešķiru. Ideālā gadījumā rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze uzdevumu piešķiru izpildīšanai. Taču rezervācijas var būt balstītas uz pieejamību, un projekta gaitā uzdevumu laiki var mainīties. Tādēļ rezervāciju un piešķiru brīvais savienojums nodrošina elastību.

Veidlapas **Projekts** cilne **Saskaņošana** ļauj projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un to piešķires projekta darba grupām.

Cilnē **Saskaņošana** rezervācijas un piešķires katram darba grupas dalībniekam ir arī parādītas līdz atsevišķa uzdevuma piešķires līmenim. Stundas tiek rādītas šūnās, kuras apzīmē laika periodus no mēnešiem līdz dienām.

Šajā cilnē ir redzama arī projekta vispārējā neto kopsumma kopā ar **Kopsummas** kolonnu.

Katram resursam šī cilne aprēķina atšķirību starp darba grupas dalībnieka rezervācijām un darba grupas dalībnieka uzdevumu piešķiru apkopojumu. Ideālā gadījumā šai atšķirībai vajadzētu būt 0 (nulle). Citiem vārdiem sakot — starp rezervācijām un piešķirēm nevajadzētu būt nekādai starpībai. Atšķirības tiek iekrāsotas un ieēnotas, lai pievērstu uzmanību diviem tālāk aprakstītajiem apstākļiem.

- **Rezervācijas deficīts** — rezervācijas deficīts rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var vēlēties izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību.
- **Rezervāciju pārsniegšana** — rezervāciju pārsniegšana rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem. Šis apstāklis var būt pieņemams gadījumos, kad resurss projektam tika rezervēts vēl pirms tam, kad radās uzdevuma piešķire. Taču citos gadījumos resursu nav plānots piešķirt uzdevumiem. Šādos gadījumos projektu vadītājam ir jāapsver resursa rezervācijas atcelšana, lai šo noslodzi varētu izmantot citam projektam.

Reizēm, kad laiku skatāt augstākā līmenī nekā dienas līmenis (piemēram, mēneša līmenī), varat pamanīt, ka neto starpība resursam ir nulle (citiem vārdiem sakot, rezervācijas = piešķires). Taču, ja laiku skatāt nedēļas līmenī, varat redzēt, ka pirmajā nedēļā piešķires ir nulle stundu un rezervācijas ir 40 stundas, bet otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir nulle stundu. Kopumā rezervācijas un piešķires ir saskaņotas, bet katrai nedēļai tās atšķiras.

Kad laiku skatāties augstākos līmeņos, šūnām cilnē **Saskaņošana** ir indikators, lai informētu jūs, ka pastāv atšķirības zemākos līmeņos. Veicot dubultklikšķi uz šūnas, varat tuvināt, lai apskatītu atšķirību. Pēc tam varat noklikšķināt ar peles labo pogu, lai tālinātu. Atlasot kādu resursu un pēc tam režģa rīkjoslā izmantojot vadīklu **Nākamā atšķirība** , varat pāriet uz nākamo atšķirību starp šī resursa rezervācijām un piešķirēm. Pēc tam varat izmantot vadīklu **Iepriekšējā atšķirība** , lai dotos atpakaļ. Varat arī izslēgt atšķirību indikatoru un navigācijas uzvedību sadaļā **Iestatījumi**.


Ja jums ir uzdevumu piešķires kādam resursam, bet nav nevienas rezervācijas, lapā **Projekti** , cilnē **Saskaņošana** atlasiet rezervāciju deficītu un pēc tam atlasiet vienumu **Paplašināt rezervāciju**. Tiek parādīts dialoglodziņš **Paplašināt rezervāciju** , un tajā ir redzama rezervācija, kura ir nepieciešama, lai novērstu šo resursu deficītu. Tur ir redzamas arī resursu esošās rezervācijas visos projektos vai citos plānojamos elementos. Ja atlasāt **Labi** , lai izveidotu rezervāciju attiecīgajam resursam neatkarīgi no šī resursa pieejamības, varat izraisīt virsrezervāciju.

Pēc tam projektu vadītājs vai resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu visas situācijas, kur resursa rezervācija pārsniedz tā noslodzi.

