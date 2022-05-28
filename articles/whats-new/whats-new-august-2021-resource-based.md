---
title: Jaunumi 2021. gada augustā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā tēmā ir sniegta informācija par 2021. gada augustā pieejamajiem kvalitātes atjauninājumiem Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594173"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. gada augustā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

   - Project Operations Microsoft Dataverse vides versijā 4.13.0.152.
   - Projektu vadība un grāmatvedība Dynamics 365 Finance vides versijā 10.0.20.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- **Apstiprinājuma kopas**: apstiprinājuma kopas grupē laiku, izdevumus vai materiālu izmantošanas apstiprinājuma pieprasījumus mazākās operāciju apakškopās. Izmantojot šo grupēšanu, projekta ietvaros apstiprinājumus var apstrādāt noteiktā secībā, kā arī var veikt atkārtotus mēģinājumus un secīgošanu. Grupējot pieprasījumus, tiek uzlabota apstiprinājumu apstrādes uzticamība un izsekošana lielam apstiprinājumu apjomam. Lai iegūtu papildinformāciju, skatiet sadaļu [Apstiprinājumu kopas](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu.

Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Aktivizējiet jaunu kartes versiju, atlasot **Tabulas karšu versijas**, atlasot jaunāko versiju un pēc tam saglabājot atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, sākot karti, rodas problēma, izpildiet instrukcijas dubultās rakstīšanas problēmu novēršanas ceļvedī sadaļā [Kartes trūkstošu tabulas kolonnu problēma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2295625 | Atskaites punkta nosaukums ir jākopē no rēķinu grafika uz rēķinu rindas informāciju. |
| Cenu noteikšana un norēķini | 2316323 | Atlaidi nevar rediģēt proforma rēķinā Project Operations scenārijiem, kuru pamatā ir resursi. |
|   Iespēju pārvaldība | 2338619 | Biznesa kārtulas **Iespēja** un **Piedāvājums** ir jāizsauc tikai lapās. |
| Resursu pārvaldība | 2316523 | Izmantojot **Sūtīt pieprasījumu** no resursu prasības, kurai ir pievienota loma, nevajadzētu parādīt kļūdu. |
| Resursu pārvaldība | 2326885 | Izveidojot resursu vajadzību ar projekta starpniecību, nevajadzētu parādīt kļūdu. |
| Laiks un izdevumi | 2335584 | Novecojušas uzdevumu plūsmas laika ierakstā. |
| Laiks un izdevumi | 2336884 | Laika ievades pogai **Kopēt nedēļu** ir jādarbojas vairāk nekā tikai pašreizējam lietotājam. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu vadība un uzskaite Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Komandējumi un izdevumi | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nepareizas pārdevēja un pārdošanas nodokļa transakciju summas tiek iegrāmatotas, ja izdevumi tiek izveidoti no kredītkartes transakcijas. |
| Komandējumi un izdevumi | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Nepareizais norēķins ir rindas, kas tiek izveidotas, ģenerējot maksājumu žurnālu. |
| Komandējumi un izdevumi | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nepareizas pārdošanas nodokļa transakciju summas tiek iegrāmatotas, ja izdevumi tiek izveidoti no kredītkartes transakcijas. |
| Komandējumi un izdevumi | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Izmaksu rindas dzēšana var aizņemt daudz laika. |
| Projekta uzskaite | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistēma neatbalsta nepārtrauktas skaitļu secības iestatīšanu, kad pēc KB 4619395 lietošanas tiek grāmatots aprēķins. |
| Projekta uzskaite | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Pārdevēja rēķinu grāmatošana var neizdoties, parādot kļūdas ziņojumu "Dokumenta transakciju bilance nav noslēgta 17.05.2021. (uzskaites valūta: 0,00 — atskaišu valūta: 0,01)" |
