---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā veikt darbības ar faktiskajiem darbiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852553"
---
# <a name="actuals"></a>Faktiskie dati 

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Faktiskie dati attiecas uz pārskatīto un apstiprināto finanšu un plānošanas norisi projektā. Tās tiek izveidotas laika, izmaksu, materiālu lietojuma ierakstu, kā arī ierakstu un rēķinu apstiprinājuma rezultātā.

## <a name="journal-lines-and-time-submission"></a>Žurnāla rindu un laika iesniegšana

Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Laika un materiālu

Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.

### <a name="fixed-price"></a>Fiksētas cenas

Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.

### <a name="default-pricing"></a>Noklusējuma cenu noteikšana

Noklusējuma cenu izveides loģika atrodas žurnāla rindā. Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu. Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.

Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Resursu vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā. Varat pievienot pielāgotu lauku laika ierakstam. Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**. Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes. Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Žurnāla rindu un pamata izdevumu iesniegšana

Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Laika un materiālu

Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.

### <a name="fixed-price"></a>Fiksētas cenas

Kad iesniegtais pamata izdevumu ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.

### <a name="default-pricing"></a>Noklusējuma cenu noteikšana

Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija. Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta. Lauki, kas ietekmē noklusējuma cenas, piemēram, **Transakcijas kategorija** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā. Tomēr tas darbojas tikai tad, ja cenrāža cenu noteikšanas metode ir **Cena par vienību**. Ja cenu noteikšanas metode ir **Pašizmaksa** vai **Uzcenojums augstāks par izmaksu**, izmaksu ieraksta izveides laikā ievadītā cena tiek izmantota izmaksām, un cena pārdošanas piedāvājuma rindā tiek aprēķināta, pamatojoties uz cenu noteikšanas metodi. 

Izmaksu ierakstam var pievienot pielāgotu lauku. Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**. Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes. Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Žurnāla rindu un materiālu lietojuma žurnāla iesniegšana

Papildinformāciju par izdevumu ierakstu skatiet šeit: [Materiālu lietojuma žurnāls](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Laika un materiālu

Kad iesniegts materiālu lietojuma žurnāls ieraksts tiek saistīts ar projektu, kas tiek kartēts ar laika un materiālu līguma rindu, sistēma izveido divas rindu rindas (vienu par izmaksām un vienu par rēķinā neietverto pārdošanu).

### <a name="fixed-price"></a>Fiksētas cenas

Kad iesniegtais materiālu lietojuma ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.

### <a name="default-pricing"></a>Noklusējuma cenu noteikšana

Materiālu noklusējuma cenu ievadīšanas loģika tiek pamatota uz produktu un vienību kombināciju. Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta. Lauki, kas ietekmē noklusējuma cenas, piemēram, **Produkta ID** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā. Tomēr tas darbojas tikai kataloga produktiem. Ierakstāmiem produktiem cena, kas ievadīta, izveidojot materiālu lietojuma žurnāla ierakstu, tiek izmantota izmaksu un pārdošanas cenai raksta rindās. 

Ierakstam **Materiālu lietojuma žurnāls** var pievienot pielāgotu lauku. Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**. Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes. Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Ierakstu žurnālu izmantošana izmaksu reģistrēšanai

Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs. Žurnālus var izmantot šādiem mērķiem:

- Pārvietojiet transakciju faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
