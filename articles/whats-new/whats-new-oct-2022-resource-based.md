---
title: 2022. gada oktobra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada oktobra laidienā scenārijiem, kuru pamatā ir resursi/krājumi.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806758"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. gada oktobra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.57.0.176
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.30.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Projektu plānošana un izsekošana | **Projekta operācijas ārējā plānošana**<br>Ārējais plānošanas režīms ļauj klientiem vietēji izveidot, atjaunināt un dzēst entītijas, kas ir saistītas ar darba sadalījuma struktūrām (WBS), izmantojot vietējos Dataverse API, bez pašreizējiem ierobežojumiem, ko ievieš Project tīmeklī. | [Ārējā plānošana](/dynamics365/project-operations/project-management/external-scheduling) |
| Izvietošana un konfigurācija | <p>**Atļauja klientiem izvēlēties izvietošanas veidu**<br>Produkta vadīti Project Operations atjauninājumi (PDU) tiek izmantoti, lai automātiski instalētu Project Operations duālās rakstīšanas risinājumu, kad vidē ir instalēti divkodolu un orķestrācijas risinājumi.</p><p>Šis līdzeklis ievieš jaunu **risinājuma jaunināšanas uzvedības** parametru projekta parametros. Ja šis parametrs ir iestatīts tikai **uz Lite**, PUD vairs automātiski neinstalēs Project Operations dual-write risinājumu, pat ja vidē ir instalēti divkodolu un orķestrācijas risinājumi. Šāda rīcība dos labumu klientiem, kuri plāno izmantot duālās rakstīšanas risinājumus, lai integrētu pārdošanas pasūtījumus finanšu un operāciju programmās, bet vēlas izmantot Project Operations Lite režīmā (tas ir, bez integrācijas finanšu un operāciju programmās).</p> | |
| Cenu noteikšana un norēķini | <p>**Valūtas konvertēšana izdevumu neapmaksātai pārdošanas transakcijai integrētajās vidēs**<br>Klientiem, kuri izmanto Project Operations, kas integrētas ar Finance and Operations programmām (tas ir, resursu / neuzkrāto izvietošanas tipu), valūtas kursi parasti tiek apgūti Finance and Operations programmās. Tomēr, ja izdevumu kategorijas cena ir jānosaka, izmantojot cenas aprēķināšanas metodi "izmaksās" vai "uzcenojums virs izmaksām", kad debitoram tiek izrakstīts rēķins, valūtas kurss, kas tiek izmantots, lai aprēķinātu pārdošanas apjomu, izmanto valūtas Dataverse maiņas kursus, nevis valūtas maiņas kursus no finance and operations programmām.</p><p>Šī funkcija ievieš jaunu **valūtas konvertēšanas uzvedības** parametru projekta parametros. Ja šis parametrs ir iestatīts uz **Paplašināts ar atkāpšanos**, neapmaksātās pārdošanas summas izdevumu transakcijās tiek aprēķinātas, izmantojot valūtas maiņas kursus no finance and operations programmām.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2316317 | Sistēma ļauj izveidot rēķinus, kuriem nav apmaksājamu transakciju. |
| Cenu noteikšana un norēķini | 2737300 | Pārbaudiet **lauka Klients** pieejamību, pirms tiek piekļūts veidlapai. |
| Cenu noteikšana un norēķini | 2744948 | Pievienojiet nulles pārbaudi norēķinu metodei. |
| Cenu noteikšana un norēķini | 2763515 | Nulles atsauces kļūdas apstrāde, ja trūkst rēķina pārdošanas līguma. |
| Cenu noteikšana un norēķini | 2844301 | Partijas rēķina izveide neizdodas kļūdas dēļ. |
| Cenu noteikšana un norēķini | 2845869 | Nepareiza organizācijas pakalpojuma glabāšana. |
| Cenu noteikšana un norēķini | 2853729 | Loma un Cena tiek atjaunināta, kad tiek mainīts norēķinu veids. |
| Cenu noteikšana un norēķini | 2940350 | Ja faktiskās cenas ir noteiktas, automātiski jāievada tikai aktīvie cenrāži. |
| Izvietošana un konfigurācija | 3001206 | Entītija msdyn\_ replaylogheader neļauj veikt klientu organizāciju jaunināšanu. |
| Iespēju pārvaldība | 2755582 | Nulles atsauces izņēmumu rokturis dalīto norēķinu kārtulu palīgā. |
| Iespēju pārvaldība | 2761477 | Ja tiek izmantoti dalīti norēķini, dzēšot atskaites punktu (galveni), tiek atstāti nezināmu atskaites punktu skaita atskaites punkti. |
| Iespēju pārvaldība | 2767595 | Kad materiāla lietojuma ieraksts tiek atvērts galvenajā veidlapā, ieraksta rezervējamais resurss tiek mainīts uz lietotāju, kurš pašlaik ir pierakstījies. |
| Projektu plānošana un izsekošana | 2790384 | Pending OperationSet taimauts ir pārāk īss. |
| Projektu plānošana un izsekošana | 2957840 | Uzdevumus nevar saglabāt, un kolonnas nevar pievienot **lapai Uzdevumi** integrētajās projekta operācijās. |
| Resursu pārvaldība | 2751560 | Nekonsekventas vēlamās organizācijas vienības resursu prasībās. |
| Apakšlīgumu slēgšana | 2853245 | Atbilstība kreditora rēķina rindas faktiskajiem datiem neatjaunina verifikācijas statusu, ja līguma rinda jau ir saistīta ar kreditora rēķina rindu. |
| Apakšlīgumu slēgšana | 2907231 | Kreditoru rēķinu procesa posmā nevar virzīties uz priekšu. |
| Laiks un izdevumi | 2867363 | Ieraksti neizkrīt no skata Prombūtne/Brīvdienas apstiprināšanai, kad tie ir novietoti rindā apstiprināšanai. |
| Laiks un izdevumi | 2894405 | TESA: neizmantotais POC direktorijs izraisa atbilstības problēmas. |

### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
