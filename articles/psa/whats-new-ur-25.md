---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 25, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922553"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu izlaidums 25. Šīs versijas būves numurs ir V 3.10.43.76, un tā parasti ir pieejama, izmantojot 2020. gada oktobra pašatjauninājumu.

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
