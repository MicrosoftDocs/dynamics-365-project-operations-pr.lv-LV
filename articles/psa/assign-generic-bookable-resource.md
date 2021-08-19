---
title: Vispārējo rezervējamo resursu piešķiršana uzdevumam un projekta darba grupai
description: Šajā tēmā ir sniegta informācija par vispārējo resursu rezervēšanu uzdevumiem un projektu darba grupām.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d9a81d7242e78dafad871bb07c03459f1de21884d196c6ee7dd9619b2c410404
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007110"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Vispārējo rezervējamo resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Papildus nosaukto vai reālo resursu rezervēšanas un piešķiršanas projektam, projekta uzdevumiem varat piešķirt vispārējos resursus. Šos resursus var izmantot kā vietturus nosauktajiem resursiem, līdz esat gatavs projektam piešķirt darbiniekus, izmantojot norādītos resursus. 

1. Programmā Project Service Automation (PSA) atveriet lapu **Projekts** un cilnē **Grafiks** ievadiet vispārējā resursa amata nosaukumu grafika šūnā **Resurss**. Vai arī noklikšķiniet uz ikonas **Resurss**, lai atvērtu resursu atlasītāju, un pēc tam ievadiet tā vispārējā resursa nosaukumu, ko vēlaties izveidot.

![Vispārējā darba grupas dalībnieka izveide un piešķiršana.](media/RM-how-to-9.png)

Šādi tiks atvērts panelis **Ātrā izveide: projekta darba grupas dalībnieks**. 

2. Ievadiet vispārējā resursu darba grupas dalībnieka lomu un organizācijas struktūrvienību un pēc tam noklikšķiniet uz **Saglabāt**.

![Vispārējā darba grupas dalībnieka ātrā izveide.](media/RM-how-to-10.png)

3. Pēc jaunā vispārējā resursu darba grupas dalībnieka izveidošanas tas tiek piešķirts uzdevumam. Šo vispārējo resursu varat turpināt piešķirt citiem uzdevumu grafikā esošajiem uzdevumiem.

![Esošu vispārējo darba grupas dalībnieku nozīmēšana uzdevumiem.](media/RM-how-to-11.png)

4. Pēc tam, kad ir piešķirts vispārējais resurss, varat ģenerēt resursu vajadzību un to izpildīt, tieši rezervējot vai iesniedzot resursa pieprasījumu resursu pārvaldniekā.

![Vajadzības ģenerēšana vispārējam darba grupas dalībniekam.](media/RM-how-to-12.png)

Darba grupas dalībnieku režģī varat ne tikai izmantot resursu atlasītāju, kā minēts iepriekš, bet varat arī tiešā veidā pievienot vispārējos resursus. Resursi tiek pievienoti, izmantojot resursu vajadzību, kuras pamatā ir sākuma/beigu datumi un piešķiršanas metode, kas norādīta panelī **Ātrā izveide: projekta darba grupas dalībnieks.**

Pastāv atšķirība, ja vispārējo darba grupas dalībnieku pievienojat tieši un pēc tam vispārējam resursam piešķirat vairāk uzdevumu, nekā tam ir pieejamas izpildei nepieciešamās stundas. Noklikšķiniet uz **Ģenerēt vajadzību**, lai atkārtoti ģenerētu vajadzību un līdzsvarotu nepieciešamās stundas ar piešķirēm.

Varat arī noklikšķināt uz saites **Resursu vajadzība** darba grupas režģī, lai atvērtu vajadzības un pievienotu prasmes, vēlamos resursus utt.

![Resursa prasība.](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]