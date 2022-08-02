---
title: Jaunumi 2021. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada jūnija projekta operāciju laidienā uz resursiem/nepiegādātiem scenārijiem.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028255"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations programmas Dynamics 365 Dataverse vides versijā 4.11.0.156 vai 4.11.0.164.
- Projektu vadība un uzskaite finanšu un operāciju programmu vidēs versija 10.0.19.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Spēja dzēst [projekta rēķina priekšlikuma rindas scenāriju pielāgošanai](../invoicing/correct-project-invoice-proposals.md).
- Priekšmetisko izmaksu rindās tiek atainoti apakškategoriju nosaukumi izmaksu atskaitē [Jauna veida izdevumu atskaites–jauni līdzekļi](../expense/expense-reports-reimagined.md#new-features).
- Veidojot jaunas izmaksas, maksāšanas metode ir pieejama jaunajā izmaksu rūtī.
- Projektu plānošanas API vispārīga pieejamība. Šī jaunā funkcionalitāte ļauj klientiem programmiski veikt projekta uzdevumu, resursu piešķīrumu, uzdevumu atkarību un projekta darba grupas dalībnieku ierakstu izveides, atjaunināšanas un dzēšanas operācijas. Papildinformāciju skatiet sadaļā [Projektu plānošanas API izmantošana operāciju veikšanai un entītiju plānošanai](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. 

Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finanšu un operāciju programmu risinājuma versiju. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Aktivizējiet jaunu kartes versiju, atlasot **Tabulas karšu versijas**, atlasot jaunāko versiju un pēc tam saglabājot atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, sākot karti, izpildiet instrukcijas dubultās rakstīšanas problēmu novēršanas ceļveža sadaļā [Kartes trūkstošu tabulas kolonnu problēma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2281417 | Novērsta problēma saistībā ar automātiskās rēķinu izveides darbības kļūmi, izmantojot rēķinu grafiku. |
| Cenu noteikšana un norēķini | 2287835 | Uzlabota rēķinu apstiprināšanas veiktspēja. |
| Iespēju pārvaldība | 2222555 | Izmantojot **Importēt no projekta aprēķina**, materiālu aprēķinu iekļaujamība ir pareizi jāiekopē piedāvājuma rindas detalizētajā informācijā. |
| Iespēju pārvaldība | 2223427 | Darbībai **GenerateRetainersFromRetainerScheduleOptions** tagad ir atļauts veikt pielāgojumus. |
| Iespēju pārvaldība | 2277528 | Fiksētu norēķinu atskaites punktu vērtību aprēķins projekta līguma rindām ar vairākiem klientiem. |
| Projektu plānošana un izsekošana | 2226110 | Novērsta intermitējoša problēma ar funkciju **Ģenerēt prasību** režģī **Projekta darba grupa**. |
| Projektu plānošana un izsekošana | 2208109 | Lietotāji nevar izveidot projektu vienā valūtā ar saistītiem uzdevumiem citā valūtā. |
| Projektu plānošana un izsekošana | 2258228 | Ir atjaunināts to lauku saraksts, ko atļauts modificēt ar **Plānošanas** entītijām, izmantojot plānošanas API. |
| Projektu plānošana un izsekošana | 2293989 | **Projekta uzdevumu** režģī ir jānodod pareizā valoda un reģionālie iestatījumi. |
| Resursu pārvaldība | 2220493 | Uzlabota lietotāju pieredze **Uzdevumu** režģī, ātri atzīmējot resursa pieprasījumu kā pabeigtu. |
| Resursu pārvaldība | 2330496 | Novērsta **Plānošanas paneļa** ielādes problēma. (Kvalitātes atjauninājums ir pieejams versijā 4.11.0.164) |
| Laiks un izdevumi | 2194431 | Režģī **Laika ievade** nedēļas sākumam jābūt, kā tas ir iestatīts **Sistēmas iestatījumos**. |
| Laiks un izdevumi | 2277311 | Pēc vērtības dzēšanas **Laika ievades** režģa šūnā kursors paliek režģī. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu vadība un uzskaite Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formu piezīmes** un **Formu iestatījumi** nav redzami sadaļā **Projektu pārvaldības iestatījumi** sadaļā Finanšu juridiskās personas, kas tie ir integrēti Project Operations. |
| Projektu pārvaldība un uzskaite | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Noklusējuma apraksts par PVN ir tukšs, ja **Grāmatošanas veids** = **PVN** projekta rēķina dokumentiem. |
| Projektu pārvaldība un uzskaite | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dubultas transakcijas tiek grāmatotas, ja Dataverse ar Project Operations tiek izmantoti uz uzdevumiem balstīti norēķini. |
| Projektu pārvaldība un uzskaite | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Izmantojot Project Operations integrāciju, pabeigtība procentos ieņēmumu atpazīšanā ir nepareiza. |
| Projektu pārvaldība un uzskaite | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Ieņēmumu uzkrājums tiek dubultots neizlemtā kreditora rēķinā Project Operations integrētajā scenārijā. |
| Projektu pārvaldība un uzskaite | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Integrācijas žurnālu nevar grāmatot, ja ieņēmumu profila noteikums ir iestatīts kā **Grupa**. |
| Projektu pārvaldība un uzskaite | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nevar grāmatot pirkuma rēķinu projekta pirkuma pasūtījumiem, kuros ir rindas ar vairākām mērvienībām. |
| Projektu pārvaldība un uzskaite | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Noklusējuma finanšu dimensiju projektā nevar atjaunināt, izmantojot projektu datu entītiju **V2**. |
| Projektu pārvaldība un uzskaite | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Projekta aprēķina izveides pakešveida apstrādes pabeigšanai nepieciešams pārāk ilgs laiks. |
| Projektu pārvaldība un uzskaite | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Dzēšot līgumu, tiek dzēsta arī ar klientu saistītā adrese. |
| Komandējumi un izdevumi | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Izdevumu atskaites apstiprinājuma darbplūsmas nosacījums nav novērtēts pareizi. |
| Komandējumi un izdevumi | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Izdevumu atskaites politika nenovērtē projekta ID pareizi. |
| Komandējumi un izdevumi | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Darbība **Sadalīt pa personām starpuzņēmuma izdevumu transakcijām** nedarbojas pareizi. |
| Komandējumi un izdevumi | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Izdevumu atskaites rindu pamatojumi tiek netīšām dzēsti, dzēšot noteiktus komandējuma pieprasījumus. Tā notiek, ja izdevumu atskaites un komandējuma pieprasījuma RecId ir vienādi. |
| Komandējumi un izdevumi | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Rodas problēma izdevumu mobilajā programmā, ja izdevumu atskaišu politikā tiek pieprasīts lauks **Projekta ID**. |
| Komandējumi un izdevumi | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Starpuzņēmuma izmaksas, kas saistītas ar projektu, nevar rediģēt. Tā vietā tiek parādīts šāds kļūdas ziņojums: "Kā objekta atsauce nav iestatīts objekta gadījums". |
| Komandējumi un izdevumi | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Pēc izdevumu atskaites grāmatošanas bankas apakšgrāmatā tiek iekļauta nepareiza valūta un summa. |
| Komandējumi un izdevumi | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Ir veikti uzlabojumi attiecībā uz līdzekli *Dzēst kredītkartes transakcijas*.  |
| Komandējumi un izdevumi | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Izmaksas pārskatā iekļautais PVN netiek konsekventi aprēķināts, ja juridiskai personai ir norādīta atšķirīga pārskata valūta. |
| Komandējumi un izdevumi | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Veiktspēja tiek ietekmēta, pievienojot jaunas komandējuma skaidras naudas izmaksas. |
| Komandējumi un izdevumi | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Izmaksu politikas kārtulas netiek aktivizētas izdevumu atskaitē. |
| Komandējumi un izdevumi | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Augšupielādējot jaunu koplietojamu kategoriju, izmantojot datu pārvaldības struktūru, tiek noņemtas visas apakškategorijas visām koplietotajām kategorijām. |
| Komandējumi un izdevumi | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Izveidojot izdevumu rindu un pēc tam atlasot kategoriju, tiek parādīts šāds kļūdas ziņojums: "PVN grupas DOM un PVN grupas STD kombinācija nav derīga". |
| Komandējumi un izdevumi | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Izdevumu mobilajā programmā ir sinhronizācijas problēmas. |
