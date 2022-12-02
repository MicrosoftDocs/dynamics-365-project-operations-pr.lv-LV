---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 34, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928671"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 34. Šai versijai būvējuma numurs ir V3.10.55.38, un tā ir vispārīgi pieejama ar pašatjauninājumu 2021. gada jūlijā.

## <a name="update-release-34"></a>Atjauninājumu izlaidums 34

### <a name="bug-fixes"></a>Kļūdu labojumi
Ir novērstas tālāk norādītās problēmas.

**VispārīgI**

- Izstrādātāja vadīti atjauninājumi neaktivizē jauno moderno apstiprināšanas darbplūsmu.
- **Apstiprinājuma kopas** galvenajā lapā trūkst atribūtu **Mērķa statuss** un **Darbības tips**.

**Laiks un izdevumi**

- Nevar apstiprināt atsaukšanas pieprasījumu, izmantojot moderno apstiprināšanas plūsmu.
- Nedēļas laika ierakstu kopēšana nedarbojas, kopējot ierakstus, kas nav saistīti ar lietotāju, kurš ir pieteicies.

**Projektu plānošana**

- Importējot no Microsoft Project darbvirsmas pievienojumprogrammas, resursu piešķiršanas kontūras tiek bojātas.

**Resursu pārvaldība**

- Publicējot projektu no Microsoft Project darbvirsmas klienta pievienojumprogrammas, tiek mainīts esošo prasību beigu datums.
- Decimāldaļas precizitāte pārsniedz divus ciparus aiz komata paplašinājuma rezervēšanas apstiprinājuma dialoglodziņā.

**Pārdošana**

- Projekta līgumam pievienojot uz produktu balstītu rindu ar esošu produktu, tiek parādīt izņēmums **atslēga nav atrasta vārdnīcā**.
- Interesentus nevar kvalificēt, ja pasūtījuma tips tiek kartēts no interesenta uz iespēju.
