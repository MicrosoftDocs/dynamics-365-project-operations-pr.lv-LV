---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 29, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 29. Šīs versijas būvējuma numurs ir V3.10.47.7, un tas parasti ir pieejams, izmantojot 2021. gada februāra pašatjauninājumu.

## <a name="update-release-29"></a>Atjauninājumu izlaidums 29

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Laika ierakstu režģī lietotāji nevar redzēt darba stundas, kas reģistrētas dienās, kuras nav darba dienas.
- Apstiprinātos izdevumu ierakstus var rediģēt režģī.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Trūkst validācijas loģikas, lai nodrošinātu, ka resursu piešķiršanas darba stundas nevar būt negatīvas.
- Pielāgotā darbība **AssignResourcesForTask** atjaunina visus laukus, nevis tikai mainītos laukus.
- Kopējot projektu vidē ar spraudņiem vai darbplūsmām, kas reģistrētas notikumā **CreateProject**, **msdyn_bulkgenerationstatus** atribūta atjaunināšana **CopyWBSToProject** neizdodas.
- Izvēršot projekta kalendāru, darbdienas netiek kārtotas augošā secībā, kas izraisa dažu projekta uzdevumu atjauninājumu kļūmi.
- Mainot projekta vadītāju esošā projektā, tiek aktivizēta organizācijas vienības noklusējuma loģika.

**Pārdošana**

Ir novērstas tālāk norādītās problēmas.

- Lapas **Līgums** cilnes **Līguma izpilde** inicializēšanas laikā neizdodas, ja nav līguma rindu.