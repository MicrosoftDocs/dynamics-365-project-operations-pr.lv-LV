---
title: Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi
description: Šajā rakstā ir izskaidrots, kā projekta prasībām var nodrošināt personālu, izmantojot līgumdarbiniekus vai apakšlīguma noslodzi programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522445"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Vispārējos projekta darba grupas dalībniekus var iekļaut personālā ar darbiniekiem vai līgumdarbiniekiem. Komplektējot projekta personālu ar līgumdarbiniekiem, varat ierobežot personāla opcijas līdz noteiktiem līgumdarbiniekiem, kas ir piešķirti apakšlīguma rindai. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Personāla resursu prasību meklēšana ar noteiktai apakšlīguma rindai piederošiem līgumdarbiniekiem

Lai meklētu un iekļautu personālā resursu prasības ar noteiktai apakšlīguma rindai piederošiem līgumdarbiniekiem, veiciet tālāk norādītās darbības.

1. Izveidojiet vispārēju projekta darba grupas dalībnieku, kam ir atsauce uz apakšlīgumu un apakšlīguma rindu.
2. Ģenerējiet resursa prasību šim vispārējam projekta darba grupas dalībniekam, izmantojot pogu **Ģenerēt prasību** projekta darba grupas dalībnieku apakšrežģī.
3. Atlasiet darba grupas dalībnieka rindu un pēc tam apakšrežģī atlasiet pogu **Rezervēt**. 
4. Tādējādi tiek atvērts plānošanas panelis ar prasības kontekstu. Kopā ar citiem atribūtiem, piemēram, datumu, lomu un organizācijas vienību laukiem, plānošanas paneļa filtri arī tiek automātiski aizpildīti ar resursu prasības piegādātāja, apakšlīguma un apakšlīguma rindas rindu laukiem.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un parāda tos sarakstā. 
6. Atlasiet kādu no filtrētajiem resursiem un rezervējiet resursu prasībai. 
7. Tiek izveidots projekta darba grupas dalībnieks, kam tiek atjauninātas atsauces uz apakšlīgumu un apakšlīguma rindu. Dodieties uz **Projekta aprēķini** un atlasiet **Atjaunināt cenas**, lai skatītu resursu piešķīruma atjauninātās izmaksas. 

> [!NOTE]
> Projekta darba grupas dalībnieka atjaunināšana ar apakšlīguma un apakšlīguma rindas atsauci rezervācijas laikā ne vienmēr var būt iespējama, ja resurss ir piešķirts vairākām apakšlīgumu rindām. Ja sistēma nevar atjaunināt projekta darba grupas dalībnieku ar apakšlīgumu un apakšlīguma rindu, atveriet projekta darba grupas dalībnieka ierakstu un manuāli atjauniniet šos laukus, lai finanšu izmaksu aprēķins precīzi atspoguļotu apakšuzņēmēja izmaksas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Resursu prasību meklēšana un iekļaušana personālā ar jebkuru līgumdarbinieku

Lai meklētu resursu prasības un iekļautu tās personālā ar jebkuru līgumdarbinieku, izpildiet tālāk norādītās darbības.

1. Izveidojiet vispārēju projekta darba grupas dalībnieku.
2. Ģenerējiet resursa prasību šim vispārējam projekta darba grupas dalībniekam, izmantojot pogu **Ģenerēt prasību** projekta darba grupas dalībnieku apakšrežģī.
3. Atlasiet darba grupas dalībnieka rindu un pēc tam apakšrežģī atlasiet pogu **Rezervēt**. 
4. Tādējādi tiek atvērts plānošanas panelis ar prasības kontekstu. Kopā ar citiem atribūtiem, piemēram, datumu, lomu un organizācijas vienību laukiem, plānošanas paneļa filtri arī tiek automātiski aizpildīti ar resursu prasības piegādātāja, apakšlīguma un apakšlīguma rindas rindu laukiem. Tā kā prasībai nebija aizpildītas apakšlīguma vai apakšlīguma rindu vērtības, šie atribūti filtru rūtī būs tukši.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un parāda tos sarakstā.
6. Filtru rūtī atjauniniet lauku **Darbinieka tips** uz **Līguma darbinieks**, lai meklēšanu ierobežotu līdz līgumdarbiniekiem. Filtru rūtī atjauniniet lauku **Piegādātājs**, lai atlasītu piegādātāju un tādējādi ierobežotu meklēšanu, lai rādītu tikai noteiktam piegādātāja uzņēmumam piederīgus līgumdarbiniekus.
7. Sarakstā atlasiet līgumdarbinieku un rezervējiet resursu prasībai.
8. Tiek izveidots projekta darba grupas dalībnieks. Tomēr projekta darba grupas dalībnieks netiek atjaunināts ne ar vienu apakšlīgumu vai apakšlīguma rindu, tādēļ resursu piešķīrumam netiks noteiktas izmaksas, izmantojot apakšlīguma izcenojumu. Manuāli atjauniniet projekta darba grupas dalībnieku ar apakšlīguma rindu un pārejiet uz **Projekta aprēķini**, un atlasiet **Atjaunināt cenas**, lai skatītu resursa piešķīruma atjauninātās izmaksas.

> [!NOTE]
> Projekta darba grupas dalībnieki, kuru **Darbinieka tips** ir **Līgumdarbinieks**, bet nav apakšlīguma atsauces, ir atzīmēti ar **Nederīgs** režģī **Projekta darba grupas dalībnieki**. Ja pastāv projekta darba grupas dalībnieki ar šo statusu, atveriet projekta darba grupas dalībnieka ierakstu un manuāli atjauniniet apakšlīgumu un apakšlīguma rindas laukus, lai finanšu izmaksu aprēķins precīzi atspoguļotu apakšuzņēmēja izmaksas cilnē **Aprēķini**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
