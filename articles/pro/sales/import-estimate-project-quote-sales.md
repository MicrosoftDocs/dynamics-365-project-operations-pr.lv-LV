---
title: Projekta aprēķinu importēšana uz projekta piedāvājuma rindu — Lite
description: Šajā tēmā sniegta informācija par to, kā importēt aprēķinus no projekta piedāvājuma rindā.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5ac7827f3499aafb63f6bc0b8580ca52e883f272464532bd353170a12b3ae55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986140"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekta aprēķinu importēšana uz projekta piedāvājuma rindu 

_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_

Ja projekts ir izveidots posmā pirms pārdošanas, varat izvēlēties no projekta importēt finanšu aprēķinu projekta piedāvājuma rindā.

1. Pārliecinieties, ka projekta piedāvājuma rindas laukā **Projekts** ir projekta informācija.
2. Cilnē **Piedāvājuma rindas informācija** atlasiet vienumu **Importēt no projekta aprēķina**.
3. Atveras dialoga lapa; tajā atlasiet vienu no šīm kopsavilkuma opcijām.

  - **Transakciju klase**
  - **Kategorija**
  - **Loma** 
  - **Projekta uzdevums**

Pamatojoties uz veikto atlasi, projekta aprēķini par visām darījumu klasēm, kas iekļautas šajā piedāvājuma rindā, tiek kopētas. Lai pārbaudītu, kādas transakciju klases ir iekļauti, projekta piedāvājuma rindā atlasiet cilni **Vispārīgi** un pārbaudiet vērtības **Iekļaut laiku**, **Iekļaut izdevumus**, **Iekļaut materiālus** un **Iekļaut maksu**.  Lai pārbaudītu, kādi uzdevumi ir iekļauti, piedāvājuma rindā atlasiet cilni **Apmaksājamie uzdevumi**.

Atkarībā no saistītajiem uzdevumiem un iekļauto darījumu klasēm, šo uzdevumu un darījumu klašu kombināciju aprēķini tiek importēti piedāvājuma rindā.

Importējot aprēķinus, sistēma pēc noklusējuma nosaka cenu pēc projekta cenrāžiem, kas piesaistīti piedāvājumam, un norēķinu tipam, kas iestatīts projekta piedāvājuma rindā. Ja kāds uzdevums, loma vai kategorija projekta piedāvājuma rindā ir iestatīta kā neiekļaujama rēķinā, importētā aprēķina rinda tiks iestatīta kā neiekļaujama rēķinā, un tā netiks pieskaitīta piedāvājuma rindas aprēķinātajai vērtībai.

Ja piedāvājuma rindai ir rindas informācija, piedāvājuma rindas lauki **Piedāvātā vērtība** un **Aprēķinātais nodoklis** tiek apkopoti, un tos nevar rediģēt.

Kad ir atlasītas vairākas kopsavilkuma opcijas, sistēma cenšas apkopot visas atlasītās opcijas. Rezultātā importēto piedāvājuma rindu izvade būs lielāka nekā tad, ja atlasījāt tikai vienu kopsavilkuma opciju.

Piemēram, ja projektam bija šādi izdevumu rindu aprēķini.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |

Kad lietotājs atlasa kopsavilkumu pēc Darījumu klases, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Kad lietotājs atlasa kopsavilkumu pēc Darījumu klases un Kategorijas, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| | Viesnīca | 10/1/2020 | 6 | Vairāk nekā 200 | 1200 |

Kad lietotājs atlasa kopsavilkumu pēc Darījumu klases, Kategorijas un Lapas mezgla uzdevuma, tiek importēta šāda informācija. Ņemiet vērā, ka šis rezultāts ir tāds pats, kāds bija projektā.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
