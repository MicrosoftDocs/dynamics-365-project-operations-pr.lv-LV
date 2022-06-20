---
title: Apakšlīgumu resursu piešķīrumu izmaksu novērtējums
description: Šajā rakstā ir paskaidrots, kā Microsoft Dynamics 365 Project Operations aprēķina apakšuzņēmēju resursu piešķires izmaksu novērtējumu.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932351"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Apakšlīgumu resursu piešķīrumu izmaksu novērtējums

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšuzņēmēju projekta grupas dalībnieku uzdevumu piešķires tiek izmaksātas, izmantojot **iepirkuma** cenrādi, kas pievienots apakšlīgumam saistītajā grupas dalībnieka ierakstā. Tas atšķiras no tā, kā tiek aprēķinātas darbinieku resursu piešķiršanas izmaksas, ja darbinieku resursu uzdevumu piešķires tiek izmaksātas, izmantojot **izmaksu** cenrādi, kas pievienots projekta līguma vienībai. 

Vispārīgiem projekta grupas dalībniekiem, kuriem ir apakšuzņēmuma līgumi, piešķires tiek izmaksātas, izmantojot uz lomām balstītus cenu iestatījumus iepirkuma cenrādī, kas pievienots apakšuzņēmuma līgumam pievienotajā pirkšanas cenrādī. Pirkšanas cenas var iestatīt arī īpaši katram resursam. Šīm resursiem raksturīgajām cenām tiks piešķirta prioritāte, ja izmaksas uzdevumu piešķires nosauktiem projekta grupas dalībniekiem ir līgumdarbinieki. 

Prioritāte lomai specifiskas pirkšanas cenas izmantošanai salīdzinājumā ar resursu specifisko cenu nosaka cenu dimensijas prioritātes iestatīšana parametros **> uz summu balstītās cenu dimensijas**.

Šī dinamiski iegūto cenu funkcionalitāte, pamatojoties uz apakšuzņēmēju pirkšanas cenu dimensiju iestatījumiem, ir līdzīga tam, kā tiek iegūtas izmaksu un rēķinu likmes pilnas slodzes darbiniekiem. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Uzdevumu piešķiru izveide apakšuzņēmēju resursu izmaksu novērtējumu iegūšanai

Uzdevumu piešķires apakšuzņēmējiem var izveidot divos veidos: 
- **Izmantojot cilni Uzdevumi**.
- **Izmantojot cilni Komanda**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resursu piešķirju izveide, izmantojot cilni Uzdevumi
**Izmantojot cilnes Uzdevumi** sarakstu **Resursi** noteiktam uzdevumam, varat izveidot uzdevumu piešķiri nosauktam resursam vai vispārējam resursam. Ja uzdevuma nolaižamajā **izvēlnē Piešķirtie resursi** atlasāt nosauktu resursu un šis resurss ir līgumdarbinieks, uzdevumam tiek piešķirts nosauktais resurss un tiek izveidots atbilstošs projekta grupas dalībnieka ieraksts ar iestatītu darbinieka tipu, kas iestatīts uz **Līgumdarbinieks** un **Derīgums** ir iestatīts uz **Nederīgs**. Kā nākamo soli jums būs jāatver projekta komandas dalībnieka ieraksts un jāizvēlas apakšuzņēmuma un apakšuzņēmuma rinda. Tas atjauninās uzdevuma piešķiri, lai būtu atsauce uz apakšuzņēmuma un apakšuzņēmuma rindu, kā arī atjauninās grupas dalībnieka statusu uz **Derīgs**.

Ja izvēlaties izveidot vispārēju grupas dalībnieku no uzdevuma nolaižamā **saraksta Piešķirtie resursi**, **vispārējais grupas dalībnieka izveides** dialogs ļaus atlasīt apakšuzņēmuma un apakšuzņēmuma rindu. Kad uzdevumam ir piešķirts vispārējais resurss un izveidots atbilstošais projekta grupas dalībnieka ieraksts, jūs pamanīsit, ka projekta grupas dalībnieka ieraksts ir izveidots ar darbinieka tipu, kas iestatīts uz **Līguma darbinieks** un **derīgums ir iestatīts** uz **Derīgs**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekta grupas dalībnieku izveide, izmantojot cilni Komanda
Izmantojot projekta cilni Komanda, varat izveidot vispārīgu vai nosauktu grupas dalībnieku. Veidojot grupas dalībnieku, varat atlasīt apakšuzņēmuma un apakšuzņēmuma rindu. Pēc grupas dalībnieka izveides grupas dalībnieks uzdevumam ir jāpiešķir, izmantojot **uzdevuma nolaižamo izvēlni Piešķirtie resursi**. 

## <a name="updating-estimates"></a>Aplēšu atjaunināšana
Kad uzdevumiem ir piešķirti projekta grupas dalībnieki, jums būs jāpārvietojas uz **projekta cilni Novērtējumi** un jāatlasa **Atjaunināt cenas**, lai nodrošinātu, ka apakšuzņēmēja resursu piešķires izmaksu likmes tiek atjauninātas, pamatojoties uz apakšuzņēmējam pievienoto pirkšanas cenrādi. Aprēķini netiek ģenerēti nepiešķirtiem uzdevumiem programmā Microsoft Dynamics 365 Project Operations. Tā rezultātā jums būs jāizveido uzdevumu uzdevumi, lai noteiktu cenu un maksātu dažādus uzdevumus savā projektā. 

> [PIEZĪME!] Projekta grupas dalībnieki, kuru tips ir **Darbinieks kā** līgumdarbiniekam **, bet kuriem nav apakšuzņēmuma atsauces, projekta grupas dalībnieku** režģī tiek atzīmēti kā **nederīgi** **.** Ja ir kāds projekta grupas dalībnieks ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma un apakšuzņēmuma rindu laukus, lai finanšu izmaksu novērtējums precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē Novērtējumi**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
