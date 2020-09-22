---
title: Projektu līgumi
description: Šajā tēmā ir sniegti projektu līgumu piemēri, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī to, kā pārvaldīt līgumus un izrakstīt rēķinus projektu klientiem.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753516"
---
# <a name="project-contracts"></a>Projektu līgumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti projektu līgumu piemēri, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī to, kā pārvaldīt līgumus un izrakstīt rēķinus projektu klientiem.

Projekta līgumam izveidotā projekta tips nosaka metodi, kas tiek izmantota, lai izrakstītu rēķinus projekta klientiem. Var mainīt projekta līgumu un saistīto projektu, bet nevar mainīt projekta tipu. 

Izmantojot projekta līgumu, vienlaicīgi var izrakstīt rēķinu par vienu vai vairākiem projektiem. Projekta līgums arī palīdz garantēt konsekventu rēķinu izrakstīšanas procedūru katram apakšprojektam projekta struktūrā. 

Katram projektam, kam tiks izrakstīts rēķins, jābūt saistītam ar projekta līgumu. Projekta līguma iestatījumi attiecas uz visiem projektiem un apakšprojektiem, kas ir saistīti ar šo projekta līgumu. 

Projekta līgumā var norādīt vienu vai vairākus finansējuma avotus. Tāpēc varat sadalīt rēķinu starp vairākiem finansētājiem, iestatīt finansējuma ierobežojumus, lai finansējuma avoti netiktu izrakstīti lielāki par noteiktu summu, un konfigurēt finansēšanas kārtulas izdevumu segšanai.

## <a name="funding-for-project-contracts"></a>Projekta līgumu finansēšana
Dažos projekta līgumos ir norādīts, ka vairākas puses kopīgi atbild par projekta izmaksu finansēšanu. Lūk, daži piemēri:

-   Liels klients, kam ir vairākas nodaļas, pieprasa, lai projekta finansējums tiktu sadalīts pēc nodaļas.
-   Jūsu uzņēmums koplieto liela projekta izmaksas ar ārēju organizāciju.
-   Ceļu projektu kopīgi finansē divas pašvaldības.
-   Tilta projektu finansē valsts dotācija un privāta korporācija.

Programmā Dynamics 365 Finance varat sadalīt rēķinu par vienu transakciju vai veselu projektu, izmantojot vairākus klientus, dotācijas vai organizācijas. 

Projektos, kuriem ir vairāki finansētāji, visas puses, kas sniedz ieguldījumu avansā finansēta projekta finansēšanā, sauc par finansējuma avotiem. Pēc tam, kad klients, organizācija vai dotācija ir definēta kā finansējuma avots, to var piešķirt vienai vai vairākām finansēšanas kārtulām. Finansēšanas kārtulas satur kritērijus, kas nosaka, kā maksas tiek piešķirtas dažādiem projekta finansējuma avotiem. 

Tā kā uzkrātās preces, piemēram, tās, kas tiek iekļautas pirkuma pieprasījumos un pirkuma pasūtījumos, nevar sadalīt, izmaksu summu dalīšanas laikā nevar sadalīt vairāku finansējuma avotu starpā. Tāpēc finansējuma avota vērtība joprojām ir 0 (nulle), līdz tiek iegrāmatota krājumu izejas plūsma. Kad krājuma izejas plūsma ir iegrāmatota, izmaksu summa tiek sadalīta atbilstoši projekta sadalījuma kārtulām.

Tālāk ir norādītas dažas darbības, ko varat veikt, lai atvieglotu rēķinu sadalīšanu starp vairākiem finansējuma avotiem:

