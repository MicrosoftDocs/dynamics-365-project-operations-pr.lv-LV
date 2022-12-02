---
title: Vajadzību viegla rezervēšana
description: Šajā rakstā ir sniegta informācija par to, kā viegli rezervēt vajadzības.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8192047639823bc594803d6d10759be28f6db3ed
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928947"
---
# <a name="soft-book-requirements"></a>Vajadzību viegla rezervēšana

[!include [banner](../includes/psa-now-project-operations.md)]

Resursu vajadzību var viegli rezervēt. Stingrā rezervēšana izveido piedāvājumu, kas patērē resursa noslodzi. Pēc tam šis piedāvājums tiek nosūtīts atpakaļ prasītājam apstiprināšanai. Vieglā rezervācija veic resursa pagaidu pievienošanu projekta darba grupai, un tai ir cits statuss plānošanas panelī, taču tā nepatērē resursa noslodzi. Lai veiktu vieglu resursa rezervēšanu, izmantojot plānošanas paneli, iestatiet laukam **Rezervācijas statuss** vienumu **Viegla**.

![Rezervācijas statusam iestatīta opcija Viegla.](media/Resource-Management-image77.png)

Kad cilnē **Darba grupa** ir atvērts skats **Nosaukti darba grupas dalībnieki**, šis resurss tiek parādīts tur. Viegli rezervētās stundas ir norādītas kolonnā **Viegli rezervētās stundas**.

![Viegli rezervētās stundas skatā Nosaukti darba grupas dalībnieki.](media/Resource-Management-image78.png)

Viegli rezervētos darba grupas dalībniekus var nozīmēt uzdevumiem.

![Viegli rezervētie darba grupas dalībnieki nozīmēti uzdevumam.](media/Resource-Management-image79.png)

Cilnē **Saskaņošana** netiek rādītas viegli rezervēto resursu rezervācijas, jo cilnē **Saskaņošana** tiek ņemtas vērā tikai stingrās rezervācijas.

![Viegli rezervēts resurss bez rezervācijām cilnē Saskaņošana.](media/Resource-Management-image80.png)

> [!NOTE]
> Nevar veikt vieglu resursa rezervēšanu no vajadzības, kas ģenerēta no vispārēja darba grupas dalībnieka.

Plānošanas panelī resursa vieglai rezervācijai tiek izmantotas citas krāsas.

![Vieglā rezervēšana plānošanas panelī.](media/Resource-Management-image81.png)

Lai vieglo rezervāciju pārveidotu par stingro rezervāciju, plānošanas panelī ar peles labo pogu noklikšķiniet uz vieglās rezervācijas un pēc tam atlasiet vienumu **Mainīt statusu** \> **Stingrā rezervācija** \> **Stingrā**.

![Rezervācijas statusa mainīšana uz iestatījumu Stingrā.](media/Resource-Management-image82.png)

Rezervācija ir mainīta, un tās statuss ir mainīts plānošanas panelī. Tā kā rezervācijas statuss tagad ir **Stingrā**, resurss tiek parādīts kā rezervēts un tā noslodze un pieejamība tiek pielāgota.

Varat izmantot to pašu metodi, lai atceltu stingro rezervāciju vai vieglo rezervāciju, izmantojot plānošanas paneli.

Lai pārveidotu resursu, kam veikta viegla rezervācija, uz stingro rezervāciju projekta cilnē **Darba grupa**, atlasiet resursu un pēc tam atlasiet **Apstiprināt**.

![Komanda Apstiprināt.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
