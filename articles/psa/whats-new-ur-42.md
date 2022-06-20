---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 42, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami atjaunināšanas laidienā Microsoft Dynamics 365 Project Service Automation 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912724"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti projektu pakalpojumu automatizācijas atjaunināšanas laidienam 42, V3. Šai versijai ir būvēšanas numurs V3.10.73.61, un tā parasti ir pieejama, izmantojot pašreklāmu 2022. gada aprīlī.

## <a name="update-release-42"></a>Atjauninājumu izlaidums 42

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**

- Kad laika grafiks tiek noraidīts, lietotājs, kurš to noraidīja, tiek nepareizi identificēts kā **sistēma**.
- Importējot laika ierakstus, **trūkst resursu kategorijas** vērtības.
- Projektu apstiprinātāji var apstiprināt iesniegtos projektus, ja viņu atļaujas nav īpaši iestatītas uz **Var apstiprināt**.

**Pārdošana**

- Ja faktiskie dokumenti tiek reģistrēti uzdevumos, kas nav saknes līmeņa uzdevumi, faktiskās izmaksas tiek nepareizi apkopotas.
