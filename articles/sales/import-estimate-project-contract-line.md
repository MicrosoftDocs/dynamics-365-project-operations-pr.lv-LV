---
title: Aprēķina importēšana uz projekta līguma rindu
description: Šajā tēmā sniegta informācija par to, kā importēt aprēķinus no projekta līguma rindā.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea513ca8126eadbf563f3c6cb3e966f81703ae805d12881f865cdc1dd77e191d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990100"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Aprēķina importēšana uz projekta līguma rindu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Risinājumā Dynamics 365 Project Operations varat importēt aprēķinu projekta balstīta līguma rindā no projekta.

1. Pārbaudiet, vai projekta līguma rindas lauks **Projekts** ir aizpildīts.
2. Cilnes **Līguma rindas informācija** apakšrežģī atlasiet vienumu **Importēt no projekta aprēķina**. Tiek atvērta dialoga lapa ar kopsavilkuma opcijām. Pieejamās kopsavilkuma opcijas ir **Darījumu klase**, **Kategorija**, **Loma** un **Projekta uzdevums**. Pamatojoties uz kopsavilkuma atlasi, tiek kopēti projekta aprēķini par visām darījumu klasēm, kas iekļautas šajā līguma rindā. 
3. Lai pārbaudītu, kādas darījumu klases ir ietvertas, cilnes **Vispārīgi** līguma rindā pārbaudiet vērtības laukos **Iekļaut laiku**, **Iekļaut izdevumus** un **Iekļaut maksas**.

Importējot aprēķinus, lietojumprogramma pēc noklusējuma nosaka cenu pēc projekta cenrāžiem, kas piesaistīti līgumam, un norēķinu tipa iestatījumam līguma rindā. Ja kāda loma vai kategorija līguma rindā ir iestatīta kā neiekļaujama rēķinā, importētā aprēķina rinda šai lomai vai kategorijai ir iestatīta kā neiekļaujama rēķinā, un tā netiks pieskaitīta līguma rindas vērtībai.

Ja līguma rindai ir rindas informācija, līguma rindas lauki **Līguma vērtība** un **Aprēķinātais nodoklis** tiek apkopoti, un tos nevar rediģēt.

Kad ir atlasītas vairākas kopsavilkuma opcijas, sistēma cenšas izmantot visas atlasītās opcijas. Apkopošanas izvades rezultātā tiek importēts vairāk līguma rindu nekā tad, ja atlasāt tikai vienu kopsavilkuma opciju.

Piemēram, ja projektam bija šādi izdevumu rindu aprēķini.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases**, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases** un **Kategorijas**, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Viesnīca | 10/1/2020 | 6 | Vairāk nekā 200 | 1200 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases**, **Kategorijas** un **Lapas mezgla uzdevuma**, tiek importēta šāda informācija. Ņemiet vērā, ka šis rezultāts ir tāds pats, kāds bija projektā.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]