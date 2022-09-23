---
title: Apakšlīgumu resursu piešķīrumu izmaksu novērtējums
description: Šajā rakstā ir paskaidrots, kā Microsoft Dynamics 365 Project Operations aprēķina ar apakšlīgumiem saistīto resursu cesiju izmaksu tāmi.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522665"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Apakšlīgumu resursu piešķīrumu izmaksu novērtējums

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Apakšuzņēmuma līgumu projekta grupas dalībnieku uzdevumu piešķiršana tiek apmaksāta, **izmantojot pirkšanas** cenrādi, kas pievienots apakšlīgumam saistītajā grupas dalībnieku ierakstā. Tas atšķiras no tā, kā tiek izmaksātas darbinieku resursu piešķiršanas izmaksas, ja darbinieku resursu uzdevumu piešķiršana tiek apmaksāta, izmantojot **izmaksu** cenrādi, kas ir pievienots projekta līgumslēdzēja vienībai. 

Vispārējiem projekta grupas dalībniekiem, kuriem ir apakšlīgums, par cesijām tiek maksāts, izmantojot uz lomām balstītu cenu iestatījumu apakšuzņēmuma līgumam pievienotajā pirkšanas cenrādī. Pirkšanas cenas var iestatīt arī tieši katram resursam. Šīm resursiem raksturīgajām cenām tiks piešķirta prioritāte, ja nosaukto projekta grupas dalībnieku uzdevumu uzdevumu izmaksas ir līgumdarbinieki. 

Lomai atbilstošas pirkšanas cenas, salīdzinot ar resursiem specifisku, izmantošanas prioritāti nosaka cenu dimensijas prioritātes iestatīšana parametros **> uz apjomu balstītas cenu noteikšanas dimensijās**.

Šī dinamiski atvasināmo cenu funkcionalitāte, pamatojoties uz dimensiju iestatīšanu apakšuzņēmēju iepirkuma cenām, ir līdzīga tam, kā tiek iegūtas izmaksu un rēķinu likmes pilnas slodzes darbiniekiem. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Uzdevumu piešķiršanu izveide apakšuzņēmēju resursu izmaksu tāmes iegūšanai

Uzdevumu piešķiršanu apakšuzņēmējiem var izveidot divos veidos: 
- **Izmantojot cilni Uzdevumi**.
- **Izmantojot cilni Komanda**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resursu piešķiršanas izveide, izmantojot cilni Uzdevumi
**Izmantojot sarakstu** Resursi **cilnē Uzdevumi** konkrētam uzdevumam, varat izveidot uzdevuma piešķiršanu nosauktam resursam vai vispārīgam resursam. Ja atlasāt nosauktu resursu no **uzdevuma nolaižamās izvēlnes Piešķirtie resursi** un šis resurss ir līgumdarbinieks, nosauktais resurss tiek piešķirts uzdevumam un tiek izveidots atbilstošs projekta grupas dalībnieka ieraksts ar darbinieka tipu, kas iestatīts uz **Līgumdarbinieks** un **Derīgums** ir iestatīts uz **Nederīgs**. Nākamajā solī jums būs jāatver projekta grupas dalībnieka ieraksts un jāizvēlas apakšlīguma un apakšlīguma rindiņa. Tas atjauninās uzdevumu piešķiršanu, lai būtu atsauce uz apakšuzņēmuma līgumu un apakšlīgumu līniju, kā arī atjauninās komandas dalībnieka statusu uz **Derīgs**.

Ja izvēlaties izveidot vispārīgu darba grupas dalībnieku no **uzdevuma nolaižamās izvēlnes Piešķirtie resursi**, **dialoglodziņš Vispārējs grupas dalībnieka izveide** ļaus jums atlasīt apakšlīgumu un apakšlīgumu rindu. Kad uzdevumam ir piešķirts vispārīgais resurss un ir izveidots atbilstošais projekta grupas dalībnieka ieraksts, jūs pamanīsit, ka projekta grupas dalībnieka ieraksts tiek izveidots ar darbinieka tipu, kas iestatīts uz **Līgumdarbinieks** un **Derīgums ir iestatīts** uz **Derīgs**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekta grupas dalībnieku izveide, izmantojot cilni Darba grupa
Izmantojot projekta cilni Darba grupa, varat izveidot vispārīgu vai nosauktu darba grupas dalībnieku. Veidojot darba grupas dalībnieku, varat atlasīt apakšlīguma un apakšlīguma rindu. Kad darba grupas dalībnieks ir izveidots, jums būs jāpiešķir darba grupas dalībniekam uzdevums, **izmantojot uzdevuma nolaižamo izvēlni Piešķirtie resursi**. 

## <a name="updating-estimates"></a>Tāmju atjaunināšana
Pēc tam, kad esat piešķīris uzdevumus projekta grupas dalībniekiem, jums būs jāpārvietojas **uz projekta cilni Aplēses** un jāatlasa **Atjaunināt cenas**, lai nodrošinātu, ka apakšuzņēmēju resursu piešķiršanas izmaksu likmes tiek atjauninātas, pamatojoties uz apakšlīgumam pievienoto pirkšanas cenrādi. Aprēķini netiek ģenerēti nepiešķirtiem uzdevumiem pakalpojumā Microsoft Dynamics 365 Project Operations. Tā rezultātā jums būs jāizveido uzdevumu uzdevumi, lai noteiktu cenu un maksātu par dažādiem uzdevumiem jūsu projektā. 

> [PIEZĪME!] Projekta grupas dalībnieki, kuriem ir **tips** Darbinieks kā **līgumdarbinieks**, bet kuriem nav atsauces uz apakšlīgumu, tiek atzīmēti kā **Nederīgi** **projekta grupas dalībnieku** režģī. Ja ir kādi projekta grupas dalībnieki ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindas laukus, lai finanšu izmaksu tāme precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē Aplēses**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
