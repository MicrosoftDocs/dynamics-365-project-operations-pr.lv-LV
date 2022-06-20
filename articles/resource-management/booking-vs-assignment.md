---
title: Rezervēšana/piešķires
description: Šajā rakstā ir sniegta informācija par atšķirībām starp resursu rezervācijām un resursu piešķirēm.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918597"
---
# <a name="bookings-vs-assignments"></a>Rezervēšana/piešķires

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Rezervācijas ir resursu stingra vai viegla piešķiršana projektam. Stingrās rezervācijas patērē resursu noslodzi. Rezervācijas ir organizatoriska koncepcija darba grupām, lai tās varētu saprast, kā resursi tiks piesaistīti dažādiem projektiem. Dynamics 365 Project Operations apskata rezervācija kā projekta līmeņa jēdzienu. 

Atšķirībā no rezervācijām piešķires ir resursu piešķiršana projekta uzdevumiem projekta grafikā. Resursiem var piešķirt nosaukumus, vai tie var būt vispārēji.  Ja resursa prasību atvasina no projekta uzdevumu piešķirēm, Project Operations izmanto resursu piešķires darba kontūras, lai veidotu resursa pieprasījuma informācijas kontūras. Taču netiek saglabāta atsauce uz resursa piešķirēm. No resursa prasības iegūtu rezervāciju atjauninājumi neatjaunina resursu piešķires.

Parasti resursa rezervācijas summa būs vienāda ar resursa piešķiru summu vienā vai vairākos uzdevumos. Tomēr Project Operations neparedz šādu atbilstību kā obligātu. Skats **Saskaņošana** projektu vadītājiem parāda gadījumus, kad resursu rezervācijas neatbilst piešķirēm.




[!INCLUDE[footer-include](../includes/footer-banner.md)]