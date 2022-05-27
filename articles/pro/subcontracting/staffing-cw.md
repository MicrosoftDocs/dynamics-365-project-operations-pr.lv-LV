---
title: Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi
description: Šajā tēmā paskaidrots, kā projekta prasības var nodrošināt ar personālu, izmantojot līgumdarbiniekus vai apakšuzņēmēju jaudu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574651"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Vispārīgus projekta komandas locekļus var nodarbināt ar darbiniekiem vai līgumdarbiniekiem. Pieņemot darbā projektu ar līgumdarbiniekiem, varat ierobežot personāla iespējas, attiecinot tās tikai uz konkrētiem līgumdarbiniekiem, kas ir piešķirti apakšuzņēmuma rindai. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Meklēt personāla resursu vajadzības ar līgumdarbiniekiem, kas pieder noteiktai apakšuzņēmuma līguma rindai

Lai meklētu un pieprasītu personāla resursus ar līgumdarbiniekiem, kas pieder noteiktai apakšuzņēmuma līguma rindai, rīkojieties šādi:

1. Izveidojiet vispārēju projekta grupas dalībnieku, kas atsaucas uz apakšuzņēmuma un apakšuzņēmuma rindu.
2. Ģenerēt resursu vajadzību šim vispārējam projekta grupas dalībniekam, **izmantojot projekta grupas dalībnieku apakšrežģa pogu Ģenerēt vajadzību**.
3. Atlasiet grupas dalībnieka rindu un pēc tam apakšrežģijā atlasiet **pogu Grāmata**. 
4. Tiek atvērts grafika dēlis ar vajadzību kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas vienību laukiem, grafika dēļa filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma un apakšuzņēmuma rindu laukiem no resursu vajadzības.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos. 
6. Atlasiet vienu no filtrētajiem resursiem un rezervējiet vajadzības resursu. 
7. Projekta grupas dalībnieks tiek izveidots un atjaunināts ar apakšuzņēmuma un apakšuzņēmuma rindu atsaucēm. Dodieties uz **Projekta novērtējumi** un atlasiet **Atjaunināt cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas. 

> [!NOTE]
> Projekta grupas dalībnieka atjaunināšana ar apakšlīguma un apakšuzņēmuma rindas atsauci ne vienmēr var būt iespējama rezervācijas laikā, ja resurss ir piešķirts vairākām apakšuzņēmuma rindām. Ja sistēma nevar atjaunināt projekta grupas dalībnieku ar apakšuzņēmuma un apakšuzņēmuma rindu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet šos laukus, lai finanšu izmaksu tāme precīzi atspoguļotu apakšuzņēmēja izmaksas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Meklēt un personāla resursu vajadzības ar jebkuru līgumdarbinieku

Lai meklētu un pieprasītu personāla resursus ar jebkuru līgumdarbinieku, rīkojieties šādi:

1. Izveidojiet vispārēju projekta grupas dalībnieku.
2. Ģenerēt resursu vajadzību šim vispārējam projekta grupas dalībniekam, **izmantojot projekta grupas dalībnieku apakšrežģa pogu Ģenerēt vajadzību**.
3. Atlasiet grupas dalībnieka rindu un pēc tam apakšrežģijā atlasiet **pogu Grāmata**. 
4. Tiek atvērts grafika dēlis ar vajadzību kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas vienību laukiem, grafika dēļa filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma un apakšuzņēmuma rindu laukiem no resursu vajadzības. Tā kā prasībai nebija aizpildītas apakšuzņēmuma vai apakšuzņēmuma rindas vērtības, filtra rūtī šie atribūti būs tukši.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos.
6. **Atjauniniet filtra rūts lauku Darbinieka tips** uz Līgumdarbinieks **,** lai meklēšanu attiecinātu tikai uz līgumdarbiniekiem. Atjaunināt **kreditoru** filtru rūtī, lai atlasītu kreditoru, lai ierobežotu meklēšanu, lai rādītu tikai līgumdarbiniekus, kas pieder noteiktam kreditora uzņēmumam.
7. Sarakstā atlasiet līgumdarbinieku un rezervējiet vajadzības resursu.
8. Tiek izveidots projekta grupas dalībnieks. Tomēr projekta grupas dalībnieks netiek atjaunināts ar apakšuzņēmuma vai apakšuzņēmuma rindu, tāpēc resursu piešķiršana netiks izmaksāta, izmantojot apakšuzņēmuma cenu noteikšanu. Manuāli atjauniniet projekta grupas dalībnieku ar apakšuzņēmuma rindu un dodieties uz **Projekta novērtējumi** un atlasiet **Atjaunināt cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas.

> [!NOTE]
> Projekta grupas dalībnieki, kuru tips ir **Darbinieks kā** līgumdarbiniekam **, bet kuriem nav apakšuzņēmuma atsauces, projekta grupas dalībnieku** režģī tiek atzīmēti kā **nederīgi** **.** Ja ir kāds projekta grupas dalībnieks ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma un apakšuzņēmuma rindu laukus, lai finanšu izmaksu novērtējums precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē Novērtējumi**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
