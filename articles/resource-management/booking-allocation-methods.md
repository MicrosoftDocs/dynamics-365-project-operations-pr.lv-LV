---
title: Atļauto metožu rezervēšana
description: Šajā tēmā sniegta informācija par to, kā rezervācijas sadalījuma metodes darbojas programmā Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897685"
---
# <a name="booking-allocation-methods"></a>Atļauto metožu rezervēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Ja pievienojat darba grupas dalībnieku tieši projektam cilnē **Darba grupa** vai rezervējat resursu projektam vai prasībai plānošanas panelī, varat izmantot dažas atšķirīgas rezervāciju piešķiršanas metodes. Šajā rakstā ir paskaidrots, kā darbojas katra no metodēm un kuru metožu izmantošana var izraisīt resursu rezervācijas pārsniegšanu.

## <a name="booking-allocation-methods"></a>Atļauto metožu rezervēšana

Varat izmantot sešas rezervācijas sadalījuma metodes:

- [Pilna noslodze](#full)
- [Atlikusī noslodze](#remaining)
- [Noslodzes procentuālā vērtība](#percentage)
- [Vienmērīgs laika sadalījums](#evenly)
- [Sākotnējās slodzes stundas](#front)
- [Nav](#none)

### <a name="full-capacity"></a><a name="full"></a>Pilna noslodze 
Pilnas noslodzes metode: izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā un veidā. Piemēram, ja resursa kalendārs ir iestatīts kā astoņas darba stundas dienā, piecas dienas nedēļā, iestatot sākuma un beigu datumu, kas attiecas uz piecām darba dienām, resurss tiek rezervēts uz 40 stundām. Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 40 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

### <a name="remaining-capacity"></a><a name="remaining"></a>Atlikusī noslodze
Atlikušās noslodzes metode ir pieejama tikai tad, ja rezervējat tieši projektam, izmantojot plānošanas paneli. Izmantojot šo metodi, tiek rezervēta resursa pieejamā noslodze noteiktajā datumu diapazonā. Piemēram, ja resursa noslodze ir 40 stundas nedēļā un tas jau ir rezervēts uz 10 stundām, rezervējot ar atlikušas noslodzes metodi tai pašai nedēļai, tiek veikta rezervācija atlikušajām 30 stundām attiecīgajā nedēļā.

### <a name="percentage-capacity"></a><a name="percentage"></a>Noslodzes procentuālā vērtība
Noslodzes procentuālās vērtības metode — rezervē resursa noslodzes procentuālo vērtību norādītajā laika posmā un veidā. Piemēram, ja resursa kalendārs ir iestatīts kā astoņas darba stundas dienā, piecas dienas nedēļā, iestatot sākuma un beigu datumu, kas attiecas uz piecām darba dienām ar 50 % noslodzi, resurss tiek rezervēts uz 20 stundām. Atsevišķas rezervācijas dienā ir vienlīdzīgi sadalītas pa laika periodu, piemēram, četras stundas dienā (šajā piemērā). Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 20 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Vienmērīgs laika sadalījums
Sadalīt stundas vienmērīgi: šī metode rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā. Piemēram, ja rezervējat resursu 20 stundas piecu dienu periodā, šī metode sadala 20 stundas vienmērīgi pa četrām stundām dienā. Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 20 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

### <a name="front-load-hours"></a><a name="front"></a>Sākotnējās slodzes stundas
Sākotnējās slodzes stundas: rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā. Sākotnējās slodzes stundas patērē resursa pieejamo noslodzi secībā “Vispirms patērēts”. Piemēram, ja resursa darba grafiks ir astoņas stundas dienā, piecas dienas nedēļā un resursam pašreiz nav rezervāciju, resursa rezervācijai 20 stundām piecu darba dienu periodā ir šāds dienas rezervācijas modelis: 

|                           |    1. diena    |    2. diena    |    3. diena    |    4. diena    |    5. diena    |    Kopā    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Esošās rezervācijas**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Jauna rezervācija**          |    8        |    8        |    4        |    0        |    0        |    20       |

Sākotnējās slodzes metode ņem vērā esošās rezervācijas un pieejamo noslodzi. Piemēram, ja viens un tas pats resurss jau ir rezervēts 20 stundas darba nedēļā, jaunas rezervācijas patērē pārējo noslodzi šādi:

|                     | 1. diena | 2. diena | 3. diena | 4. diena | 5. diena | Kopā |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Esošās rezervācijas** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Jauna rezervācija**       | 0     | 0     | 4     | 8     | 8     | 20    |

Tā kā tiek ņemta vērā pieejamā noslodze, var tikt parādīts kļūdas ziņojums, ja resursam ir nav atlikušas noslodzes, ko var izmantot rezervācijā. Izmantojot šo metodi, rezervāciju nevar pārsniegt.

### <a name="none"></a><a name="none"></a>Nav
Metode Nav ir pieejama tikai tad, ja rezervācija tiek veikta projekta cilnē **Darba grupa**. Izmantojot šo metodi, resurss tiek pievienots kā darba grupas dalībnieks projektā, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi. Šī metode tiek izmantota, ja projekta izveides laikā tiek pievienots projektu vadītāju darba grupas noklusējuma dalībnieks. Projektu vadītāja lietotājs, kas izveidoja projektu pēc noklusējuma tiek pievienots projektam, lai projekta entītijas ierakstam būtu īpašnieks un projektā nebūtu neviena apstiprinātāja. Tā kā šim lietotājam nav rezervāciju, ja vēlaties rezervēt resursu, varat dzēst un atkārtoti pievienot to, izmantojot citu piešķiršanas metodi, vai pievienot resursu uzdevumiem un pēc tam izmantot sadaļu **Paplašinātās rezervācijas**cilnē **Saskaņošana**, lai sadalēm izveidotu rezervācijas.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Sadales metodes, kas izraisa rezervācijas pārsniegšanu
Ja resurss jau ir iesaistīts citos projektos (vai piesaistīts citiem darba pasūtījumiem vai plānojamām entītijām), tālāk norādītas sadales metodes izraisa rezervācijas pārsniegšanu.

- Pilna noslodze
- Noslodzes procentuālā vērtība
- Sadalīt stundas vienmērīgi

Izmantojot vienu no šīm trīs sadales metodēm, netiks parādīts paziņojums, ja attiecīgā resursa rezervācija būs pārsniegta. Lai labotu pārsniegto rezervāciju, nepieciešams izmantot plānošanas paneli.
