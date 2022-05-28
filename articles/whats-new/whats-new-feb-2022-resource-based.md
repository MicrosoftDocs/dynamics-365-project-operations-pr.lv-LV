---
title: Jaunumi 2022. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2022. gada februāra projekta operāciju laidienā resursu/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600843"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.28.0.120
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.24

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

- Sākot ar šo laidienu, vienam projektam varat pievienot līdz 300 komandas dalībniekiem. Iepriekš komandas dalībnieku skaita ierobežojums bija 150. Plašāku informāciju skatiet [Project limits](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations divu rakstīšanas karšu atjauninājumi

Šajā sarakstā ir parādītas divu rakstīšanas kartes, kas ir modificētas vai pievienotas projekta operāciju 2022. gada februāra laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Projekta operāciju integrācijas projekta izdevumu eksporta entītija (msdyn\_ izdevumi) | 1.0.0.3 | Paplašināts projekta aktivitāšu sinhronizācijai uz Dataverse. |

Pašreizējo projektu operāciju divrakstā karšu sarakstu un versijas skatiet rakstā [Project Operations divu rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti duālās rakstīšanas problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulas kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2415109 | Noklusējuma vērtībai **laukā Operāciju apmaksas nosacījumi** jābūt projekta līguma debitora ierakstam un proformas rēķina ierakstam. |
| Cenu noteikšana un norēķini | 2497369 | Materiāla korekcijai jāatbilst datuma vērtībai **korekcijas** parametros. |
| Cenu noteikšana un norēķini | 2498697 | Uzlabota laika ieraksta atsaukšanas **drošības** konfigurācija. |
| Cenu noteikšana un norēķini | 2513824 | Uz resursiem balstītiem scenārijiem darbību kategorijas ID projekta operācijās nedrīkst pārsniegt 28 rakstzīmes. |
| Cenu noteikšana un norēķini | 2517455 | Nedrīkst **pieļaut, ka darbību Atsvaidzināt rēķina rindas darbības** vienam un tam pašam rēķinam tiek aktivizētas vairākas vienlaicīgas reizes. |
| Cenu noteikšana un norēķini | 2517465 | Deaktivizēt **rēķina rindas detalizēto informāciju** darbība ir bloķēta, jo tā netiek atbalstīta. |
| Cenu noteikšana un norēķini | 2556660 | Fiksēja datuma efektivitātes pārbaudi, kas tiek veikta cenrādī, kas ir pievienots projekta parametru ierakstam. |
|   Iespēju pārvaldība | 2369202 | Laboja biznesa loģiku, kas pārbauda, vai cenrāžus, kuru efektivitātes datumi pārklājas, var pievienot vienam un tam pašam projekta līgumam. |
|   Iespēju pārvaldība | 2385965 | Laboja darbību **lapas Projekta līgums** cilnē Klienti **,** atlasot **Saglabāt un aizvērt**. |
| Laiks un izdevumi | 2538503 | Pēc izdevumu pārskata iegrāmatošanas projekta uzdevumam jābūt pieejamam **entītijā** Projekts faktiskais. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu vadība un uzskaite Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Kreditora kredīta notu importēšanas laikā rodas kļūda. Kļūdas ziņojumā ir teikts: "Uzkrājumu summa nevar būt lielāka par atlikušo neto summu." |
| Projektu pārvaldība un uzskaite | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ja rēķina priekšlikumā ir iekļautas nulles summas maksas darbības, kas ir nemainīgas pārdošanas faktiskās, rēķinu izrakstīšana nevar notikt. |
| Projektu pārvaldība un uzskaite | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Grāmatotās izmaksas nav pareizas pēc pirkšanas cenas atjaunināšanas un **aktivizēšanas izmaiņu pārvaldības** aktivizēšanas.|
| Projektu pārvaldība un uzskaite | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fiksētas cenas projekta grāmatošanas novērtējums izmanto nepareizu valūtu un summu budžeta dokumentā pat tad, ja ir iespējota **opcija Iespējot projekta līguma valūtu budžeta aprēķina** līdzeklim. |
| Projektu pārvaldība un uzskaite | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extension** nevajadzētu veikt zvanu, lai iespējotu izmaiņu izsekošanu, nepieķerot izņēmumus entītijām, kurām ir konfigurācijas atslēgas, kas nav iespējotas. |
| Projektu pārvaldība un uzskaite | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Pakešuzdevums tiek fiksēts, grāmatojot vairākus papildu žurnālus un rodas kļūda. |
| Komandējumi un izdevumi | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Tā kā norēķinu jautājums ir saistīts ar naudas avansiem izdevumu pārskatos, nodokļa summa netiek segta kā daļa no naudas avansa. |
| Komandējumi un izdevumi | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | PVN informācija nav iekļauta **pārskatā Izdevumi - grāmatotās darbības**. |
| Komandējumi un izdevumi | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Ieņēmumu **minimuma** izdevumu politikas pārkāpums nepareizi parāda brīdinājumu par izdevumu pārskatiem. |
| Komandējumi un izdevumi | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projekta darbība neiekļauj neatgūstamu PVN kopējā pārdošanas summā, ja darbība ir nobraukuma izdevumu rezultāts. |
| Komandējumi un izdevumi | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ja detalizētajai rindai ir nodoklis, nevar mainīt specifikāciju rindas datumu, un rodas pirmdokumenta stāvokļa kļūda. |

## <a name="removed-and-deprecated-features"></a>Noņemti un novecojuši līdzekļi

Tēmā [Projekta operācijas](removed-depreciated-features-project.md) noņemtie vai novecojušie līdzekļi apraksta līdzekļus, kas ir noņemti Dynamics 365 Project Operations vai novecojuši programmai.

- Noņemtais līdzeklis vairs nav pieejams produktā.
- Novecojis līdzeklis netiek aktīvi izstrādāts, un nākamajā atjauninājumā tas var tikt noņemts.

Paziņojums par nolietošanos tiks parādīts tēmā [Projekta operācijas](removed-depreciated-features-project.md) noņemtie vai novecojušie līdzekļi 12 mēnešus pirms jebkura līdzekļa noņemšanas no produkta.

Ja tiek pārtrauktas izmaiņas, kas ietekmē tikai kompilācijas laiku, bet ir bināras saderīgas ar smilškasti un ražošanas vidēm, nolietojuma laiks būs mazāks par 12 mēnešiem. Parasti šīs izmaiņas ir funkcionāli atjauninājumi, kas jāveic kompilatoram.
