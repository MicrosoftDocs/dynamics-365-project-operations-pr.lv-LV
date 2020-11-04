---
title: Projekta līguma rindas apmaksājamo komponentu konfigurēšana
description: Šajā tēmā ir sniegta informācija par iekļautiem, apmaksājamiem un neapmaksājamiem komponentiem līguma rindās.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080381"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projekta līguma rindas apmaksājamo komponentu konfigurēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta līguma rindā ir iekļautu, apmaksājamu un neapmaksājamu komponentu jēdziens.

Iekļautajiem komponentiem ir piemērojamas norēķinu metodes, klienta dalījumi, nepārsniedzami ierobežojumi un rēķina biežuma iestatījumi, kas definēti projekta līguma rindā.

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, atjauninot lauku **Norēķinu tips**.

Apmaksājamus komponentus var definēt lomās un darījumu kategorijās.

Projekta līguma rindai apmaksas apjoms, kas definēts tikai pēc lomas, attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** projekta līguma rindā ir iestatīts uz **Nē** , cilne **Apmaksājamās lomas** nav pieejama.

Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** projekta līguma rindā ir iestatīts uz **Nē** , cilne **Apmaksājamās kategorijas** nav pieejama.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktā projekta līguma rindā.

Lomas norēķinu tipu atjauniniet projekta piedāvājuma rindas cilnes **Apmaksājamās lomas** apakšrežģa **Apmaksājamās lomas** laukā **Norēķinu tips**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā projekta līguma rindā.

Darījuma norēķinu tipu atjauniniet projekta piedāvājuma rindas cilnes **Apmaksājamās kategorijas** apakšrežģa **Apmaksājamās lomas** laukā **Norēķinu tips**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana

Aprēķins vai faktiski dati, kas izveidoti par laiku, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauts lauks Laiks un loma līguma rindā būs konfigurēta kā apmaksājama.

Aprēķins vai faktiski dati, kas izveidoti par izdevumiem, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauti izdevumi un darījuma kategorija līguma rindā būs konfigurēta kā apmaksājama.

| Iekļauts laiks | Iekļauti izdevumi | Loma | Kategorija | Uzdevums |
| --- | --- | --- | --- | --- |
| Jā | Jā | Izrakstāms rēķins | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Nav apmaksājams | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| Jā | Jā | Nav apmaksājams | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| No | Jā | Nevar iestatīt | Izrakstāms rēķins | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams |
| No | Jā | Nevar iestatīt | Nav apmaksājams | Norēķini par laika faktiskajiem datiem: Nav pieejams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams |
| Jā | No | Izrakstāms rēķins | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Apmaksājams </br>Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |
| Jā | No | Nav apmaksājams | Nevar iestatīt | Norēķini par laika faktiskajiem datiem: Nav apmaksājams </br> Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams |
