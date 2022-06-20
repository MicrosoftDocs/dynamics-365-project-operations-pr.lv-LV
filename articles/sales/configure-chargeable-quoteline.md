---
title: Rēķinā iekļaujamo uzdevumu konfigurēšana projekta piedāvājuma rindā
description: Šajā rakstā sniegta informācija par iekļautiem, maksas un neapmaksājamiem komponentiem uz projektu balstītās piedāvājuma rindās.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915561"
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
| Nr. | Jā | Nevar iestatīt | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Nr. | Jā | Nevar iestatīt | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | Nr. | Izrakstāms rēķins | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |
| Jā | Nr. | Nav apmaksājams | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |


[!INCLUDE[footer-include](../includes/footer-banner.md)]