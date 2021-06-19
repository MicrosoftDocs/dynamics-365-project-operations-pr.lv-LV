---
title: Rēķinā iekļaujamo uzdevumu konfigurēšana projekta piedāvājuma rindā
description: Šajā tēmā ir sniegta informācija par iekļautajiem, rēķinā iekļaujamajiem un rēķinā neiekļaujamajiem komponentiem projekta piedāvājuma rindās.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9febf305e3cd29bab42cd6c83a941f7b494fa56
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013585"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Rēķinā iekļaujamo uzdevumu konfigurēšana projekta piedāvājuma rindā

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta piedāvājuma rindā var būt iekļautie komponenti un rēķinā iekļaujamie komponenti.

Uz iekļautajiem komponentiem attiecas norēķinu metodes, klientu sadalījumu, nepārsniedzamo ierobežojumu un rēķinu izrakstīšanas biežuma iestatījumi, kas definēti projekta piedāvājuma rindā.
Iekļauto komponentu apakškopu var atzīmēt kā rēķinā iekļaujamu, izmantojot vienumu **Norēķinu tips**. Piedāvājuma rindas kontekstā var atlasīt vienu no tālāk norādītajām lauka **Norēķinu tips** opcijām.

   - Izrakstāms rēķins
   - Nav iekļaujams rēķinā

Rēķinā iekļaujamos komponentus var definēt lomās un darbību kategorijās.

Iekļaujamība, kas ir definēta projekta piedāvājuma rindas lomās, attiecas tikai uz darbību klasi **Laiks**. Ja projekta piedāvājuma rindā ir iestatījums **Iekļaut laiku** = **Nē**, cilne **Rēķinā iekļaujamās lomas** nav pieejama.

Iekļaujamība, kas ir definēta projekta piedāvājuma rindas darbību kategorijās, attiecas tikai uz darbību klasi **Izdevumi**. Ja projekta piedāvājuma rindā ir iestatījums **Iekļaut izdevumus** = **Nē**, cilne **Rēķinā iekļaujamās kategorijas** nav pieejama.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu
Loma projekta piedāvājuma rindā var būt rēķinā iekļaujama vai rēķinā neiekļaujama. Lomas norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamās lomas**. Lai to paveiktu, atjauniniet lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās lomas**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu
Darbību kategorija projekta piedāvājuma rindā var būt rēķinā iekļaujama vai rēķinā neiekļaujama. Darbības norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamās kategorijas**. Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**. 

## <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana

Izveidotais laika aprēķins vai faktiskais laiks tiks uzskatīts kā rēķinā iekļaujams tikai tad, ja laiks būs iekļauts piedāvājuma rindā un loma būs konfigurēta kā rēķinā iekļaujama.
Izveidotais izdevumu aprēķins vai faktiskie izdevumi tiks uzskatīti kā rēķinā iekļaujami tikai tad, ja izdevumi būs iekļauti piedāvājuma rindā un darbību kategorija piedāvājuma rindā būs konfigurēta kā rēķinā iekļaujama. Tālāk esošajā tabulā ir parādīti iekļaujamības nokklusējumi katram faktiskajam ierakstam. Noklusējumu pamatā ir iekļautie komponenti un piedāvājuma rindā iestatītais norēķinu tips.

| Iekļauts laiks | Iekļauti izdevumi | Loma | Kategorija | Uzdevums |
| --- | --- | --- | --- | --- |
| Jā | Jā | Izrakstāms rēķins | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Nav apmaksājams | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Nav apmaksājams | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| No | Jā | Nevar iestatīt | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| No | Jā | Nevar iestatīt | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | No | Izrakstāms rēķins | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |
| Jā | No | Nav apmaksājams | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |


[!INCLUDE[footer-include](../includes/footer-banner.md)]