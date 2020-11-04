---
title: Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana
description: Šajā tēmā ir sniegta informācija par to, kā rezervēt nosauktos resursus projekta darba grupām un piešķirt tās uzdevumiem.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080563"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta darba grupai varat pievienot nosauktu resursu, to tieši rezervējot darba grupai. Lai to paveiktu, izpildiet tālāk norādītās darbības.

1. Programmā Project Service Automation dodieties uz sadaļu **Projekti** un atveriet projektu, kam veicat rezervāciju.
2. Lapas **Projekts** cilnē **Darba grupa** noklikšķiniet uz **Jauns**. 

![Darba grupas dalībnieka pievienošana no darba grupas cilnes](media/RM-how-to-1.png)

3. Dialoglodziņā **Ātrā izveide: projekta darba grupas dalībnieks** atlasiet rezervējamo resursu. Lauks **Loma** tiks aizpildīts ar resursa noklusējuma lomu, ja tam tā ir piešķirta. Ja nepieciešams, lomu var mainīt. 
4. Atlasiet, no kura datuma līdz kuram resurss būs nepieciešams, un atlasiet resursa noslodzes piešķiršanas metodi. 
5. Ja vēlaties, lai darba grupas dalībnieks būtu projekta apstiprinātājs, atlasiet **Jā** laukā **Projekta apstiprinātājs**. Tas nozīmē, ka darba grupas dalībnieks var apstiprināt šim projektam iesniegtos laika un izdevumu ierakstus. 
6. Noklikšķiniet uz **Saglabāt**.

![Darba grupas dalībnieka pievienošana ātrās izveides veidlapā](media/RM-how-to-2.png)


Tagad rezervēto resursu varat piešķirt projekta uzdevumiem. Lapā **Projekts** noklikšķiniet uz cilnes **Grafiks** , lai jaunajam resursam piešķirtu uzdevumus. Resursu atlasītājā, kas palaists no uzdevumu režģa lauka **Resursi** , tiks parādīti darba grupas dalībnieki, kurus varat atlasīt.

![Darba grupas dalībnieka piešķiršana uzdevumam grafika cilnē](media/RM-how-to-3.png)

Project Service Automation (PSA) 3. versijā resursu rezervācijas un uzdevumu piešķires nav cieši savienotas. Tas nozīmē, ka tad, kad grafikā izmantojat resursu atlasītāju, darba grupas dalībniekiem varat piešķirt uzdevumus ar stundu skaitu, kas pārsniedz to rezervācijas projektā.
Atšķirības starp darba grupas dalībnieku rezervācijām un piešķirēm varat skatīt cilnē **Darba grupa** vai cilnē **Resursu saskaņošana**. Atšķirības starp resursu rezervācijām un piešķirēm varat saskaņot arī detalizētākā līmenī.

![Cilne Resursu saskaņošana](media/RM-how-to-4.png)

Varat arī izmantot resursu atlasītāju cilnē **Grafiks** , lai meklētu un atlasītu rezervējamos resursus, kas vēl nav daļa no projekta darba grupas. Tie tiek parādīti resursu atlasītājā kā **Citi resursi**.

![Darba grupā neiekļauta dalībnieka resursa piešķiršana uzdevumam](media/RM-how-to-5.png)

Veicot šo darbību, resurss tiek pievienots projekta darba grupai un piešķirts uzdevumam, taču netiek ģenerētas rezervācijas.

![Darba grupas dalībnieks ar piešķirēm un bez rezervācijām](media/RM-how-to-6.png)

Varat izmantot cilnes **Saskaņošana** rezervācijas paplašināšanas iespēju vai vienumu **Plānošanas panelis** , lai rezervētu resursa noslodzi uz projektā.

![Rezervāciju paplašināšana darba grupas dalībniekam resursu saskaņošanas cilnē](media/RM-how-to-7.png)

Pēc tam, kad darba grupas dalībnieks ir rezervēts projektā, varat izmantot rezervāciju uzturēšanas iespēju vai vienumu Plānošanas panelis, lai tiešā veidā pārvaldītu to rezervācijas.
