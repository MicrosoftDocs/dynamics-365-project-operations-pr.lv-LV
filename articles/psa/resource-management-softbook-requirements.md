---
title: Vajadzību viegla rezervēšana
description: Šajā tēmā ir sniegta informācija par to, kā viegli rezervēt vajadzības.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080654"
---
# <a name="soft-book-requirements"></a>Vajadzību viegla rezervēšana

Resursu vajadzību var viegli rezervēt. Stingrā rezervēšana izveido piedāvājumu, kas patērē resursa noslodzi. Pēc tam šis piedāvājums tiek nosūtīts atpakaļ prasītājam apstiprināšanai. Vieglā rezervācija veic resursa pagaidu pievienošanu projekta darba grupai, un tai ir cits statuss plānošanas panelī, taču tā nepatērē resursa noslodzi. Lai veiktu vieglu resursa rezervēšanu, izmantojot plānošanas paneli, iestatiet laukam **Rezervācijas statuss** vienumu **Viegla**.

![Rezervācijas statusam iestatīta opcija Viegla](media/Resource-Management-image77.png)

Kad cilnē **Darba grupa** ir atvērts skats **Nosaukti darba grupas dalībnieki** , šis resurss tiek parādīts tur. Viegli rezervētās stundas ir norādītas kolonnā **Viegli rezervētās stundas**.

![Viegli rezervētās stundas skatā Nosaukti darba grupas dalībnieki](media/Resource-Management-image78.png)

Viegli rezervētos darba grupas dalībniekus var nozīmēt uzdevumiem.

![Viegli rezervētie darba grupas dalībnieki nozīmēti uzdevumam](media/Resource-Management-image79.png)

Cilnē **Saskaņošana** netiek rādītas viegli rezervēto resursu rezervācijas, jo cilnē **Saskaņošana** tiek ņemtas vērā tikai stingrās rezervācijas.

![Viegli rezervēts resurss bez rezervācijām cilnē Saskaņošana](media/Resource-Management-image80.png)

> [!NOTE]
> Nevar veikt vieglu resursa rezervēšanu no vajadzības, kas ģenerēta no vispārēja darba grupas dalībnieka.

Plānošanas panelī resursa vieglai rezervācijai tiek izmantotas citas krāsas.

![Vieglā rezervēšana plānošanas panelī](media/Resource-Management-image81.png)

Lai vieglo rezervāciju pārveidotu par stingro rezervāciju, plānošanas panelī ar peles labo pogu noklikšķiniet uz vieglās rezervācijas un pēc tam atlasiet vienumu **Mainīt statusu** \> **Stingrā rezervācija** \> **Stingrā**.

![Rezervācijas statusa mainīšana uz iestatījumu Stingrā](media/Resource-Management-image82.png)

Rezervācija ir mainīta, un tās statuss ir mainīts plānošanas panelī. Tā kā rezervācijas statuss tagad ir **Stingrā** , resurss tiek parādīts kā rezervēts un tā noslodze un pieejamība tiek pielāgota.

Varat izmantot to pašu metodi, lai atceltu stingro rezervāciju vai vieglo rezervāciju, izmantojot plānošanas paneli.

Lai pārveidotu resursu, kam veikta viegla rezervācija, uz stingro rezervāciju projekta cilnē **Darba grupa** , atlasiet resursu un pēc tam atlasiet **Apstiprināt**.

![Komanda Apstiprināt](media/Resource-Management-image83.png)
