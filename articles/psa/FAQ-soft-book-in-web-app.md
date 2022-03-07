---
title: Kā es varu "viegli rezervēt" resursus programmas versijā 2.x?
description: Šajā rakstā ir izklāstīts, kā programmā Project Service viegli rezervēt projekta darba grupas dalībniekus.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d7eb9e3baea3c3f696845905a2522940d14bba8a8d42917f8fe1b90c7c443747
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993925"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kā viegli rezervēt resursus tīmekļa programmā (Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Varat eksperimentāli plānot vai viegli rezervēt resursu projekta darba grupai, lai parādītu, ka plānojat piešķirt resursu projektam. Vieglās rezervācijas nepatērē resursa pieejamo noslodzi. Darba grupas dalībniekus, kas ir viegli rezervēti, nevar piešķirt projekta uzdevumiem. Tikai resursus ar statusu “Stingri rezervēts” un saistību tipu “Saistīts” var piešķirt uzdevumiem (pieņemot, ka resursam ir pietiekami daudz stingrās rezervācijas stundu, lai segtu piešķiršanu).

Viegli rezervētie projekta darba grupas dalībnieki tiek parādīti darba grupas dalībnieku režģī, bet viegli rezervētās stundas tiek rādītas kolonnā Vieglā rezervācija. Tie parādās arī plānošanas panelī. Tas nenorāda noslodzes patēriņu, jo vieglā rezervācija nepatērē resursa noslodzi.

Ir trīs veidi, kā viegli rezervēt darba grupas dalībnieku projektam programmā Project Service version 2.x. Jūs varat veikt vieglo rezervāciju plānošanas panelī, izmantot līdzekli Uzturēt rezervācijas vai izveidot vispārēju resursu. Šīs metodes ir aprakstītas tālāk.

## <a name="soft-book-with-the-schedule-board"></a>Vieglā rezervēšana plānošanas panelī

Lai veiktu vieglo rezervēšanu plānošanas panelī, rīkojieties šādi: 
1. Atveriet plānošanas paneli.
2. Plānošanas paneļa rezervēšanas prasību paneļa apakšdaļā atlasiet cilni Projekts.
3. Atrodiet projektu, kuram vēlaties viegli rezervēt resursu. Ja jums ir daudz projektu, noklikšķiniet uz kolonnas Projekts virsraksta un pēc tam lietojiet filtru, lai atrastu savu projektu.
4. Noklikšķiniet uz projekta, pēc tam velciet un nometiet to resursa laika režģī.
5. Labajā pusē tiek atvērts panelis Resursa rezervācijas izveide. Pielāgojiet sākuma un beigu datumu, atlasiet rezervācijas statusu kā Viegls un iestatiet stundas. 
6. Noklikšķiniet uz Rezervēt.
7. Tagad projektā resurss tiks rādīts kā darba grupas dalībnieks ar viegli rezervētam stundām kolonnā Vieglā rezervācija.

Ņemiet vērā, ka nevarat piešķirt resursam uzdevumus darba sadalījuma struktūrā (WBS), jo resursiem ir jābūt stingri rezervētiem darba grupā, lai to varētu piešķirt.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Vieglā rezervēšana, izmantojot līdzekli Uzturēt rezervācijas

