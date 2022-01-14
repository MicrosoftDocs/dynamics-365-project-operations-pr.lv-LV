---
title: Personāla personāls projektā ar līgumdarbiniekiem un apakšuzņēmēju jaudu
description: Šajā tēmā ir paskaidrots, kā projekta prasībām var būt personāls, izmantojot līgumdarbiniekus vai apakšuzņēmēju noslodzi programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903717"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Personāla personāls projektā ar līgumdarbiniekiem un apakšuzņēmēju jaudu

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Vispārējo projektu grupas dalībnieku personāls var būt personāls ar darbiniekiem vai līgumdarbiniekiem. Strādājot projektā ar līgumdarbiniekiem, personāla iespējas var ierobežot līdz noteiktiem līgumdarbiniekiem, kas piešķirti apakšuzņēmuma līguma rindai. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Meklēt personāla resursu vajadzības ar līgumdarbiniekiem, kas pieder noteiktai apakšuzņēmuma rindai

Lai meklētu un personāla resursu vajadzības ar līgumdarbiniekiem, kas pieder pie noteiktas apakšuzņēmuma rindas, rīkojieties šādi:

1. Izveidojiet vispārēju projekta grupas dalībnieku, kas atsaucas uz apakšuzņēmuma līgumu un apakšuzņēmuma rindu.
2. Ģenerēt resursu vajadzību šim vispārējam projekta grupas dalībniekam, izmantojot **pogu Ģenerēt vajadzību projekta grupas dalībnieku** apakšrežģī.
3. Atlasiet grupas dalībnieka rindu un pēc tam **apakšrežģī** atlasiet pogu Rezervēt. 
4. Tādējādi grafika padome tiek atvērta ar vajadzības kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas vienību laukiem, Schedule Board filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma līguma un apakšuzņēmuma rindu laukiem no resursu vajadzības.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos. 
6. Atlasiet vienu no filtrētajiem resursiem un rezervējiet resursu vajadzībai. 
7. Projekta grupas dalībnieks tiek izveidots un atjaunināts ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu atsaucēm. Dodieties uz **Projekta budžeti** un atlasiet Atjaunināt **cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas. 

> [!NOTE]
> Projekta grupas dalībnieka atjaunināšana ar apakšuzņēmuma līgumu un apakšuzņēmuma līguma rindas atsauci ne vienmēr var būt iespējama rezervēšanas laikā, ja resurss ir piešķirts vairākām apakšuzņēmuma līnijām. Ja sistēma nevar atjaunināt projekta grupas dalībnieku ar apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet šos laukus, lai finanšu izmaksu novērtējums precīzi atspoguļotu apakšuzņēmēja izmaksas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Meklēt un personāla resursu vajadzības ar jebkuru līgumdarbinieku

Lai meklētu un personāla resursu prasības ar jebkuru līgumdarbinieku, rīkojieties šādi:

1. Izveidojiet vispārīgu projekta grupas dalībnieku.
2. Ģenerēt resursu vajadzību šim vispārējam projekta grupas dalībniekam, izmantojot **pogu Ģenerēt vajadzību projekta grupas dalībnieku** apakšrežģī.
3. Atlasiet grupas dalībnieka rindu un pēc tam **apakšrežģī** atlasiet pogu Rezervēt. 
4. Tādējādi grafika padome tiek atvērta ar vajadzības kontekstu. Kopā ar citiem atribūtiem, piemēram, datumiem, lomu un organizācijas vienību laukiem, Schedule Board filtri tiek automātiski aizpildīti arī ar kreditora, apakšuzņēmuma līguma un apakšuzņēmuma rindu laukiem no resursu vajadzības. Tā kā prasībā nebija aizpildītas apakšlīgumu vai apakšuzņēmuma rindu vērtības, šie atribūti filtru rūtī būs tukši.
5. Sistēma meklē resursus, kas atbilst filtra kritērijiem, un uzskaita tos.
6. Atjauniniet **filtra rūts lauku Darbinieka tips** uz Līguma **darbinieks**, lai ierobežotu meklēšanu līdz līgumdarbiniekiem. Atjaunināt **kreditoru** filtra rūtī, lai atlasītu kreditoru, kas ierobežo meklēšanu un rāda tikai tos līgumdarbiniekus, kas pieder noteiktam kreditora uzņēmumam.
7. Sarakstā atlasiet līgumdarbinieku un rezervējiet resursu vajadzībai.
8. Tiek izveidots projekta grupas dalībnieks. Tomēr projekta grupas dalībnieks netiek atjaunināts ar apakšuzņēmuma līgumu vai apakšuzņēmuma rindu, tāpēc resursu piešķiršana netiks maksāta, izmantojot apakšuzņēmuma līgumu cenas. Manuāli atjauniniet projekta grupas dalībnieku ar apakšuzņēmēja rindu un dodieties uz **Projekta budžeti** un atlasiet Atjaunināt **cenas**, lai skatītu resursu piešķiršanas atjauninātās izmaksas.

> [!NOTE]
> Projekta grupas dalībnieki, kuru tips ir **Darbinieks** kā **Līgumdarbinieks**, bet kuriem nav apakšuzņēmuma līguma atsauces, projekta grupas dalībnieku režģī tiek atzīmēti **kā** **nederīgi**. Ja ir kāds projekta grupas dalībnieks ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma līgumu un apakšuzņēmuma rindu laukus, lai finanšu izmaksu novērtējums precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē** Novērtējumi. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
