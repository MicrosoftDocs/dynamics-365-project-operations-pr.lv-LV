---
title: 2021. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Project Operations Lite izvietošanas 2021. gada septembra izlaiduma ietvaros par resursu balstītiem/krājumu nebalstītiem scenārijiem.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923381"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šis raksts attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

   - Project Operations Microsoft Dataverse vides versijā 4.14.0.99.
   - Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja startējot karti rodas problēma, tad sekojiet instrukcijām [Trūkstošo tabulu kolonnu karšu problēma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā duālās rakstīšanas problēmu novēršanas rokasgrāmatā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Laiks un izdevumi | 1811407 | Koriģēta projekta apstiprinātāju drošības loma izmaksu ierakstu apstiprināšanai. |
| Laiks un izdevumi | 1811438 | Koriģēta projekta apstiprinātāju drošības loma laika ierakstu apstiprinājuma atcelšanai. |
| Laiks un izdevumi | 2370126 | Atjauninātas **Projekta uzdevumu** un **Lomu** ikonas **Laika ieraksta** entītijai. |
| Laiks un izdevumi | 2379879 | Izlabota **nedēļas kopēšanas** funkcija laika ierakstam, kad tālrunī izmantojat Dynamics 365. |
| Cenu noteikšana un norēķini | 2371906 | Proforma rēķina kopsumma nedrīkst būt pielāgojama Project Operations uz resursiem balstītiem izvietojumiem. |
| Cenu noteikšana un norēķini | 2385802 | Novērsta kļūda, kas rodas ar negatīvām faktiskajām stundām, kad tiek atsvaidzinātas projekta kopsummas. |
| Cenu noteikšana un norēķini | 2389675 | Uzlabota proformas rēķina apstiprinājuma uzvedība. Ilgtermiņa uzdevuma entītijai ir jāņem vērā darbība, kas ir nepieciešama, lai ierakstītu grāmatvedības apstiprinājuma rezultātus. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu pārvaldība un uzskaite programmā Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Komandējumi un izdevumi | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kreditora un pārdošanas nodokļa transakciju summas, kas ir grāmatotas no izdevumiem, kura ir izveidotas no kredītkaršu transakcijām, nav pareizas. |
| Komandējumi un izdevumi | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Ģenerējot maksājumu žurnālu, tiek izveidotas nepareizas apmaksas rindas. |
| Komandējumi un izdevumi | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kreditora un pārdošanas nodokļa transakciju summas, kas ir grāmatotas no izdevumiem, kuras ir izveidotas no kredītkaršu transakcijām, nav pareizas. |
| Komandējumi un izdevumi | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Izmaksu rindas dzēšana var aizņemt daudz laika. |
| Projekta uzskaite | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Pēc pieteikšanās KB 4619395 netiek atbalstīta numuru sērijas mainīšana uz **Nepārtraukta** , un, publicējot novērtējumu, rodas šāda kļūda: "Sistēma neatbalsta numuru sērijas iestatījuma "Nepārtraukta" Proj_X." |
| Projekta uzskaite | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Piegādātāja rēķina grāmatošana var neizdoties, un var tikt parādīts šāds kļūdas ziņojums: "Transakcijas dokumenti neatbilst kopš 2021. gada 17. maija" . (grāmatvedības valūta: 0,00 — atskaišu valūta: 0,01)." |
