---
title: Kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753485"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation atjauninājuma izlaidums 13, 3. versija
Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

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

     - Novērsts: nulles atsauces izņēmums, piešķirot darba grupas dalībnieku, kad **TransactionType** trūkst **Vienību** un **DefaultGroup**iestatījuma informācijas.

- Sales

     - Novērsts: transakciju tipu ierakstu dublikāts atgriež kļūdu, kad ir izveidoti lomu cenrāža ieraksti.
     - Novērsts: papildu pogas **Jaunas iespējas**, **Piedāvājums**, **Pasūtījuma rinda**un **Produkta pievienošana** ir redzamas komandu, piedāvājumu, pasūtījumu produktu un no projekta rindu apakšrežģa komandas.


