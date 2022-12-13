---
title: Aprēķinu importēšana no projekta uz projekta līguma rindu
description: Šajā rakstā sniegta informācija par to, kā importēt finanšu aprēķinus no projekta līguma rindā.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824684"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Aprēķinu importēšana no projekta uz projekta līguma rindu

_**Attiecas uz:** Lite izvietošanu - darījums proforma rēķinu izrakstīšanai, Projekta operācijas uz resursiem / bez krājumiem balstītiem scenārijiem_ _

Risinājumā Dynamics 365 Project Operations varat importēt aprēķinu projekta balstīta līguma rindā no projekta.

1. Pārbaudiet, vai projekta līguma rindas lauks **Projekts** ir aizpildīts.
2. Cilnes **Līguma rindas informācija** atlasiet vienumu **Importēt no projekta aprēķina**. Tiek atvērta dialoga lapa ar kopsavilkuma opcijām. Pieejamās kopsavilkuma opcijas ir **Darījumu klase**, **Kategorija**, **Loma** un **Projekta uzdevums**.
3. Pamatojoties uz kopsavilkuma atlasi, tiek kopēti projekta aprēķini par visām darījumu klasēm un uzdevumi, kas iekļautas šajā līguma rindā. Lai pārbaudītu, kādas darījumu klases ir ietvertas, cilnes **Vispārīgi** projekta līguma rindā pārbaudiet vērtības laukos **Iekļaut laiku**, **Iekļaut izdevumus** un **Iekļaut maksas**. 
4. Lai skatītu, kādi uzdevumi ir iekļauti, līguma rindā atlasiet cilni **Apmaksājamie uzdevumi**. Pamatojoties uz saistītajiem uzdevumiem, kuru lauks **Iekļautās darījumu klases** ir iestatīts uz **Jā**, visi šo uzdevumu un transakciju klašu kombināciju aprēķini tiek importēti līguma rindā.

Importējot aprēķinus, sistēma pēc noklusējuma nosaka cenu pēc projekta cenrāžiem, kas piesaistīti līgumam, un norēķinu tipa iestatījumam līguma rindā. Ja kāds uzdevums, loma vai kategorija līguma rindā ir iestatīta kā neiekļaujama rēķinā, importētā aprēķina rinda tiks iestatīta kā neiekļaujama rēķinā, un tā netiks pieskaitīta līguma rindas vērtībai.

Ja līguma rindai ir rindas informācija, līguma rindas lauki **Līguma vērtība** un **Aprēķinātais nodoklis** tiek apkopoti, un tos nevar rediģēt.

Kad ir atlasītas vairākas kopsavilkuma opcijas, sistēma cenšas izmantot visas atlasītās opcijas. Apkopošanas izvades rezultātā tiek importēts vairāk līguma rindu nekā tad, ja atlasāt tikai vienu kopsavilkuma opciju.

Piemēram, ja projektam ir šādi izdevumu rindu aprēķini.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases**, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases** un **Kategorijas**, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Viesnīca | 10/1/2020 | 6 | Vairāk nekā 200 | 1200 |

Kad lietotājs atlasa kopsavilkumu pēc **Darījumu klases**, **Kategorijas** un **Lapas mezgla uzdevuma**, tiek importēta šāda informācija. Ņemiet vērā, ka šis rezultāts ir tāds pats, kāds ir projektā.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
