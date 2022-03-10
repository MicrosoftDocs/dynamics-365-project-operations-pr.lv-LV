---
title: Projekta piedāvājuma rindas pārskats
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 2f2d38c7fb3bc3ec26cf64525ef8275adecafd7fc48e97d6daef595d341c045d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001575"
---
# <a name="project-based-quote-lines-overview"></a>Projekta balstīta piedāvājuma rindu pārskats 

_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_

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
| Nosaukums/vārds, uzvārds | Piedāvājuma rindas nosaukums, kas palīdz noteikt prognozējamā piedāvājuma komponentu. | Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Rēķinu izrakstīšanas metode | No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā. Šajā laukā ir divi galvenie līgumu slēgšanas modeļi, kurus Dynamics 365 Project Operations atbalsta:</br>- fiksēta cena;</br>- laiks un materiāli.| Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Project | Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē. Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu. Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.|
| Iekļautie uzdevumi | Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem. Šim laukam ir šādas iespējamās vērtības:</br>- visi projekta uzdevumi;</br>- tikai atlasītie projekta uzdevumi.</br>Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**. | Projekta lapā atlasot **Tikai atlas‪ītie projekta uzdevumi**, cilnē **Uzdevuma norēķinu iestatīšana** varat atlasīt noteiktus uzdevumus, lai tos saistītu ar šo piedāvājuma rindu. Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut laiku | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā laika transakcijas vai darbaspēka izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut izdevumus | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā izdevumi tiks iekļauti šīs piedāvājuma rindas aprēķinā. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut materiālu | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā. Vērtība **Nē** norāda, ka atlasītajā projektā materiālu izmaksas netiks iekļautas šīs piedāvājuma rindas aprēķinā. Vērtība **Jā** norāda, ka atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Iekļaut maksu | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā maksas tiks iekļautas šīs piedāvājuma rindas aprēķinā. Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas. Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Minētā summa | Šī ir summa, kas klientam tiks piedāvāta par visu šajā projekta piedāvājuma rindā prognozēto darbu. No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā. Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Aprēķinātais nodoklis | Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai. Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Piedāvātā summa pēc nodokļa atskaitīšanas | Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms. Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Nepārsniedzamais ierobežojums | Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |
| Klienta budžets | Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas. | Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi

**1. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projekts tiek iekļauts piedāvājuma rindā.

**2. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.

**3. kārtula**: ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.

**4. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.

**5. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Iespēja</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Piedāvājums</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Piedāvājuma rinda</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Iekļautie uzdevumi</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Iekļaut laiku</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Iekļaut izdevumus</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Iekļaut materiālu</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Iekļaut</strong>
                </p>
                <p>
                    <strong>Maksa</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Derīgs/Nav derīgs</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Iemesls</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks, materiāli un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Laiks, materiāli un maksas P1 projektā ir ietvertas rindā QL1. <br>
Izdevumi P1 projektā ir ietverti rindā QL2. <br>
Latrā piedāvājuma rindā ietvertās vērtības nepārklājas, tāpēc ir derīgas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="41" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums </p>
                <p>
Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai </p>
                <p>
QL2 ietver laiku, izdevumus un maksas par visu projektu P1 un tāpēc pārklājas ar to, kas ir iekļauts Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Atbilstoši 3. kārtulai </p>
                <p>
Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.
                </p>
                <p>
QL2 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.
                </p>
                <p>
Vienīgā papildu validācija attiecas uz QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas, lai nodrošinātu nepārklāšanos. To veic sistēma, kad tiek saistīti uzdevumi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Atbilstoši 5. kārtulai Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tādēļ abi tie var novērtēt vienu un to pašu projekta komponentu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
2. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Atbilstoši 4. kārtulai Q1 un Q2 ir divi piedāvājumi par atšķirīgām iespējām, tādēļ abi tie nevar novērtēt vienu un to pašu projekta komponentu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. cet. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visi projekta uzdevumi vai tukšs </p>
            </td>
            <td width="45" valign="top">
                <p>
Jā </p>
            </td>
            <td width="46" valign="top">
                <p>
Jā </p>
            </td>
            <td width="43" valign="top">
                <p>
Jā </p>
            </td>
            <td width="41" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