-   Norādiet, ka visas projektā ievadītās darbības izmanto tādu pašu pārdošanas valūtu, kāda ir projekta līgumam.
-   Iestatiet finansējuma ierobežojumus, lai finansējuma avotam netiktu izrakstīts rēķins, kas nav lielāks par noteiktu projekta summu.
-   Konfigurējiet finansējuma kārtulas un finansējuma ierobežojumus katram darba ņēmējam, precei, kategorijai, kategoriju grupai un transakciju veidam (vai visiem transakciju veidiem).
-   Atlasiet neobligātu sākumu un beigu datumu, lai definētu periodu, kurā ir derīga katra finansējuma kārtula.
-   Norādiet procentus, par kuriem atbild katrs finansējuma avots.
-   Norādiet finansējuma avotu, kas ir atbildīgs par starpību noapaļošanu, kuras izraisa finansējuma piešķiršanas aprēķini.
-   Iestatiet kārtulas, kas nosaka, kā ārējiem klientiem tiek izrakstīti rēķini par projekta izmaksām un kā tās tiek iekasētas no iekšējām organizācijām.
-   Ierakstiet transakcijas aizturētā finansējuma kontā, līdz var iegūt papildu finansējumu, vai līdz izlemjat šīs izmaksas segt iekšēji.

Lai noteiktu, kuru nodokļu grupu saistīt ar transakciju, projekts tiek meklēts nodokļu grupas piešķiršanai. Ja projekta līmenī nav veikts nodokļu grupas piešķīrums, tiek meklēts projekta līgums.

### <a name="example-multiple-funding-sources-simple"></a>Piemērs: Vairāki finansējuma avoti (vienkārši)

Tālāk sniegtajā tabulā ir sniegti scenāriji, kā pārvaldīt finansējuma sadali starp vairākiem finansējuma avotiem. Šie scenāriji ir balstīti šādos pieņēmumos:

-   Prioritārie iestatījumi tiek iedalīti līdzekļu piešķiršanā, pirms tiek piemēroti citi finansējuma kārtulas kritēriji.
-   Nav norādīts datumu diapazons, lai definētu periodu d, kurā ir derīga finansējuma kārtula.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenārijs</strong></td>
<td><strong>Finansējuma avots</strong></td>
<td><strong>Piešķīruma procenti</strong></td>
<td><strong>Piešķīruma prioritāte</strong></td>
</tr>
<tr class="even">
<td>Jūs vēlaties piešķirt izmaksas vienam finansējuma avotam, kamēr nav iztērēti tā līdzekļi, piešķirt izmaksas otram finansējuma avotam, kamēr tā līdzekļi nav izsmelti, un visbeidzot piešķirt atlikušās izmaksas trešajam finansējuma avotam.</td>
<td><ul>
<li>Finansējuma　avots　1</li>
<li>Finansējuma　avots　2</li>
<li>Finansējuma　avots　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Jūs vēlaties piešķirt 75 procentus no izmaksām vienam finansējuma avotam un 25% otram finansējuma avotam. Ja kāds no šiem finansējuma avotiem ir izsmelts, jūs vēlaties samaksāt atlikušās izmaksas no trešā finansējuma avota.</td>
<td><ul>
<li>Finansējuma　avots　1</li>
<li>Finansējuma　avots　2</li>
<li>Finansējuma　avots　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Jūs vēlaties piešķirt 75 procentus no izmaksām vienam finansējuma avotam un 25% otram finansējuma avotam. Ja kāds no šiem finansējuma avotiem ir izsmelts, jūs vēlaties sadalīt atlikušās izmaksas starp trešo finansējuma avotu un ceturto finansējuma avotu.</td>
<td><ul>
<li>Finansējuma　avots　1</li>
<li>Finansējuma　avots　2</li>
<li>Finansējuma　avots　3</li>
<li>Finansējuma　avots　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Jūs vēlaties piešķirt pirmos 25 procentus no izmaksām vienam finansējuma avotam un pārējo — otram finansējuma avotam.</td>
<td><ul>
<li>Finansējuma　avots　1</li>
<li>Finansējuma　avots　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Piemērs: Vairāki finansējuma avoti (sarežģīti)

Jums ir trīs finansējuma avoti, kurus vēlaties izmantot šādā secībā:

