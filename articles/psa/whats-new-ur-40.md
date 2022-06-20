---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 40, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami atjaunināšanas laidienā Microsoft Dynamics 365 Project Service Automation 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912801"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti projektu pakalpojumu automatizācijas atjaunināšanas laidienam 40, V3. Šīs versijas būvējuma numurs ir V3.10.61.61, un tas parasti ir pieejams, izmantojot 2022. gada februāra pašatjauninājumu.

## <a name="update-release-40"></a>Atjauninājumu izlaidums 40

### <a name="features"></a>Līdzekļi
Jaunināšanas no Project Service Automation uz Project Operations 1. posms - Lite tiks izlaists 2022. gada februārī visiem klientiem. Lai pārbaudītu atbilstību, skatiet rakstu [Jaunināšana no projektu pakalpojumu automatizācijas uz projekta operācijām](upgrade-project-operations-non-stocked.md). Ja lietojumprogramma jūsu instancē netiek rādīta administrēšanas Power Platform centrā, sazinieties ar atbalsta dienestu un pieprasiet, lai lidojums tiktu iespējots jūsu vidēm. Jūsu pieprasījumā ir jāiekļauj to vides ID saraksts, kuros ir jāiespējo lidojums.

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**
- Ja laika ieraksts tiek noraidīts vai atcelts, trūkst piezīmes ieraksta. 

**Pārdošana**

- Atjauninot izmaksu vai pārdošanas aprēķinus, izmantojot gatavus spraudņus, jums ir nepareizi atļauts nosūtīt JSON derīgās kravas, kas nav derīgas ārpus lietotāja interfeisa.
- Atjauninot piedāvājuma rindas, izmantojot ātro skatu, ir atļauts aktivizēt piedāvājumus.
