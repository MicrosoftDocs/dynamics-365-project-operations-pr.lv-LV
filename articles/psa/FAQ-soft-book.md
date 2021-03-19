---
title: Pasīvā resursa rezervācija
description: Šajā tēmā ir sniegta informācija par to, kā varbūtēji ieplānot vai pasīvi rezervēt projekta darba grupas dalībniekus.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 1d2044692d1c6d694a1365be76dd8e7ddafd376d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285987"
---
# <a name="soft-book-a-resource"></a>Pasīvā resursa rezervācija

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Varat eksperimentāli plānot vai viegli rezervēt resursu projekta darba grupai, lai parādītu, ka plānojat piešķirt resursu projektam. Vieglās rezervācijas nepatērē resursa pieejamo noslodzi, un jūs varat piešķirt viegli rezervētos darba grupas dalībniekus projekta uzdevumiem. Tā kā vieglā rezervācija nepatērē resursa noslodzi, joprojām varat stingri rezervēt resursu citiem uzdevumus tādā pašā laika periodā. Vispārējos resursus nevar pasīvi rezervēt, un pasīvā rezervācija nevar izpildīt vispārīgā resursa pieprasījumu.

Pasīvi rezervētie projekta darba grupas dalībnieki ir uzskaitīti cilnē **Darba grupa** lapā **Projekts**, kur to pasīvi rezervētās stundas ir redzamas skata **Nosauktie darba grupas dalībnieki** kolonnā **Pasīvi rezervētās stundas** Pasīvi rezervētie darba grupas dalībnieki ir uzskaitīti arī plānošanas panelī. Tā kā tie ir rezervēti pasīvi, plānošanas panelī šiem resursiem netiek rādīts noslodzes patēriņš. Pasīvi rezervētais laiks neparādās cilnē **Saskaņošana**, ne ar laukā **Paplašinātās rezervācijas** plānošanas paneļa cilnē **Saskaņošana**. 

Darba grupas dalībnieku viegli rezervēt projektā var divējādi: tieši plānošanas panelī vai pievienojot darba grupas dalībnieku cilnē **Darba grupa**. 

## <a name="soft-book-from-the-schedule-board"></a>Pasīvā rezervēšana no plānošanas paneļa
Izpildiet tālāk aprakstītās darbības, lai pasīvi rezervētu resursu no plānošanas paneļa. 

1. Atveriet plānošanas paneli un pēc tam panelī **Rezervācijas prasības** atlasiet cilni **Projekts**.
2. Atrodiet projektu, kuram vēlaties pasīvi rezervēt resursu. Ja sarakstā ir daudz projektu, atlasiet **Projekts** kolonnas virsrakstu un pēc tam izmantojiet šo filtrēšanu, lai meklētu vienu vai vairākus projektus.
3. Noklikšķiniet uz projekta, pēc tam velciet un nometiet to resursa laika režģī.
5. Panelī **Izveidot resursa rezervāciju** pielāgojiet sākuma un beigu datumu, iestatiet **Rezervācijas statuss** uz **Pasīvs** un pēc tam iestatiet stundas. 
6. Noklikšķiniet uz **Rezervēt**. Tagad resurss projektā tiek rādīts cilnē **Darba grupa**. Skata **Nosauktais darba grupas dalībnieks** kolonnā **Pasīvi rezervētās stundas** tagad redzēsit pasīvi rezervētās stundas.

> [!NOTE]
> Ņemiet vērā, ka tagad varat piešķirt pasīvo rezervāciju uzdevumiem cilnē **Plānošana**. Cilnē **Saskaņošana** resursam tiek radīts rezervāciju trūkums attiecībā pret uzdevumu piešķiri, jo cilnē **Saskaņošana** tiek ņemtas vērā tikai stingrās rezervācijas. Varat izmantot līdzekli **Paplašinātās rezervācijas**, lai stingri rezervētu resursu un novērstu stingro rezervāciju trūkumu attiecībā pret resursu piešķīrumiem. Jums būs manuāli jāatceļ resursa vieglā rezervācija, izmantojot līdzekli **Uzturēt rezervācijas**.

