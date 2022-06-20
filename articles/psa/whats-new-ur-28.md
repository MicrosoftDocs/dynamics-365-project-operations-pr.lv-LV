---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation Update Release 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930603"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti project service automation V3, Update Release 28 Šai versijai ir būvēšanas numurs V3.10.46.32 un tā parasti ir pieejama, izmantojot pašrealizāciju 2021. gada janvārī.

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
