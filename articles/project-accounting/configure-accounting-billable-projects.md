---
title: Konfigurēt apmaksājamo projektu uzskaiti
description: Šajā tēmā ir sniegta informācija par apmaksājamu projektu uzskaites iespējām.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4398ef44d4211a2921270bebe38fc92f18503854
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287652"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurēt apmaksājamo projektu uzskaiti

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations atbalsta dažādas grāmatvedības opcijas apmaksājamiem projektiem, kas ietver laika un materiālu, un fiksētas cenas transakcijas.

- **Laika un materiālu darījumi**: par šiem darījumiem tiek izrakstīts rēķins kā par darba norisēm, pamatojoties uz stundu patēriņu, izdevumiem, elementiem vai maksām projektā. Šīs darījumu izmaksas var saskaņot ar katra darījuma ieņēmumiem, un par projektu izrakstīts rēķins kā par darba norisēm. Projekta ieņēmumus var arī uzkrāt laikā, kad notiek darījums. Rēķinu izrakstīšanas laikā tiek atzīti ieņēmumi un, ja piemērojams, uzkrātie ieņēmumi tiek atgriezti.
- **Fiksētas cenas darījumi**: par šiem darījumiem tiek izrakstīts rēķins atbilstoši norēķinu grafikam, kura pamatā ir projekta līgums. Fiksētas cenas darījumu ieņēmumus var atpazīt rēķinu izrakstīšanas vai aprēķināšanas laikā un periodiski grāmatot, izmantojot metodi **Pabeigts līgums** vai **Pabeigtie procenti**.

Projekts tiek uzskatīts par apmaksājamu, ja tas ir saistīts ar vienu vai vairākām līguma rindām. Projekta līguma rinda pati definē, kādas norēķinu metodes un darījumu tipi ir atļauti.

Piemēram, uzņēmums Fabrikam Robotics ir uzvarējis projekta līgumu ar korporāciju Adatum par aprīkojuma optimizāciju. Adatum maksās fiksētu summu 10 000 USD apmērā, lai segtu radušos projekta izdevumus. Šī ir fiksētas cenas norēķinu metode. Par projekta laiku un maksām tiek izrakstīts rēķins atbilstoši to patēriņam. Šī ir laika un materiālu norēķinu metode. Viss darbs tiks izsekots, izmantojot atsevišķu projektu ar nosaukumu Adatum aprīkojuma optimizācija.

Projekta darba grupas dalībnieks atzīmē, ka ir astoņas darba stundas strādājis pie projekta Adatum aprīkojuma optimizācija. Kad projekta vadītājs apstiprina šo laiku, sistēma izmanto laika un materiālu norēķinu metodi, lai izveidotu faktiskos darījumus, rēķinu un uzskaiti. Šis darījums netiks iekļauts fiksētās cenas ieņēmumu tāmes aprēķinā.

Cits projekta darba grupas dalībnieks iesniedz ceļa izdevumus 2000,00 USD apmērā projektā Adatum aprīkojuma optimizācija. Kad projekta vadītājs apstiprina šo iesniegto informāciju, sistēma izmanto fiksētās cenas norēķinu metodi, lai izveidotu faktiskos darījumus un uzskaiti par šiem projekta izdevumiem. Klientam netiks izrakstīts rēķins, pamatojoties uz šo darījumu. Tā vietā tam tiks izrakstīts rēķins, izmantojot atsevišķi konfigurētus norēķinu atskaites punktus. Šis izdevumu darījums, kā arī izdevumu aprēķini tiks iekļauti fiksētās cenas ieņēmumu tāmes aprēķinā.

Uzskaites principi projekta darījumiem tiek definēti projekta izmaksu un ieņēmumu profilos. Katram projekta darījumam sistēma nosaka atbilstošus projekta izmaksu un ieņēmumu profilus, izmantojot konfigurētās projekta izmaksu un ieņēmumu profila kārtulas.

## <a name="define-project-cost-and-revenue-profiles"></a>Projekta izmaksu un ieņēmumu profilu definēšana 

Projekta izmaksu un ieņēmumu profili nosaka uzskaites kārtulas projekta darījumiem. Šos profilus konfigurē Projekta pārvaldībā un uzskaitē. 

