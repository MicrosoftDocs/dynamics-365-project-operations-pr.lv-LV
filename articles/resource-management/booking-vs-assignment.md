---
title: Rezervēšana/piešķires
description: Šajā tēmā ir sniegta informācija par atšķirībām starp resursu rezervācijām un resursu piešķirēm.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841181"
---
# <a name="bookings-vs-assignments"></a>Rezervēšana/piešķires

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Rezervācijas ir resursu stingra vai viegla piešķiršana projektam. Stingrās rezervācijas patērē resursu noslodzi. Rezervācijas ir organizatoriska koncepcija darba grupām, lai tās varētu saprast, kā resursi tiks piesaistīti dažādiem projektiem. Dynamics 365 Project Operations apskata rezervācija kā projekta līmeņa jēdzienu. 

Atšķirībā no rezervācijām piešķires ir resursu piešķiršana projekta uzdevumiem projekta grafikā. Resursiem var piešķirt nosaukumus, vai tie var būt vispārēji.  Ja resursa prasību atvasina no projekta uzdevumu piešķirēm, Project Operations izmanto resursu piešķires darba kontūras, lai veidotu resursa pieprasījuma informācijas kontūras. Taču netiek saglabāta atsauce uz resursa piešķirēm. No resursa prasības iegūtu rezervāciju atjauninājumi neatjaunina resursu piešķires.

Parasti resursa rezervācijas summa būs vienāda ar resursa piešķiru summu vienā vai vairākos uzdevumos. Tomēr Project Operations neparedz šādu atbilstību kā obligātu. Skats **Saskaņošana** projektu vadītājiem parāda gadījumus, kad resursu rezervācijas neatbilst piešķirēm.


