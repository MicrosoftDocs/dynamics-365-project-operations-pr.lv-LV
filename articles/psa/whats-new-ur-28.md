---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150632"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu laidiens 28. Šīs versijas būves numurs ir V3.10.46.32, un tā parasti ir pieejama, izmantojot 2021. gada janvāra pašatjauninājumu.

## <a name="update-release-28"></a>Atjauninājumu izlaidums 28

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Lietotāji var izmantot **Lielapjoma rediģēšanu**, lai atjauninātu apstiprinātos un iesūtītos laika ierakstus.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Gadījumos, kad uzdevuma GUID interpretē kā numuru, uzdevumus nevar atvērt rediģēšanai, izmantojot **Rediģēt uzdevumu** lentē, kas atrodas lapā **Darba sadalījuma struktūra**.

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Kad tiek izsaukts spraudnis **GetEstimatesForProject**, tiek ģenerēts nulles atsauces izņēmums.
- **Atzīmēt gatavu rēķinam** atskaites punkta režģī tikai daļēji atjaunina atribūtus, izņemot atribūtu **InvoiceStatus**, kurš tiek atjaunināts.



[!INCLUDE[footer-include](../includes/footer-banner.md)]