Lai izveidotu jaunu projekta izmaksu un ieņēmumu profilu, izpildiet tālāk norādītās darbības. 

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Projekta izmaksu un ieņēmumu profili**. 
2. Atlasiet vienumu **Jauns**, lai izveidotu jaunu projekta izmaksu un ieņēmumu profilu.
3. Laukā **Nosaukums** ievadiet profila nosaukumu un īsu aprakstu.
4. Laukā **Norēķinu metode** atlasiet **Laiks un materiāli** vai **Fiksēta cena**.
5. Izvērsiet FastTab cilni **Virsgrāmata**. Šīs cilnes lauki definē uzskaites principus, ko izmanto, kad projekta darījumi tiek ierakstīti žurnālā, izmantojot Project Operations integrācijas žurnālu, un pēc tam par tiem tiek izrakstīts rēķins, izmantojot Projekta rēķina priekšlikumu.
6. Atlasiet atbilstošo informāciju šajos laukos FastTab cilnē **Virsgrāmata**:

    - **Izmaksu grāmatošana – stunda**:

       - *Bez virsgrāmatas*: laika darījumu izmaksas netiks grāmatotas Virsgrāmatā, grāmatojot Project Operations integrācijas žurnālu. Tomēr grāmatvedis var grāmatot izmaksas vēlāk, izmantojot funkciju Grāmatot izmaksas.
       - **Bilance**: laika darījumu izmaksas tiks ierakstītas Virsgrāmatas konta tipā *WIP – izmaksu vērtība* un kreditētas kontā *Algu sadalījuma konts* Virsgrāmatas grāmatošanas iestatījumā. Grāmatvedis izmantos funkciju Grāmatot izmaksas, lai šīs izmaksas no Bilances konta periodiski pārvietotu uz Peļņas un zaudējumu kontu.
       - **Peļņa un zaudējumi**: grāmatojot Project Operations integrācijas žurnālu, laika darījuma izmaksas tiks ierakstītas Virsgrāmatas konta tipā *Izmaksas* un kreditētas kontā *Algu sadalījuma konts*, kas definēts cilnē **Izmaksas** lapā **Virsgrāmatas grāmatošanas iestatīšana** (**Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Grāmatošana** \> **Virsgrāmatas grāmatošanas iestatīšana**). Šī ir visizplatītākais laika un materiālu darījumu iestatījums.
        - *Nekad neizmantot Virsgrāmatu*: laika darījumu izmaksas nekad netiks grāmatotas Virsgrāmatā.

    - **Izmaksu grāmatošana — izdevumi**:

         - **Bilance**: grāmatojot Project Operations integrācijas žurnālu, izdevumu darījumu izmaksas tiek ierakstītas Virsgrāmatas konta tipā *WIP – izmaksu vērtībā*, kā definēts cilnē **Izmaksas** lapā **Virsgrāmatas grāmatošanas iestatīšana** un piešķirts ieskaita konta žurnāla rindā. Noklusējuma ieskaita konti izdevumiem ir definēti sadaļā **Projekta pārvaldība un uzskaite** > **Iestatīšana** \> **Grāmatošana** \> **Noklusējuma ieskaita konti izdevumiem**. Grāmatvedis izmantos funkciju **Grāmatot izmaksas**, lai šīs izmaksas no bilances konta periodiski pārvietotu uz peļņas un zaudējumu kontu.
        - **Peļņa un zaudējumi**: grāmatojot Project Operations integrācijas žurnālu, izdevumu darījumu izmaksas tiek ierakstītas Virsgrāmatas konta tipā *Izmaksas*, kā definēts cilnē **Izmaksas** lapā **Virsgrāmatas grāmatošanas iestatīšana** un piešķirts ieskaita konta žurnāla rindā. Noklusējuma ieskaita konti izdevumiem ir definēti sadaļā **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Grāmatošana** \> **Noklusējuma ieskaita konti izdevumiem**.
       
    - **Par kontu rēķinu izrakstīšanu**:

        - **Bilance**: grāmatojot Projekta rēķina priekšlikumu, starpkonta darījums (rēķina izrakstīšanas atskaites punkts) tiks piešķirtas Virsgrāmatas konta tipam *WIP rēķins izrakstīts — kontā*, kas definēts cilnē **Ieņēmumi** lapā **Virsgrāmatas grāmatošanas iestatīšana**, un ierakstīts Klienta bilances kontā.
         - **Peļņa un zaudējumi**: grāmatojot Projekta rēķina priekšlikumu, starpkonta darījums (rēķina izrakstīšanas atskaites punkts) tiks piešķirtas Virsgrāmatas konta tipam *Ieņēmumu rēķins izrakstīts — kontā*, kas definēts cilnē **Ieņēmumi** lapā **Virsgrāmatas grāmatošanas iestatīšana**, un ierakstīts Klienta bilances kontā. Klienta bilances konti tiek definēti sadaļā **Debitori** \> **Iestatīšana** \> **Klientu grāmatošanas profili**.

   Definējot grāmatošanas metodes Laika un materiālu norēķinu metodēm, var gūt ieņēmumus pēc darījuma veida (stunda, izdevumi un maksa). Ja opcija **Uzkrāt ieņēmumus** ir iestatīta uz **Jā**, tad pārdošanas darījumi, par kuriem nav izrakstīts rēķins, Project Operations integrācijas žurnālā tiks ierakstītas vispārējā virsgrāmatā. Pārdošanas vērtība tiek ierakstīta kontā **WIP — pārdošanas vērtības konts** un piešķirta kontam **Uzkrātie ieņēmumi — pārdošanas vērtība**, kas tika iestatīts lapā **Virsgrāmatas grāmatošanas iestatīšana**, cilnē **Ieņēmumi**. 
  
  > [!NOTE]
  > Opcija **Uzkrāt ieņēmumus** ir pieejama tikai tad, ja attiecīgā darījuma tipa **Izmaksas** ir grāmatotas peļņas un zaudējumu kontos.
    