## <a name="soft-book-on-the-team-tab"></a>Vieglā rezervācija cilnē Darba grupa

Varat pievienot darba grupas dalībniekus tieši cilnē **Darba grupa** un tad mainīt to rezervācijas statusu no **Stingri** uz **Pasīvi**, izmantojot līdzekli **Uzturēt rezervācijas**. Pievienojot darba grupas dalībnieku šādā veidā, tam vienmēr tiks veikta stingrā rezervācija, ja vien neatlasīsiet sadalījuma metodi kā **Nav**.

Lai izmantotu šo metodi, veiciet šādas darbības:

1. Lapas **Projekts** cilnē **Darba grupa** noklikšķiniet uz **Jauns**.
2. Atlasiet rezervējamo resursu, lomu, sākuma un beigu datumus.
3. Atlasiet piešķires metodi, kas nav **Nav**.
4. Atlasiet vienumu **Saglabāt**. Jūs redzēsit resursu režģī un tā stundas kolonnā **Stingri rezervētās stundas**.
5. Uzturiet resursa rezervāciju, atlasot vienumu **Uzturēt rezervācijas**.
6. Kad tiek atvērts plānošanas panelis, izvērsiet resursu, lai parādītu tā rezervācijas. Rezervācija būs norādīta kā **Stingra**.
7. Noklikšķiniet ar peles labo pogu un sadaļā **Mainīt statusu** atlasiet vienumu **Pasīvā rezervācija** \> **Pasīvā**. Rezervācijas statuss tagad ir **Pasīvā**.
8. Pēc plānošanas paneļa aizvēršanas redzēsiet, ka skatā **Nosauktie darba grupas dalībnieki** resursa stundas cilnes **Darba grupa** režģī ir pārvietotas no kolonnas **Stingri rezervētās stundas** uz kolonnu **Pasīvi rezervētās stundas**.

> [!NOTE]
> Stingri rezervējot resursu darba grupā un pēc tam piešķirot uzdevumus plānā, ja izmantojat līdzekli **Uzturēt rezervācijas**, lai mainītu statusu no **Stingra** uz **Pasīva**, šim resursam tiek saglabāti uzdevumu piešķīrumi. Tomēr cilnē **Saskaņošana** resursam būs rezervāciju trūkums, jo, saskaņojot rezervācijas ar piešķīrumiem, tiek ņemtas vērā tikai stingrās rezervācijas. Varat izmantot līdzekli **Rezervāciju paplašināšana** cilnē **Saskaņošana**, lai stingri rezervētu resursu un novērstu stingro rezervāciju trūkumu attiecībā pret resursu piešķīrumiem. Jums būs jāatceļ resursa vieglā rezervācija, izmantojot līdzekli **Uzturēt rezervācijas**.

Kad esat gatavs mainīt izvēles viegli rezervēto darba grupas dalībnieka resursu uz stingri rezervētu darba grupas dalībnieku, rīkojieties šādi:

1. Plānošanas panelī izvērsiet resursu, lai parādītu tā rezervācijas. Redzēsiet rezervāciju, kas atzīmēta kā **Pasīvā**.
2. Ar peles labo pogu noklikšķiniet uz rezervācijas, sadaļā **Mainīt statusu** atlasiet vienumu **Stingrā rezervācija** \> **Stingrā** Rezervācijas statuss tagad ir **Stingrā**.
3. Pēc plānošanas paneļa aizvēršanas un pāriešanas atpakaļ uz projektu,un cilnes **Darba grupa** atvēršanas redzēsiet, ka skatā **Nosauktie darba grupas dalībnieki** resursa stundas cilnē **Darba grupa** ir pārvietotas no kolonnas **Pasīvi rezervētās stundas** uz kolonnu **Stingri rezervētās stundas**. Ja resurss tika piešķirts uzdevumiem, tam vairs netiks rādīts rezervāciju trūkums cilnē **Saskaņošana**, jo tā rezervācijas tagad ir stingras.



[!INCLUDE[footer-include](../includes/footer-banner.md)]