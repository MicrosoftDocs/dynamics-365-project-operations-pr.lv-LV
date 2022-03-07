---
title: Jaunumi vai izmaiņas 2021. gada maijā Project Operations krājumos/ražošanā balstītiem scenārijiem
description: Šajā tēmā ir sniegta informācija par 2021. gada maijā pieejamajiem kvalitātes atjauninājumiem Project Operations krājumos/ražošanā balstītiem scenārijiem.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: c4f58842c33ec5f45a6cd9ea4bd0e73b0aa693b7cecf63bfa8889a5671840d7b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991135"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>Jaunumi vai izmaiņas 2021. gada maijā Project Operations krājumos/ražošanā balstītiem scenārijiem

**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.19
 
### <a name="quality-updates"></a>Kvalitātes atjauninājumi
                                                                                                                                                                                  
| Līdzekļu apgabals                      | Atsauces numurs| Kvalitātes atjauninājums                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektu pārvaldība un uzskaite | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | Importēšana neizdodas, ja projekta vienumu žurnāla rindām ir izslēgtas entītiju validācijas.                                                                                                                                                   |
| Projektu pārvaldība un uzskaite | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | NP kontu pārskatā ir ar uzmeklēšanu **GeneralSerumsEntry** saistīta veiktspējas problēma.                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | NP projektā trūkst finanšu dimensiju.                                                                                                                                                                                                    |
| Projektu pārvaldība un uzskaite | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | Rēķina priekšlikuma publicēšana neizdodas, jo **ProjBudgetReductionHistory** ir piešķirts nepareizs **ProjBudgetAllocationLineIdSales**.                                                                                                                           |
| Projektu pārvaldība un uzskaite | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | Pēc XML faila importēšanas Vispārīgais žurnāls parāda nepareizus dokumentu numurus.                                                                                                                                                              |
| Projektu pārvaldība un uzskaite | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | Darba sadalījuma struktūras veidnē rodas kļūda.                                                                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Ja **Formu piezīmes** un **Formu iestatīšana** ir integrētas Project Operations, tās nav redzamas projektu pārvaldības iestatījumos sadaļā Finanšu juridiskās personas.                                                                                                             |
| Projektu pārvaldība un uzskaite | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | Starpuzņēmumu pārdošanas pasūtījumu atcelšana neizdodas, uzrādot šādu kļūdu: "Nevar rediģēt ierakstu pirkuma pasūtījuma rindās (PurchLine). Atjaunināšanas konflikts radās cita lietotāja procesa dēļ, dzēšot ierakstu vai mainot vienu vai vairākus ieraksta laukus." |
| Projektu pārvaldība un uzskaite | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | Projekta transakcijas korekcija rada nepareizu projekta izmaksu finanšu dimensiju.                                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | Kreditora rēķinam ir papildu uzvedne, kad tiek apstrādāts ar projektu saistīts pirkuma pasūtījums.                                                                                                                                                 |
| Projektu pārvaldība un uzskaite | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | Darba laika uzskaites tabulas rindas nevar apstiprināt, un rodas šāda kļūda: "Darbplūsmas aktivizēšanas nosacījums nav derīgs. Ziņojiet par šo problēmu sistēmas administratoram."                                                                          |
| Projektu pārvaldība un uzskaite | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | Ja tiek parādīts kļūdas ziņojums: "Nevar mainīt projekta līgumu, jo saistītajam projektam XXXXXX ir transakcija," līgumu joprojām var mainīt projekta līmenī.                                                                           |
| Projektu pārvaldība un uzskaite | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | Ja tiek parādīts kļūdas ziņojums: "Par šo daudzumu nevar izrakstīt rēķinu, jo krājumu transakcijas ar statusu Atskaitīts nav pietiekamas," pirkuma pasūtījuma rēķinu nevar publicēt pēc krājumu pārrēķināšanas.                             |
| Projektu pārvaldība un uzskaite | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | Ja ir iespējota resursu pieprasījuma darbplūsma, mēģinot atvērt lapas ar projekta resursu pieejamības vadīklu, rodas veiktspējas problēmas.                                                                                                               |
| Projektu pārvaldība un uzskaite | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | Pēc rēķina kārtulas pievienošanas, lai projektu līgumā norādītu citu projektu, rēķina statuss tiek mainīts uz **Rēķinā neiekļaujams**.                                                                                                                                |
| Projektu pārvaldība un uzskaite | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | Rodas kļūda, ja projekta pirkuma pasūtījumā tiek noņemts priekšapmaksas rēķins un ir iespējots parametrs **Grāmatot priekšapmaksas izmaksas pret projektu**.                                                                                                        |
| Projektu pārvaldība un uzskaite | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | Grāmatojot projekta pirkuma pasūtījuma rēķinu, rodas kļūda, jo trūkst vienuma automātiskās atzīmēšanas.                                                                                                                            |
| Projektu pārvaldība un uzskaite | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Noklusējuma apraksts par PVN ir tukšs, ja grāmatošanas veids ir vienāds ar PVN projekta rēķina dokumentiem.                                                                                                                                           |
| Projektu pārvaldība un uzskaite | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | Projekta pirkuma pasūtījumā tiks parādīts kļūdas ziņojums, ja dzēsīsiet saistīto atcelto krājumu vajadzības pārdošanas pasūtījumu.                                                                                                                                 |
| Projektu pārvaldība un uzskaite | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | Ja projekta krājumu vajadzību pirkuma pasūtījumi tiek atzīmēti un atzīme tiek noņemta, tiek zaudētas atsauces.                                                                                                                                                               |
| Projektu pārvaldība un uzskaite | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | Pastāv problēma ar samazinātā daudzuma noklusējuma vērtību, drukājot projekta krājumu vajadzību izdošanas sarakstu.                                                                                                                                                 |
| Projektu pārvaldība un uzskaite | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | Aprēķinātā pārdošanas cena nav pareiza, ja ir pārāk liela piegāde.                                                                                                                                                                                 |
| Projektu pārvaldība un uzskaite | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | Tiek grāmatots nepareizs apgrūtinājums, ja rēķina priekšlikumā ieturējums tiek atcelts bez rēķina daudzuma.                                                                                                                                                |
| Projektu pārvaldība un uzskaite | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | Ģenerējot darba laika uzskaites tabulas periodu, pirmais periods tiek parādīts kā 53. nedēļa.                                                                                                                                                                         |
| Projektu pārvaldība un uzskaite | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Noklusējuma projekta veidiem integrācijas Dynamics 365 Project Service Automation parametros ir jābūt Laiks un Materiāli un Fiksēta cena.                                                                                                         |
| Projektu pārvaldība un uzskaite | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | Dzēšot rēķina priekšlikumu ar norēķinu noteikumiem, tiek ģenerēti grāmatojumi.                                                                                                                                                                              |
| Projektu pārvaldība un uzskaite | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | Nevar dzēst galīgo izmaksu novērtējumu dzēšanas apstrādē, izmantojot izpildes laika procentos metodi, jo sistēma neatpazīst ieņēmumus.                                                                                                                                      |
| Projektu pārvaldība un uzskaite | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | Grāmatojot projekta izmaksu novērtējumu, grāmatojuma izmaksu novērtējuma ieraksts netiek izveidots.                                                                                                                                                                            |
| Projektu pārvaldība un uzskaite | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | Galvenais konts neizlemta kreditora rēķinā nav atrasts starpuzņēmuma rēķina izrakstīšanas laikā.                                                                                                                                                               |
| Projektu pārvaldība un uzskaite | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | Ja līgumā ir iekļautas elementu prasības, nevar pievienot otru finansējuma avotu.                                                                                                                                                         |
| Projektu pārvaldība un uzskaite | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Izmantojot **Projekts** > **Budžets** > **Pārskatījumi** > **Jauns** > **Importēt**, sistēma izveido projekta budžeta pārskatījumus visiem projektiem.                                                                                                                         |
| Projektu pārvaldība un uzskaite | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  Pielāgojot transakciju dažādām transakcijām un uzskaites valūtām, grāmatojuma un virsgrāmatas ieraksti ir nepareizi.                                                                                                                                       |
| Projektu pārvaldība un uzskaite | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Fiksētās izmaksas ir pārmērīgas ar neatskaitāmo nodokļu summām.                                                                                                                                                                                   |
| Projektu pārvaldība un uzskaite | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Izveidojot grāmatojamu rēķinu transakcijai, netiek paņemtas nekādas dimensijas.                                                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | Izveidojot neizlemtu kreditora rēķinu, kas nav saistīts ar pirkuma pasūtījumu, tiek izsaukta metode **PurchTotals.purchNewTotalAmount()**, izraisot veiktspējas problēmu.                                                                                   |
| Projektu pārvaldība un uzskaite | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | Kolonnās **Patērētais budžets** un **Atlikušais budžets** tiek rādītas nepareizas projekta budžeta bilances summas.                                                                                                                                                |
| Projektu pārvaldība un uzskaite | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Transakcija tiek grāmatota divreiz, ja Dataverse ar Project Operations tiek izmantoti uz uzdevumiem balstīti norēķini.                                                                                                                                         |
| Projektu pārvaldība un uzskaite | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Izmantojot Project Operations, ieņēmumu atpazīšanas pabeigtība procentos ir nepareiza.                                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Ieņēmumu uzkrājums tiek dubultots, izmantojot neizlemtu kreditora rēķinu Project Operations integrētajā scenārijā.                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | Grāmatojot projekta darba laika uzskaites tabulu, tiek izveidoti transakciju dublikāti.                                                                                                                                                                        |
| Projektu pārvaldība un uzskaite | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | Rodas kļūda, grāmatojot krājumu patēriņa žurnālu attiecībā pret darba pasūtījumu.                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | Projekta ražošanas pasūtījumu nevar pabeigt, jo šādas kļūdas dēļ: "Kā objekta atsauce nav iestatīts objekta gadījums".                                                                                                                           |
| Projektu pārvaldība un uzskaite | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Integrācijas žurnālu nevar grāmatot, ja ieņēmumu profila noteikums ir iestatīts kā **Grupas iestatījumi**.                                                                                                                                                           |
| Projektu pārvaldība un uzskaite | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nevar grāmatot pirkuma rēķinu projekta pirkuma pasūtījumam, kurā ir rindas ar vairākām mērvienībām.                                                                                                                                             |
| Projektu pārvaldība un uzskaite | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Projekta noklusējuma finanšu dimensiju nevar atjaunināt, izmantojot datu entītiju **Projects V2**.                                                                                                                                                          |
| Projektu pārvaldība un uzskaite | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Projekta pārdošanas pasūtījumam nevar izveidot kredīta notu, ja nodokļu valūta atšķiras no uzņēmuma valūtas.                                                                                                                     |
| Projektu pārvaldība un uzskaite | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | Rodas problēma, ja tiek izveidots rēķina priekšlikums, kas ietver vairāk nekā 100 norēķinu kārtulas.                                                                                                                                                                  |
| Projektu pārvaldība un uzskaite | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Projekta aprēķina izveides pakešveida apstrādes pabeigšanai nepieciešams pārāk ilgs laiks.                                                                                                                                                                      |
| Projektu pārvaldība un uzskaite | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | Izpildot funkcionalitāti **Aizpildīt projekta resursus visos uzņēmumos**, rodas šāda kļūda: "Nederīgs objekta nosaukums ResRollupCalendar".                                                                                                                                   |
| Projektu pārvaldība un uzskaite | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Dzēšot līgumu, tiek dzēsta arī ar klientu saistītā adrese.                                                                                                                                                                    |
| Komandējumi un izdevumi                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Izdevumu atskaites apstiprinājuma darbplūsmas nosacījums nav pareizi novērtēts.                                                                                                                                                                           |
| Komandējumi un izdevumi                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Izdevumu atskaites politika nenovērtē projekta ID pareizi.                                                                                                                                                                                   |
| Komandējumi un izdevumi                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Darbība **Sadalīt pa personām** starpuzņēmuma izdevumu transakcijām nedarbojas pareizi.                                                                                                                                                                |
| Komandējumi un izdevumi                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Dažkārt izdevumu atskaites rindas pamatojumi tiek dzēsti, dzēšot komandējuma pieprasījumus. Tā notiek, ja izdevumu atskaites un komandējuma pieprasījuma RecId ir vienāds.                                                            |
| Komandējumi un izdevumi                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Rodas problēma ar izdevumu mobilo programmu, ja izdevumu atskaišu politika pieprasa lauku **Projekta ID**.                                                                                                                                                |
| Komandējumi un izdevumi                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Mēģinot rediģēt ar projektu saistītus starpuzņēmuma izdevumus, tiek parādīts šāds kļūdas ziņojums: "Kā objekta atsauce nav iestatīts objekta gadījums".                                                                           |
| Komandējumi un izdevumi                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Pēc izdevumu atskaites grāmatošanas bankas apakšgrāmatā tiek iekļauta nepareiza valūta un summa.                                                                                                                                                                |
| Komandējumi un izdevumi                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | Projekta fiksētās izmaksas netiek atbrīvotas pēc tam, kad tiek slēgts komandējuma pieprasījums ar fiksētām izmaksām.                                                                                                                                              |
| Komandējumi un izdevumi                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Ir veikti uzlabojumi attiecībā uz līdzekli Dzēst kredītkartes transakcijas.                                                                                                                                                                                           |
| Komandējumi un izdevumi                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Izdevumu atskaitē iekļautais PVN aprēķins netiek veikts konsekventi, ja juridiskajai personai ir norādīta atšķirīga atskaišu valūta.                                                                                                         |
| Komandējumi un izdevumi                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Veiktspēja tiek ietekmēta, pievienojot jaunas komandējuma skaidras naudas izmaksas.                                                                                                                                                                                         |
| Komandējumi un izdevumi                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Izdevumu politikas kārtula netiek aktivizēta izdevumu atskaitē.                                                                                                                                                                                            |
| Komandējumi un izdevumi                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Augšupielādējot jaunu koplietojamu kategoriju, izmantojot datu pārvaldības struktūru, tiek noņemtas visas apakškategorijas visām koplietotajām kategorijām.                                                                                                                         |
| Komandējumi un izdevumi                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Izveidojot izdevumu rindu un atlasot kategoriju, rodas šāda kļūda: "PVN grupas DOM un PVN grupas STD kombinācija nav derīga".                                                                  |
| Komandējumi un izdevumi                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Pastāv sinhronizācijas problēmas ar izdevumu mobilo programmu. 

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi
Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties Lifecycle Services (LCS) un skatīt plānotos regulēšanas atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]