7. Izvērsiet FastTab cilni **Aprēķins**. Šīs cilnes laukos definējiet aprēķina iestatījumus fiksētas cenas ieņēmumu aprēķiniem. Šīs cilnes lauki attiecas tikai uz Projekta izmaksu un ieņēmumu profiliem ar norēķinu metodi **Fiksēta cena**.
8. Atlasiet atbilstošo informāciju šajos laukos FastTab cilnē **Aprēķins**:

    - **Projekta pabeigšanas aprēķinos izmantotais princips**:

        - **Pabeigts līgums**: izmaksu saskaņošana un ieņēmumu atzīšana netiek veikta ātrāk par projekta beigām. Līdz brīdim, kad projekts ir pabeigts, izmaksas bilancē atspoguļo kā WIP.
        - **Pabeigtie procenti**: uzkrātie ieņēmumi tiek aprēķināti un grāmatoti virsgrāmatā katrā periodā, pamatojoties uz projekta pabeigšanas daļu procentos. Ir pieejamas vairākas metodes, lai aprēķinātu pabeigtības procentuālo vērtību. Šīs metodes var būt automātiskas, pamatojoties uz konfigurāciju, vai manuālas.
        - **Bez WIP**: šo iestatījumu izmanto fiksētas cenas projektiem ar īsu laika periodu un gadījumos, kad rēķins tiek izrakstīts un izmaksas notiek vienā un tajā pašā periodā. Šajā gadījumā lauka vērtība **Starpkonta rēķini** FastTab cilnē **Virsgrāmata** tiek automātiski iestatīta uz **Peļņa un zaudējumi**, lai nodrošinātu ieņēmumu atzīšanu rēķina izrakstīšanas brīdī. Šī projekta izmaksu un ieņēmumu profilam netiek izmantots Ieņēmumu aprēķina process.

    - **Atbilstības princips**: šis lauks nosaka, kā aprēķinātā pārdošanas vērtība (uzkrātie ieņēmumi) tiks grāmatota virsgrāmatā.

        - Izmantojot principu **Pārdošanas vērtība**, sistēma aprēķina pārdošanas vērtību, salīdzinot izmaksas un ieņēmumus un pēc tam tos grāmatojot kā vienu summu.
        - Izmantojot principu **Ražošanas un peļņa**, sistēma sadala pārdošanas vērtību realizētajās izmaksās un aprēķinātajā peļņā. Tās tiek grāmatotas atsevišķi.

    - **Izmaksu veidnes**: ļauj sagrupēt projekta darījumus, pamatojoties uz darījuma tipu un projekta kategoriju, un definēt pabeigtības procentuālās vērtības aprēķina kārtulas šīm grupām.
    - **Perioda kodi**: definējiet biežumu, ar kādu noteiktam Projekta izmaksu un ieņēmumu profilam veic ieņēmumu aprēķinus.
    - **Aprēķinu kategorijas**: izmanto pārdošanas vērtības (uzkrāto ieņēmumu) grāmatošanai Projekta darījumos. Vispirms konfigurējiet īpašu projekta kategoriju darījuma tipam **Maksa** un pēc tam iestatiet karodziņu **Aprēķins** šai projekta kategorijai. Tālāk atkarībā no atlasītā atbilstības principa izvēlieties šo projekta kategoriju vērtībā **Pārdošana** vai laukā **Peļņa** Projekta izmaksu un ieņēmumu profilā.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Projekta izmaksu un ieņēmumu profilu parauga konfigurācijas

