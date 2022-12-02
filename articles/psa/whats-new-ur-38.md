---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 38, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 38. atjauninājumu laidienā, V3.
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

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 38, V3. Šīs versijas būvējuma numurs ir V3.10.59.117, un tā ir pieejama 2021. gada decembra pašatjauninājumā.

## <a name="update-release-38"></a>Atjauninājumu izlaidums 38

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**

- Rodas izņēmums, ja apstiprinājuma kopas žurnālu garums pārsniedz 100 000 ierakstu.
- Lietotāji nevar piekļūt režģim **Laika ieraksts** no galvenās lapas **Laika ieraksts**.
- Dialoglodziņā **Laika ierakstu importēšana** netiek rādīts teksts, ja nav importēšanai atbilstošu vienumu.
- Lietotāji var izveidot apstiprinājuma kopas, kuru lauka **Mērķa statuss** iestatījums ir **Nav zināms**.

**Projekta pārvaldība**

- Kad sākas vasaras laiks, resursu piešķīrumos UTC(+09:30) un UTC(+10:00) netiek pareizi rādītas resursu kontūras.
- Lauks **Papildu kolonna** dažās lokalizācijās darba sadalījuma struktūrai ir paslēpts.
- Kalendāra vadīklas datuma atlasītājs režģī **Projekta uzdevums** nav pareizi lokalizēts ķīniešu valodā.

**Pārdošana**

- Vērtības **Līguma veiktspēja** un **Projekta faktiskās izmaksas** nesakrīt, ja rezervējamie resursi, kam ir atšķirīgas līgumslēdzējas vienības un valūtas, iesniedz laika ierakstus.
- Pielāgota darbplūsma, lai automātiski apstiprinātu rēķinus, neizdodas, ja rēķini tiek importēti kā pārvaldīts risinājums. Tiek rādīts šāds ziņojums: “Microsoft.Xrm.Sdk.InvalidPluginExecutionException ziņojums: Nederīgs rēķina statuss”.
- Kad kā apkopošanas opcija tiek izvēlēta **Sakne** un projektam ir aprēķini no dažādām transakciju klasēm (piemēram, laika, izdevumu un materiālu aprēķinu kombinācija), sistēma apkopo transakciju rindas kā vienu maksas rindu.
- Scenārijos, kur izdevumu rinda tiek pievienota pirms līguma rindas saistīšana ar projektu, laukā **Atjaunināt cenu** netiek ievadīts pareizais izcenojums kā noklusējuma vērtība.
- Entītijās **Projekts** un **Uzdevums** nav atļauts izmantot negatīvas pārdošanas summas.
