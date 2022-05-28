---
title: Maksas komponentu konfigurēšana projekta līguma rindā
description: Šajā tēmā ir sniegta informācija par iekļautiem, apmaksājamiem un neapmaksājamiem komponentiem līguma rindās.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bd419e189cd063f1cb2a1f0ecd3cd6450de0996b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586629"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Maksas komponentu konfigurēšana projekta līguma rindā

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta līguma rindā ir iekļautu, apmaksājamu un neapmaksājamu komponentu jēdziens.

Iekļautajiem komponentiem ir piemērojamas norēķinu metodes, klienta dalījumi, nepārsniedzami ierobežojumi un rēķina biežuma iestatījumi, kas definēti projekta līguma rindā.

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, atjauninot lauku **Norēķinu tips**.

Apmaksājamus komponentus var definēt lomās un darījumu kategorijās.

Projekta līguma rindai apmaksas apjoms, kas definēts tikai pēc lomas, attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** projekta līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nav pieejama.

Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** projekta līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nav pieejama.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktā projekta līguma rindā.

Atjauniniet lomas norēķinu tipu projekta līguma rindas cilnes **Rēķinā iekļaujamās lomas** apakšrežģa **Rēķinā iekļaujamās lomas** laukā **Norēķinu tips**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā projekta līguma rindā.

Atjauniniet transakcijas norēķinu tipu projekta līguma rindas cilnes **Rēķinā iekļaujamās kategorijas** apakšrežģa **Rēķinā iekļaujamās lomas** laukā **Norēķinu tips**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana

Aprēķins vai faktiski dati, kas izveidoti par laiku, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauts lauks Laiks un loma līguma rindā būs konfigurēta kā apmaksājama.

Aprēķins vai faktiski dati, kas izveidoti par izdevumiem, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauti izdevumi un darījuma kategorija līguma rindā būs konfigurēta kā apmaksājama.

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
