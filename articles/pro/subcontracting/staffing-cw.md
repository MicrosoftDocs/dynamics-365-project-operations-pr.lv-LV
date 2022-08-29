---
title: Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi
description: Šajā rakstā ir paskaidrots, kā projekta prasības var nodarbināt, izmantojot līgumdarbiniekus vai ar apakšuzņēmuma līgumiem saistītus darbiniekus korporācijā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261264"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Vispārējie projekta komandas locekļi var būt darbinieki ar darbiniekiem vai līgumdarbiniekiem. Strādājot projektā ar līgumdarbiniekiem, varat ierobežot savas personāla iespējas, attiecinot tās tikai uz konkrētiem līgumdarbiniekiem, kas ir norīkoti apakšuzņēmuma līgumu līnijā. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Personāla resursu prasību meklēšana ar līgumdarbiniekiem, kas pieder konkrētai apakšlīguma līnijai

Lai meklētu un nodrošinātu personāla resursu vajadzības ar līgumdarbiniekiem, kas pieder noteiktai apakšlīguma līnijai, rīkojieties šādi:

1. Izveidojiet vispārīgu projekta grupas dalībnieku, kas atsaucas uz apakšuzņēmuma līgumu un apakšuzņēmuma līgumu līniju.
2. Ģenerējiet resursu nepieciešamību šim vispārīgajam projekta grupas dalībniekam, **izmantojot pogu Ģenerēt prasības** apakštīklā projekta grupas dalībnieki.
3. Atlasiet grupas dalībnieka rindu un pēc tam apakštīklā atlasiet **pogu Rezervēt**. 
4. Tādējādi tiek atvērts plānošanas panelis ar prasību kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas struktūrvienības laukiem, plānošanas paneļa filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma līguma un apakšuzņēmuma līgumu rindas laukiem no resursu nepieciešamības.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos. 
6. Atlasiet vienu no filtrētajiem resursiem un rezervējiet resursu šai prasībai. 
7. Tiek izveidots un atjaunināts projekta grupas dalībnieks ar apakšuzņēmuma līgumu un apakšlīgumu rindas atsaucēm. Dodieties uz **Project Estimates** un atlasiet **Atjaunināt cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas. 

> [!NOTE]
> Projekta grupas dalībnieka atjaunināšana ar apakšlīguma un apakšuzņēmuma līguma rindiņas atsauci ne vienmēr var būt iespējama rezervācijas laikā, ja resurss ir piešķirts vairākām apakšuzņēmuma līgumu rindām. Ja sistēma nevar atjaunināt projekta grupas dalībnieku ar apakšlīguma un apakšlīguma rindu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet šos laukus, lai finanšu izmaksu tāme precīzi atspoguļotu apakšuzņēmēja izmaksas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Jebkura līgumdarbinieka meklēšana un personāla resursu prasības

Lai meklētu un pieprasītu personāla resursus ar jebkuru līgumdarbinieku, rīkojieties šādi:

1. Izveidojiet vispārīgu projekta grupas dalībnieku.
2. Ģenerējiet resursu nepieciešamību šim vispārīgajam projekta grupas dalībniekam, **izmantojot pogu Ģenerēt prasības** apakštīklā projekta grupas dalībnieki.
3. Atlasiet grupas dalībnieka rindu un pēc tam apakštīklā atlasiet **pogu Rezervēt**. 
4. Tādējādi tiek atvērts plānošanas panelis ar prasību kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas struktūrvienības laukiem, plānošanas paneļa filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma līguma un apakšuzņēmuma līgumu rindas laukiem no resursu nepieciešamības. Tā kā prasībai nebija aizpildītas apakšuzņēmuma līgumu vai apakšlīgumu rindas vērtības, šie atribūti filtra rūtī būs tukši.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos.
6. Atjauniniet **filtra rūts lauku Nodarbinātais tips** uz **Līgumdarbinieks**, lai ierobežotu meklēšanu līdz līgumdarbiniekiem ar līgumu. Atjauniniet **kreditoru** filtru rūtī, lai atlasītu kreditoru, kas ierobežo meklēšanu, lai parādītu tikai līgumdarbiniekus, kas pieder noteiktam kreditora uzņēmumam.
7. Sarakstā atlasiet līgumdarbinieku un rezervējiet resursus šai prasībai.
8. Tiek izveidots projekta grupas dalībnieks. Tomēr projekta grupas dalībniekam netiek atjaunināts neviens apakšlīgums vai apakšlīguma līnija, tāpēc resursu piešķiršana netiks apmaksāta, izmantojot apakšuzņēmuma līgumu cenu. Manuāli atjauniniet projekta grupas dalībnieku ar apakšuzņēmuma līgumu rindiņu un dodieties uz **Projektu tāmes** un atlasiet **Atjaunināt cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas.

> [!NOTE]
> Projekta grupas dalībnieki, kuriem ir **tips** Darbinieks kā **līgumdarbinieks**, bet kuriem nav atsauces uz apakšlīgumu, tiek atzīmēti kā **Nederīgi** **projekta grupas dalībnieku** režģī. Ja ir kādi projekta grupas dalībnieki ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindas laukus, lai finanšu izmaksu tāme precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē Aplēses**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
