---
title: Pārskats faktiski
description: Šajā tēmā ir sniegta informācija par projekta faktiskajiem datiem.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014665"
---
# <a name="actuals-overview"></a>Pārskats faktiski

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faktiskie dati ir darba apjoms, kas ir pabeigts projektā. Projekta faktiskos datus var izsekot līdz to avota dokumentiem. Šie avota dokumenti ietver laika, izdevumu un žurnālu ierakstus, kā arī rēķinus.

![Kā projekta faktiskie dati tiek izsekoti līdz avota dokumentiem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Laika ieraksta iesniegšana

Kad programmā PSA tiek iesniegts laika ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas. Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai. Kad tiek iesniegts laika ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām. 

Noklusējuma cenu ievadīšanas loģika atrodas žurnāla rindā. Visas lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu. Šajos laukos ir iekļauts transakcijas datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī. 

Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izraisa atbilstošu cenu, kas pēc noklusējuma ir jāievada žurnāla rindā. Ja laika ierakstā pievienojat pielāgotu lauku un vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.

## <a name="submitting-an-expense-entry"></a>Izdevumu ieraksta iesniegšana

Kad programmā PSA tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas. Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai. Kad tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.

Loģika, kas paredzēta izdevumu noklusējuma cenu ievadīšanai, ir atkarīga no izdevumu kategorijas, kas atlasīta lapā **Izdevumu ieraksts**. Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta. Tomēr pašai cenai summa, ko lietotājs ir ievadījis, tiek pēc noklusējuma iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.

Pašreizējā PSA versijā nav pieejams no kategorijas atkarīgs noklusējuma cenu par vienību ieraksts izdevumu ierakstos.

## <a name="using-entry-journals-to-record-costs"></a>Ierakstu žurnālu izmantošana izmaksu reģistrēšanai

Programmā PSA ierakstu žurnāli ļauj ierakstīt izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs. Žurnālā ir virsraksts, rindas un darbība **Apstiprināt**. Piedāvājam dažus scenārijus, kuros jūs varētu izmantot žurnālu.

- Jums projektā Ir jāieraksta materiālu faktiskās izmaksas un pārdošana.
- Jums ir jāpārvieto transakciju faktiskie dati no citas sistēmas uz PSA.
- Jums ir jāieraksta izmaksas, kas radās citā sistēmā, piemēram, sagādes vai apakšlīgumu slēgšanas izmaksas.

> [!IMPORTANT]
> Ierakstu žurnālu izmantošana, lai izveidotu faktiskos rezultātus, ir jāveic tikai lietotājam, kas pilnībā pārzina grāmatvedības ietekmi, kāda ir attiecībā uz faktiskajiem projektiem. Tas ir tāpēc, ka lietojumprogramma neapstiprina žurnāla rindas tipu vai saistīto izcenojumu, kas ievadīts žurnāla rindā. Ņemot vērā šī žurnāla tipa ietekmi, esiet piesardzīgs, kam tiek nodrošināta piekļuve, lai izveidotu ierakstu žurnālus.     


## <a name="recording-actuals-based-on-project-events"></a>Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem

PSA ieraksta finanšu transakcijas, kas notiek projekta laikā. Šīs transakcijas tiek ierakstītas kā **faktiskie dati**. Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.

**Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība**

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

**Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības**

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