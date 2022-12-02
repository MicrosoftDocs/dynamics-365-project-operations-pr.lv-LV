---
title: Ievades žurnālu izveide un apstiprināšana
description: Šajā rakstā ir sniegta informācija par to, kā izveidot un apstiprināt ierakstu žurnālus programmā Microsoft Dynamics 365 Project Operations.
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

Ierakstu žurnālus izmanto, lai ierakstītu faktiskos datus tieši programmā Microsoft Dynamics 365 Project Operations. Izmantojot ierakstu žurnālus, programmā Project Operations nav jāievada laika, izmaksu un materiālu lietojuma žurnāli.

Viens ierakstu žurnāls ļauj izveidot vairākas žurnāla rindas. Kad tiek apstiprināts žurnāls, ierakstu žurnāla rinda reģistrē faktisko datu vienumu šādai informācijai:

- Izmaksas vai ieņēmumi atkarībā no atlasītā transakcijas tipa.
- Atlasītā transakcijas klase. Pieejamās klases ir **Laiks**, **Izmaksas**, **Materiāls**, **Honorārs**, **Atskaites punkts** un **Nodoklis**.
- Projekts un/vai uzdevums, kas atlasīts žurnāla rindā.

Lai programmā Project Operations izveidotu ierakstu žurnālu, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Pārdošana** \> **Transakcijas** \> **Žurnāli**.
2. Saraksta lapas **Ierakstu žurnāli** darbību rūtī atlasiet **Jauns**, lai izveidotu žurnālu.
3. Lapas **Jauns žurnāls** laukā **Apraksts** ievadiet žurnāla aprakstu.
4. Pārliecinieties, vai laukam **Žurnāla tips** ir iestatīta vērtība **Ieraksts**, un pēc tam atlasiet **Saglabāt**. Kad jaunais ierakstu žurnāls ir saglabāts, žurnāla lapā parādās cilne **Žurnāla rindas**.
5. Cilnē **Žurnāla rindas** rīkjoslā virs režģa atlasiet **Jauns**, lai izveidotu ierakstu žurnāla rindu.
6. Ierakstu žurnāla rindas izveides dialoglodziņā **Ātrā izveide** iestatiet laukus, kā aprakstīts tālāk sniegtajā tabulā.

    | Kolonna | Apraksts | Funkcionālā ietekme |
    | --- | --- | --- |
    | Darījuma klase | Žurnāla rinda var tikt klasificēta kādā no sešām transakciju klasēm: **Laiks**, **Izdevumi**, **Materiāli**, **Honorārs**, **Atskaites punkts** vai **Nodoklis**. | Transakciju klase **Nodoklis** programmā Project Operations ir novecojusi. <br> Ja izveidojat transakciju klasi **Nodoklis**, tā netiek apstrādāta rēķinu izveides laikā vai izmaksu vai ieņēmumu aprēķinos. **Atskaites punkts** ir tikai ieņēmumu transakciju klase. <br>Transakciju klase **Honorārs** tiek rādīta kā avanss, kas tika saņemts no klienta. Tā vienmēr ir jāizveido kā rēķinā iekļautas un rēķinā neiekļautas pārdošanas žurnāla rindu pāris. |
    | Transakcijas tips | Transakciju tipi **Izmaksas**, **Starporganizāciju pārdošana** un **Resursu struktūrvienības izmaksas** ir jāizmanto, lai ierakstītu izmaksas.<br> Transakciju tipi **Rēķinā neiekļautā pārdošana** un **Rēķinā iekļautā pārdošana** jāizmanto, lai ierakstītu ieņēmumus. | Transakciju klase **Honorārs** darbojas tikai ar transakciju tipiem **Rēķinā neiekļautā pārdošana** un **Rēķinā iekļautā pārdošana**.<br> Transakciju klase **Atskaites punkts** darbojas tikai ar transakcijas tipu **Rēķinā iekļautā pārdošana**. <br>Transakciju tipi **Starporganizāciju pārdošana** un **Resursu struktūrvienības izmaksas** ir attiecināmi tikai uz transakciju klasi **Laiks**, un tie ir pieejami tikai ierakstu žurnālos Lite izvietošanas scenārijā, bet ne izvietojot Project Operations resursu/krājumos nebalstītos scenārijos. |
    | Atlasīt produktu | Ja ir atlasīta transakciju klase **Materiāls**, šajā laukā varat norādīt, vai materiālu transakcija, kam veidojat žurnāla rindu, ir esošs produkts vai ierakstāms produkts. | Ja atlasāt **Ierakstāms produkts**, varat ievadīt produkta nosaukumu. |
    | Produkts | Atsauce uz preci no kataloga. | |
    | Apraksts | Žurnāla rindas apraksts, kas atvieglo identificēšanu. | Rēķinā neiekļauto pārdošanu žurnāla rindām šī vērtība tiek lietota kā apraksts, veidojot rēķina rindu informāciju. |
    | Ārējais apraksts | Žurnāla rindas apraksts, ko var izmantot koplietošanai ar ārējām ieinteresētajām pusēm. | Rēķinā neiekļauto pārdošanu žurnāla rindām šī vērtība tiek lietota kā ārējais apraksts, veidojot rēķina rindu informāciju. Tā var tikt parādīta arī rēķinā, kas tiek nosūtīts klientam. |
    | Norēķinu tips | Vērtība, kas norāda, vai žurnāla rinda tiks uzskatīta par iekļaujamu rēķinā, bezmaksas vai rēķinā neiekļaujamu komponentu projektā. | Parastā plūsmā rēķina tips tiek atvasināts no līgumā iestatītajiem nosacījumiem, par kuriem ir panākta vienošanās. Tomēr, kad tiek ierakstīta žurnāla rinda, šajā laukā var ievadīt vērtību. |
    | Dokumenta datums | Izmantojiet datumu, kad notika transakcija. | |
    | Sākuma datums | Izmantojiet datumu, kad notika transakcija. | Šo lauku izmanto, lai salīdzinātu ar rēķina izveides datumu transakcijām ar tipu **Rēķinā neiekļautā pārdošana**. Šis salīdzinājums palīdzēs izlemt, vai transakcijas datums ir nākotnē vai pagātnē. Rēķinam tiks pievienotas tikai transakcijas ar datumu pagātnē. |
    | Beigu datums | Izmantojiet datumu, kad notika transakcija. | |
    | Uzskaites datums | Izmantojiet datumu, kad tiks ierakstīta grāmatvedības ietekme. | |
    | Līguma rindas klients | Pēc noklusējuma, ja līguma rindā ir tikai viens klients, šis lauks tiek iestatīts klientam līguma rindā, kad tiek saglabāta žurnāla rinda. Ja līguma rindā ir vairāki klienti, atlasiet pareizo klientu līguma rindā. | Ja sistēma nevar noteikt līguma rindas klientu žurnāla rindā un ja tas nav norādīts no žurnāla rindas izveidotā tipa **Rēķinā neiekļautā pārdošana** faktisko datu vienumā, par faktisko datu vienumu netiks izrakstīts rēķins. |
    | Project | Atlasiet projektu, kurā ierakstīt faktisko datu vienumu. | Pamatojoties uz atlasīto projektu, transakciju klasi un uzdevumu, sistēma mēģinās noteikt līgumu, līguma rindu un līguma rindas klientu. |
    | Uzdevums | Atlasiet uzdevumu, kurā ierakstīt faktisko datu vienumu. | Ja līguma iestatīšanas laikā saistījāt uzdevumus ar līguma rindām, sistēma izmantos atlasīto uzdevumu kopā ar projektu un transakciju klasi, lai noteiktu līgumu, līguma rindu un līguma rindas klientu. |
    | Darbības kategorija | Atlasiet transakciju kategoriju, kurā ierakstīt faktisko datu vienumu. | Attiecībā uz izdevumiem atlasītā transakciju kategorija nosaka noklusējuma cenu, kas saglabāšanas laikā tiks ievadīta žurnāla rindā. |
    | Loma | Šis lauks attiecas uz laika žurnāla rindām. Atlasiet lomu resursam, kas pavadīja laiku pie projekta un/vai uzdevuma. | Ja laika žurnāla rindām, ievadot noklusējuma resursu izmaksas un rēķinu likmes, izmantojat standarta konfigurāciju, atlasītā loma tiek izmantota kopā ar resursu vienību, lai noteiktu noklusējuma cenu, kas tiks ievadīta žurnāla rindā, kad tā tiek saglabāta. Ja noklusējuma cenu ievadei izmantojat pielāgotu konfigurāciju, šī konfigurācija ir jāpārskata, lai noteiktu, vai noklusējuma cenu vērtību ievadei tiek izmantots lauks **Loma**. |
    | Apakšuzņēmēja līgums | Ja žurnāla rinda apzīmē apakšlīguma noslodzi vai apakšuzņēmēju izdevumus vai materiālus, atlasiet attiecīgo apakšlīgumu. | Kad tiek ierakstītas izmaksu žurnāla rindas, atlasītais apakšlīgums nosaka cenrādi, kas tiek izmantots noklusējuma vienības izmaksu ievadīšanai. |
    | Apakšuzņēmēja līguma rinda | Ja žurnāla rinda apzīmē apakšlīguma noslodzi vai apakšuzņēmēju izdevumus vai materiālus, atlasiet attiecīgo apakšlīguma rindu. | Kad tiek ierakstītas izmaksu žurnāla rindas, atlasītā apakšlīguma rinda nodrošina, ka apakšlīguma rindā pieejamie noslodzes aprēķini ir pareizi. |
    | Summas metode | Pēc noklusējuma šis lauks ir iestatīts uz **Jāreizina daudzums ar cenu**. Izmantojot šo metodi, summa tiek aprēķināta kā *Daudzums* × *Cena*. Cita atbalstītā metode ir **Fiksēta cena**. Lietojot šo metodi, cena tiek iestatīta uz summu, un daudzums aprēķinā netiek izmantots. | |
    | Vienības grafiks un vienība | Kopā vienības grafiks un vienība identificē daudzuma vienību. | Vienības un transakciju kategorijas kombinācija tiek izmantota, lai ievadītu noklusējuma cenas izdevumiem. Project Operations noklusējuma konfigurācijā vienības, lomas un resursu vienības kombinācija tiek izmantota, lai ievadītu noklusējuma cenas laikam. Ja noklusējuma cenu ievadei ir pielāgota konfigurācija, tā tiek izmantota kopā ar vienību. Produkta un vienības kombinācija tiek izmantota, lai ievadītu noklusējuma cenas materiāliem. |
    | Daudzums | Ievadiet daudzumu. | |
    | Cenrādis | Ja, veidojot žurnāla rindu, cenas lauks tiek atstāts tukšs, tiks izmantotas saistītās vērtības, lai ievadītu noklusējuma cenas, atkarībā no transakciju klases. Ja, veidojot žurnāla rindu, cena tiek ievadīta, tiek izmantota šī cena. | |
    | Nodoklis | Ievadiet jebkuru nodokļu summu. | Atkarībā no ievadītās nodokļu summas kopējā summa tiek aprēķināta kā *Summa* + *Nodoklis*. |