1.  Izmantot finansējuma avotu 2 un finansējuma avotu 3 vienlīdzīgi, līdz ir izsmelts finansējuma avots 2.
2.  Turpināt izmantot finansējuma avotu 3, līdz tas ir izsmelts.
3.  Pēc tam, kad ir izsmelts finansējuma avots 3, lietot finansējuma avotu 1.

Lai sasniegtu šo mērķi, jums ir jārīkojas šādi:

-   Iestatiet finansējuma avota 2 un finansējuma avota 3 finansējuma ierobežojumus uz to atbilstošajām summām.
-   Izveidojiet šādas finansējuma kārtulas:
    -   1. kārtula (1. prioritāte): piešķirt 50 procentus transakciju finansējuma avotam 2 un 50 procentus finansējuma avotam 3.
    -   2. kārtula (2. prioritāte): piešķirt 100 procentus transakciju finansējuma avotam 3.
    -   3. kārtula (3. prioritāte): piešķirt 100 procentus transakciju finansējuma avotam 1.

Šāds iestatījums darbojas, jo transakcijas tiek pārbaudītas iepretim kārtulām un ierobežojumiem, lai noteiktu, vai kāds no tiem ir piemērojams transakcijai. Ja transakcijai nav piemērojamas konkrētas kārtulas vai ierobežojumi, ir spēkā Visu transakciju kārtula. Visu transakciju kārtula atbilst visām transakcijām. 

Ja tiek atrasta kārtula, kura atbilst transakcijai, vispirms tiek piemērota šai kārtulai piešķirtie procenti, taču vienīgi pēc tam, kad atbilstības tiek pārbaudītas attiecībā pret jebkādiem iestatītiem ierobežojumiem. Ja ir sasniegts ierobežojums un ir izsmelti finansējuma avota līdzekļi, ar finansējuma ierobežojumu saistītā finansējuma kārtula netiek ņemta vērā un programma pārbauda nākamo spēkā esošo kārtulu. 

Dažos gadījumos saskaņā ar kārtulu var piešķirt tikai daļu no transakcijas. Tas var notikt tādēļ, ka, piešķirot transakciju, ir sasniegts ierobežojums. Šādā gadījumā atbilstoši šai kārtulai tiek piešķirta tikai konkrēta summa, piemēram, 50% katram finansējuma avotam. Šāda situācija ir 1. kārtulā, kura aprakstīta iepriekš šajā sadaļā. Atlikums tiek sadalīts atbilstoši secības nākamajām kārtulām. 

