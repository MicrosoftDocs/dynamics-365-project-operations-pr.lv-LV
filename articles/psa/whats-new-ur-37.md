---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 37, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 37. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593483"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 37, V3. Šai versijai ir kompilācijas numurs V3.10.58.120, un tā ir pieejama, izmantojot automātisko atjauninājumu 2021. gada novembrī.

## <a name="update-release-37"></a>Atjauninājumu izlaidums 37

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**
- Lietotāji nevar dzēst laika ierakstu, notīrot šūnu.
- Skatā **Mani nesekmīgie apstiprinājumi** skats ietver tikai projekta apstiprinājumus, kuru statuss ir **Iesniegts**.

**Projekta pārvaldība**
- Atverot projektu Microsoft datora pievienojumlietojumprogrammā, lietotāji saņem kļūdas ziņojumu Null Reference Exception, ja Projekta darba grupas dalībnieka pozīcijas nosaukums ir tukšs.
- Lapā **Projekta uzdevums** nav pogas **Saglabāt**, tapēc lietotāji nevar saglabāt izmaiņas.
- Lietotāji nevar izdzēst projektu, kam ir uzdevums, kas saistīts ar piedāvājumu ar statusu **Ir spēkā**.

**Pārdošana**
- Lapā **Projekts** lauks **Valūta** tiek atjaunināts, lai atbilstu izmantotās veidnes valūtai.
- Izmaksas tiek aprēķinātas nepareizi uzdevumiem, kuriem ir vairākas valūtas.
