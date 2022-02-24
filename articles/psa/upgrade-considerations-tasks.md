---
title: Jaunināšanas apsvērumi darba sadalījuma struktūrai
description: Šajā tēmā ir sniegta informācija par darba sadalījuma struktūras jaunināšanu no programmas Project Service Automation 2.x uz 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149552"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Jaunināšanas apsvērumi darba sadalījuma struktūrai

[!include [banner](../includes/psa-now-project-operations.md)]

Šajā tēmā ir sniegta informācija par darba sadalījuma struktūras jaunināšanu no programmas Project Service Automation 2.x uz 3.x. Šajā tēmā ir definēts labs projekta stāvoklis programmā Project Service Automation (PSA), kas ir nepieciešams sekmīgai jaunināšanai. Ir pieejama arī informācija par vispārējiem bloķēšanas nosacījumiem, kas var izraisīt jaunināšanas kļūmi. Papildinformāciju par projekta uzdevumu un to funkciju definēšanu projekta grafikā skatiet sadaļā [Projektu grafiki](project-creating.md).

## <a name="key-entities"></a>Galvenās entītijas
Lai iegūtu precīzu darba sadalījuma struktūru, kas jau ir ielādēta ar resursiem, ir nepieciešamas šādas entītijas:

- [Projekts](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projekta darba grupa](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projekta uzdevums](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Resursu piešķires](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projekta uzdevuma atkarība](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Rezervējamie resursi](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Lai definētu resursu ielādētu darba sadalījuma struktūru, ir jāveic šādas darbības:

1. Izveidojiet jaunu projektu. Papildinformāciju par to, kā izveidot jaunu projektu, skatiet [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Izveidojiet vienu vai vairākus uzdevumus. Papildinformāciju par to, kā izveidot uzdevumu, skatiet [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definējiet uzdevumu atkarības. Papildinformāciju skatiet tēmā [Projekta uzdevuma atkarība](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Projektam nozīmējiet projekta grupas dalībniekus. Papildinformāciju skatiet [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Uzdevumiem nozīmējiet projekta darba grupas dalībniekus. Papildinformāciju skatiet [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projekta darba grupas attiecības

Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:
- Visiem projekta grupas dalībniekiem ir jābūt saistītiem ar rezervējamo resursu.
- Visiem projekta grupas dalībniekiem ir jābūt saistītiem ar vienu un to pašu projektu. 

## <a name="project-task-relationships"></a>Projekta uzdevumu attiecības
Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:

- Visi saistītie uzdevumi ir jāsaista ar vienu un to pašu projektu.
- Katram rindas uzdevumam ir jābūt pamatuzdevumam.
- Katram uzdevumam ir jābūt pamatprojektam.

### <a name="valid-conditions"></a>Derīgi nosacījumi

- Visiem uzdevumu ilgumiem jābūt lielākiem par vai vienādiem ar (> =) vienu stundu un mazākiem par 1 800 000 minūtēm (1 250 dienām).*
- Visiem uzdevumiem ir jābūt sākuma datumam, kas nav agrāks par 01.01.2000.*
- Visiem uzdevumiem ir jābūt sākuma datumam, kas nav vēlāks kā 17 gadi pēc šīs dienas.*
- Visiem uzdevumiem sākuma datumam ir jābūt agrākam vai vienādam ar to pabeigšanas datumu.
- Visiem transakciju tipiem pēc klasifikācijām (izdevumi, materiāls, nodoklis un laiks) ir jābūt norādītām vērtībām attiecībā uz **Noklusējuma vienību** un **Vienības grupu**.
- Ir jāizvairās no datu formātu rakstīšanas ar burtiem.

### <a name="potential-mitigation-steps"></a>Potenciālās samazināšanas darbības
- Izmantojiet detalizēto atrašanu, lai identificētu projekta uzdevumus, kas nesatur projekta ID.
- Izmantojiet detalizēto atrašanu, lai identificētu projekta uzdevumus, kuru plānotais ilgums pārsniedz > 1 800 000.
- Pirms datu izmaiņu veikšanas jāizpēta visi pielāgojumi, kas saistīti ar entītiju, kas, iespējams, ir izraisījuši datu nokļūšanu sliktā stāvoklī. Šie pielāgojumi ir jāskata, lai turpinātu jebkurus ar datiem saistītos atjauninājumus.
- Noteiktajiem uzdevumiem, kas ir nošķirti no vecākprojekta, apsveriet iespēju dzēst šos uzdevumus, ja tie nav nepieciešami vai tie ir jāsaista ar pareizo primāro projektu.
- Visiem uzdevumiem, kuru ilgums pārsniedz 1250 dienas, apsveriet iespēju pievienot vairākus uzdevumus, lai atspoguļotu kopējo ilgumu, ja tas ir iespējams.

> [!NOTE]
> Ar zvaigznīti (\*) atzīmētajiem elementiem ir ierobežojumi, kas ir saistīti ar faktu, ka klientu attiecību pārvaldība (CRM) atbalsta tikai 7320 atkārtošanās paplašinājumus. Nepārsniedziet šo ierobežojumu.

## <a name="resource-assignment-relationships"></a>Resursa piešķiršanas attiecības
Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:

- Visām resursu piešķirēm darba sadalījuma struktūrā ir jābūt saistītiem ar vienu un to pašu projektu.
- Visām resursu piešķirēm darba sadalījuma struktūrā ir jābūt saistītiem ar projekta grupas dalībniekiem vienā un tajā pašā projektā.

### <a name="potential-mitigation-steps"></a>Potenciālās samazināšanas darbības
- Norādiet visus uzdevumus, kas neatbilst iepriekš aprakstītajiem nosacījumiem.  
- Visas resursu piešķires, kas vairs nav derīgas, ir jāizdzēš.

## <a name="project-task-dependency-relationships"></a>Projekta uzdevuma atkarības attiecības
Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:

- Visām projekta uzdevuma atkarībām ir jābūt saistītām ar vienu un to pašu projektu.
- Uzdevumam nevar būt vienas un tās pašas atkarības atsauces vairāk nekā vienu reizi.
