---
title: Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada aprīļa laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110893"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.41.0.45
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.26.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Iepirkumu kategorijas var izmantot projektu pirkumu pasūtījumos un neizpildītiem piegādātāja rēķiniem. Papildinformāciju skatiet rakstā [Iepirkumu kategoriju izmantošana ar projekta pirkuma pasūtījumiem un neizpildītiem piegādātāja rēķiniem](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā tabulā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada marta laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija msdyn\_projectvendorinvoicelines | 1.0.0.4 | Šī karte atbalsta iepirkumu kategoriju izmantošanu ar pirkumu pasūtījumiem un neizpildītiem piegādātāja rēķiniem. |

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| ------------ | ---------------- | -------------- |
| Laiks un izdevumi | 2573900 | Pēc noklusējuma ir jāiespējo līdzeklis **Mūsdienīgi apstiprinājumi**. |
| Cenu noteikšana un norēķini | 2603313 | Novērsta ierakstu dublikāta kļūda, kas neļāva pievienot piedāvājumu un līgumu rindas, kam ir produkts. |
| Izvietošana un konfigurācija | 2611368 | Klientiem ir jābūt iespējai pievienot līdz piecām pielāgotām entītijām risinājumam, izmantojot moderno programmu noformētāju. |
| Laiks un izdevumi | 2628285 | Novērsta problēma, kas ietekmē iespēju iestatīt pareizo resursa kategoriju laika ieraksta importēšanas laikā. |
|   Iespēju pārvaldība| 2628815 | Atjaunināts piedāvājuma rindas detalizētās informācijas apraksta rakstzīmju ierobežojums, lai tas atbilstu uzdevuma tēmas rakstzīmju ierobežojumam, tādējādi ļaujot sekmīgi importēt uzdevumus, kuru tēmas garums pārsniedz 100 rakstzīmes. |
| Laiks un izdevumi| 2629547 | Projekta apstiprinājumu laukam **Iesniedza** jānorāda lietotājs, kas ir iesniedzis ierakstu. |
| Laiks un izdevumi| 2629865 | Lauks **Kopēt kategoriju** uzdevumos, kad tiek kopēti projekti. |
| Laiks un izdevumi| 2636463 | Laboti apstiprinājumu filtri moderno apstiprinājumu veidlapās. |
| Projektu plānošana un izsekošana | 2648300 | Novērsta problēma, kas neļauj mainīt projekta īpašnieku. |
| Cenu noteikšana un norēķini | 2563000 | Rēķinā neiekļautas pārdošanas žurnāla rindas, kur valūta atšķiras no līguma valūtas, nedrīkst tikt atļautas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu pārvaldība un uzskaite programmā Dynamics 365 Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
