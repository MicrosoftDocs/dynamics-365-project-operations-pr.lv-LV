---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 45, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 45. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169182"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 45, V3. Šai versijai būvējuma numurs ir V3.10.76.168, un tā ir vispārīgi pieejama ar pašatjauninājumu 2022. gada jūlijā.

## <a name="update-release-45"></a>Atjauninājumu izlaidums 45

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Pārdošana**

- Lietotāji nevar veiksmīgi izveidot rēķinus pēc tam, kad viņi mēģina izveidot rēķinu bez rēķinā neiekļautām pārdošanām, ja viņi skata arī to pašu lapas instanci un to neatsvaidzina.

**Laiks un izdevumi**

- Ja ir iespējoti mūsdienīgie apstiprinājumi un tiek apstiprināts atsaukts projekts, ieraksta posms tiek nepareizi atjaunināts uz **Pieprasījuma atsaukšana apstiprināta**.
- Ja ir iespējoti mūsdienīgie apstiprinājumi un mākoņa plūsmu funkcionalitāte ir neaktīva, apstiprināšanas process nav sekmīgs, un iesniedzošie vai apstiprinošie lietotāji netiek informēti.
