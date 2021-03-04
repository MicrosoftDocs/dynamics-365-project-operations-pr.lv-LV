---
title: Uz projektiem balstītu līguma rindu maksas komponentu konfigurēšana — Lite
description: Šajā tēmā ir sniegta informācija par to, kā projektu operācijās līguma rindām pievienot apmaksājamus komponentus.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513888"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Uz projektiem balstītu līguma rindu maksas komponentu konfigurēšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta līguma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.

Iekļautie komponenti ir komponenti, uz kuriem attiecas tālāk minētais.

  - Norēķinu metode un klientu sadalījums
  - Nepārsniedzamie ierobežojumi 
  - Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta līguma rindā

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**. Lauks **Rēķina tips** ir opciju kopa, kas līguma rindas kontekstā ļauj izmantot šādas vērtības:

  - Izrakstāms rēķins
  - Nav iekļaujams rēķinā

Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.

Iekļaujamība rēķinā tiek definēta par projekta līguma rindas uzdevumiem un tā attiecas uz visām rindā iekļautajām darījumu klasēm. Ja lauks **Iekļaut uzdevumus** līguma rindā ir tukšs vai iestatīts uz **Viss projekts**, cilne **Rēķinā iekļaujamie uzdevumi** nebūs pieejama.

Apmaksas apjoms, kas definēts pēc lomām projekta līguma rinai, attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** līguma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nebūs pieejama.

Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nebūs pieejama.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu

Projekta uzdevums var būt apmaksājams vai neapmaksājam noteiktā līguma rindā, kas nodrošina šādas iestatīšanas iespējas.

Ja projekta līguma rindā ir iekļauts lauks **Laiks** un noteikts uzdevums, **T1** ir saistīts ar to kā apmaksājams. Ja ir otra līguma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt T1 uzdevumu līguma rindā kā neapmaksājamu. Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi ir neapmaksājami.

Uzdevuma norēķinu tipu var konfigurēt līguma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** līguma rindu uzdevumu apakšrežģī. Vai arī varat atjaunināt lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās līguma rindas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.

Lomu norēķina veidu var konfigurēt līguma rindas cilnē **Apmaksājamās lomas**. Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās lomas**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.

Darījuma norēķina veidu var konfigurēt projekta līguma rindas cilnē **Apmaksājamās kategorijas**. Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana

Aprēķins vai faktiski dati, kas izveidoti par laiku, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauts lauks **Laiks** un lauki **Uzdevums** un **Loma** līguma rindā būs konfigurēta kā apmaksājama.

Aprēķins vai faktiski dati, kas izveidoti par izdevumiem, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļautas kategorijas **Izdevumi** un lauki **Uzdevums** un **Darījums** līguma rindā būs konfigurēta kā apmaksājama.


| Iekļauts laiks | Iekļauti izdevumi | Iekļauti uzdevumi | Loma           | Kategorija       | Uzdevums                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Jā           | Jā              | Viss projekts | Izrakstāms rēķins     | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**           |
| Jā           | Jā              | Atlasītie uzdevumi | Izrakstāms rēķins     | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**           |
| Jā           | Jā              | Atlasītie uzdevumi | Nav iekļaujams rēķinā | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Nav apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**       |
| Jā           | Jā              | Atlasītie uzdevumi | Izrakstāms rēķins     | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Nav apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams** |
| Jā           | Jā              | Atlasītie uzdevumi | Nav iekļaujams rēķinā | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Nav apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams** |
| Jā           | Jā              | Atlasītie uzdevumi | Nav iekļaujams rēķinā | Nav iekļaujams rēķinā | Norēķini par laika faktiskajiem datiem: **Nav apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams** |
| No            | Jā              | Viss projekts | Nevar iestatīt   | Izrakstāms rēķins     | Norēķini par laika faktiskajiem datiem: **Nav pieejams**</br>Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**          |
| No            | Jā              | Viss projekts | Nevar iestatīt   | Nav iekļaujams rēķinā | Norēķini par laika faktiskajiem datiem: **Nav pieejams**</br> Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams**     |
| Jā           | No               | Viss projekts | Izrakstāms rēķins     | Nevar iestatīt   | Norēķini par laika faktiskajiem datiem: **Apmaksājams** </br> Norēķinu veids par izdevumu faktiskajiem datiem: **Nav pieejams**        |
| Jā           | No               | Viss projekts | Nav iekļaujams rēķinā | Nevar iestatīt   | Norēķini par laika faktiskajiem datiem: **Nav apmaksājams** </br>Norēķinu veids par izdevumu faktiskajiem datiem: **Nav pieejams**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]