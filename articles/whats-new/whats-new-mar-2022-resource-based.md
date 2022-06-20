---
title: Jaunumi 2022. gada martā — Project Operations resursu/bez krājumu pamatotiem scenārijiem
description: Šajā rakstā sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2022. gada marta projekta operāciju laidienā resursu/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910915"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada martā — Project Operations resursu/bez krājumu pamatotiem scenārijiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.30.0.99
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.25

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Dienasnauda tagad tiek atbalstīta jaunajā un pārveidotajā mūsdienu izdevumu darbvietā. Uzņēmumi, kas izmanto dienasnaudu, var iespējot šo funkciju, lai lietotājiem būtu vienkāršs veids, kā iesniegt un saņemt atlīdzību par dienasnaudas izdevumiem. Plašāku informāciju skatiet [Per dienasnaudas izdevumos](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā sarakstā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas projekta operāciju 2022. gada marta laidienā.

| **Entītiju karte** | **Atjauninātā versija** | **Komentāri** |
| --- | --- | --- |
| Projekta operāciju integrācija projekta kreditora rēķina rindas eksporta entītija msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Kartējumi atjaunināti, lai līdzinātos ar kreditora rēķina rindas entītiju programmā Dataverse. <br>Neaktivizējiet kartēšanas versiju 1.0.0.4. Tas būs gatavs lietošanai kombinācijā ar Finance vides versiju 10.0.26 nākamajā ikmēneša atjauninājumā. |

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti dual-write problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Laiks un izdevumi | 2388011 | Lielapjoma apstiprināšanas laikā rādīt noraidījuma komentārus laika ierakstu iesniedzējiem. |
| Projektu plānošana un izsekošana | 2495294 | Detalizēta informācija par projektu nedrīkst būt rediģējama lapā Detalizēta informācija par **uzdevumu**. |
| Cenu noteikšana un norēķini | 2499605 | Līguma atskaites punkti, kas izveidoti no piedāvājuma atskaites punktiem, ir nepareizi atzīmēti kā tikai lasāmi. |
| Projektu plānošana un izsekošana | 2506050 | Operāciju kopa paliek gaidīšanas režīmā vienu stundu, ja nav izmaiņu, ko saglabāt. Pēc tam kopa tiek nepareizi atzīmēta kā **neveiksmīga**, bet tā ir jāaizpilda nekavējoties. |
| Cenu noteikšana un norēķini | 2507401 | Noklusējuma līguma vienības tiek nepareizi ievadītas projektos nepareizas kešatmiņas dēļ. |
| Cenu noteikšana un norēķini | 2541660 | **Pārdošanas pasūtījuma izveides validācijai** divrakstā jābūt tikai uz projektiem balstītiem pasūtījumiem. |
| Cenu noteikšana un norēķini | 2552745 | Nodoklis netiek sadalīts starp klientiem, kuri ir iestatījuši dalītās norēķinu kārtulas. |
| Cenu noteikšana un norēķini | 2558859 | Uzlaboti kļūdu ziņojumi, iestatot cenu dimensijas. |
| Cenu noteikšana un norēķini | 2558933 | **Importēšana no projekta aplēsēm** neizdodas, ja **MSDYN\_ projekts** tiek pievienots kā cenu dimensija. |
| Cenu noteikšana un norēķini | 2559101 | Projekta parametru dzēšana nav bloķēta un rada problēmas. |
|   Iespēju pārvaldība | 2570390 | Divrakstīšanas spraudnis liek konta tipam piedāvājumos, pasūtījumos un iespējās būt **Klientam**, pat ja šis konta tips nav pareizs. |
| Cenu noteikšana un norēķini | 2586097 | Sadalīto izmaksu faktiskās izmaksas netiek atsauktas, kad projekts tiek noņemts no projekta līguma rindas. |
| Cenu noteikšana un norēķini | 2589619 | Nodoklis par rakstīšanas materiālu tiek pavairots uz nemainīgiem pārdošanas faktiskajiem izdevumiem un rēķinu. |
|   Iespēju pārvaldība | 2594015 | Piedāvājumu nevar slēgt kā uzvarētu klientiem, kuriem ir **Net60** apmaksas nosacījumi. |
| Projektu plānošana un izsekošana | 2595841 | Programmā Project for the Web lietotāji saņem kļūdas ziņojumu par trūkstošo **msdyn\_ faktisko sākšanu**, kad viņi izveido jaunu resursu pieprasījumu. |
| Laiks un izdevumi | 2602511 | Laika **ierakstu laukā Noraidīts tiek rādīta** **sistēma**, nevis nosaukts lietotājs kā noraidītājs. |
| Laiks un izdevumi | 2602528 | Projekta apstiprinātājs var apstiprināt laiku projektiem, kuros tie nav norādīti kā apstiprinātāji. |
| Cenu noteikšana un norēķini | 2608550 | Labojuma rēķinu var apstiprināt pat tad, ja oriģinālā nav izmaiņu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu vadība un uzskaite Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Lauka Kategorijas ID **atļautajā garumā** pastāv neatbilstība starp finanšu un projekta operācijām. |
| Projektu pārvaldība un uzskaite | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fiksētas cenas projektus nevar izslēgt, ja **lauks Starpkonta rēķini** ir iestatīts uz **Peļņa un zaudējumi** un **tiek izmantots princips Pabeigts procents**. |
| Projektu pārvaldība un uzskaite | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nepareiza noklusējuma PVN grupa tiek ievadīta no projekta iestatījuma izdevumu rindās projektu operāciju integrācijas žurnālā. |
| Projektu pārvaldība un uzskaite | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Projekta rēķina priekšlikuma virsrakstu dimensijas nevar rediģēt integrētā izvietošanā ar projekta operācijām. |
| Projektu pārvaldība un uzskaite | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Starpuzņēmumu kreditoru rēķinus nedrīkst integrēt .Dataverse |
| Projektu pārvaldība un uzskaite | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Debitora bilances valūtā un pārskata valūtā ir neatbilstība. |
| Projektu pārvaldība un uzskaite | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projekta rēķinu var grāmatot pat tad, ja debitors ir aizturēts visiem rēķiniem. |
| Projektu pārvaldība un uzskaite | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Projektu **rēķinu priekšlikumos, kuriem ir skati Virsraksts** **un** Rindas, trūkst pogas Dzēst visas **rindas**. |
| Projektu pārvaldība un uzskaite | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Grāmatojot kreditora rēķinu, rodas šāda kļūda: "Rēķina uzskaites datumam jābūt tajā pašā grāmatvedības gadā, kurā atrodas saistītais iepirktais pasūtījums. Palaidiet pirkšanas pasūtījuma gada beigu procesu vai mainiet datumu uz pašreizējo grāmatvedības gadu." |
| Komandējumi un izdevumi | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Projekta fiksētās izmaksas netiek atbrīvotas pēc tam, kad ir atbrīvotas ceļojuma pieprasījuma piesaistītās izmaksas. |
| Komandējumi un izdevumi | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Iesniedzot izdevumu pārskatu, rodas šāda kļūda: "Steka izsekošana: uzņēmums nepastāv." |
| Komandējumi un izdevumi | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | **Noklusējuma projekta ID** netiek ievadīts izdevumu pārskatos, ja projektā ir atlasīts **parametrs Pieprasīt aktivitāti žurnālam**. |
| Komandējumi un izdevumi | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Poga **Grāmatot izdevumus** nedarbojas pareizi projekta operācijās resursu/neuzkrātiem scenārijiem. |
| Komandējumi un izdevumi | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Ir problēma ar **likmi par jūdzi** nobraukuma izdevumu pārskatā, kas ietver pasažierus. |
| Komandējumi un izdevumi | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Izdevumu nobraukuma rādītāji darbiniekiem netiek pareizi summēti, ja nobraukuma likmes līmeņu izdevumu kategorijā tiek izmantoti **divi dažādi transportlīdzekļu tipi**. |
| Komandējumi un izdevumi | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Ceļojuma pieprasījuma rindas lauka Projekts **uzmeklēšana** neatgriež pareizo projektu sarakstu. |
| Komandējumi un izdevumi | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Pārskatā redzamais** nobraukums parāda brīdinājumu par izdevumu pārskatiem. |
| Komandējumi un izdevumi | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Ieejas plūsmas optiskās rakstzīmju atpazīšanas (OCR) pakalpojums nedarbojas, jo pastāv problēma ar izdevumu OCR pakalpojuma URL. |
| Komandējumi un izdevumi | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ja ir aktivizēta **funkcija Iespēja ātri** uzskaitīt periodiskos izdevumus, summas izdevumu pārskatu itemizācijas rindās maina summas ikreiz, **kad tiek atvērta lapa Itemize**. |
| Komandējumi un izdevumi | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Izdevumu pārskatu nevar dzēst, ja pagaidu sarakstā ir vairāki apstiprinātāji. |

## <a name="removed-and-deprecated-features"></a>Noņemti un novecojuši līdzekļi

Rakstā Projekta [operācijas](removed-depreciated-features-project.md) noņemtie vai novecojušie līdzekļi apraksta līdzekļus, kas ir noņemti vai novecojuši programmai Dynamics 365 Project Operations.

- Noņemtais līdzeklis vairs nav pieejams produktā.
- Novecojis līdzeklis netiek aktīvi izstrādāts, un nākamajā atjauninājumā tas var tikt noņemts.

Paziņojums par nolietošanos tiks parādīts [projekta operāciju](removed-depreciated-features-project.md) rakstā Noņemtie vai novecojušie līdzekļi 12 mēnešus pirms jebkura līdzekļa noņemšanas no produkta.

Ja tiek pārtrauktas izmaiņas, kas ietekmē tikai kompilācijas laiku, bet ir bināras saderīgas ar smilškasti un ražošanas vidēm, nolietojuma laiks būs mazāks par 12 mēnešiem. Parasti šīs izmaiņas ir funkcionāli atjauninājumi, kas jāveic kompilatoram.
