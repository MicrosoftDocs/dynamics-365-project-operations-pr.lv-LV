---
title: Jaunumi 2022. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2022. gada februāra laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932995"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.28.0.120
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.24.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

- Šajā laidienā vienam projektam var pievienot līdz pat 300 darba grupas dalībniekus. Iepriekš darba grupas dalībnieku skaita ierobežojums bija 150. Papildinformāciju skatiet rakstā [Projekta ierobežojumi](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations duālās rakstīšanas kartes atjauninājumi

Tālāk redzamajā sarakstā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada februāra laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Project Operations integrācijas projekta izdevumu eksporta entītija (msdyn\_expenses) | 1.0.0.3 | Paplašināts projekta darbību sinhronizācijai ar Dataverse. |

Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2415109 | Noklusējuma vērtībai laukā **Operāciju maksājumu nosacījumi** ir jābūt projekta līguma klienta ierakstam un pro formas rēķina ierakstam. |
| Cenu noteikšana un norēķini | 2497369 | Materiālu korekcijai ir jāatbilst datuma vērtībai parametros **Korekcija**. |
| Cenu noteikšana un norēķini | 2498697 | Uzlabota drošības konfigurācija opcijai **Laika ierakstu atsaukšana**. |
| Cenu noteikšana un norēķini | 2513824 | Resursos balstītiem scenārijiem transakciju kategorijas ID garums programmā Project Operations nedrīkst pārsniegt 28 rakstzīmes. |
| Cenu noteikšana un norēķini | 2517455 | Darbībai **Atsvaidzināt rēķina rindas transakcijas** nedrīkst ļauj tikt ierosinātai vairākas reizes vienlaicīgi vienam un tam pašam rēķinam. |
| Cenu noteikšana un norēķini | 2517465 | Darbība **Deaktivizēt rēķina rindas informāciju** tiek bloķēta, jo tā netiek atbalstīta. |
| Cenu noteikšana un norēķini | 2556660 | Labota datuma spēkā esamības pārbaude, kas tiek veikta cenrādim, kas pievienots projekta parametru ierakstam. |
|   Iespēju pārvaldība | 2369202 | Labota uzņēmējdarbības loģika, kas pārbauda, vai cenrāži, kam pārklājas spēkā stāšanās datumi, var tikt pievienoti vienam un tam pašam projekta līgumam. |
|   Iespēju pārvaldība | 2385965 | Labota uzvedība cilnē **Klienti** lapā **Projekta līgums**, atlasot opciju **Saglabāt un aizvērt**. |
| Laiks un izdevumi | 2538503 | Projekta uzdevumam ir jābūt pieejamam entītijā **Projekta faktiskie dati** pēc izdevumu pārskata grāmatošanas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu pārvaldība un uzskaite programmā Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Piegādātāja kredīta notu importēšanas laikā rodas kļūda. Kļūdas ziņojumā ir noteikts, ka “Paturētā summa nevar būt lielāka par atlikušo neto summu”. |
| Projektu pārvaldība un uzskaite | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ja rēķina priekšlikumā tiek iekļautas transakcijas ar nulles summas maksu, kas ir rēķinā neiekļautas faktiskās pārdošanas, rēķinu nevar izrakstīt. |
| Projektu pārvaldība un uzskaite | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Grāmatotās izmaksas nav pareizas pēc tam, kad ir atjaunināta pirkuma cena un iespējota opcija **Aktivizēt izmaiņu pārvaldību**.|
| Projektu pārvaldība un uzskaite | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fiksētas cenas projekta grāmatošanas aprēķinos tiek izmantota nepareizā valūta un summa aprēķinu dokumentā, pat ja ir iespējots līdzeklis **Iespējot projekta līguma valūtu novērtējuma aprēķinam**. |
| Projektu pārvaldība un uzskaite | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** paplašinājums nedrīkst ierosināt izmaiņu izsekošanas iespējošanu, neiztverot izņēmumus entītijām, kurām ir neiespējotas konfigurācijas atslēgas. |
| Projektu pārvaldība un uzskaite | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Pakešuzdevums ir fiksēts, kad tiek grāmatoti vairāki detalizēti žurnāli un rodas kļūda. |
| Komandējumi un izdevumi | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Tā kā rodas segšanas problēma, kas ir saistīta ar naudas avansiem izdevumu pārskatos, nodokļu summa netiek segta kā daļa no naudas avansa. |
| Komandējumi un izdevumi | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informācija par pārdošanas nodokļiem nav iekļauta pārskatā **Izdevumi — grāmatotās transakcijas**. |
| Komandējumi un izdevumi | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Izdevumu politikas pārkāpums **Nepieciešami čeki** nepareizi rāda brīdinājumu izdevumu pārskatos. |
| Komandējumi un izdevumi | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projekta transakcijā nav iekļauts neatgūstams pārdošanas nodoklis kopējā pārdošanas summā, kad transakcija ir izveidota nobraukuma izdevumiem. |
| Komandējumi un izdevumi | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ja detalizētā rindā ir nodoklis, detalizētās rindas datumu nevar mainīt, un rodas avota dokumenta statusa kļūda. |

## <a name="removed-and-deprecated-features"></a>Noņemti un novecojuši līdzekļi

Rakstā [Noņemtie vai novecojuši līdzekļi programmā Project Operations](removed-depreciated-features-project.md) ir aprakstīti līdzekļi, kas ir noņemti vai novecojuši programmā Dynamics 365 Project Operations.

- Noņemtais līdzeklis vairs nav pieejams produktā.
- Novecojis līdzeklis nav aktīvā izstrādē, un to var noņemt turpmākā atjauninājumā.

Paziņojums par līdzekļu novecošanu tiks publicēts rakstā [Noņemtie vai novecojuši līdzekļi programmā Project Operations](removed-depreciated-features-project.md) 12 mēnešus pirms jebkādu līdzekļu noņemšanas no produkta.

Svarīgām izmaiņām, kas ietekmē tikai kompilēšanas laiku, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, novecošanas laiks būs īsāks par 12 mēnešiem. Parasti tās ir funkcionālas izmaiņas, kas jāveic kompilatoram.
