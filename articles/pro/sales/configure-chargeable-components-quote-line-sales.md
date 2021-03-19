---
title: Piedāvājuma rindas maksas komponentu konfigurēšana — Lite
description: Šajā tēmā ir sniegta informācija par apmaksājamu un neapmaksājamu komponentu iestatīšanu projekta piedāvājuma rindā.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273882"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Piedāvājuma rindas maksas komponentu konfigurēšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājuma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.

Uz iekļautajiem komponentiem attiecas tālāk norādītais.

  - Norēķinu metode un klientu sadalījums
  - Nepārsniedzamie ierobežojumi 
  - Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta piedāvājuma rindā

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**. Lauks **Norēķinu tips** ir opciju kopa, kas piedāvājuma rindas kontekstā ļauj izmantot šādas vērtības:

  - Izrakstāms rēķins
  - Nav iekļaujams rēķinā

Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.

Iekļaujamība rēķinā tiek definēta par piedāvājuma rindu un tā attiecas uz visām rindā iekļautajām darījumu klasēm. Ja lauks **Iekļaut uzdevumus** ir tukšs vai iestatīts uz **Viss projekts**, cilne **Apmaksājamie uzdevumi** nav pieejama.

Iekļaujamību rēķinā definē lomām piedāvājuma rindai, un tā attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nav pieejama.

Apmaksas apjoms tiek definēts pēc darījumu kategorijām piedāvājuma rindai, un tas attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nav pieejama.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu

Projekta uzdevums var būt apmaksājams vai neapmaksājam noteiktā projekta piedāvājuma rindā, kas nodrošina šādas iestatīšanas iespējas.

Ja projekta piedāvājuma rindā ir iekļauts **Laiks** un uzdevums **T1**, uzdevums tiek saistīts ar piedāvājuma rindu kā apmaksājams. Ja ir otra piedāvājuma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt **T1** uzdevumu piedāvājuma rindā kā neapmaksājamu. Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi uzdevumā ir neapmaksājami.

Uzdevuma norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** apakšrežģī **Piedāvājuma rindas uzdevumi**. Vai arī varat atjaunināt projekta uzdevuma norēķinu veida lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās piedāvājuma rindas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktas projekta piedāvājuma rindas kontekstā.

Lomas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās lomas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās lomas**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā piedāvājuma rindā.

Transakcijas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās kategorijas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās kategorijas**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana
Aprēķins vai faktiski dati, kas izveidoti par laiku, tiks uzskatīti par apmaksājamiem tikai tad, ja piedāvājuma rindā būs iekļauts lauks **Laiks** un lauki **Uzdevums** un **Loma** piedāvājuma rindā būs konfigurēta kā apmaksājama.

Aprēķins vai faktiski dati, kas izveidoti par izdevumiem, tiks uzskatīti par apmaksājamiem tikai tad, ja piedāvājuma rindā būs iekļauta kategorija **Izdevumi** un lauki **Uzdevums** un **Darījuma kategorija** piedāvājuma rindā būs konfigurēta kā apmaksājama.

| Iekļauts laiks | Iekļauti izdevumi | Iekļautie uzdevumi | Loma | Kategorija | Uzdevums | Norēķini |
| --- | --- | --- | --- | --- | --- | --- |
| Jā | Jā | Viss projekts | Izrakstāms rēķins | Izrakstāms rēķins | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Tikai atlasītie uzdevumi | Izrakstāms rēķins | Izrakstāms rēķins | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Apmaksājams</br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Tikai atlasītie uzdevumi | Nav iekļaujams rēķinā | Izrakstāms rēķins | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav apmaksājams</br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Tikai atlasītie uzdevumi | Izrakstāms rēķins | Izrakstāms rēķins | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav apmaksājams</br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | Jā | Tikai atlasītie uzdevumi | Nav apmaksājams | Izrakstāms rēķins | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav apmaksājams</br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | Jā | Tikai atlasītie uzdevumi | Nav apmaksājams | Nav apmaksājams | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav apmaksājams</br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| No | Jā | Viss projekts | Nevar iestatīt | Izrakstāms rēķins | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| No | Jā | Viss projekts | Nevar iestatīt | Nav iekļaujams rēķinā | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | No | Viss projekts | Izrakstāms rēķins | Nevar iestatīt | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Apmaksājams</br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |
| Jā | No | Viss projekts | Nav iekļaujams rēķinā | Nevar iestatīt | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]