---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 15, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 15, 3. versijā
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585157"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation atjauninājumu izlaidums 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 15. Šai versijai ir būvējuma numurs V 3.10.5.28, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2020. gada janvārī.

## <a name="update-release-15"></a>Atjauninājumu izlaidums 15 

### <a name="enhancements"></a>Uzlabojumi

- Projekta pārvaldība

### <a name="bug-fixes"></a>Kļūdu labojumi

- Laiks un izdevumi

  - Novērsts: ielādes kļūda apstrādes pievienošana saskaņošanas skatā.
  - Novērsts: projekta resursu centrmezgls: **Pārdēvēt** summu, lai mazinātu neskaidrības.
  - Novērsts: pielāgot skatu **Kopēšanas laika ievades kolonnas**, lai iekļautu tipu.
  - Novērsts: rediģējot laika ieraksta ilgumu režģa skatā, izmantojot decimālskaitļus, dažiem skaitļiem rodas nezināma kļūda.

- Projekta pārvaldība

  - Novērsts: nolaižamā izvēlne **Lietošana izsekošanas skatā** tagad tiek izvērsta, pamatojoties uz opciju platumu.
  - Novērsts: kad projekti tiek pārvaldīti + 13 laika joslā, uzdevumu aprēķinos var tikt parādīti neprecīzi rezultāti.
  - Novērsts: **Darba grupas dalībnieka beigu laiks** ir izlabots, izmantojot 24 stundu kalendāru.
  - Novērsts: atkārtoti aktivizēt **BPF** **msdyn_project** galvenajā formā.
  - Novērsts: piešķiru aprēķins vairs neignorē vienu dienu.
  - Novērsts: projekta veidlapai ir pievienots jauns paziņojuma reklāmkarogs, ja laika josla starp lietotāju un projektu atšķiras.

- Sales

  - Novērsts: izmaksu novērtējuma kategorijas uzmeklēšanu var izmantot, lai filtrētu dublikātus.
  - Novērsts: kods rīkā **PluginDomain. ExecuteInTryCatchBlock (..)** vairs neslēpj izņēmuma izcelsmi.
  - Novērsts: **projekta uzmeklēšanas** **vaicājuma rindas** veidlapā vairs netiek parādīts kļūdas ziņojums, ja ir vairāk nekā 1000 projektu.
  - Novērsts: **novērtējumu** režģis darba aplēsēm un izdevumu aplēsēm tagad rāda pareizo valūtas simbolu.
  - Novērsts: pēc organizācijas atjauninājumiem PSA no atjauninājuma izlaiduma 14 līdz atjauninājuma izlaidumam 15 cilne **Plānot** vairs netiek rādīta veidlapā **Projekts** kā tukšs lauks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