Laiks un materiāli — bez WIP

![Izmaksu un ieņēmumu profils: laiks un materiāli — bez WIP](media/time-material-no-wip.png)

Laiks un materiāli — WIP (ieņēmumi)

![Izmaksu un ieņēmumu profils: laiks un materiāli — WIP](media/time-material-with-wip.png)

Fiksēta cena — bez WIP

![Izmaksu un ieņēmumu profils: fiksēta cena — bez WIP](media/fixed-price-no-wip.png)

Fiksēta cena — pabeigts līgums

![Izmaksu un ieņēmumu profils: fiksēta cena — pabeigts līgums](media/fixed-price-completed-contract.png)

Fiksēta cena — pabeigtības procentuālā vērtība

![Izmaksu un ieņēmumu profils: fiksēta cena — pabeigtības procentuālā vērtība](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Projekta izmaksu un ieņēmumu profilu uzskaites notikumu paraugi.

| Uzskaites notikums                  | Laiks un materiāli — bez WIP                       | Laiks un materiāli — WIP                                                                                           | Fiksēta cena — bez WIP                                            | Fiksēta cena — pabeigts līgums                                                                            | Fiksēta cena — pabeigtības procentuālā vērtība                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Laika darījumu reģistrācija žurnālā    | Debets — izmaksas <br>Kredīts — algu sadalījums          | Debets — izmaksas <br>Kredīts — algu sadalījums <br>Debets — WIP pārdošanas vērtība <br>Kredīts — uzkrāto ieņēmumu pārdošanas vērtība                | Debets — izmaksas <br>Kredīts — algu sadalījums                         | Debets — izmaksas <br>Kredīts — algu sadalījums                                                                    | Debets — izmaksas <br>Kredīts — algu sadalījums                       |
| Izdevumu reģistrācija žurnālā | Debets — izmaksas <br>Kredīts — ieskaita konts izdevumiem | Debets — izmaksas <br>Kredīts — ieskaita konts izdevumiem <br>Debets — WIP pārdošanas vērtība <br>Kredīts — uzkrāto ieņēmumu pārdošanas vērtība      | Debets — izmaksas <br>Kredīts — ieskaita konts izdevumiem                 | Debets — izmaksas<br> Kredīts — ieskaita konts izdevumiem                                                            | Debets — izmaksas <br>Kredīts — ieskaita konts izdevumiem               |
| Rēķina izrakstīšana klientam                | Debets — klienta bilance <br>Kredīts — ieņēmumi, par ko izrakstīts rēķins | Debets — klienta bilance <br>Kredīts — ieņēmumi, par ko izrakstīts rēķins <br>Kredīts — WIP pārdošanas vērtība Debets — uzkrāto ieņēmumu pārdošanas vērtība | Debets — klienta bilance <br>Kredīts — ieņēmumi, par ko izrakstīts rēķins — kontā | Debets — klienta bilance <br>Kredīts — WIP — izrakstīts rēķins kontā                                                  | Debets — klienta bilance <br>Kredīts — WIP — izrakstīts rēķins kontā    |
| Ieņēmumu aprēķina grāmatošana             | Nav piemērojams                                   | Nav piemērojams                                                                                                    | Nav lietojams                                                  | Debeta — WIP izmaksu vērtība <br>Kredīts — izmaksas                                                                         | Debets — WIP — pārdošanas vērtība <br>Kredīts — uzkrāto ieņēmumu pārdošanas vērtība |
| Novērst                         | Nav piemērojams                                   | Nav piemērojams                                                                                                    | Nav lietojams                                                  | Kredīts — WIP izmaksu vērtība <br>Debets — izmaksas <br>Kredīts — uzkrāto ieņēmumu pārdošanas vērtība <br>Kredīts — WIP — izrakstīts rēķins kontā | Kredīts — WIP — izrakstīts rēķins kontā <br>Kredīts — WIP pārdošanas vērtība     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projekta izmaksu un ieņēmumu profila kārtulu konfigurēšana

Projekta izmaksu un ieņēmumu profila kārtulas nosaka Projekta izmaksu un ieņēmumu profilu, kas jāizmanto, apstrādājot apmaksājamos projekta darījumus. Definējiet kārtulas sadaļā **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Grāmatošana** \> **Projekta izmaksu un ieņēmumu profila kārtulās**.

Kārtulas var definēt pēc projekta līguma, projekta grupas vai konkrētiem projektiem atsevišķi. Sistēma vienmēr vispirms izvēlas visaugstākās detalizācijas kārtulu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]