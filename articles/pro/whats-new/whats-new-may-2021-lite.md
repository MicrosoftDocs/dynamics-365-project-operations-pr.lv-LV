---
title: 2021. gada maija jaunumi — Project Operations Lite izvietošana
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada maija Project Operations Lite izvietošanas laidienam.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060442"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>2021. gada maija jaunumi — Project Operations Lite izvietošana

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

   - Project Operations Dataverse vides versijā 4.10.0.186.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- [Plānošanas režīmi](../../project-management/scheduling-modes.md): projektu vadītāji tagad var definēt, vai projektu vajadzētu pārvaldīt, izmantojot fiksēta ilguma, fiksēta darba vai fiksētu vienību plānošanas režīmu.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2224568 | Pievienota loģika, lai iespējotu pielāgojumus, kas ietver rēķina apstiprinājuma spraudņa aktivizēšanu. |
| Cenu noteikšana un norēķini | 2101098 | Uzlabota noklusējuma lauku loģika attiecībā uz pro formas rēķinu. Šie lauki ir **Rēķina adrese**, **Rēķina saņēmēja nosaukums** un **Maksājuma nosacījumi**. Tagad lauki pēc noklusējuma tiek aizpildīti no atbilstošā projekta līguma klienta ieraksta. |
| Cenu noteikšana un norēķini | 2021413 | Ir atjaunināti lauki **Faktiskās izmaksas** un **Pārdošana** entītijā **Uzdevums**, lai ietvertu pārdošanas vērtības no rēķinos ietvertajiem un neietvertajiem uzdevumu izdevumiem. |
| Cenu noteikšana un norēķini | 2182110 | Kopējot projekta līgumu, līguma rindas ID tiek atkārtoti ģenerēts mērķa projekta līgumā, lai nodrošinātu tā unikālitāti. |
| Iespēju pārvaldība | 2186741 | Ir pievienotas validācijas, lai lauku **Izcelsme** un transakcijas veidu nevarētu atjaunināt esoša piedāvājuma rindas informācijā. |
| Iespēju pārvaldība | 2191353 | Atskaites punktu izveide nedrīkst tikt atļauta laika un materiālu līguma rindās. |
| Iespēju pārvaldība | 2216956 | Novērstas problēmas ar **cenu atjaunināšanu**. |
| Plānošana un izsekošana | 2182979 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka izmaksu novērtējuma rindas tiek kopētas no sākotnējā projekta. |
| Plānošana un izsekošana | 2184144 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka resursa pozīcijas nosaukums tiek kopēts no sākotnējā projekta. |
| Plānošana un izsekošana | 2184799 | Pastiprināta kontrole, kopējot projektu, lai kopēšanas laikā nevarētu mainīt prognozēto sākuma datumu. |
| Plānošana un izsekošana | 2185134 | Projekta kopēšanas laikā mērķa projekta prognozētais sākuma datums ir iestatīts uz šodienas datumu. |
| Plānošana un izsekošana | 2196373 | Pārbaudiet, vai, kopējot projektu, projekta vadītāja un darba grupas dalībnieku ieraksti netiek dublēti projekta darba grupā. |
| Plānošana un izsekošana | 2211833 | Resursu piešķīrumi tiek kopēti no avota projekta uzdevuma uz mērķa projektu. |
| Plānošana un izsekošana | 2186541 | Novērstas problēmas režģī **Novērtējums**, kad tiek veikta grupēšana pēc parametra **Resurss**. |
| Plānošana un izsekošana | 2166906 | Transakcijas kategorija no uzdevuma ir jākopē uz entītiju **Resursu piešķiršana**. |
| Resursu pārvaldība | 2125362 | Novērstas problēmas ar vispārīgās darba grupas dalībnieka izveidi, izmantojot metodi, kuras pamatā ir stundas. |
| Laiks un izdevumi | 2113603 | Novērsta ar pielāgošanu saistītā problēma, noņemot atribūtus no lapas **Laika ievade**. Tagad sistēma pārbauda, vai lapā ir atribūts, pirms piekļūstat tam, izmantojot skriptu. |
| Laiks un izdevumi | 2204377 | Kopētajiem laika intervāliem ir automātiski jāparādās, kad atlasāt **Kopēt nedēļu**. |
| Laiks un izdevumi | 2209059 | Lauks **Statuss** ir rediģējams Dynamics 365 Field Service laika ierakstiem. |
