---
title: Jaunumi 2021. gada decembra Project Operations Lite izvietošanā
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Project Operations Lite izvietošanas 2021. gada decembra izlaiduma ietvaros.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914089"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Jaunumi 2021. gada decembra Project Operations Lite izvietošanā

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

### <a name="subcontract-management"></a>Pakārtotā pārvaldība 

- [Apakšlīguma projekta darba grupas dalībnieki](../subcontracting/subcontracting-project-team-members.md): projekta vadītājs var izveidot nosauktus vai vispārējus darba grupas dalībniekus ar apakšlīgumiem un apakšlīgumu rindām, lai ietekmētu personāla izveidi un aprēķinus.
- [Apakšlīguma iespējas projekta grupas dalībniekiem](../subcontracting/subcon-options.md): veicot personāla komplektēšanas izvēles nosauktiem vai vispārējiem projekta darba grupas dalībniekiem, projekta vadītājs var pārskatīt esošos apakšlīgumus vai izveidot jaunus apakšlīgumus vienam vai vairākiem projekta darba grupas dalībniekiem. 
- [Apakšlīgumu resursu piešķīrumu izmaksu novērtējums](../subcontracting/costing-subcon-ra.md): projekta izmaksu aprēķinos tiks ņemti vērā apakšlīgumu resursu piešķīrumi, un to izmaksas tiks noteiktas, izmantojot pirkumu cenrāžus, kas saistīti ar apakšlīgumiem. 
- [Plānošanas paneļa konfigurēšana, lai parādītu līguma darbiniekus un apakšlīguma noslodzi](../subcontracting/configure-sb-subcon.md): plānošanas panelis programmā Project Operations tagad var tikt konfigurēts, lai meklētu un ieteiktu rezervējamo resursu līgumdarbinieku tipu un apakšlīgumu noslodzi ar darbiniekiem. Šo konfigurāciju var lietot, meklējot resursus saistībā ar personāla komplektēšanu konkrētai projekta prasībai vai meklējot ārpus projekta prasības konteksta.
- [Projekta personāla veidošana ar līguma darbiniekiem un apakšlīguma noslodzi](../subcontracting/staffing-cw.md): tagad līgumdarbiniekus var rezervēt projektiem, izmantojot plānošanas paneļa pieredzi.
- [Laika, izmaksu un materiālu izlietojuma reģistrēšana projektiem ar apakšlīguma komponentiem](../subcontracting/recording-subcon-actuals.md): līgumdarbinieki var ierakstīt laiku un izdevumus, un arī projekta darba grupas dalībnieki var ierakstīt iegādātos materiālus, izmantojot projekta apakšlīgumu. Tā rezultātā tiek ierakstītas precīzas izmaksas par projektiem, kuros tiek izmantota iegādātā noslodze vai materiāli.
- [Apakšlīguma statusa pārejas](../subcontracting/subcon-states.md): apakšlīgumus var apstiprināt, lai pabeigtu pārrunas ar piegādātāju, slēgts, lai norādītu piegādes pabeigšanu, vai atcelt, lai norādītu līguma izbeigšanu ar piegādātāju pirms piegādes pabeigšanas.

### <a name="task-planning"></a>Uzdevumu plānošana
- Uzlabota problēmu novēršana sistēmas administratoriem. Ja lietotājs nevar atvērt projektu, administrators var pārskatīt ar licencēm nesaistītas kļūdas, kas ģenerētas Project for the Web, [projektu plānošanas žurnālos](../../project-management/schedule-api-logs.md).
- [Uzdevumu kontrolsarakstu izmantošana risinājumā Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programmā Microsoft Project for the Web varat pievienot uzdevumam kontrolsarakstu, lai sekotu noteiktiem elementiem.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Plānošana un izsekošana | 2392596 | Plānošanas API tagad ļauj atjaunināt laukus **Atlikušais ieguldījums**, **Ieguldījums pabeigts** un **% pabeigti**. |
| Plānošana un izsekošana | 2478497 | Plānošanas API lauki **Darbības numurs** un **Uzdevuma ID** var būt tukši ievadē, jo sistēma tos aizpildīs, izmantojot automatizētu numerāciju.|
| Laiks un izdevumi | 2468135 | Apstiprinājuma mēģinājumu skaits tiek samazināts no pieciem līdz trim. |
| Laiks un izdevumi | 2468188 | Novērsta problēma ar žurnāla tekstu, kas pārsniedz maksimālo garumu entītijas **anotācija** atribūtā **notetext**. |
