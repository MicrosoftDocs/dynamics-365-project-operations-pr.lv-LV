---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 38, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami atjaunināšanas laidienā Microsoft Dynamics 365 Project Service Automation 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915194"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti projektu pakalpojumu automatizācijas atjaunināšanas laidienam 38, V3. Šīs versijas būvējuma numurs ir V3.10.59.117, un tā ir pieejama 2021. gada decembra pašatjauninājumā.

## <a name="update-release-38"></a>Atjauninājumu izlaidums 38

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**

- Izņēmums ir tad, ja apstiprinājuma kopu žurnālu garums pārsniedz 100 000 ierakstu.
- Lietotāji nevar piekļūt **laika ieraksta** režģim no galvenās lapas Laika ieraksts.**·**
- Dialoglodziņā **Laika ievades importēšana** netiek rādīts teksts, ja neviens vienums nav piemērots importēšanai.
- Lietotāji var izveidot apstiprinājumu kopas, **kurās lauks Mērķa statuss** ir iestatīts uz **Nezināms**.

**Projekta pārvaldība**

- Sākoties vasaras laikam, kontūras netiek rādītas pareizi resursu piešķirēs UTC(+09:30) un UTC(+10:00).
- Lauks **Papildu kolonna** darba sadalījuma struktūrām dažās lokalizācijās ir paslēpts.
- Kalendāra vadīklas datuma atlasītājs projekta uzdevumu **režģī** nav pareizi lokalizēts ķīniešu valodai.

**Pārdošana**

- **Līguma izpilde** un **projekta faktiskās izmaksu** vērtības neatbilst, ja reģistrējamie resursi, kuriem ir dažādas līguma vienības un valūtas, iesniedz laika ierakstus.
- Pielāgota darbplūsma rēķinu automātiskai apstiprināšanai neizdodas, ja rēķini tiek importēti kā pārvaldīts risinājums. Tiek parādīts šāds ziņojums: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Nederīgs rēķina statuss."
- Ja **sakne** ir atlasīta kā summēšanas opcija un projektam ir aprēķini no darbību klašu maisījuma (piemēram, laika, izdevumu un materiālu novērtējumu kombinācija), sistēma apkopo visas darbību klases kā vienu maksas rindu.
- Scenārijos, kad izdevumu rinda tiek pievienota pirms līguma rindas saistīšanas ar projektu, pareizās cenas netiek ievadītas kā noklusējuma vērtība **laukā Atjaunināt cenu**.
- Projekta un uzdevuma entītijās negatīvas pārdošanas summas nav **atļautas**.**·**
