---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 23, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150047"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation atjauninājumu izlaidums 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

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
