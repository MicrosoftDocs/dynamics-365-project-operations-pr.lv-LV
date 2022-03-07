---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 31, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002160"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 31. Šīs versijas būvējuma numurs ir V3.10.52.77, un tā ir vispārīgi pieejama, izmantojot 2021. gada maija pašatjauninājumu.

## <a name="update-release-31"></a>Atjauninājumu izlaidums 31

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Laika ievades vadības komandu pogas lapā **Rezervējams resurss** nebija saprotamas.
- Apstiprinot laika ierakstu, vienumā **Project.SetTrackingFields** tika ģenerēts nulles atsauces izņēmums.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- **Izveidot darba grupas dalībnieku** nepareizi parāda rezervācijas iestatīšanas metadatu iestatījumu vienumam **Noklusējuma rezervācijas iesniegtais statuss**.
- Jauninot no PSA 1.X to 3.X, jaunināšanas process neizdodas posmā **UpgradeResourceRequirements**.


**Pārdošana**

Ir novērstas tālāk norādītās problēmas.

- Faktisko ieņēmumu summas izsekošanas režģī tiek konvertētas projekta valūtā.
- Nav skaidra valūtas noklusējuma vērtība, izveidojot žurnālu rindas, piedāvājumu rindas un līgumu rindas scenārijos, kuros organizācijas bāzes valūta atšķiras no projekta valūtas.
- Vaicājums **Neapstiprināta labojuma žurnāla validācija** nefiltrē pēc projekta.
- Atlikušais pārdošanas apjoms projektā tiek aprēķināts nepareizi.
- Piedāvājumi, kuru pamatā ir kontaktpersona, neizdodas, kad tie tiek izveidoti bez cenrāža.
- Atlasot **Apstiprināt rēķinu**, vairs netiek rādīts apstrādes skaitītājs.
- Atlasot **Izveidot rēķinu**, vairs netiek rādīts apstrādes skaitītājs.
- Slēdzot piedāvājumu kā zaudētu, netiek atceltas rezervācijas.







