---
title: Atļauto metožu rezervēšana pakalpojumā Project Service Automation
description: Šajā tēmā ir sniegta informācija par dažādiem veidiem, kā var rezervēt piešķīrumus.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f0f4f5c68698fbe88de968e65a65b316b10872d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590125"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Atļauto metožu rezervēšana pakalpojumā Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Ja pievienojat darba grupas dalībnieku tieši projektam cilnē **Darba grupa** vai rezervējat resursu projektam vai prasībai plānošanas panelī, varat izmantot dažas atšķirīgas rezervāciju piešķiršanas metodes. Šajā rakstā ir paskaidrots, kā darbojas katra no metodēm un kuru metožu izmantošana var izraisīt resursu rezervācijas pārsniegšanu.

## <a name="full-capacity"></a>Pilna noslodze 
Pilnas noslodzes metode: izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā un veidā. Piemēram, ja resursa kalendārs ir iestatīts kā astoņas darba stundas dienā, piecas dienas nedēļā, iestatot sākuma un beigu datumu, kas attiecas uz piecām darba dienām, resurss tiek rezervēts uz 40 stundām. Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 40 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

## <a name="remaining-capacity"></a>Atlikusī noslodze
Atlikušās noslodzes metode ir pieejama tikai tad, ja rezervējat tieši projektam, izmantojot plānošanas paneli. Izmantojot šo metodi, tiek rezervēta resursa pieejamā noslodze noteiktajā datumu diapazonā. Piemēram, ja resursa noslodze ir 40 stundas nedēļā un tas jau ir rezervēts uz 10 stundām, rezervējot ar atlikušas noslodzes metodi tai pašai nedēļai, tiek veikta rezervācija atlikušajām 30 stundām attiecīgajā nedēļā.

## <a name="percentage-capacity"></a>Noslodzes procentuālā vērtība
Noslodzes procentuālās vērtības metode — rezervē resursa noslodzes procentuālo vērtību norādītajā laika posmā un veidā. Piemēram, ja resursa kalendārs ir iestatīts kā astoņas darba stundas dienā, piecas dienas nedēļā, iestatot sākuma un beigu datumu, kas attiecas uz piecām darba dienām ar 50 % noslodzi, resurss tiek rezervēts uz 20 stundām. Atsevišķas rezervācijas dienā ir vienlīdzīgi sadalītas pa laika periodu, piemēram, četras stundas dienā (šajā piemērā). Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 20 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

## <a name="evenly-distribute-hours"></a>Sadalīt stundas vienmērīgi
Sadalīt stundas vienmērīgi: šī metode rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā. Piemēram, ja rezervējat resursu 20 stundas piecu dienu periodā, šī metode sadala 20 stundas vienmērīgi pa četrām stundām dienā. Rezervācija notiek, neņemot vērā resursa atlikušo noslodzi. Ja resurss šajā periodā jau ir rezervēts citiem projektiem, 20 stundas tiek rezervētas kā papildu stundas, potenciāli pārsniedzot rezervācijas.

## <a name="front-load-hours"></a>Sākotnējās slodzes stundas
Sākotnējās slodzes stundas: rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā. Sākotnējās slodzes stundas patērē resursa pieejamo noslodzi secībā “Vispirms patērēts”. Piemēram, ja resursa darba grafiks ir astoņas stundas dienā, piecas dienas nedēļā un resursam pašreiz nav rezervāciju, resursa rezervācijai 20 stundām piecu darba dienu periodā ir šāds dienas rezervācijas modelis: 

|         Rezervācijas          |    1. diena    |    2. diena    |    3. diena    |    4. diena    |    5. diena    |    Kopsumma    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Esošās rezervācijas    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Jauna rezervācija          |    8        |    8        |    4        |    0        |    0        |    20       |

Sākotnējās slodzes metode ņem vērā esošās rezervācijas un pieejamo noslodzi. Piemēram, ja viens un tas pats resurss jau ir rezervēts 20 stundas darba nedēļā, jaunas rezervācijas patērē pārējo noslodzi šādi:

|   Rezervācijas          | 1. diena | 2. diena | 3. diena | 4. diena | 5. diena | Kopsumma |
|---------------------|-------|-------|-------|-------|-------|-------|
| Esošās rezervācijas | 8     | 8     | 4     | 0     | 0     | 20    |
| Jauna rezervācija       | 0     | 0     | 4     | 8     | 8     | 20    |

Tā kā tiek ņemta vērā pieejamā noslodze, var tikt parādīts kļūdas ziņojums, ja resursam ir nav atlikušas noslodzes, ko var izmantot rezervācijā. Izmantojot šo metodi, rezervāciju nevar pārsniegt.

## <a name="none"></a>Nav
Metode Nav ir pieejama tikai tad, ja rezervācija tiek veikta projekta cilnē **Darba grupa**. Izmantojot šo metodi, resurss tiek pievienots kā darba grupas dalībnieks projektā, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi. Šī metode tiek izmantota, ja projekta izveides laikā tiek pievienots projektu vadītāju darba grupas noklusējuma dalībnieks. Projektu vadītāja lietotājs, kas izveidoja projektu pēc noklusējuma tiek pievienots projektam, lai projekta entītijas ierakstam būtu īpašnieks un projektā nebūtu neviena apstiprinātāja. Tā kā šim lietotājam nav rezervāciju, ja vēlaties rezervēt resursu, varat dzēst un atkārtoti pievienot to, izmantojot citu piešķiršanas metodi, vai pievienot resursu uzdevumiem un pēc tam izmantot sadaļu **Paplašinātās rezervācijas** cilnē **Saskaņošana**, lai sadalēm izveidotu rezervācijas.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Sadales metodes, kas izraisa rezervācijas pārsniegšanu
Ja resurss jau ir iesaistīts citos projektos (vai piesaistīts citiem darba pasūtījumiem vai plānojamām entītijām), tālāk norādītas sadales metodes izraisa rezervācijas pārsniegšanu.

- Pilna noslodze
- Noslodzes procentuālā vērtība
- Sadalīt stundas vienmērīgi

Izmantojot vienu no šīm trīs sadales metodēm, netiks parādīts paziņojums, ja attiecīgā resursa rezervācija būs pārsniegta. Lai labotu pārsniegto rezervāciju, nepieciešams izmantot plānošanas paneli.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
