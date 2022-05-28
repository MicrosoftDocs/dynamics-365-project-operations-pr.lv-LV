---
title: Kas jauns 2021. gada decembris - Project Operations lite izvietošana
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Project Operations lite izvietošanas 2021. gada decembra laidienā.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585387"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Kas jauns 2021. gada decembris - Project Operations lite izvietošana

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

### <a name="subcontract-management"></a>Apakšuzņēmuma līgumu pārvaldība 

- [Apakšuzņēmuma līgumi par projekta komandas locekļiem](../subcontracting/subcontracting-project-team-members.md): projekta vadītājs var izveidot nosauktus vai vispārīgus komandas locekļus ar apakšuzņēmuma līgumiem un apakšuzņēmuma līgumu līnijām, lai ietekmētu personālu un novērtējumu.
- [Apakšuzņēmuma līgumu slēgšanas iespējas projekta komandas locekļiem](../subcontracting/subcon-options.md): Veicot personāla izvēli nosauktiem vai vispārīgiem projekta komandas locekļiem, projekta vadītājs var pārskatīt esošos apakšlīgumus vai izveidot jaunus apakšlīgumus vienam vai vairākiem projekta komandas locekļiem. 
- [Apakšuzņēmēju resursu piešķires](../subcontracting/costing-subcon-ra.md) izmaksu novērtējums: projekta izmaksu novērtējumā tiks ņemtas vērā apakšuzņēmēju resursu piešķires un tām tiks izmaksātas izmaksas, izmantojot pirkšanas cenrāžus, kas saistīti ar apakšuzņēmuma līgumiem. 
- [Konfigurēt grafika valdi, lai rādītu līgumdarbiniekus un apakšuzņēmēju noslodzi](../subcontracting/configure-sb-subcon.md): grafika paneli projekta operācijās tagad var konfigurēt, lai kopā ar darbiniekiem meklētu un ieteiktu līgumdarbinieku reģistrējamo resursu tipu un apakšuzņēmēju noslodzi. Šo konfigurāciju var lietot, meklējot resursus konkrētas projekta prasības personāla kontekstā vai meklējot ārpus projekta prasības konteksta.
- [Projekta personāls ar līgumdarbiniekiem un apakšuzņēmēju spējām](../subcontracting/staffing-cw.md): līgumdarbiniekus tagad var rezervēt projektos, kas izmanto grafiku sastādīšanas pieredzi.
- [Ieraksta laiku, izdevumus un materiālu patēriņu projektos apakšuzņēmēju komponentiem](../subcontracting/recording-subcon-actuals.md): līgumdarbinieki var reģistrēt laiku un izdevumus, un projekta komandas locekļi var arī reģistrēt to materiālu izmantošanu, kas iegādāti, izmantojot apakšlīgumu par projektu. Tā rezultātā tiks reģistrētas precīzas izmaksas projektiem, kas izmanto iegādāto jaudu vai materiālus.
- [Valsts pārejas uz apakšuzņēmuma līgumu](../subcontracting/subcon-states.md): apakšuzņēmuma līgumus var apstiprināt, lai pabeigtu sarunas ar piegādātāju, slēgt, lai norādītu uz piegādes pabeigšanu, vai atcelt, lai norādītu uz līguma izbeigšanu ar piegādātāju pirms piegādes pabeigšanas.

### <a name="task-planning"></a>Uzdevumu plānošana
- Uzlabota problēmu novēršana sistēmas administratoriem. Ja lietotājs nevar atvērt projektu, administrators projektu plānošanas žurnālos [var pārskatīt ar licenci nesaistītas](../../project-management/schedule-api-logs.md) kļūdas, kas ģenerētas no project tīmeklī tīmeklī.
- [Izmantojiet uzdevumu kontrolsarakstus programmā Microsoft Project tīmeklim](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programmā Microsoft Project for the web uzdevumam varat pievienot kontrolsarakstu, lai sekotu noteiktiem vienumiem.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Plānošana un izsekošana | 2392596 | Ieplānot API tagad ļauj atjaunināt laukus **Atlikusī** piepūle, **Pabeigtā** piepūle un **% pabeigts**. |
| Plānošana un izsekošana | 2478497 | Grafiskie API **darbības numurs** un **uzdevuma ID** lauki ievades laikā var būt tukši, jo sistēma tos aizpildīs, izmantojot automatizētu numerāciju.|
| Laiks un izdevumi | 2468135 | Atkārtoto mēģinājumu skaits tiek samazināts no pieciem uz trim. |
| Laiks un izdevumi | 2468188 | Novērsta problēma ar žurnāla tekstu, kas pārsniedz anotācijas entītijas piezīmjteksta **atribūta** maksimālo garumu **.** |
