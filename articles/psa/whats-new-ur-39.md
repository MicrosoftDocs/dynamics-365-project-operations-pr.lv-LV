---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 39, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami atjaunināšanas laidienā Microsoft Dynamics 365 Project Service Automation 39, V3.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922461"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti projektu pakalpojumu automatizācijas atjaunināšanas laidienam 39, V3. Šai versijai ir būvēšanas numurs V3.10.60.170, un tā parasti ir pieejama, izmantojot pašreklāmu 2022. gada janvārī.

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
