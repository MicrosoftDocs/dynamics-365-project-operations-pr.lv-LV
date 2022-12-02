---
title: Apakšlīgumu resursu piešķīrumu izmaksu novērtējums
description: Šajā rakstā ir izskaidrots, kā programma Microsoft Dynamics 365 Project Operations aprēķina apakšlīgumu resursu piešķīrumu izmaksu novērtējumu.
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

Apakšlīgumu projekta darba grupas dalībnieku uzdevumu piešķīrumu cena tiek noteikta, izmantojot cenrādi **Pirkums**, kas pievienots saistītā darba grupas dalībnieka ieraksta apakšlīgumam. Tas atšķiras no veida, kā tiek noteikta darbinieku resursu piešķīrumu cena, kur darbinieku resursu uzdevumu piešķīrumu cenas tiek noteiktas, izmantojot cenrādi **Izmaksas**, kas ir pievienots projekta līgumslēdzēja vienībai. 

Vispārējiem projekta darba grupas dalībniekiem, kuriem ir apakšlīgums, piešķīrumu cena tiek noteikta, izmantojot uz lomu balstītu iestatījumu pirkuma cenrādi, kas pievienots apakšlīgumam. Pirkuma cenas var iestatīt arī atsevišķi katram resursam. Šīm atsevišķu resursu cenām tiek piešķirta prioritāte, kad nosauktu projekta darba grupas dalībnieku uzdevumu piešķīrumi, kuriem tiek noteikta cena, ir līgumdarbinieki. 

Lomai specifisko iegādes cenu prioritāti pret resursam specifisku cenu nosaka cenu noteikšanas prioritātes dimensijas iestatījums sadaļā **Parametri > Uz summu balstītas cenu noteikšanas dimensijas**.

Šī dinamiskās cenu atvasināšanas funkcionalitāte, kas balstīta uz apakšuzņēmēju pirkuma cenu dimensijas iestatījumu, darbojas līdzīgi kā izmaksu un norēķinu likmju atvasināšana pilna laika darbiniekiem. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Uzdevumu piešķīrumu izveide, lai iegūtu apakšuzņēmēju resursu izmaksu aprēķinus

Uzdevumu piešķīrumus apakšuzņēmējiem var izveidot divos veidos: 
- izmantojot cilni **Uzdevumi**;
- izmantojot cilni **Darba grupa**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resursu piešķīrumu izveide, izmantojot cilni Uzdevumi
Izmantojot sarakstu **Resursi** cilnē **Uzdevumi** noteiktam uzdevumam, varat izveidot uzdevuma piešķīrumu nosauktam resursam vai vispārējam resursam. Ja atlasāt nosauktu resursu uzdevuma nolaižamajā sarakstā **Piešķirtie resursi** un šis resurss ir līgumdarbinieks, uzdevumam tiek piešķirts nosauktais resurss un tiek izveidots atbilstošs projekta darba grupas dalībnieka ieraksts ar darbinieka tipu, kas iestatīts kā **Līgumdarbinieks**, un vienuma **Derīgums** iestatījums ir **Nederīgs**. Nākamajā darbībā jums ir jāatver projekta darba grupas dalībnieka ieraksts un jāatlasa apakšlīgums un apakšlīguma rinda. Tādējādi uzdevuma piešķīrums tiek atjaunināts, lai tajā būtu atsauce uz apakšlīgumu un apakšlīguma rindu, un darba grupas dalībnieka statuss tiks atjaunināts uz **Derīgs**.

Ja atlasāt vispārēju darba grupas dalībnieku nolaižamajā uzdevuma sarakstā **Piešķirtie resursi**, dialoglodziņā **Vispārēja darba grupas dalībnieka izveide** varat atlasīt apakšlīgumu un apakšlīguma rindu. Piešķirot vispārēju resursu uzdevumam un izveidojot atbilstošo projekta darba grupas dalībnieka ierakstu, jūs ievērosit, ka projekta darba grupas dalībnieka ieraksts ir izveidots ar darbinieka tipu **Līgumdarbinieks** un **Derīgums** ir iestatīts uz **Derīgs**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekta darba grupas dalībnieku izveide, izmantojot cilni Darba grupa
Izmantojot projekta cilni Darba grupa, varat izveidot vispārīgu vai nosauktu darba grupas dalībnieku. Veidojot darba grupas dalībnieku, varat atlasīt apakšlīgumu un apakšlīguma rindu. Pēc darba grupas dalībnieka izveides šis darba grupas dalībnieks ir jāpiešķir uzdevumam, izmantojot uzdevuma nolaižamo sarakstu **Piešķirtie resursi**. 

## <a name="updating-estimates"></a>Aprēķinu atjaunināšana
Kad projekta darba grupas dalībnieki ir piešķirti uzdevumiem, jāpāriet uz cilni **Aprēķini** projektā un jāatlasa **Atjaunināt cenas**, lai nodrošinātu, ka apakšuzņēmēja resursu piešķīrumu izmaksu likmes tiek atjauninātas, pamatojoties uz apakšlīgumam pievienoto pirkumu cenrādi. Nepiešķirtiem uzdevumiem aprēķini programmā Microsoft Dynamics 365 Project Operations netiek ģenerēti. Tāpēc ir jāizveido uzdevumu piešķīrumi, lai noteiktu cenu un izmaksas dažādiem uzdevumiem projektā. 

> [PIEZĪME!] Projekta darba grupas dalībnieki, kuru **Darbinieka tips** ir **Līgumdarbinieks**, bet nav apakšlīguma atsauces, ir atzīmēti ar **Nederīgs** režģī **Projekta darba grupas dalībnieki**. Ja pastāv projekta darba grupas dalībnieki ar šo statusu, atveriet projekta darba grupas dalībnieka ierakstu un manuāli atjauniniet apakšlīgumu un apakšlīguma rindas laukus, lai finanšu izmaksu aprēķins precīzi atspoguļotu apakšuzņēmēja izmaksas cilnē **Aprēķini**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
