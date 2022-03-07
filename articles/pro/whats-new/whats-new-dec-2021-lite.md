---
title: Jaunumi 2021. gada decembris - projekta operāciju lite izvietošana
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada decembra projekta operāciju lite izvietošanas laidienā.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942986"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Jaunumi 2021. gada decembris - projekta operāciju lite izvietošana

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šī tēma attiecas uz šādiem Microsoft komponentiem un versijām Dynamics 365 Project Operations:

- Projekta operācijas Dataverse vides versijā 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

### <a name="subcontract-management"></a>Apakšuzņēmuma līgumu pārvaldība 

- [Apakšuzņēmuma līgumu slēgšana projekta grupas dalībniekiem](../subcontracting/subcontracting-project-team-members.md) : projekta vadītājs var izveidot nosauktus vai vispārīgus grupas dalībniekus ar apakšuzņēmuma līgumu līnijām un apakšuzņēmuma līnijām, lai ietekmētu personāla komplektēšanu un novērtēšanu.
- [Apakšuzņēmuma līgumu slēdzot opcijas projekta grupas dalībniekiem](../subcontracting/subcon-options.md) : veicot personāla izvēli nosauktiem vai vispārīgiem projekta grupas dalībniekiem, projekta vadītājs var pārskatīt esošos apakšuzņēmuma līgumus vai izveidot jaunus apakšuzņēmuma līgumus vienam vai vairākiem projekta grupas dalībniekiem. 
- [Apakšuzņēmēju resursu piešķires izmaksu novērtējums](../subcontracting/costing-subcon-ra.md) : projekta izmaksu aprēķinā tiks ņemti vērā apakšuzņēmēju resursu piešķīrumi un izmaksas, izmantojot ar apakšuzņēmuma līgumu slēgumiem saistītos iepirkuma cenrāžus. 
- [Konfigurējiet plānošanas padomi, lai parādītu līgumdarbiniekus un apakšuzņēmēju noslodzi](../subcontracting/configure-sb-subcon.md) : projekta operāciju plānošanas dēli tagad var konfigurēt tā, lai kopā ar darbiniekiem meklētu un ieteiktu līgumdarbiniekam rezervējamo resursu tipu un apakšuzņēmēju noslodzi. Šo konfigurāciju var lietot, meklējot resursus saistībā ar personāla komplektēšanu noteiktai projekta vajadzībai vai meklējot ārpus projekta prasības konteksta.
- [Personāla personāls projektā ar līgumdarbiniekiem un apakšuzņēmēju spējām](../subcontracting/staffing-cw.md) : līgumdarbiniekus tagad var rezervēt projektos, izmantojot grafiku valdes pieredzi.
- [Laika, izdevumu un materiālu izmantošanas reģistrēšana projektos apakšuzņēmēju komponentiem](../subcontracting/recording-subcon-actuals.md) : līgumdarbinieki var reģistrēt laiku un izdevumus, un projekta grupas dalībnieki var arī reģistrēt to materiālu izmantošanu, kas iegādāti, izmantojot projekta apakšuzņēmuma līgumu. Tā rezultātā tiks ierakstītas precīzas izmaksas projektiem, kuros tiek izmantota iegādātā jauda vai materiāli.
- [Valsts pārejas uz apakšuzņēmuma līgumu](../subcontracting/subcon-states.md) : apakšuzņēmuma līgumus var apstiprināt, lai pabeigtu sarunas ar pārdevēju, slēgti, lai norādītu piegādes pabeigšanu, vai atcelti, lai norādītu līguma izbeigšanu ar pārdevēju pirms piegādes pabeigšanas.

### <a name="task-planning"></a>Uzdevumu plānošana
- Uzlabota problēmu novēršana sistēmas administratoriem. Ja lietotājs nevar atvērt projektu, administrators var pārskatīt ar licenci nesaistītas kļūdas, kas ģenerētas no project tīmeklim [projektu plānošanas žurnālos](../../project-management/schedule-api-logs.md).
- [Izmantojiet uzdevumu kontrolsarakstus programmā Microsoft Project tīmeklim](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programmā Microsoft Project tīmeklim varat pievienot kontrolsarakstu uzdevumam, lai sekotu noteiktiem vienumiem.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Plānošana un izsekošana | 2392596 | Plānot API tagad ļauj atjaunināt **atlikušos centienus**, **Pabeigtās pūles** un % **pabeigt**. |
| Plānošana un izsekošana | 2478497 | Ieplānot API **aktivitātes numuru un uzdevuma ID laukus** **ievades** laikā var aizpildīt, jo sistēma tos aizpildīs, izmantojot automātisko numerēšanu.|
| Laiks un izdevumi | 2468135 | Atkārtoto apstiprinājuma mēģinājumu skaits tiek samazināts no pieciem līdz trim. |
| Laiks un izdevumi | 2468188 | Novērsta problēma ar žurnāla tekstu, kas pārsniedz maksimālo garumu **anotācijas entītijas piezīmju teksta** **atribūtā.** |