Tālāk sniegtajā tabulā šis scenārijs ir apskatīts sīkāk.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokuss</strong></td>
<td><strong>Detalizēta informācija</strong></td>
</tr>
<tr class="even">
<td>Finansēšanas kārtulas</td>
<td><ul>
<li>1. kārtula (1. prioritāte): visas transakcijas. Piešķirt finansējuma avotu 2 pie 50% un finansējuma avotu 3 pie 50%.</li>
<li>2. kārtula (2. prioritāte): visas transakcijas. Piešķirt finansējuma avotu 3 pie 100%.</li>
<li>3. kārtula (2. prioritāte): visas transakcijas. Piešķirt finansējuma avotu 1 pie 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansējuma ierobežojumi</td>
<td><ul>
<li>Finansējuma avota 1 ierobežojums = 10 000,00</li>
<li>Finansējuma avota 2 ierobežojums = 500,00</li>
<li>Finansējuma avota 3 ierobežojums = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcija 1</td>
<td><strong>Transakcijas summa:</strong> 100,00<strong>Finansējums: </strong> Transakcija tiek izmaksāta atbilstoši vienīgi 1. kārtulai, jo transakcija tiek pilnībā izmaksāta pēc 1. kārtulas piemērošanas. Transakciju finansē vienlīdzīgi starp finansēšanas avotu 2 un finansēšanas avotu 3.
<ul>
<li>Finansējuma avots 2: 50,00</li>
<li>Finansējuma avots 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcija 2</td>
<td><strong>Transakcijas summa:</strong> 5 000,00<strong>Finansējums:</strong> Transakcija tiek izmaksāta atbilstoši visām trim kārtulām. <strong>1. kārtula</strong>
<ul>
<li>Finansējuma avots 2: 450,00</li>
<li>Finansējuma avots 3: 450,00</li>
</ul>
<strong>2. kārtula</strong>
<ul>
<li>Finansējuma avots 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>3. kārtula</strong>
<ul>
<li>Finansējuma avots 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Katram finansējuma avotam sadalītie kopējie līdzekļi</td>
<td><ul>
<li>Finansējuma avots 1: 3.850,00</li>
<li>Finansējuma avots 2: 500,00</li>
<li>Finansējuma avots 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Norēķinu kārtulas
Ar klientu vienojoties par projekta līgumu, jūs definējat, kā un kad izrakstīsit klientam rēķinu par projektā ieguldīto darbu. Pēc projekta līguma un projekta iestatīšanas varat projektam iestatīt norēķinu kārtulas. Norēķinu kārtulas balstās projekta nosacījumos, kuri tiek konkretizēti projekta līgumā. Norēķinu kārtulas, kuras varat izveidot, ir atkarīgas no projekta līguma nosacījumiem un projekta veida, piemēram, laika un materiāla vai fiksētas maksas, kuru saistāt ar norēķinu kārtulu. Projekta līgumam var izveidot vairāk nekā vienu norēķinu kārtulu. Varat arī piešķirt norēķinu kārtulu vairākiem projektiem, kas ir saistīti ar to pašu projekta līgumu un kuriem ir līdzīgi norēķinu nosacījumi. 

Varat iestatīt šādus norēķinu kārtulu veidus:

-   **Piegādes vienība** — Izrakstiet klientam rēķinu pēc tam, kad izpildāt piegādes vienību. Piegādes vienības tiek definētas līgumā.
-   **Norise** — Izrakstiet klientam rēķinu, kad pabeidzat noteiktu projekta daļu. Varat iestatīt norēķinu kārtulu, lai tiktu aprēķināts izpildītā darba īpatsvars, vai varat manuāli aprēķināt izpildītā darba īpatsvaru un summu, par kuru klientam izrakstīt rēķinu.
-   **Atskaites punkts** — Izrakstiet klientam rēķinu par pilno projekta atskaites punkta summu, kad šis atskaites punkts ir sasniegts.
-   **Maksa** — Izrakstiet klientam rēķinu par saviem pakalpojumiem, plus pārvaldības maksu, kas parasti ir procents no pakalpojumu izmaksām.
-   **Laiks un materiāls** — Izrakstiet klientam rēķinu par projektam izlietotā laika un materiālu vērtību.

Visiem norēķinu kārtulu veidiem varat norādīt ieturējumu procentus, kas tiek atskaitīti no klienta rēķiniem, līdz projekts sasniedz noteiktu posmu. Maksājuma ieturējumu procenti ir norādīti projekta līgumā. Summu aprēķina, pamatojoties uz un atņemot no klienta rēķina rindu kopējās vērtības. 

Norēķinu kārtulām **Laiks un materiāls** un **Progress** varat piešķirt maksas kategorijas. Maksas kategorijas norāda uz transakcijām, kuras vajadzētu iekļaut klientu rēķinos. 

Kad esat gatavi klientam izrakstīt rēķinu, šī projekta rēķina summa tiek aprēķināta, balstoties norēķinu kārtulās un tiek ģenerēts projekta rēķina piedāvājums. 

Šajās sadaļās ir sniegti piemēri, kas parāda, kā iestatīt un pārvaldīt projekta norēķinu kārtulas.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta piegādāto vienību skaitā

Jūsu organizācija noslēdz līgumu, lai klienta darbiniekiem nodrošinātu kopumā piecus apmācību kursus, kas izmaksā 10 000 par vienu kursu. Pēc katra kursa jūs klientam izrakstāt rēķinu. 

