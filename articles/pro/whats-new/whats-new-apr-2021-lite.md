---
title: 2021. gada aprīļa jaunumi — Project Operations Lite izvietošana
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada aprīļa Project Operations Lite izvietošanas laidienam.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 868d6daf8ac3ad9ef4245cef3c74a735137d3903
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994100"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>2021. gada aprīļa jaunumi — Project Operations Lite izvietošana

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

  - Project Operations Dataverse vides versijā 4.9.0.221 

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Krājumos neesoši materiāli projektiem. Galvenās iespējas ietver:
  - Krājumos neesošu materiālu novērtēšanu un cenu noteikšanu projekta pārdošanas ciklā. Plašāka informācija: [Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem (Lite)](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Krājumos neesošu materiālu izmantošanas izsekošana projekta piegādes laikā. Papildinformāciju skatiet rakstā [Materiālu lietojuma reģistrēšana projektos un projektu uzdevumos](../../material/material-usage-log.md).
  - Krājumos neesošu materiālu izmaksu izmantošana rēķinos. Papildinformāciju skatiet šeit: [Neizrakstīto rēķinu pārvaldība (Lite)](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Jaunie API programmā Dynamics 365 Dataverse ļauj izveidot, atjaunināt un dzēst operācijas ar **plānošanas entītijām**. Papildinformāciju skatiet šeit: [Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2224568 | Pievienota loģika, lai iespējotu pielāgojumus, kas ietver rēķina apstiprinājuma spraudņa aktivizēšanu. |
| Cenu noteikšana un norēķini | 2101098 | Ir uzlabota noklusējuma lauku loģika pro forma rēķinam: lauki **Rēķina adrese**, **Rēķina saņēmējs** un **Maksājumu nosacījumi** tagad pēc noklusējuma tiek aizpildīti ar informāciju no atbilstošā projekta līguma klienta ieraksta. |
| Cenu noteikšana un norēķini | 2021413 | Ir atjaunināti lauki **Faktiskās izmaksas** un **Pārdošana** entītijā **Uzdevums**, lai ietvertu pārdošanas vērtības no rēķinos ietvertajiem un neietvertajiem uzdevumu izdevumiem. |
| Cenu noteikšana un norēķini | 2182110 | Kopējot projekta līgumu, līguma rindas ID tiek atkārtoti ģenerēts mērķa projekta līgumā, lai nodrošinātu tā unikālitāti. |
| Iespēju pārvaldība | 2186741 | Ir pievienotas validācijas, lai lauku **Izcelsme** un **Transakcijas veids** nevarētu atjaunināt esoša piedāvājuma rindas informācijā. |
| Iespēju pārvaldība | 2191353 | Atskaites punktus nevar veidot laika un materiālu līguma rindās. |
| Iespēju pārvaldība | 2216956 | Novērstas problēmas ar **cenu atjaunināšanu**. |
| Plānošana un izsekošana | 2182979 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka izmaksu novērtējuma rindas tiek kopētas no sākotnējā projekta. |
| Plānošana un izsekošana | 2184144 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka resursa pozīcijas nosaukums tiek kopēts no sākotnējā projekta. |
| Plānošana un izsekošana | 2184799 | Projekta kopija: pastiprināta kontrole, lai kopēšanas laikā nevarētu mainīt prognozēto sākuma datumu. |
| Plānošana un izsekošana | 2185134 | Projekta kopija: projekta prognozētais sākuma datums ir iestatīts uz šodienas datumu. |
| Plānošana un izsekošana | 2196373 | Projekta kopija: pārbaudiet, vai projekta vadītāja un darba grupas dalībnieku ieraksti netiek dublēti projekta darba grupā. |
| Plānošana un izsekošana | 2211833 | Projekta kopija: resursu piešķīrumi tiek kopēti no avota projekta uzdevuma uz mērķa projektu. |
| Plānošana un izsekošana | 2186541 | Novērstas problēmas režģī **Novērtējums**, kad tiek veikta grupēšana pēc resursa. |
| Plānošana un izsekošana | 2166906 | Transakcijas kategorija no uzdevuma ir jākopē uz entītiju **Resursu piešķiršana**. |
| Resursu pārvaldība | 2125362 | Novērstas problēmas ar vispārīgās darba grupas dalībnieka izveidi, izmantojot metodi, kuras pamatā ir stundas. |
| Laiks un izdevumi | 2113603 | Novērsta ar pielāgošanu saistītā problēma, noņemot atribūtus no lapas **Laika ievade**. Tagad sistēma pārbauda, vai lapā ir atribūts, pirms piekļūstat tiem, izmantojot skriptu. |
| Laiks un izdevumi | 2204377 | Kopētajiem laika intervāliem ir automātiski jāparādās, kad atlasāt **Kopēt nedēļu**, ievadot laiku. |
| Laiks un izdevumi | 2209059 | Lauku **Statuss** var rediģēt Dynamics 365 Field Service laika ierakstiem. |
