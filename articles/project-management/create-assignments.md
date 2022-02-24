---
title: Resursu piešķiru izveidošana
description: Šajā tēmā ir sniegta informācija par vispārīgu un nosauktu resursu piešķiru izveidi.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 829c1d1de7270e7cafbb98ef80235ae6404f77f7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131757"
---
# <a name="create-resource-assignments"></a>Resursu piešķiru izveidošana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Resursu piešķire ir projekta darba grupas dalībnieka tieša saistība ar lapas mezgla uzdevumu. Šajā tēmā ir sniegta informācija par dažādajiem veidiem, kādos var piešķirt resursus.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vispārēja darba grupas dalībnieka izveide, izmantojot uzdevumu piešķiri


Izveidojot vispārēju darba grupas dalībnieku, izmantojot uzdevumu piešķiri, jūs izveidojat vietturi vai vispārēju resursu. Šis vispārējais resurss apraksta tā nosauktā resursa īpašības, kuram būtu vēlams strādāt pie uzdevumiem. Pēc tam jūs ģenerējat prasību vai iesniedzat pieprasījumu, izmantojot prasību, kas tiek izmantota nosauktā resursa meklēšanai un rezervēšanai.

1. Uzdevuma režģī Plānot šūnā **Resurss** atlasiet ikonu Resurss.
2. Ierakstiet nosaukumu, ko lietot kā viettura resursa nosaukumu. Piemēram, programmas vadītājs
3. Atlasiet vienumu **Izveidot** un pēc tam laukā **Projekta darba grupas dalībnieka ātrā izveide** iestatiet lomu vispārējam resursam.
4. Pēc vajadzības piešķiriet uzdevumus šim viettura resursam, atlasot resursu vienumā **Resursa atlase** šim uzdevumam. Resursi ir uzskaitīti sadaļā **Darba grupas dalībnieki**.
5. Kad esat pabeidzis vispārējā resursa piešķiršanu, atlasiet vispārējo resursu cilnē **Darba grupa** un atlasiet **Izveidot prasību**, lai izveidotu resursa prasību vispārējam resursam.
6. Vispārējam resursam atlasiet vienumu **Rezervēt** un pēc tam varat izmantot paneli Plānot, lai atrastu un rezervētu reālu resursu. Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam.
7. Kad vispārējais resurss ir pilnībā izpildīts (daļēja resursa prasības izpilde neveido resursa piešķiri) ar nosauktu resursu, vispārējais resurss tiek izņemts no darba grupas. Uzdevumu piešķires attiecībā uz vispārējo resursu tiek piešķirtas nosauktajam resursam, kas atbilst vispārējā resursa prasībai.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nosaukta resursa piešķiršana no visu rezervējamo resursu saraksta

Varat izmantot meklēšanas lodziņu **Resursu atlasītājs**, lai meklētu visus aktīvos rezervējamos resursus un piešķirtu tos jebkuram lapas mezgla uzdevumam. Šādā veidā piešķirtie resursi tiek pievienoti darba grupai bez jebkādām rezervācijām. Tas ir līdzīgi kā pievienot darba grupas dalībnieku un atlasīt **Nav** kā piešķiršanas metodi. Šis resurss cilnēs **Darba grupa**, **Resursa piešķiršana** un **Saskaņošana** tiek rādīts kā resursi, kuriem ir tikai piešķīrumi un rezervāciju trūkums. Ja vēlaties izmantot to pieejamību, rezervējiet tos.

1. Uzdevumu režģī, panelī vai laika skalā pārejiet uz šūnu **Piešķirts**.
2. Meklēšanas lodziņā sāciet rakstīt vārdu. Sadaļā **Resursu atlasītājs** pie **Citi resursi** tiek rādīti nosaukuma meklēšanas rezultāti.
3. Atlasiet resursu, kuru vēlaties piešķirt uzdevumam, vai atlasiet resursa nosaukumu sadaļā **Citiem darba grupas resursi**.