Iestatot līguma norēķinu kārtulas, jūs izmantojat šādas vērtības:

-   Piegādes vienība ir viens mācību kurss.
-   Vienības cena ir 10 000 par vienu mācību kursu.
-   Kopējais vienību skaits ir pieci mācību kursi.

Kad ir izpildīts viens mācību kurss, varat izveidot rēķinu par 10 000 — par pirmo piegādāto vienību — un rēķinu nosūtīt klientam.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Piemērs: Izveidojiet norēķinu kārtulu, kura balstās konkrētos projekta izpildes procentos (manuāls aprēķins)

Jūsu organizācija — programmatūras konsultāciju uzņēmums — noslēdz ar klientu līgumu, lai izstrādātu daļu no klienta izstrādāta produkta. Jūsu organizācija piekrīt programmatūras kodu piegādāt sešu mēnešu laikā. Klients piekrīt par darbu jūsu organizācijai izmaksāt kopumā 100 000. Jūs izveidojat norēķinu kārtulu, lai klientam izrakstītu rēķinu, pamatojoties uz projektā izpildītā darba procentiem, kā norādīts līgumā.

-   Pirmā mēneša beigās jūs tiekaties ar klientu, lai noteiktu, kāda daļa darba ir izpildīta. Pēc tam, kad jūs un klients izskata projektu, jūs izlemjat, ka ir izpildīti 15 procenti darba.
-   Jūs izrakstāt rēķinu par 15 000 (15 procenti no 100 000) un to nosūtāt klientam.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Piemērs: Izveidojiet norēķinu kārtulu, kura balstās konkrētos projekta izpildes procentos (automātisks aprēķins)

Jūsu organizācija — programmatūras izstrādes uzņēmums — piekrīt klientam izstrādāt izmaksas uzskaites pakotni par 30 000. Klients piekrīt maksāt jūsu organizācijai, pamatojoties uz izpildītā darba daļu procentos. Saskaņā ar jūsu aplēsēm projekta izmaksas ir 20 000. Projekta līgumā ir norādītas tās darba kategorijas, kuras izmantojat norēķinu procesā. Jūs iestatāt norēķinu kārtulas, kuras automātiski aprēķina rēķina summas par katrai kategorijai izpildīto darba daļu. Jūs iestatāt budžetu katrai kategorijai:

-   **Izstrāde** – izmaksas ir 15 000 un ieņēmumi 20 000
-   **Instalēšana** – izmaksas ir 5 000 un ieņēmumi 10 000

Klientam izrakstot rēķinu pirmoreiz, rēķina summa tiek aprēķināta automātiski, pamatojoties uz šādu informāciju:

-   Pēc mēneša projekta darbinieks iesniedz projekta laika uzskaites tabulu. Darbinieka laika izmaksas ir 5000 par izstrādi un 1000 par instalēšanu. No izstrādes darba ir pabeigti 33 procenti (5000 faktiskās izmaksas / 15 000 budžeta izmaksas), bet no instalēšanas darba ir izpildīti 20 procenti (1000 faktiskās izmaksas / 5000 budžeta izmaksas).
-   Automātiski tiek aprēķināta rēķina summa 8667 apmērā (33 procenti no 20 000 + 20 procenti no 10 000).
-   Jūs izrakstāt rēķinu par 8667 un to nosūtāt klientam.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta noteiktos atskaites punktos

Jūsu organizācija — pārvaldības konsultāciju uzņēmums — piekrīt veikt tirgus izpēti klienta produktam, kuru klients plāno tirgot. Klients piekrīt izmantot jūsu pakalpojumus uz trim mēnešiem — sākot ar martu — un piekrīt jūsu organizācijai samaksāt 50 000. Projektam ir trīs atskaites punkti:

-   1. atskaites punkts: Patērētāju datu ievākšana — 31. marts.
-   2. atskaites punkts: Patērētāju datu analīze — 30. aprīlis
-   3. atskaites punkts: Produkta ilgtspējas priekšlikuma prezentācija — 31. maijs