## <a name="confirm-an-entry-journal"></a>Ierakstu žurnāla apstiprināšana

Pēc visu žurnāla rindu ievadīšanas ierakstu žurnālā varat apstiprināt žurnālu. Šajā procesā katra žurnāla rinda tiek ierakstīta kā faktiskie dati atbilstošajos projektos.

Pēc žurnāla apstiprināšanas nevienu no tā rindām vairs nevar rediģēt.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiskie dati, kas izveidoti ar ierakstu žurnāla apstiprināšanu

Ir dažas galvenās atšķirības starp faktiskajiem datiem, kas tiek veidoti, izmantojot Ierakstu žurnāla apstiprinājumu, un faktiskajiem datiem, kas izveidoti laika, izmaksu un materiālu lietojuma žurnālu apstiprināšanas laikā, un rēķinu apstiprinājumu programmā Project Operations.

- Ierakstu žurnālos netiek neizmantoti transakciju savienojumi, lai faktiskās izmaksas saistītu ar rēķinos neiekļautajām faktiskajām pārdošanām. Faktiskie dati, kas tiek veidoti, kad tiek apstiprināti laika, izmaksu un materiālu lietojuma žurnālu ieraksti, vienmēr izmanto transakciju savienojumus, lai saistītu izmaksas un rēķinā neiekļautās faktiskās pārdošanas.
- Ierakstu žurnālos netiek neizmantota transakciju izcelsme, lai faktiskās izmaksas un rēķinos neiekļautās faktiskās pārdošanas saistītu ar jebkādu sākotnējo ierakstu. Faktiskie dati, kas tiek veidoti, kad tiek apstiprināti laika, izmaksu un materiālu lietojuma žurnālu ieraksti, vienmēr izmanto transakciju izcelsmi, lai saistītu izmaksas un rēķinā neiekļautās faktiskās pārdošanas ar sākotnējo laika ierakstu.
- Kad tiek izrakstīts rēķins par rēķinā neiekļautām faktiskajām pārdošanām, kas izveidotas ar ierakstu žurnāla apstiprinājumu, rēķinā iekļautās faktiskās pārdošanas, kas izveidotas rēķina apstiprināšanas laikā, tiek saistītas ar rēķinā neiekļautajām faktiskajām pārdošanām līdzīgā veidā kā rēķinā neiekļautās faktiskās pārdošanas, kas izveidotas, apstiprinot laika, izdevumu un materiālu lietojuma žurnālus.
- Ierakstu žurnāla rindas, kas tiek izveidotas laikam, ko ievadījuši starporganizāciju resursi, neizraisa tipu **Resursu struktūrvienības izmaksas** un **Starporganizāciju pārdošana** faktisko datu automātisku izveidi. Šie faktiskie dati ir jāizveido manuāli. Šī uzvedība atšķiras no to laika ierakstu uzvedības, ko ieraksta starporganizāciju resursi. Tādā gadījumā, kad laiks tiek apstiprināts, lietojumprogramma automātiski izveido projektā tipa **Izmaksas** faktiskos datus un tipu **Resursu struktūrvienības izmaksas** un **Starporganizāciju pārdošana** darbinieka atbildīgajā nodaļā. Pēc tam tā izmanto transakciju savienojumus, lai saistītu šos faktiskos datus kopā, un transakciju izcelsmi, lai saistītu tos ar sākotnējo laika ierakstu.
- Kad ierakstu žurnāli tiek apstiprināti, tie izveido faktiskos datus. Taču šo faktisko datu labošanai nevar izmantot labojumu žurnālus. Šī uzvedība atšķiras no tādu faktisko datu scenārija, kas tiek izveidoti, kad tiek apstiprināti laika, izmaksu un materiālu lietojuma žurnāli. Tādā gadījumā lietojumprogramma ļauj izmantot labojumu žurnālus, lai labotu faktiskajos datos jebkādas kļūdas, ja vien par šiem faktiskajiem datiem vēl nav izrakstīts rēķins. Ja par tiem jau ir izrakstīts rēķins, joprojām varat labot faktisko datu vērtību, ja sagatavojat klientam pilnu kredītu par šo faktisko datu vienumu.

> [!NOTE]
> Ierakstu žurnāls neievieš striktas noklusējuma kārtulas. Tāpēc izmantojiet šos ierakstu žurnālus pēc iespējas mazāk un ievērojiet piesardzību un uzmanību, lai neizveidotu sistēmā nederīgus finanšu datus. Lai izveidotu faktiskos datus, vienmēr izmantojiet laika, izmaksu un materiālu lietojuma žurnālus, atskaites punkta un honorāra iestatījumu projekta līgumos, kā arī projekta rēķina apstiprinājuma procesu, nevis ierakstu žurnālus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
