---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 38, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 38. atjauninājumu laidienā, V3.
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901513"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 38, V3. Šīs versijas būvējuma numurs ir V3.10.59.117, un tā ir pieejama 2021. gada decembra pašatjauninājumā.

## <a name="update-release-38"></a>Atjauninājumu izlaidums 38

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**

- Izņēmums rodas, ja apstiprinājuma kopas žurnālu garums pārsniedz 100 000 ierakstu.
- Lietotāji nevar piekļūt **laika ievades** režģim no **galvenās lapas Laika** ieraksts.
- **Dialoglodziņā Laika ievades importēšana** netiek rādīts teksts, ja neviens vienums nav piemērots importēšanai.
- Lietotāji var izveidot apstiprinājuma kopas, kurās **lauks Mērķa statuss ir** iestatīts uz **Nezināms**.

**Projekta pārvaldība**

- Kontūras netiek rādītas pareizi resursu piešķirēs UTC(+09:30) un UTC(+10:00), kad sākas vasaras laiks.
- **Lauks Papildu kolonna darba sadalījuma struktūrām ir** paslēpts dažās lokalizācijās.
- Kalendāra vadīklas datumu atlasītājs **projekta uzdevumu** režģī nav pareizi lokalizēts ķīniešu valodai.

**Pārdošana**

- **Līguma izpildes** un projekta faktisko izmaksu vērtības **nesakrīt**, ja rezervējamie resursi, kuriem ir dažādas līgumslēdzējas vienības un valūtas, iesniedz laika ierakstus.
- Pielāgota darbplūsma, lai automātiski apstiprinātu rēķinus, neizdodas, ja rēķini tiek importēti kā pārvaldīts risinājums. Tiek parādīts šāds ziņojums: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice status."
- Ja **sakne ir atlasīta kā** summēšanas opcija un projektam ir novērtējumi no darbību klašu kombinācijas (piemēram, laika, izdevumu un materiālu novērtējumu kombinācija), sistēma apkopo darījumu klases kā vienu maksas rindu.
- Scenārijos, kad izdevumu rinda tiek pievienota pirms līguma rindas saistīšanas ar projektu, laukā Atjaunināt cenu netiek ievadīta pareiza cenu noteikšana kā noklusētā **vērtība**.
- Projekta un uzdevumu entītijās nav atļautas negatīvas **pārdošanas** **summas**.
