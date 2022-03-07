---
title: Jaunumi vai izmaiņas 2021. gada martā — Project Operations krājumu/ražošanas scenārijiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada marta Project Operations laidienam, kas paredzēts krājumu/ražošanas scenārijiem.
author: andchoi
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: d1a4658c8eec23f6816b58de42d785d769050b07
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997025"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>Jaunumi vai izmaiņas 2021. gada martā — Project Operations krājumu/ražošanas scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.17

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā
Šajā laidienā ir ietverti tālāk minētie līdzekļi.

  - [Projekta rēķinu priekšlikumu veiktspēja](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals                        | Atsauces numurs | Kvalitātes atjauninājums                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektu pārvaldība un uzskaite | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | Pēc krājumu pārrēķināšanas netiek atjauninātas negatīvās grāmatotās projektu transakcijas.                                                                                                                      |
| Projektu pārvaldība un uzskaite | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | Ja līdzekļu avotam nav piešķirta transakcija vai rēķins, šo līdzekļu avotu var dzēst.                                                                                                           |
| Projektu pārvaldība un uzskaite | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | Faktiskajās aprēķinu transakcijās netiek rādītas izmaksu un preču transakcijas no iepriekšējā perioda.                                                                                                       |
| Projektu pārvaldība un uzskaite | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | Projekta vienumu prasību specifikācijai neatbilst virsgrāmatas apraksta vērtība.                                                                                                              |
| Projektu pārvaldība un uzskaite | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | Kad projektam tiek grāmatoti žurnāli, finanšu dimensijas neietver darbinieku un vienību kuponā.                                                                               |
| Projektu pārvaldība un uzskaite | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | Projekta rēķina kopsummā atjauninot rindas neto summu, pārdošanas summa tiek aizpildīta ar pielāgoto summu grāmatotajā transakcijā.                                                                               |
| Projektu pārvaldība un uzskaite | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | Rēķinā netiek atlasīta projekta ID atsauce, kad tiek pārskatītas piegādātāja rēķina rindas lapā **Piegādātāju rēķinu apmaksa**.                                                                                                   |
| Projektu pārvaldība un uzskaite | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Lapā **Kontā** nav pareiza līguma summa fiksētas cenas projektam ar vairākiem līdzekļu avotiem.                                                                                                  |
| Projektu pārvaldība un uzskaite | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | Fiksētas cenas projektam uzkrātās izmaksas netiek pielāgotas pat pēc tam, kad ir tiek grāmatoti ierobežojumi.                                                                                                                                |
| Projektu pārvaldība un uzskaite | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | Kredīta statuss netiek atjaunināts, kad projekta pārdošanas pasūtījumam tiek izrakstīts rēķins, izmantojot rēķina priekšlikumu.                                                                                                  |
| Projektu pārvaldība un uzskaite | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | Kad par pirkuma pasūtījumu ir izrakstīts rēķins un rēķinā ir iekļauta sagādes kategorija un prece, klients saņem nepareizu konta informāciju.                                                                                              |
| Projektu pārvaldība un uzskaite | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | Projektu rēķinu ierosinājumiem, kas tiek ģenerēti, izmantojot periodiskus pakešuzdevumus, ir transakciju dublikāti ar nulles summu.                                                                                                  |
| Projektu pārvaldība un uzskaite | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | Izpildot projekta peļņas un zaudējumu atskaites, noņemiet kļūdu ierobežojuma pārbaudi.                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | Izmaksas, kas tiek grāmatotas, izmantojot starpuzņēmumu atkārtotu maksas iekasēšanu, neparāda peļņas un zaudējumu ievadi, kad tiek izmantota funkcionalitāte **Grāmatot izmaksas** **projekta kodā Laiks un materiāls**.                                                         |
| Projektu pārvaldība un uzskaite | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Fiksētas cenas projektu grāmatotajām projektu transakcijām nedarbojas filtrs **Rēķina statuss**.                                                                                                   |
| Projektu pārvaldība un uzskaite | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | Laika grafika ieraksti tiek dublēti, jo ir dublikāti deleģētajiem ierakstiem.                                                                                                                                           |
| Projektu pārvaldība un uzskaite | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Atgriezeniskais aptuvenais ierobežojums nedarbojas lapā **Periodisks**.                                                                                                                                                 |
| Projektu pārvaldība un uzskaite | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | Modulī **Projekta pārvaldība un grāmatvedība** nevar atlasīt pareizos datus no opcijas **Pielāgot transakcijas**, pievienojot papildu diapazonu. Filtrs **Papildu** tiek ignorēts.                      |
| Projektu pārvaldība un uzskaite | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | Pēc uzdevuma reģistrēšanas nevar atiestatīt ražošanas pasūtījuma statusu.                                                                                                              |
| Projektu pārvaldība un uzskaite | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | Netiek rezervētas projekta preces, kurām ir automātiskās rezervēšanas un garantēšanas iespēja.                                                                                                                      |
| Projektu pārvaldība un uzskaite | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Līdzeklis **Grāmatvedības pielāgošana** rada problēmu ar virsgrāmatas kontiem, kuriem ir atlasīta opcija **Neatļaut manuālu ievadi**.                                                                     |
| Projektu pārvaldība un uzskaite | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | Projektu izrakstos laukā **Uzkrāt ieņēmumus — pārdošanas vērtība** nav jābūt nekādai vērtībai, ka aprēķins tiek noņemts.                                                                                 |
| Projektu pārvaldība un uzskaite | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | Projekta izmaksu un pārdošanas cenas ir nepareizas, projektam izmantojot lomu cenu noteikšanu.                                                                                                                        |
| Projektu pārvaldība un uzskaite | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | Project Operations honorāra korekcijas rēķins nedarbojas pēc daļējas honorāra korekcijas.                                                                                                                   |
| Projektu pārvaldība un uzskaite | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | Opcija **Noņemt saiti** ir jāiespējo tikai tad, ja atceļat starpuzņēmumu iegādes pasūtījumu.                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | NP — pārdošanas vērtību grāmatošanas funkcija, izrakstot starpuzņēmumu projektā rēķinu, atlasa neparedzētu uzņēmumu.                                                                                                                  |
| Projektu pārvaldība un uzskaite | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | Maksa no norēķinu kārtulas netiek pārrēķināta, kad rēķina priekšlikumā ir riondas, kas ir atlasītas kredītpiezīmēm.                                                                                            |
| Projektu pārvaldība un uzskaite | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | Lapā Schedule of Expenditures of Federal Awards Inquiry tiek parādītas kvīšu summas, kad projekta rēķina priekšlikums netiek palaists izdevumu transakcijai.                                               |
| Projektu pārvaldība un uzskaite | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | WIP izmaksas nav pareizas projekta izrakstā par pakalpojuma vienumu, kam ir projektu grupa **Bilance**.                                                                                               |
| Projektu pārvaldība un uzskaite | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | Ar projektu saistītajā brīva teksta rēķinā nevar veikt labojumus.                                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | Kad projekta transakcija tiek pielāgota nulles pārdošanas cenai, tiek izveidota jauna pielāgota transakcija ar rēķina statusu **Bez maksas**.                                                               |
| Projektu pārvaldība un uzskaite | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | Grāmatojot projekta korekciju, rodas problēma, ja tiek pielāgotas vairākas rindas vienlaikus.                                                                                                                               |
| Projektu pārvaldība un uzskaite | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | Ja produkta izmaksas un nepieciešamo preču daudzums mainās pēc iepakojuma specifikācijas grāmatošanas, korekcija tiek grāmatota ar nepareizu izmaksu summu.                                                                   |
| Projektu pārvaldība un uzskaite | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | Finanšu dimensijas tiešās piegādes pasūtījumam ir nepareizas un ir aizstātas ar pārdošanas pasūtījuma finanšu dimensijām.                                                              |
| Projektu pārvaldība un uzskaite | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | Negatīva daudzuma projekta žurnāla rinda neatjaunina prognozi, ja prognozes daudzums ir nulle.                                                                                        |
| Projektu pārvaldība un uzskaite | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | Mēģina importēt preču prasības, izmantojot Microsoft Excel rezultātus saņemšanas datuma kļūdā.                                                                                                                                                    |
| Projektu pārvaldība un uzskaite | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | Kad rēķins ir iegrāmatots, projekta vienuma transakcijas atsauce uz piegādātāja rēķina transakciju netiek atjaunināta.                                                                                               |
| Projektu pārvaldība un uzskaite | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Grāmatojot projekta rēķina priekšlikumu, var rasties šāda kļūda: “Ja tiek pievienots ieturētais avansa rēķins, transakcija netiek līdzsvarota pārskata valūtā.”                                                                    |
| Projektu pārvaldība un uzskaite | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | Ja izmantojat projekta izkārtojumu, projekta ID un projekta nosaukums netiek aizpildīti atskaitē **Piegādātāja maksājumu saglabāšana**.                                                                                              |
| Projektu pārvaldība un uzskaite | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | Kad projekts tiek izveidots, izmantojot datu entītiju, virsgrāmatas grāmatošanas secības prioritāte ir nepareiza.                                                                                                                      |
| Projektu pārvaldība un uzskaite | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | Izmaksu summa ir nepareiza grāmatotajām projekta transakcijām, kas tiek ģenerētas, pamatojoties uz pirkuma pasūtījumu ar pārdevēja paturēšanu. Tā rezultātā projekta izrakstos un izmaksu vadībā fiksētas cenas projektiem tiek ģenerētas nepareizas vērtības. |
| Projektu pārvaldība un uzskaite | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | Atjauninot virsrakstu, projekta pārdošanas piedāvājums nepareizi atjaunina vienības cenu.                                                                                                                    |
| Projektu pārvaldība un uzskaite | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Strādājot ar honorāriem programmā Project Operations, līguma noklusējuma projekta maiņa pēc tam, kad ir izrakstīti rēķini par priekšmaksājumiem, rada problēmu ar ienākošajiem atskaitījumiem.                                                                        |
| Projektu pārvaldība un uzskaite | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | Ir mainīta piegādātāju rēķinu datuma un projekta pārdošanas cenu atjaunināšana.                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | Problēmas rodas, pielāgojot starpuzņēmumu transakcijas ar atšķirīgiem valūtas kursiem.                                                                                                                |
| Projektu pārvaldība un uzskaite | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | Fiksētās izmaksas ar vienību prasību un pirkuma pasūtījumu ir nepareizas pasūtījuma rēķina procesā ar daļēju produktu saņemšanu un daļēju rēķinu izrakstīšanu.                                                |
| Projektu pārvaldība un uzskaite | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | Rodas nepareizas vērtības, ja aprēķins tiek mainīts ar valūtas kursu.                                                                                                                                             |
| Projektu pārvaldība un uzskaite | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | Darbs stundās tiek automātiski dzēsts darba sadalījuma struktūras veidnē uzdevuma līmenī.                                                                                                                         |
| Projektu pārvaldība un uzskaite | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | Atjauninot piedāvājuma statusu uz **Zaudēts**, visi piedāvājumi, kuru statuss ir **Izveidots** vai **Nosūtīts**, tiek atjaunināti uz **Zaudēts**.                 |
| Projektu pārvaldība un uzskaite | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | Ja piegādes datums ir nākotnē, pārdošanas rēķins nav redzams rēķina priekšlikumā.                                                                                                                  |
| Projektu pārvaldība un uzskaite | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | Entītijai **Projekta vienumu žurnāla rindas** ir mainīta biznesa loģika.                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | Uzkrātie ieņēmumi starpuzņēmumu klienta rēķinā neatbilst darba laika uzskaites tabulai un ārvalstu valūtas pārvērtēšanai.                                                                                 |
| Projektu pārvaldība un uzskaite | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | Iesniegtās izmaksas tiek aprēķinātas nepareizi pēc tam, kad projekta pirkuma pasūtījuma rindā tika izveidots atgādinājums par piegādi, izmantojot projekta iegādes pieprasījumu vai projektu.                    |
| Projektu pārvaldība un uzskaite | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | Pielāgojot projektu, var rasties šāda kļūda: “Krājumu vienībās netiek atjaunināti finanšu dati.”                                                                                                             |
| Projektu pārvaldība un uzskaite | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Programmā Project Operations noņemot projektu no līguma, būtu jāatiestata līguma noklusējuma projekts.                                                                                       |
| Projektu pārvaldība un uzskaite | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | Piemērojot nodokļus, projekta izmaksu pārdošanas cena ir nepareiza.                                                                                                                                         |
| Projektu pārvaldība un uzskaite | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | Projektam tiek grāmatots nepareizs vajadzīgo preču daudzums, ja projekta pirkuma pasūtījuma rinda tiek atjaunināta ar papildu rēķiniem.                                                                                                 |
| Projektu pārvaldība un uzskaite | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Programmā Project Operations starpuzņēmumu rēķinā tiek rādītas nepareizas izdevumu rindas sarakstā **Pievienot rindu**.                                                                                                |
| Projektu pārvaldība un uzskaite | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | Lauks **Piegādātāja konts** ir tukšs lapā **Projekta grāmatotā transakcija**, kad transakcijas tiek grāmatotas, izmantojot rēķinu reģistru un rēķina apstiprinājumu.                                                                  |
| Projektu pārvaldība un uzskaite | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | Sākotnējais projekta datums netiek ņemts vērā labojumā, un rodas problēma, ja **Izmantot korekcijas datumu kā jaunu projekta datumu** tiek iestatīts uz **Nē**.                                                                     |
| Projektu pārvaldība un uzskaite | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | Pārdošanas cena vispārējā žurnālā un izdevumu žurnālā, kas saistīta ar projektu, tiek nepareizi aprēķināta, ja transakcijas valūta atšķiras no uzņēmuma valūtas.                                     |
| Projektu pārvaldība un uzskaite | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | Pārdošanas transakcijas netiek rādītas projekta pirkuma pasūtījuma rēķina daļējos rēķinos.                                                                                                                          |
| Projektu pārvaldība un uzskaite | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | Projekta grāmatveža un projekta vadītāja lomas nevar izveidot darba laika žurnālus ar apstiprinājuma grupas iestatījumu.                                                                                                         |
| Projektu pārvaldība un uzskaite | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Nevar grāmatot izmaksu atskaiti, kas importēta, izmantojot Microsoft Excel.                                                                                                                                                              |
| Projektu pārvaldība un uzskaite | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | Nevar izveidot darba laika uzskaites tabulas politiku, jo lauks **Ziņojums** nav aktīvs.                                                                                                                               |
| Projektu pārvaldība un uzskaite | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | Pastāv problēma, kad tiek atļauta piegādātāja transakciju atsaukšana starpuzņēmumu scenārijos. Tas attiecas gan uz piegādātāju rēķiniem, gan uz izmaksu atskaitēm.                                                                                 |
| Projektu pārvaldība un uzskaite | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | Sadalījumus apstiprinātās darba laika uzskaites tabulās nevar atiestatīt.                                                                                                                                                     |
| Projektu pārvaldība un uzskaite | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | Tiek parādītas nepareizas vērtības, kad tiek atsaukts aprēķins ar valūtas kursu darba laika un preču žurnāliem.                                                                                                                  |
| Projektu pārvaldība un uzskaite | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | Projekta korekcija nepareizi atjaunina pārdošanas apjomu ar netiešajām izmaksām.                                                                                                                              |
| Projektu pārvaldība un uzskaite | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | Grāmatojot darba laika žurnālu, rodas šāda kļūda: “Dimensijas vērtība nav norādīta.”                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | Projekta līgumā ar citu valūtu nav pareizi aprēķināta uzskaites valūta kuponā.                                                                                              |
| Projektu pārvaldība un uzskaite | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | Starpuzņēmumu darba laika uzskaites tabulas WIP grāmatošanai tiek izmantots nepareizs pārdošanas WIP konts.                                                                                                                                     |
| Projektu pārvaldība un uzskaite | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | Projekta piedāvājums nepareizi aprēķina cenas, kad tiek piemērota atlaide un tiek atjaunināta noliktava.                                                                                                       |
| Projektu pārvaldība un uzskaite | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | Veicot pārrēķinu pēc preču izmaksu korekcijas izmantošanas projekta transakcijā, tiek parādīts šāds kļūdas ziņojums: “Pārrēķins tiek apturēts kļūdas dēļ.”                                                               |
| Projektu pārvaldība un uzskaite | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | Kad ieņēmumu uzkrāšanas laikā transakcijas tiek pielāgotas no apmaksājamām uz neapmaksājamām, netiek izveidoti virsgrāmatas ieraksti.                                                                                              |
| Projektu pārvaldība un uzskaite | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | Kad ir ieslēgta projekta piegādātāja rēķina saglabāšanas funkcija **Iespējot izmaksu summas aprēķinu**, netiek izveidots **ProjTrans** ar apmaksu, kad ir saņemta apmaksa.                                             |
| Projektu pārvaldība un uzskaite | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | Lapā **Rēķina priekšlikuma izveide** ir vairākas problēmas.                                                                                                                                                     |
| Projektu pārvaldība un uzskaite | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations lapā **Pirkuma līgums** nav redzamas finanšu juridiskās entītijas, kas ir integrētas programmā Project Operations.                                                                                             |
| Projektu pārvaldība un uzskaite | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | Papildu žurnālus nevar grāmatot ar grāmatvedības datumu slēgtā periodā, pat ja ir ieslēgta opcija **Automātiski iestatīt grāmatvedības datumu nākamajam atvērtajam periodam**.                                                |
| Projektu pārvaldība un uzskaite | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse integrācijas kļūdas dēļ nevar pārvērst piedāvājumu, kas ir uzvarēts programmā Project Operations.                                                                                                                                       |
| Projektu pārvaldība un uzskaite | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Programmā Project Operations rodas kļūdas ziņojums, mēģinot saistīt līguma līniju ar projekta ID, jo tiek pārbaudīta līguma rindu un darījumu veidu pārklāšanās.                                                |
| Projektu pārvaldība un uzskaite | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** var iestatīt līdzekļu avota rēķina adresi no cita klienta.                                                                                                             |
| Projektu pārvaldība un uzskaite | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | Pēc atjauninājuma 10.0.15 standarta resursu uzmeklēšana lapās nav pieejama.                                                                                                                    |
| Projektu pārvaldība un uzskaite | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | Virsgrāmatas konts un grāmatošanas veids ir nepareizs galvenās virsgrāmatas kuponā un grāmatošanas veids ir nepareizs pirkuma pasūtījuma kvītī pakalpojuma bez krājumiem vienībai, ja projekta grupa ir iestatīta uz **Balance**.                                 |
| Projektu pārvaldība un uzskaite | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | Darbības numurs netiek rādīts neapstiprinātam piegādātāja rēķinam, kaut arī **Bloķēt pakārtotas darbības atlasi** ir iestatīta uz Nē.                                                                    |
| Projektu pārvaldība un uzskaite | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Programmā Project Operations veidojot grāmatotu rēķinu transakcijai, netiek atlasītas dimensijas.                                                                                                                   |
| Projektu pārvaldība un uzskaite | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | Projektu vadībā un uzskaitē starpuzņēmumu laika uzskaites tabulās nav precīzi atspoguļota pārskaitījuma cenas prioritāte.                                                                            |
| Projektu pārvaldība un uzskaite | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | Mantotā darba sadalījuma struktūras (WBS) klases metode, **ProjWBSUpdateController::updateOutlineNumbersAndPublishInPreOrder**, ir novecojusi.                                                                                                   |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi
Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates.md). Varat arī pieteikties LCS un skatīt plānotos reglamentējošos atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]