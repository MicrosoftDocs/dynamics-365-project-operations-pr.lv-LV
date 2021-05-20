---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948880"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu izlaidums 25. Šīs versijas būves numurs ir V 3.10.43.76, un tā parasti ir pieejama, izmantojot 2020. gada oktobra pašatjauninājumu.

## <a name="update-release-25"></a>Atjauninājumu izlaidums 25

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērsta šāda problēma:

- Laika ievadīšanas diagramma, kurā parādīti papildu dati, pamatojoties uz pārāk lielu intervāla izgūšanu.

**Resursu pārvaldība**

Ir novērsta šāda problēma:

- Pievienots pakotnes izvietošanas kods, lai izlaistu Universal Resource Scheduling ielāpa importēšanu, ja jau pastāv augstāks versijas ielāps.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Izlabotas noapaļošanas un valūtas kursa neatbilstības, kā rezultātā projekta izsekošanas tīklā ir nepareizi plānotas izmaksas.
- Atbalstiet iespēju veidlapā **Projekts** parādīt divus vai vairākus reakcijas režģus.
- Sniegta validācija, lai risinātu iespēju piešķirt uzdevumu pēc kalendāra beigu datuma, kā rezultātā resursu piešķiršana neizdevās.
- Uzlabota kļūdu apstrāde, lai risinātu atsauces Null izņēmumu, kas ģenerēts no tālāk minētajām opcijām:

    - **PreValidateProjectTeamMemberCreate** spraudnis
    - **PreValidateProjectTaskCreate**, kad projekta uzdevums ir izveidots bez saistīta projekta
    - **PreProjectTeamMemberCreate** spraudnis
    - **PostProjectTeamMemberDelete** spraudnis
    - **PreValidateProjectTaskDelete** spraudnis

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Uzlabota kļūdu apstrāde, lai risinātu atsauces Null izņēmumus, kas ģenerēti no **Projekta kopēšana: aprēķina palīga resursu pārvaldību**.
- **Nav gatavs rēķina izveidei** sadaļā **Laika un materiālu rēķinu izrakstīšanas rezerve** nenotīra norēķinu statusu.
- Labotas nepareizi nosauktas pogas **Cenas** cilnēs **Lomas cena** un **Kataloga vienumi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]