Lai veiktu vieglo rezervēšanu, izmantojot līdzekli Uzturēt rezervācijas, rīkojieties šādi:
1. Darba grupas dalībnieku režģī noklikšķiniet uz Jauns.
2. Atlasiet rezervējamo resursu, lomu, sākuma/beigu datumus.
3. Atlasiet sadalījuma metodi, kas nav Neviena:
- Pilna noslodze
- Noslodzes procentuālā vērtība
- Sadalīt vienmērīgi pa stundām
- Pa stundām — sākotnējā slodze
4. Noklikšķiniet uz Saglabāt. Jūs redzēsit resursu darba grupas režģī un stundas, kas norādītas kā Stingras.
5. Uzturiet resursa rezervāciju, noklikšķinot uz Uzturēt rezervācijas.
6. Kad tiek atvērts plānošanas panelis, izvērsiet resursu, lai parādītu tā rezervācijas. TIks parādīta rezervācija, kas norādīta kā Stingra.
7. Ar peles labo pogu noklikšķiniet uz rezervācijas, sadaļā Mainīt statusu atlasiet vienumu Vieglā rezervācija un pēc tam atlasiet Viegla. Rezervācijas statuss tagad ir Viegla.
8. Pēc plānošanas paneļa aizvēršanas redzēsit, ka resursa stundas darba grupas dalībnieku režģī ir mainījušās no Stingra uz Viegla.
Ņemiet vērā, ka stingri rezervējot resursu darba grupā un pēc tam piešķirot uzdevumus WBS, ja izmantojat līdzekli Uzturēt rezervācijas, lai mainītu statusu no Stingra uz Viegla, šim resursam tiks noņemta uzdevumu piešķire, jo uzdevumiem var piešķirt tikai stingri rezervētos resursus.

## <a name="soft-book-by-creating-a-generic-resource"></a>Vieglā rezervācija, izveidojot vispārējo resursu

Vart izveidot vieglo rezervāciju, izveidojot vispārēju resursu darba grupas dalībnieku, aiizpildot plānošanas panelī vai resursu pieprasījumā un mainot veidu rezervācijas laikā.
Lai to paveiktu, rīkojieties šādi:

1. Projekta WBS piešķiriet lomas uzdevumiem, kuriem vēlaties izveidot vispārējos darba grupas dalībiniekus.
2. Noklikšķiniet uz Izveidot projekta darba grupu.
3. Projekta darba grupas dalībnieku režģī atlasiet vispārējo resursu un noklikšķiniet uz Rezervēt.
4. Plānošanas panelī atlasiet resursu, kuru vēlaties rezervēt.
5. Plānošanas paneļa panelī Resursa rezervācijas izveide mainiet rezervācijas statusu uz Viegla.
6. Noklikšķiniet uz grāmatas Rezervēt un Iziet.

Pēc plānošanas paneļa aizvēršanas jūs redzēsiet atlasīto resursu pievienotu darba grupai ar viegli rezervētām stundas, kā arī piešķirtām stundām. Turklāt tiks rādīts, ka vispārējais resurss paliek darba grupā, norādot, ka uzdevumi ir piešķirti viegli rezervētam darba grupas dalībniekam.

Kad esat gatavs mainīt izvēles viegli rezervēto darba grupas dalībnieka resursu uz stingri rezervētu darba grupas dalībnieku, lai tam varētu piešķirt uzdevumus, rīkojieties šādi:

1. Atlasiet resursu un noklikšķiniet uz Uzturēt rezervācijas.
2. Kad tiek atvērts plānošanas panelis, izvērsiet resursu, lai parādītu tā rezervācijas. Jūs redzēsiet rezervāciju atzīmētu kā Viegla.
3. Ar peles labo pogu noklikšķiniet uz rezervācijas, sadaļā Mainīt statusu atlasiet vienumu Stingrā rezervācija un pēc tam atlasiet Stingra. Rezervācijas statuss tagad ir Stingra.
4. Pēc plānošanas paneļa aizvēršanas redzēsit, ka resursa stundas darba grupas dalībnieku režģī ir mainījušās no Viegla uz Stingra. Tagad varat piešķirt resursam uzdevumus (ja piešķiršanai uzdevumam nav līdzinājuma starp stingri rezervētajām stundām un ieguldījuma stundām). Ņemiet vērā: ja veicāt vispārējās resursu izpildes darbības iepriekš minētajā 3. punktā, mainot rezervējamā resursa, kurš ir viegli rezervēts, statusu uz Stingrs, vispārējais grupas dalībnieks tiek noņemts no darba grupas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]