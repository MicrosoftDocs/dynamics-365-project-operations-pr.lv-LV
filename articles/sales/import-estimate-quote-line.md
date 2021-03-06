---
title: Projekta aprēķinu importēšana projekta piedāvājuma rindā
description: Šajā tēmā sniegta informācija par to, kā importēt aprēķinus no projekta piedāvājuma rindā.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908359"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekta aprēķinu importēšana projekta piedāvājuma rindā

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Ja projekts ir izveidots posmā pirms pārdošanas, varat izvēlēties no projekta importēt finanšu aprēķinu projekta piedāvājuma rindā.

1. Pārliecinieties, ka projekta piedāvājuma rindas laukā **Projekts** ir projekta informācija.
2. Cilnē **Piedāvājuma rindas informācija** atlasiet vienumu **Importēt no projekta aprēķina**.
3. Atveras dialoga lapa; tajā atlasiet vienu no šīm kopsavilkuma opcijām.

  - **Transakciju klase**
  - **Kategorija**
  - **Loma** 
  - **Projekta uzdevums**

Pamatojoties uz veikto atlasi, projekta aprēķini par visām darījumu klasēm, kas iekļautas šajā piedāvājuma rindā, tiek kopētas. Lai pārbaudītu, kādas darījumu klases ir ietvertas, atlasiet cilni **Vispārīgi** projekta piedāvājuma rindā un pārbaudiet vērtības laukos **Iekļaut laiku**, **Iekļaut izdevumus** un **Iekļaut maksas**.

Importējot aprēķinus, sistēma pēc noklusējuma nosaka cenu pēc projekta cenrāžiem, kas piesaistīti piedāvājumam, un norēķinu tipam, kas iestatīts projekta piedāvājuma rindā. Ja kāda loma vai kategorija projekta piedāvājuma rindā ir iestatīta kā neiekļaujama rēķinā, importētā aprēķina rinda tiks iestatīta kā neiekļaujama rēķinā, un tā netiks pieskaitīta piedāvājuma rindas aprēķinātajai vērtībai.

Ja piedāvājuma rindai ir rindas informācija, piedāvājuma rindas lauki **Piedāvātā vērtība** un **Aprēķinātais nodoklis** tiek apkopoti, un tos nevar rediģēt.

Kad ir atlasītas vairākas kopsavilkuma opcijas, kopsavilkumā cenšas izmantot visas atlasītās opcijas. Tas nozīmē, ka importēto piedāvājuma rindu izvade būs lielāka nekā tad, ja atlasījāt tikai vienu kopsavilkuma opciju.

Piemēram, ja projektam ir šādi izdevumu rindu aprēķini.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| Uzdevums A | Lidojumi | 10/1/2020 | 4 | 400 | 1600 |
| Uzdevums B | Viesnīca | 10/1/2020 | 4 | Vairāk nekā 200 | 800 |
| Uzdevums C | Viesnīca | 11/1/2020 | 2 | Vairāk nekā 200 | 400 |

Kad lietotājs atlasa kopsavilkumu pēc Darījumu klases, tiek importēta šāda informācija.

| Uzdevums | Kategorija | Datums | Daudzums | Vienības cena | Apjoms/summa |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

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