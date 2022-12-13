---
title: Jaunumi 2022. gada oktobra Project Operations Lite izvietošanā
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations lite izvietošanas 2022. gada oktobra laidienā.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806761"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Jaunumi 2022. gada oktobra Project Operations Lite izvietošanā

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.57.0.176

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Projektu plānošana un izsekošana | **Projekta operācijas ārējā plānošana**<br>Ārējais plānošanas režīms ļauj klientiem vietēji izveidot, atjaunināt un dzēst entītijas, kas ir saistītas ar darba sadalījuma struktūrām (WBS), izmantojot vietējos Dataverse API, bez pašreizējiem ierobežojumiem, ko ievieš Project tīmeklī. | [Ārējā plānošana](/dynamics365/project-operations/project-management/external-scheduling) |
| Izvietošana un konfigurācija | <p>**Atļauja klientiem izvēlēties izvietošanas veidu**<br>Produkta vadīti Project Operations atjauninājumi (PDU) tiek izmantoti, lai automātiski instalētu Project Operations duālās rakstīšanas risinājumu, kad vidē ir instalēti divkodolu un orķestrācijas risinājumi.</p><p>Šis līdzeklis ievieš jaunu **risinājuma jaunināšanas uzvedības** parametru projekta parametros. Ja šis parametrs ir iestatīts tikai **uz Lite**, PUD vairs automātiski neinstalēs Project Operations dual-write risinājumu, pat ja vidē ir instalēti divkodolu un orķestrācijas risinājumi. Šāda rīcība dos labumu klientiem, kuri plāno izmantot duālās rakstīšanas risinājumus, lai integrētu pārdošanas pasūtījumus finanšu un operāciju programmās, bet vēlas izmantot Project Operations Lite režīmā (tas ir, bez integrācijas finanšu un operāciju programmās).</p> | |

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2316317 | Sistēma ļauj izveidot rēķinus, kuriem nav apmaksājamu transakciju. |
| Cenu noteikšana un norēķini | 2737300 | Pārbaudiet lauka Klients pieejamību, pirms tiek piekļūts veidlapai. |
| Cenu noteikšana un norēķini | 2744948 | Pievienojiet nulles pārbaudi norēķinu metodei. |
| Cenu noteikšana un norēķini | 2763515 | Nulles atsauces kļūdas apstrāde, ja trūkst rēķina pārdošanas līguma. |
| Cenu noteikšana un norēķini | 2844301 | Partijas rēķina izveide neizdodas kļūdas dēļ. |
| Cenu noteikšana un norēķini | 2845869 | Nepareiza organizācijas pakalpojuma glabāšana. |
| Cenu noteikšana un norēķini | 2853729 | Loma un Cena tiek atjaunināta, kad tiek mainīts norēķinu veids. |
| Cenu noteikšana un norēķini | 2940350 | Ja faktiskās cenas ir noteiktas, automātiski jāievada tikai aktīvie cenrāži. |
| Izvietošana un konfigurācija | 3001206 | Entītija msdyn\_ replaylogheader neļauj veikt klientu organizāciju jaunināšanu. |
| Iespēju pārvaldība | 2755582 | Nulles atsauces izņēmumu rokturis dalīto norēķinu kārtulu palīgā. |
| Iespēju pārvaldība | 2761477 | Ja tiek izmantoti dalīti norēķini, dzēšot atskaites punktu (galveni), tiek atstāti nezināmu atskaites punktu skaita atskaites punkti. |
| Iespēju pārvaldība | 2767595 | Kad materiāla lietojuma ieraksts tiek atvērts galvenajā veidlapā, ieraksta rezervējamais resurss tiek mainīts uz lietotāju, kurš pašlaik ir pierakstījies. |
| Projektu plānošana un izsekošana | 2790384 | Pending OperationSet taimauts ir pārāk īss. |
| Resursu pārvaldība | 2751560 | Nekonsekventas vēlamās organizācijas vienības resursu prasībās. |
| Apakšlīgumu slēgšana | 2907231 | Kreditoru rēķinu procesa posmā nevar virzīties uz priekšu. |
| Laiks un izdevumi | 2867363 | Ieraksti neizkrīt no skata Prombūtne/Brīvdienas apstiprināšanai, kad tie ir novietoti rindā apstiprināšanai. |
| Laiks un izdevumi | 2894405 | TESA: neizmantotais POC direktorijs izraisa atbilstības problēmas. |
