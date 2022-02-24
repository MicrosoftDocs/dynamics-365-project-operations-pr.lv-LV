---
title: Projekta balstīta līguma rindu pārskats
description: Šajā tēmā ir sniegta informācija par darbu ar projekta līguma rindām.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858167"
---
# <a name="project-based-contract-lines-overview"></a>Projekta balstīta līguma rindu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta līguma rindas risinājumā Dynamics 365 Project Operations ir izstrādātas, lai ietvertu budžeta un norēķinu līgumus noteiktiem projekta darba komponentiem saistībā ar dalību. Līguma rinda, kuras pamatā ir projekts, tiek paplašināta projekta aplēsēm un norēķinu scenārijiem, izmantojot tālāk norādītos jēdzienus.

- Rēķinu izrakstīšanas metode
- Projektu un uzdevumu kartēšana
- Iekļautās transakciju klases
- Nepārsniedzamais ierobežojums
- Iekasēšanas iestatīšana
- Novērtējumi, izmantojot līgumu rindu informāciju
- Līguma rindas klients

Tālāk sniegtajā tabulā ir iekļauti lauki, kas atrodas projekta līguma rindas cilnē **Vispārīgi**, kas palīdz izveidot pamatu detalizētam, pilnīgi jaunam novērtējumam un rēķinu izrakstīšanas nosacījumiem ar projektu saistītam darbam.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| **Nosaukums** | Līguma rindas nosaukums. Tas identificē līguma diskrēto komponentu, kas tiek novērtēts. No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošās projekta piedāvājuma rindas vērtības. | Nosaukums, kas tiek kopēts uz to projekta rēķina rindu, kura tiek izveidota no šīs līguma rindas, kad tiek izveidots rēķins. |
| **Rēķinu izrakstīšanas metode** | No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka. Tā ir opciju kopa, kas pārstāv divus galvenos līguma modeļus, ko atbalsta Project Operations:</br>- **Fiksēta cena**</br>- **Laiks un materiāls** | Par pamatu izmantojot atsauces līguma rindas norēķinu metodi, tiek veikta faktiskā darbība. Ja līguma rindai, kurai ir atsauce uz faktisko, ir iestatīts laiks un materiālu norēķinu metode, tiek izveidoti izmaksu un rēķinā neiekļauto pārdošanas darījumu faktiskie ieraksti. Ja līguma rindai, kurai ir atsauce uz faktisko, ir fiksētas cenas norēķinu metode, tiek izveidota tikai izmaksu faktiskā summa. |
| **Project** | Izmantojiet šo lauku, lai norādītu projektu, kas tiks izmantots, lai nodrošinātu darbu šajā piesaistē. | Šī vērtība tiks izmantota saistībā ar **ietvertajiem uzdevumiem** un **ietvertajām transakciju klasēm**, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu. |
| **Iekļautie uzdevumi** | Norāda, vai šajā līguma rindā ir iekļauti visi atlasītā projekta paredzētie projekta uzdevumi vai tikai uzdevumu apakškopa. Tā ir opciju kopa ar tālāk norādītajām iespējamajām vērtībām.</br>- **Visi projekta uzdevumi**</br>- **Tikai atlasītie projekta uzdevumi**. Tukša vērtība šajā laukā ir vienāda ar atlasi **Visi projekta uzdevumi**. | Ja ir atlasīts vienums **Tikai atlasītie uzdevumi**, varat atlasīt noteiktus uzdevumus un tos saistīt ar šo līguma rindu lapas **Projekts** cilnē **Uzdevumu norēķinu iestatīšana**. Šī vērtība tiks izmantota savienojumā ar **Projektu** un **Iekļautajām transakciju klasēm**, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā. |
| **Iekļaut laiku** | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā laika transakcijas vai darbaspēka izmaksas tiks iekļautas šīs līguma rindas aprēķinā. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas laika transakcijas vai darba izmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu. |
| **Iekļaut izdevumus** | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā izdevumi tiks iekļauti šīs līguma rindas aprēķinā. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas izdevumu izmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu. |
| **Iekļaut materiālus** | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā materiāli tiks iekļauti šīs līguma rindas aprēķinā. Vērtība **Nē** norāda, ka atlasītajā projektā materiālu izmaksas netiks iekļautas šīs līguma rindas aprēķinā. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu. |
| **Iekļaut maksu** | Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā maksas tiks iekļauti šīs līguma rindas aprēķinā. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas papildmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu. |
| **Līgumā paredzētā summa** | Fiksētas cenas līguma rindā šī summa ir vienošanās par vērtību, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem. Laika un materiāla līguma rindā šī summa ir aprēķināta vērtība, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem. No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka. Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas summas. | Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot summas rindu informācijā. Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu summu pirms nodokļu nomaksas. |
| **Aprēķinātais nodoklis** | Lietotājs var rediģēt šo lauku, lai ievadītu prognozējamo nodokļu summu līguma rindā. Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas nodokļu summas. | Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot nodokļu summas rindu informācijā. Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu nodokļus. |
| **Līgumā paredzētā summa pēc nodokļa atskaitīšanas** | Līguma rindas summa pēc nodokļa atskaitīšanas. Šis lauks ir tikai lasāms un aprēķināts kā **Līgumā paredzētā summa + nodoklis**. | Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai ģenerētu periodisko norēķinu atskaites punktus. |
| **Nepārsniedzamais ierobežojums** | Lietotājs var rediģēt šo lauku, un tas ir pieejams tikai projekta līguma rindās, kurās ir iestatīta laika un materiālu norēķinu metode. | Lietotājs var rediģēt šo lauku. Kad uz laiku un materiāliem attiecas šī līguma rinda, faktiskais laiks un materiāli norāda faktisko summu attiecībā pret nepārsniedzamo limitu līguma rindā. Šis novērtējums ir pabeigts pēc jau iztērēto un piešķirto summu uzskaites. |
| **Klienta budžets** | Ja līgums tika izveidots no piedāvājuma, šis lauks ir rediģējams un ir nokopēts no atbilstošā piedāvājuma rindas lauka. | Šis lauks tiek izmantots tikai informācijai, un tam nav pakārtotas nozīmes. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validācijas kārtulas projekta līguma rindu cilnē Vispārīgi norādītajām opcijām

