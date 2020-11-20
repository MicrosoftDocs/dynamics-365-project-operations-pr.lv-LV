---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā strādāt ar faktiskajiem datiem Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126318"
---
# <a name="actuals"></a>Pašreizējās 

_**Attiecas uz:** Project Operations scenārijiem, kas kas nav balstīti uz resursiem/krājumiem_

Faktiskie dati ir darba apjoms, kas ir pabeigts projektā. Tos izveido laika un izdevumu ierakstu, kā arī žurnāla ierakstu un rēķinu rezultātā.

## <a name="journal-lines-and-time-submission"></a>Žurnāla rindu un laika iesniegšana

Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Laika un materiālu

Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.

### <a name="fixed-price"></a>Fiksētas cenas

Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.

### <a name="default-pricing"></a>Noklusējuma cenu noteikšana

Noklusējuma cenu izveides loģika atrodas žurnāla rindā. Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu. Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.

Laukus, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izmanto atbilstošas cenas noteikšanai žurnāla rindā. Varat pievienot pielāgotu lauku laika ierakstam. Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.

## <a name="journal-lines-and-basic-expense-submission"></a>Žurnāla rindu un pamata izdevumu iesniegšana

Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Laika un materiālu

Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.

### <a name="fixed-price"></a>Fiksētas cenas

Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.

### <a name="default-pricing"></a>Noklusējuma cenu noteikšana

Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija. Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta. Tomēr pēc noklusējuma summa, kas ievadīta pašai cenai, tiek iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.

Izdevumu ierakstiem kategorijā valstīta cenas par vienību ievade nav pieejama.

## <a name="use-entry-journals-to-record-costs"></a>Ierakstu žurnālu izmantošana izmaksu reģistrēšanai

Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs. Žurnālus var izmantot šādiem mērķiem:

- Reģistrēt materiālu un pārdošanas faktiskās izmaksas projektā.
- Pārvietot darījuma faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.
- Reģistrēt izmaksas, kas notikušas citā sistēmā. Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.

> [!IMPORTANT]
> Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā. Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti. Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.
## <a name="record-actuals-based-on-project-events"></a>Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem

Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā. Šīs transakcijas tiek ierakstītas kā faktiskie dati. Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība

<table>
<thead>
<tr>
<th rowspan="3">Notikums</th>
<th colspan="4">Apmaksājams vai pārdots projekts</th>
<th rowspan="3">Projekts pirmspārdošanas posmā</th>
<th rowspan="3">Iekšējais projekts</th>
</tr>
<tr>
<th colspan="2">Laika un materiālu</th>
<th colspan="2">Fiksētas cenas</th>
</tr>
<tr>
<th>Faktiski</th>
<th>Transakcijas valūta</th>
<th>Fiksētas cenas</th>
<th>Transakcijas valūta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tiek izveidots laika ieraksts.</td>
<td colspan="6">Entītijā Faktiskie dati nav nevienas darbības</td>
</tr>
<tr>
<td>Tiek iesniegts laika ieraksts.</td>
<td colspan="6">Entītijā Faktiskie dati nav nevienas darbības</td>
</tr>
<tr>
<td rowspan="2">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</td>
<td>Faktiskās izmaksas</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="2">Faktiskās izmaksas</td>
<td rowspan="2">Līgumslēdzēja struktūrvienības valūta
<td rowspan="2">Faktiskās izmaksas</td>
<td rowspan="2">Faktiskās izmaksas</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="3">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</td>
<td>Faktiskās izmaksas</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="3">Faktiskās izmaksas</td>
<td rowspan="3">Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="3">Faktiskās izmaksas</td>
<td rowspan="3">Faktiskās izmaksas</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="2">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</td>
<td>Rēķinā neiekļautās pārdošanas atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="2">Rēķinā iekļautā pārdošana atskaites punktam</td>
<td rowspan="2">Projekta līguma valūta</td>
<td rowspan="2">Nav piemērojams</td>
<td rowspan="2">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="3">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</td>
<td>Rēķinā neiekļautās pārdošanas atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="2">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</td>
<td>Rēķinā iekļautā pārdošana — atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="5">
<ul>
<li>Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</li>
<li>Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></li>
</ul>
</td>
<td rowspan="5">Projekta līguma valūta</td>
<td rowspan="5">Nav piemērojams</td>
<td rowspan="5">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="3">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</td>
<td>Rēķinā iekļautā pārdošana — atsaukšana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana jaunajam daudzumam</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</td>
<td>Projekta līguma valūta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības

<table>
<thead>
<tr>
<th rowspan="3">Notikums</th>
<th colspan="4">Apmaksājams vai pārdots projekts</th>
<th rowspan="3">Projekts pirmspārdošanas posmā</th>
<th rowspan="3">Iekšējais projekts</th>
</tr>
<tr>
<th colspan="2">Laika un materiālu</th>
<th colspan="2">Fiksētas cenas</th>
</tr>
<tr>
<th>Faktiski</th>
<th>Transakcijas valūta</th>
<th>Fiksētas cenas</th>
<th>Transakcijas valūta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tiek izveidots laika ieraksts.</td>
<td colspan="6">Entītijā Faktiskie dati nav nevienas darbības</td>
</tr>
<tr>
<td>Tiek iesniegts laika ieraksts.</td>
<td colspan="6">Entītijā Faktiskie dati nav nevienas darbības</td>
</tr>
<tr>
<td rowspan="4">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</td>
<td>Faktiskās izmaksas</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="4">Faktiskās izmaksas</td>
<td rowspan="4">Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="4">Faktiskās izmaksas</td>
<td rowspan="4">Faktiskās izmaksas</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Resursu struktūrvienības izmaksas</td>
<td>Resursu struktūrvienības valūta</td>
</tr>
<tr>
<td>Starporganizāciju pārdošana</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
</tr>
<tr>
<td rowspan="5">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</td>
<td>Faktiskās izmaksas</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="5">Faktiskās izmaksas</td>
<td rowspan="5">Līgumslēdzēja struktūrvienības valūta</td>
<td rowspan="5">Faktiskās izmaksas</td>
<td rowspan="5">Faktiskās izmaksas</td>
</tr>
<tr>
<td>Resursu struktūrvienības izmaksas</td>
<td>Resursu struktūrvienības valūta</td>
</tr>
<tr>
<td>Starporganizāciju pārdošana</td>
<td>Līgumslēdzēja struktūrvienības valūta</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="2">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</td>
<td>Rēķinā neiekļautās pārdošanas atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="2">Rēķinā iekļautā pārdošana atskaites punktam</td>
<td rowspan="2">Projekta līguma valūta</td>
<td rowspan="2">Nav piemērojams</td>
<td rowspan="2">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="3">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</td>
<td>Rēķinā neiekļautās pārdošanas atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
<td rowspan="3">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="2">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</td>
<td>Rēķinā iekļautā pārdošana — atsaukšana</td>
<td>Projekta līguma valūta</td>
<td rowspan="5">
<ul>
<li>Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</li>
<li>Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></li>
</ul>
</td>
<td rowspan="5">Projekta līguma valūta</td>
<td rowspan="5">Nav piemērojams</td>
<td rowspan="5">Nav piemērojams</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td rowspan="3">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</td>
<td>Rēķinā iekļautā pārdošana — atsaukšana</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā iekļautā pārdošana jaunajam daudzumam</td>
<td>Projekta līguma valūta</td>
</tr>
<tr>
<td>Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</td>
<td>Projekta līguma valūta</td>
</tr>
</tbody>
</table>
