---
title: Ievades žurnālu izveide un apstiprināšana
description: Šajā rakstā sniegta informācija par to, kā izveidot un apstiprināt ierakstu žurnālus programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912341"
---
# <a name="create-and-confirm-entry-journals"></a>Ievades žurnālu izveide un apstiprināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Ierakstu žurnālus izmanto, lai reģistrētu faktiskos datus tieši programmā Microsoft Dynamics 365 Project Operations. Izmantojot ierakstu žurnālus, projekta operācijās nav jāievada laika, izdevumu un materiālu lietojuma žurnāli.

Viens ierakstu žurnāls ļauj izveidot vairākas žurnāla rindas. Kad žurnāls ir apstiprināts, ierakstu žurnāla rindā tiek reģistrēta faktiskā informācija par šādu informāciju:

- Izmaksas vai ieņēmumi atkarībā no atlasītā darbības tipa.
- Atlasītā darbības klase. Pieejamās klases ir **laiks**, izdevumi, **materiāli** **,** aizturētājs **,** **atskaites punkts** un **nodokļi**.
- Projekts un/vai uzdevums, kas atlasīts žurnāla rindā.

Veiciet šīs darbības, lai izveidotu ierakstu žurnālu projektu operācijās.

1. Dodieties uz **Pārdošanas** \> **transakciju** \> **žurnāliem.**
2. **Saraksta ierakstu žurnālu** saraksta lapā Darbību rūtī atlasiet **Jauns**, lai izveidotu žurnālu.
3. **Lapas Jauns žurnāls** **laukā Apraksts** ievadiet žurnāla aprakstu.
4. Pārliecinieties, **vai lauks Žurnāla tips** ir iestatīts uz **Ieraksts**, un pēc tam atlasiet **Saglabāt**. Pēc jaunā ierakstu žurnāla saglabāšanas **žurnāla lapā jāparādās cilnei Žurnāla rindas**.
5. **Cilnes Žurnāla rindas** rīkjoslā virs režģa atlasiet **Jauns**, lai izveidotu ierakstu žurnāla rindu.
6. Dialoglodziņā **Ātrā izveide** ierakstu žurnāla rindas izveidei iestatiet laukus, kā aprakstīts šajā tabulā.

    | Kolonna | Apraksts | Funkcionālā ietekme |
    | --- | --- | --- |
    | Darījuma klase | Žurnāla rindu var klasificēt vienā no sešām darbību klasēm: **Laiks**, Izdevumi **,** Materiāli **·**, **Aizturētājs**, **Atskaites punkts** vai **Nodoklis**. | Pvn **darbību** klase projekta operācijās ir novecojusi. <br> Ja izveidojat **PVN** darbību klasi, tā netiks apstrādāta, izrakstot rēķinus vai aprēķinot izmaksas vai ieņēmumus. **Atskaites punkts** ir tikai ieņēmumu darbību klase. <br>Aizturētāja **darbību** klase ir avanss, kas saņemts no debitora. Tas vienmēr jāveido kā rēķinā iekļauto pārdošanas un nemainīgo pārdošanas žurnāla rindu pāris. |
    | Transakcijas tips | Izmaksu reģistrēšanai **jāizmanto izmaksu,** starpuzņēmumu pārdošanas **un** resursu vienības pašizmaksas **darbību tipi.**<br> Ieņēmumu reģistrēšanai **jāizmanto darbību tipi Nemainīga pārdošana** un **pārdošana** rēķinos. | Saglabātāja **darbību** klase darbojas tikai ar **darbību tipiem Nemainīgā pārdošana** un **rēķinā norādītā pārdošana**.<br> Atskaites **punkta** darbību klase darbojas tikai ar **darbības tipu Rēķinā**. <br>**Interorg pārdošanas** un **resursu vienības izmaksu** darbību tipi ir piemērojami tikai **laika** darbību klasei, un tie ir pieejami tikai ierakstu žurnālos Lite izvietošanas scneario, nevis izvietojot projekta operācijas resursu / neuzkrātos scenārijos. |
    | Atlasīt produktu | Ja ir atlasīta **materiālu** darbību klase, šajā laukā var norādīt, vai būtiskā darbība, kurai veidojat žurnāla rindu, ir esoša prece vai rakstīšanas produkts. | Ja atlasāt **Ierakstāmais produkts**, var ievadīt produkta nosaukumu. |
    | Produkts | Atsauce uz preci no kataloga. | |
    | Apraksts | Žurnāla rindas apraksts, kas palīdz to viegli identificēt. | Nelīdzinātām pārdošanas žurnāla rindām vērtība tiks izmantota kā apraksts, veidojot detalizētu informāciju par rēķina rindu. |
    | Ārējais apraksts | Žurnāla rindas apraksts, ko var izmantot koplietošanai ar ārējām ieinteresētajām personām. | Nelīdzenām pārdošanas žurnāla rindām vērtība tiks izmantota kā ārējais apraksts, veidojot detalizētu informāciju par rēķina rindu. Tas var parādīties arī klientam nosūtītajā rēķinā. |
    | Norēķinu tips | Vērtība, kas norāda, vai žurnāla rinda projektā tiks uzskatīta par apmaksājamu, bezmaksas vai neapmaksājamu komponentu. | Tipiskā plūsmā norēķinu veids tiek atvasināts no līgumā iestatītajiem saskaņotajiem noteikumiem. Tomēr, ierakstot žurnāla rindu, šajā laukā var ievadīt vērtību. |
    | Dokumenta datums | Izmantojiet datumu, kad darbība notika. | |
    | Sākuma datums | Lietojiet datumu, kad darbība notika. | Šis lauks tiek izmantots salīdzināšanai ar rēķina izveides datumu darbībām, kuru tips ir **Nemainīga pārdošana**. Šis salīdzinājums palīdzēs jums izlemt, vai darījums ir nākotnes vai iepriekš datēts. Rēķinam tiks pievienotas tikai datētas darbības. |
    | Beigu datums | Lietojiet datumu, kad darbība notika. | |
    | Uzskaites datums | Izmantojiet datumu, kad tiks reģistrēta uzskaites ietekme. | |
    | Līguma rindas debitors | Pēc noklusējuma, ja līguma rindai ir tikai viens klients, šis lauks tiek iestatīts klientam līguma rindā, saglabājot žurnāla rindu. Ja līguma rindai ir vairāki debitori, atlasiet pareizo debitoru līguma rindā. | Ja sistēma nevar noteikt līguma rindas debitoru žurnāla rindā un ja tā ir tukša faktiskajā no žurnāla rindas izveidotā **tipa Nemainīgā pārdošana** faktiskajā stāvoklī, faktiskajam rēķinam netiks izrakstīts rēķins. |
    | Project | Atlasiet projektu, kurā ierakstīt faktisko. | Pamatojoties uz atlasīto projektu, darbību klasi un uzdevumu, sistēma mēģinās noteikt līgumu, līguma rindu un līguma rindas debitoru. |
    | Uzdevums | Atlasiet uzdevumu, kurā ierakstīt faktisko. | Ja līguma iestatīšanas laikā saistījāt uzdevumus ar līguma rindām, sistēma izmanto atlasīto uzdevumu kopā ar projekta un darbības klasi, lai noteiktu līgumu, līguma rindu un līguma rindas klientu. |
    | Darbības kategorija | Atlasiet darbību kategoriju, kurā ierakstīt faktisko. | Izdevumiem atlasītā darbību kategorija nosaka noklusēto cenu, kas tiks ievadīta žurnāla rindā, kad tā tiks saglabāta. |
    | Loma | Šis lauks attiecas uz laika žurnāla rindām. Atlasiet tā resursa lomu, kurš pavadīja laiku projektam un/vai uzdevumam. | Laika žurnāla rindām, ja noklusējuma resursu izmaksu un rēķinu likmju ievadīšanai izmantojat gatavu konfigurāciju, atlasītā loma tiek izmantota kopā ar resursu vienību, lai noteiktu noklusējuma cenu, kas tiks ievadīta žurnāla rindā, kad tā tiks saglabāta. Ja noklusējuma cenu ievadīšanai izmantojat pielāgotu konfigurāciju, šī konfigurācija ir jāpārskata, lai noteiktu, vai **lauks Loma** tiek izmantots noklusējuma cenu vērtību ievadīšanai. |
    | Apakšuzņēmēja līgums | Ja žurnāla rinda atspoguļo apakšuzņēmēju ražīgumu vai apakšuzņēmēju izdevumus vai materiālus, atlasiet atbilstošo apakšuzņēmuma līgumu. | Ierakstot izmaksu žurnāla rindas, atlasītais apakšuzņēmums noteiks cenrādi, kas tiek izmantots, lai ievadītu noklusējuma vienības pašizmaksu. |
    | Apakšuzņēmuma līnija | Ja žurnāla rinda attēlo apakšuzņēmuma noslodzi vai apakšuzņēmēju izdevumus vai materiālus, atlasiet atbilstošo apakšuzņēmuma rindu. | Kad izmaksu žurnāla rindas tiek ierakstītas, atlasītā apakšuzņēmuma rinda nodrošinās, ka apakšuzņēmuma rindā pieejamie noslodzes aprēķini tiek pareizi aprēķināti. |
    | Summas metode | Pēc noklusējuma šis lauks ir iestatīts uz **Reizināt daudzumu ar cenu**. Ja tiek izmantota šī metode, summa tiek aprēķināta kā *Daudzums* × *cena.* Otra atbalstītā metode ir **fiksēta cena**. Ja tiek izmantota šī metode, cena tiks iestatīta uz summu, un daudzums aprēķinā netiks izmantots. | |
    | Vienību grafiks un vienība | Kopā vienību grafiks un vienība identificē daudzuma vienību. | Vienības un darbības kategorijas kombinācija tiek izmantota, lai ievadītu izdevumu noklusējuma cenas. Projekta operāciju noklusējuma konfigurācijā vienības, lomas un resursu vienības kombinācija tiek izmantota, lai ievadītu laika noklusējuma cenas. Ja noklusējuma cenu ievadīšanai ir pielāgota konfigurācija, tā tiks izmantota kopā ar vienību. Produkta un vienības kombinācija tiek izmantota, lai ievadītu materiālu noklusējuma cenas. |
    | Daudzums | Ievadiet daudzumu. | |
    | Cenrādis | Ja žurnāla rindas izveides laikā cena paliek tukša, atbilstošās vērtības tiks izmantotas, lai ievadītu noklusējuma cenas atkarībā no darbības klases. Ja cena tiek ievadīta, veidojot žurnāla rindu, šī cena tiks izmantota. | |
    | Nodoklis | Ievadiet jebkuru nodokļa summu. | Atkarībā no ievadītās nodokļa summas paplašinātā summa tiks aprēķināta kā *summas* + *nodoklis*. |