1. kārtula: ja lauks **Iekļautie uzdevumi** ir tukšs vai iestatīts kā **Visi projekta uzdevumi**, visi projekta uzdevumi tiek iekļauti līguma rindā.

2. kārtula: kad lauks **Iekļautie uzdevumi** ir tukšs vai tieši iestatīts kā **Visiem projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā līguma projekta līguma rindā.

3. kārtula: kad lauks **Iekļautie uzdevumi** ir iestatīts kā **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās līguma projekta līguma rindās.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Līgums</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Līguma rinda</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Iekļaut materiālus</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Iekļaut</strong>
                </p>
                <p>
                    <strong>Maksa</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Derīgs/Nav derīgs</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Iemesls</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks, izdevumi un materiāli P1 projektā ir ietverti līguma rindā CL1 un CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums. Laiks, izdevumi un materiāli P1 projektā ir ietverti līguma rindā CL1 un CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Laiks, materiāli un maksas P1 projektā ir ietvertas rindā CL1.
                </p>
                <ul>
                    <li>
Izdevumi P1 projektā ir ietverti rindā CL2.
                    </li>
                </ul>
                <p>
Latrā līguma rindā ietvertās vērtības nepārklājas, tāpēc ir derīgas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tukša </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="48" valign="top">
                <p>
Jā </p>
            </td>
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nav derīgs </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2. kārtulas pārkāpums </p>
                <p>
C1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.
                </p>
                <p>
CL2 ietver laiku, materiālus, izdevumus un maksas par visu projektu P1 un tāpēc pārklājas ar to, kas ir iekļauts C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Derīgs </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Katrā kārtulā #3 </p>
                <p>
C1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.
                </p>
                <p>
CL2 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.
                </p>
                <p>
Vienīgā papildu validācija attiecas uz CL1 uzdevumu apakškopu, kas atšķiras no CL2 uzdevumu apakškopas, lai nodrošinātu nepārklāšanos. To veic sistēma, kad tiek saistīti uzdevumi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Jā </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
