---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 13, V3
description: Šajā rakstā ir sniegta informācija par jaunumiem projektu pakalpojumu automatizācijas atjauninājuma laidienā 13, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930695"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation atjauninājumu izlaidums 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti project service automation V3, Update Release 13. Šai versijai ir būvējuma numurs V3.10.3.18 , un tas ir pieejams šādā grafikā:

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
