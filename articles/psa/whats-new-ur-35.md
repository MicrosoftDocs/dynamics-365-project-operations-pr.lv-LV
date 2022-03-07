---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 35, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 35. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473274"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 35, V3. Šai versijai būvējuma numurs ir V3.10.56.110, un tā ir vispārīgi pieejama ar pašatjauninājumu 2021. gada septembrī.

## <a name="update-release-35"></a>Atjauninājumu izlaidums 35

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Laiks un izdevumi**

- Projekta apstiprinātājs saņem lasīšanas atļaujas kļūdu, kad apstiprina izmaksu ierakstus ar **Projekta apstiprinātāja** lomu.
- Projekta apstiprinātājs saņem rakstīšanas atļaujas kļūdu **msdyn_projectapproval**, kad atceļ apstiprinātu laika ierakstu ar **Projekta apstiprinātāja** lomu.
- Programmas Dynamics 365 tālrunim lietotnē Project Resource Hub modulim laika ierakstā atlasot **Kopēt nedēļu**, rodas šāda kļūda: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Politika **Mēģināt vēlreiz** automātiski apstiprina ierakstus, kas iepriekš tika noraidīti.
- Apakšrežģos **Apstiprinājumu kopas** tiek rādītas nepiemērojamas lentes darbības.
- Entītijā **Laika ievade** trūkst ikonu **Projekta uzdevums** un **Resursa loma**.
- Importējot resursu piešķīrumus, importētajiem laika ierakstiem nav pareizs ilgums tiem piešķīrumiem, kas tika izveidoti, izmantojot manuāla režīma uzdevumus.
- Lapā **Detalizētā atrašana laika ierakstiem** trūkst vienuma **Dzēst**.
- Lapā **Laika ievades informācija** trūkst vienuma **Saglabāt**. Šī problēma neļauj saglabāt izmaiņas, kad lapa tiek aizvērta.

**Projektu plānošana**

- Režģos **Resursu piešķiršana** un **Resursu saskaņošana** grupētie atribūti netiek kārtoti alfabētiskā secībā.
- Uzdevumus nevar izveidot, ja datuma uzvedība ir pielāgota kā **Tikai datums**.

**Resursu pārvaldība**

- Ja ir instalēta gan programma Dynamics 365 Field Service, gan Project Service Automation, pārklāšanās problēmas rodas, ja **Ar resursu prasību saistītais skats** ir saistīts ar galveno lapu.
- Veicot dubultklikšķi uz **Saglabāt** dialoglodziņā **Darba grupas dalībnieka ātrā izveide**, tiek liegta resursu prasības izveide.

**Pārdošana**

- Dzēšot uzdevumu, kas saistīts ar piedāvājumu, kura statuss ir **Iegūts**, tiek aktivizēts izņēmums.
