---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 37, V3
description: Šajā rakstā ir uzskaitītas funkcijas un labojumi, kas ir pieejami atjaunināšanas laidienā Microsoft Dynamics 365 Project Service Automation 37, V3.
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922507"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti projektu pakalpojumu automatizācijas atjaunināšanas laidienam 37, V3. Šai versijai ir kompilācijas numurs V3.10.58.120, un tā ir pieejama, izmantojot automātisko atjauninājumu 2021. gada novembrī.

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
