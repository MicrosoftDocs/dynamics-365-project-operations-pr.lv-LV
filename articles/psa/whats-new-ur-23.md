---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 23, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996625"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation atjauninājumu izlaidums 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 23. Šīs versijas būvējuma numurs ir V 3.10.34.30, un tas parasti ir pieejams, izmantojot 2020. gada augusta pašatjauninājumu.

## <a name="update-release-23"></a>Atjauninājumu izlaidums 23

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.
- Lai nodrošinātu jēgpilnu izņēmumu, apstrādājiet maksimālo/minimālo gadījumu ar vienumu **Projekta darba grupas dalībnieka dzēšana**.
- Piešķīruma importēšanas rezultāti tukšā noņemšanas ekrānā.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- **Resursu lietojuma režģa resursu kartē** tiek parādīti nepareizi dati, ja laika skala pārsniedz piecas dienas.
- Kad klienti izveido rezervējamu resursu, spraudnis periodiski automātiski nepievieno resursu Microsoft Office 365 grupai.
- **Saskaņošana** skatā **Nedēļas** vai **Mēneša** skatā tiek parādītas nepareizas manuālas kontūras.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Pārāk liels entītiju **RetrieveMultiple for usersettings** skaits izraisa pasliktinātu projekta apstiprinājumu un citu operāciju veiktspēju.
- **Uzdevumu plānošanas** režģa resursu uzmeklēšana ir ierobežota, parādot tikai piecus darba grupas dalībniekus no projekta darba grupas. 
- **Uzdevumu plānošanas** režģa resursu uzmeklēšana nefiltrē neaktīvos resursus.
- Manuālais režīms nedarbojas kā paredzēts projekta plānošanas darba sadalījuma struktūrā.
- **Uzdevumu plānošanas** režģī tiek rādītas **Neaktīvas transakciju kategorijas**.
- Režģī **Resursu piešķiršana** tiek veikta nepareiza noapaļošana, kad uzdevumam ir vairāki piešķīrumi.
- Viena uzdevuma plānoto izmaksu un faktisko izmaksu noapaļošanas vērtības atšķiras.

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Veicot dubultklikšķi uz **Visu transakciju kategoriju ienese**, tiek izveidotas vairākas rindas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]