Klients piekrīt samaksāt jūsu organizācijai 10 000 par pirmo atskaites punktu, 20 000 par otro atskaites punktu un 20 000 par trešo atskaites punktu. 

Izveidojot projekta līgumu, jūs piekrītat izrakstīt klientam rēķinu atbilstoši izpildītajam atskaites punktam. Norēķinu kārtula ietver šādas darbības:

-   Projekta atskaites punktu definēšana.
-   Klienta rēķinā izrakstāmās summas definēšana, kad ir izpildīts katrs atskaites punkts.

Kad 31. martā ir izpildīts pirmais atskaites punkts, jūs atzīmējat šo atskaites punktu kā izpildītu un pēc tam izrakstāt rēķinu par 10 000, un to nosūtat klientam. Atskaites punktam nav iespējams izrakstīt rēķinu, iekams nav atzīmēta atskaites punkta izpilde.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta pakalpojumos un pārvaldības maksā

Jūsu organizācija — pārvaldības konsultāciju uzņēmums — piekrīt veikt tirgus izpēti, lai novērtētu ilgtspēju produktam, kuru izstrādā jūsu klients — mazumtirdzniecības uzņēmums. Līguma noteikumos norādīts, ka jūs sniegsit savu trīs labāko pārvaldības konsultantu pakalpojumus, kuri veiks izpēti, pamatojoties uz laiku un materiāliem. Klients piekrīt maksāt 100 par stundu un 10 procentu pārvaldības maksu par projektam aprēķinātajām konsultāciju stundām. 

Iestatot projekta līgumu, izveidojiet norēķinu kārtulu, lai projektam aprēķinātajām konsultāciju stundām pieskaitītu 10 procentu pārvaldības maksu. 

Klientam izrakstot rēķinu, no klienta tiek iekasēta 10 procentu pārvaldības maksa un konsultāciju laika izmaksas. Piemēram, ja trīs konsultanti projektā kopumā nostrādāja 200 stundu, tiek izrakstīts rēķins par 22 000, pamatojoties uz šādiem aprēķiniem:

-   200 stundas ar likmi 100 par stundu = 20 000
-   10 procentu pārvaldības maksa = 2000
-   Kopējā rēķina summa = 22 000

Ja klientam maksas ir apliekamas ar nodokli un jūs projekta līgumā atlasāt pārdošanas nodokļu grupu, pārdošanas nodokļu grupa automātiski tiek ievadīta maksu norēķinu kārtulā.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Piemērs: Izveidojiet norēķinu kārtulu laika un materiālu vērtībai

Jūsu organizācija — programmatūras konsultāciju uzņēmums — piekrīt nodrošināt piecus tehniskos konsultantus, kas nākamos sešus mēnešus klientam strādās ar programmatūras izstrādes projektu. Klients piekrīt maksāt 150 par katru konsultāciju stundu plus biroja preču izmaksas. Katra mēneša beigās jūsu organizācija klientam nosūta rēķinu. 

Iestatot projekta līgumu, jūs piekrītat katru mēnesi izrakstīt klientam rēķinu par projekta laiku un materiāliem. Jūs izveidojat norēķinu kārtulu, kas ietver šādu informāciju:

-   Līguma periods ir seši mēneši.
-   Konsultāciju laiks tiek aprēķināts ar likmi 150 par stundu.
-   Biroja preces tiek izrakstītas pie izmaksām, bet projekta kopējās izmaksas nedrīkst pārsniegt 10 000.
-   Projekta laikā jūs katra kalendārā mēneša beigās izveidojat klienta rēķinu.

Pirmajā mēnesī projekta konsultanti fiksē kopumā 800 darba stundas. Projektā aprēķināto biroja preču izmaksas ir 2000. Tāpēc mēneša beigās tiek izrakstīts rēķins par 122 000, kas tiek aprēķināts kā 800 stundas ar likmi 150 par stundu, plus 2000 par biroja precēm.



