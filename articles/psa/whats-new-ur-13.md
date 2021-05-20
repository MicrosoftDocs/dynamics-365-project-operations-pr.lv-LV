---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 13, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949463"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation atjauninājumu izlaidums 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 13. Šai versijai ir būvējuma numurs V3.10.3.18 , un tas ir pieejams šādā grafikā:

- **Vispārēja pieejamība (pašatjauninājums):** 2019. gada novembris
- **Automātiskais atjauninājums:** 2019. gada decembris


## <a name="update-release-13"></a>Atjauninājumu izlaidums 13 

### <a name="bug-fixes"></a>Kļūdu labojumi

- Laiks un izdevumi

     - Novērsts: meklēšanas funkcionalitāte lapā **Izmaksu apstiprinājums** nedarbojas, meklējot pēc izdevumu mērķa.

- Resursu pārvaldība

     - Novērsts: skaitļi saskaņošanā ir atjaunināti, lai būtu pareizi pamatoti.
     - Novērsts: nosauktos resursus uzdevumiem nevar tikt piešķirti cilnē **Plānot**.

- Projekta pārvaldība

     - Novērsts: nulles atsauces izņēmums, piešķirot darba grupas dalībnieku, kad **TransactionType** trūkst **Vienību** un **DefaultGroup** iestatījuma informācijas.

- Sales

     - Novērsts: transakciju tipu ierakstu dublikāts atgriež kļūdu, kad ir izveidoti lomu cenrāža ieraksti.
     - Novērsts: papildu pogas opcijām **Jauna iespēja**, **Piedāvājums**, **Pasūtījuma rinda** un **Pievienot produktu** ir redzamas komandās Iespējām, Piedāvājumiem, Pasūtījuma produktiem un projekta rindu apakšrežģim.




[!INCLUDE[footer-include](../includes/footer-banner.md)]