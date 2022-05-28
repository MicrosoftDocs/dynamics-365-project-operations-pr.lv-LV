---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 39, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 39. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588745"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 39, V3. Šai versijai ir būvēšanas numurs V3.10.60.170, un tā parasti ir pieejama, izmantojot pašreklāmu 2022. gada janvārī.

## <a name="update-release-39"></a>Atjauninājumu izlaidums 39

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**VispārīgI**

- Ir veikti vairāki uzlabojumi arābu valodas tulkošanas vietnes kartē.

**Projekta pārvaldība**

- Kļūda rodas, mainot projekta vadītāju uz lietotāju, kurš jau ir projekta grupas dalībnieks.

**Pārdošana**

- Projekta līguma cenrāža **īpašnieks** nav pareizs, ja cenrādis tiek izveidots automātiski. 
- Cenrāža datuma efektivitāte netiek ievērota, ja cenrādis tiek lietots projekta parametram.
- Līgumslēdzējai vienībai, rediģējot divus atsevišķus piedāvājumus, var nebūt pareizās noklusējuma vērtības.
