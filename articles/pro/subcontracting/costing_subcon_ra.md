---
title: Apakšuzņēmēju resursu piešķires izmaksu novērtējums
description: Šajā tēmā ir paskaidrots, kā Microsoft Dynamics 365 Project Operations aprēķina izmaksu novērtējumu apakšuzņēmēju resursu piešķirēm.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903051"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Apakšuzņēmēju resursu piešķires izmaksu novērtējums

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšuzņēmēju projekta grupas dalībnieku uzdevumu piešķires tiek maksātas, izmantojot **pirkšanas** cenrādi, kas pievienots apakšuzņēmuma līgumam saistītā grupas dalībnieka ierakstā. Tas atšķiras no tā, kā tiek izmaksu izmaksas darbinieku resursu uzdevumiem, kur darbinieku resursu uzdevumu piešķires tiek izmaksas, izmantojot **izmaksu** cenrādi, kas piesaistīts projekta līgumslēdzējai vienībai. 

Vispārējiem projekta grupas dalībniekiem, par kuriem ir noslēgti apakšuzņēmuma līgumi, uzdevumi tiek maksāti, izmantojot lomu cenu iestatījumus pirkšanas cenrādī, kas pievienots apakšuzņēmuma līgumam. Iepirkuma cenas var iestatīt arī tieši katram resursam. Šīm resursiem specifiskajām cenām tiks piešķirta prioritāte, ja nosaukto projekta grupas dalībnieku uzdevumu piešķiršana ir līgumdarbinieki. 

Prioritāti, izmantojot konkrētai lomai specifisku pirkšanas cenu un resursu specifiskām, nosaka cenu dimensijas prioritātes iestatīšana **parametros > uz summu balstītās cenu dimensijās**.

Šī dinamiski iegūto cenu funkcionalitāte, kuras pamatā ir apakšuzņēmēju pirkšanas cenu dimensiju iestatījumi, ir līdzīga tam, kā pilnas slodzes darbiniekiem tiek iegūtas izmaksu un rēķinu likmes. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Uzdevumu uzdevumu uzdevumu izveide apakšuzņēmēju resursu izmaksu aprēķinu iegūšanai

Uzdevumu uzdevumus apakšuzņēmējiem var izveidot divos veidos: 
- Cilnes **Uzdevumi** izmantošana.
- Cilnes **Komanda** izmantošana.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resursu piešķirju izveide, izmantojot cilni Uzdevumi
Izmantojot **resursu** sarakstu **cilnē Uzdevumi** noteiktam uzdevumam, varat izveidot uzdevuma piešķiršanu nosauktam resursam vai vispārējam resursam. Ja uzdevuma nolaižamajā izvēlnē Piešķirtie resursi atlasāt nosauktu resursu **un šis resurss ir** līgumdarbinieks, nosauktais resurss tiek piešķirts uzdevumam un tiek izveidots atbilstošs projekta grupas dalībnieka ieraksts ar darbinieka tipu, kas iestatīts uz **Līguma darbinieks un** **derīgums** ir iestatīts uz **Nederīgs**. Kā nākamo soli jums būs jāatver projekta grupas dalībnieka ieraksts un jāatlasa apakšuzņēmuma un apakšuzņēmuma līgumu rinda. Tādējādi tiks atjaunināta uzdevuma piešķiršana, lai būtu atsauce uz apakšuzņēmuma līgumu un apakšuzņēmuma rindu, kā arī atjauninās grupas dalībnieka statusu uz **Derīgs**.

Ja izvēlaties izveidot vispārīgu grupas dalībnieku no **uzdevuma nolaižamās daļas Piešķirtie** resursi, **dialoglodziņš Vispārīga grupas dalībnieka izveide** ļauj atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu. Kad uzdevumam ir piešķirts vispārējais resurss un ir izveidots atbilstošais projekta grupas dalībnieka ieraksts, pamanīsit, ka projekta grupas dalībnieka ieraksts ir izveidots ar darbinieka tipu, kas iestatīts uz **Līgumdarbinieks** un **derīgums** ir iestatīts uz **Derīgs**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekta grupas dalībnieku izveide, izmantojot cilni Komanda
Izmantojot projekta cilni Komanda, varat izveidot vispārīgu vai nosauktu grupas dalībnieku. Veidojot grupas dalībnieku, varat atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu. Pēc grupas dalībnieka izveides grupas dalībnieks ir jāpiešķir uzdevumam, izmantojot **uzdevuma** nolaižamo laukumā Piešķirtie resursi. 

## <a name="updating-estimates"></a>Budžetu atjaunināšana
Kad projekta grupas dalībnieki ir piešķirti uzdevumiem, jums ir jāorientējas **uz projekta cilni Novērtējumi un** jāatlasa Atjaunināt **cenas**, lai nodrošinātu, ka apakšuzņēmēju resursu piešķires izmaksu likmes tiek atjauninātas, pamatojoties uz apakšuzņēmuma līgumam pievienoto iepirkuma cenrādi. Ņemiet vērā, ka novērtējumi nepiešķirtajiem uzdevumiem programmā Microsoft Dynamics 365 Project Operations. Tā rezultātā jums būs jāizveido uzdevumu uzdevumi, lai cena un izmaksas dažādiem uzdevumiem jūsu projektā. 

> [PIEZĪME!] Projekta grupas dalībnieki, kuru tips ir **Darbinieks** kā **Līgumdarbinieks**, bet kuriem nav apakšuzņēmuma līguma atsauces, projekta grupas dalībnieku režģī tiek atzīmēti **kā** **nederīgi**. Ja ir kāds projekta grupas dalībnieks ar šādu statusu, atveriet projekta grupas dalībnieka ierakstu un manuāli atjauniniet apakšuzņēmuma līgumu un apakšuzņēmuma rindu laukus, lai finanšu izmaksu novērtējums precīzi atspoguļotu apakšuzņēmēja izmaksas **cilnē** Novērtējumi. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
