---
title: Projekta piedāvājuma rindas pārskats — Lite
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181101"
---
# <a name="project-based-quote-lines-overview---lite"></a>Projekta piedāvājuma rindas pārskats — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē. Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.

- Rēķinu izrakstīšanas metode
- Projektu un uzdevumu kartēšana
- Iekļautās transakciju klases
- Nepārsniedzamais ierobežojums
- Iekasēšanas iestatīšana
- Aprēķins, izmantojot piedāvājuma rindas detaļas
- Piedāvājuma rindas klienti

Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem. Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Nosaukums/vārds, uzvārds | Piedāvājuma rindas nosaukums, kas palīdz identificēt aprēķināmā piedāvājuma diskrēto komponentu. | Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Rēķinu izrakstīšanas metode | No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā. Šajā laukā ir iekļauti divi galvenie līgumu slēgšanas modeļi, kurus atbalsta Dynamics 365 Project Operations:</br>- fiksēta cena;</br>- laiks un materiāli.| Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Project | Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē. Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu. Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.|
| Iekļautie uzdevumi | Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem. Šim laukam ir šādas iespējamās vērtības:</br>- visi projekta uzdevumi;</br>- tikai atlasītie projekta uzdevumi.</br>Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**. | Ja pēc tam projekta lapā ir atlasīts **Tikai atlasītie projekta uzdevumi**, cilnē **Uzdevumu norēķinu iestatīšana** var atlasīt specifiskus uzdevumus, kurus saistīt ar šo piedāvājuma rindu. Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut laiku | Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut izdevumus | Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut maksu | Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Minētā summa | Šī ir summa, kas tiks piedāvāta klientam par visu darbu, kas prognozēts šajā projekta piedāvājuma rindā. No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā. Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Aprēķinātais nodoklis | Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai. Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Piedāvātā summa pēc nodokļa atskaitīšanas | Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms. Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Nepārsniedzamais ierobežojums | Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Klienta budžets | Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas. | Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi

**1. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projekts tiek iekļauts piedāvājuma rindā.

**2. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.

**3. kārtula**: ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.

**4. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.

**5. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Iespēja</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Piedāvājums</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Piedāvājuma rinda</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Iekļautie uzdevumi</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Iekļaut laiku</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Iekļaut izdevumus</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Ietveršana</strong>
                </p>
                <p>
                    <strong>Maksa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Derīgs/Nav derīgs</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Iemesls</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Laiks un maksas P1 projektā ir ietvertas rindā QL1.
Izdevumi P1 projektā ir ietverti rindā QL2.
Nepārklājas informācija, kas iekļauta katrā piedāvājuma rindā un ir derīga.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Iepriekš norādītās 2. kārtulas pārkāpums </p>
                <p>
Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.
                </p>
                <p>
QL2 ietver laiku, izdevumus un maksas par visu P1 projektu un pārklājas ar to, kas ir iekļauts Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Saskaņā ar iepriekš minēto 3. kārtulu, </p>
                <p>
Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.
                </p>
                <p>
QL2 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopai.
                </p>
                <p>
Vienīgā papildu validācija ir ap QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas. Šādi tiek nodrošināts, ka nav pārklāšanās. To veic sistēma, kad tiek saistīti uzdevumi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pamatojoties uz 5. kārtulu, Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tāpēc tos abus var izmantot vienu un to pašu projekta komponentu aprēķināšanai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
2. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pamatojoties uz 4. kārtulu, Q1 un Q2 ir divi piedāvājumi par dažādām iespējām, tāpēc tos nevar izmantot tā paša projekta vienu un to pašu komponentu aprēķināšanai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="54" valign="top">
                <p>
Nav derīgs </p>
            </td>
        </tr>
    </tbody>
</table>