## <a name="confirm-an-entry-journal"></a>Ierakstu žurnāla apstiprināšana

Kad ierakstu žurnālā ir ievadītas visas žurnāla rindas, žurnālu var apstiprināt. Šajā procesā katra žurnāla rinda tiks ierakstīta kā faktiskā atbilstošā projektos.

Pēc žurnāla apstiprināšanas to vairs nevar rediģēt vai kādu no tā rindām.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Fakti, ko izveidojis ierakstu žurnāla apstiprinājums

Pastāv dažas būtiskas atšķirības starp faktiskajiem datiem, ko izveidojis ieraksta žurnāla apstiprinājums, un faktiskajiem datiem, kas izveidoti, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus un rēķinu apstiprinājumu projekta operācijās:

- Ierakstu žurnāli neizmanto transakciju savienojumus, lai faktisko pašizmaksu saistītu ar faktisko nemainīgo pārdošanu. Faktiskie dati, kas tiek izveidoti, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus, vienmēr izmanto transakciju savienojumus, lai sasaistītu izmaksas un nelīdzenos pārdošanas faktiskos lielumus.
- Ierakstu žurnāli neizmanto darbību izcelsmi, lai saistītu faktiskās izmaksas un nemainīgās pārdošanas faktiskās izmaksas ar jebkuru sākotnējo ierakstu. Faktiskie dati, kas tiek izveidoti, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus, vienmēr izmanto darbību izcelsmi, lai sasaistītu izmaksu un nemainīgās pārdošanas faktiskās izmaksas ar sākuma laika ierakstu.
- Ja rēķina izrakstīšanai tiek izrakstīts rēķins par neslīpētām pārdošanas faktiskajām formām, kas izveidotas ar ieraksta žurnāla apstiprinājumu, rēķina apstiprināšanas laikā izveidotās rēķinā iekļautās pārdošanas faktiskās versijas tiek saistītas ar nesegtajām pārdošanas faktiskajām formām, kas tiek izveidotas, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus.
- Ierakstu žurnāla rindas, kas izveidotas laikam, kuru ievada starporganizāciju resursi, neizraisa tipu Resursu iegūšana vienības **pašizmaksa** un **Starpkopienu pārdošana** faktisku izveidi automātiski. Šie fakti ir jāizveido manuāli. Šī darbība atšķiras no laika ierakstu izturēšanās, ko reģistrē starporganizāciju resursi. Šādā gadījumā, apstiprinot laiku, programma automātiski izveido projekta izmaksu tipa faktiskos **datus un resursa vienības pašizmaksas** un **starppirkstu pārdošanas** tipu faktiskos **datus darbinieka paša nodaļā.** Pēc tam tas izmanto transakciju savienojumus, lai sasaistītu šos faktiskos datus un transakciju izcelsmi, lai saistītu tos ar sākuma laika ierakstu.
- Kad ierakstu žurnāli ir apstiprināti, tie izveido faktiskos izdevumus. Tomēr labojumu žurnālus nevar izmantot, lai labotu šos faktiskos datus. Šī darbība atšķiras no faktiskās darbības, kas tiek izveidota, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus. Šādā gadījumā lietojumprogramma ļauj izmantot labošanas žurnālus, lai labotu faktiskos datus un novērstu kļūdas, ar nosacījumu, ka par šiem faktiskajiem dokumentiem vēl nav izrakstīts rēķins. Ja tiem jau ir izrakstīts rēķins, jūs joprojām varat labot faktisko, ja klientam tiek apstrādāts pilns šī faktiskā kredīta.

> [!NOTE]
> Ierakstu žurnāli neievieš stingras noklusējuma kārtulas. Tāpēc izmantojiet šos ierakstu žurnālus pēc iespējas mazāk un ievērojiet piesardzību un rūpējieties, lai nodrošinātu, ka sistēmā neveidojat bojātus finanšu datus. Kad vien iespējams, izmantojiet laika, izdevumu un materiālu lietojuma žurnālus, atskaites punkta un aizturētāja iestatījumus projekta līgumos un projekta rēķina apstiprināšanas procesu, nevis ierakstu žurnālus, lai izveidotu faktiskos datus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
