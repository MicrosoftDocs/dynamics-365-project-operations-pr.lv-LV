---
title: Resursa piešķiršana uzdevumam
description: Šajā tēmā ir sniegta informācija par to, kā piešķirt resursus uzdevumiem.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150002"
---
# <a name="assign-a-resource-to-a-task"></a>Resursa piešķiršana uzdevumam

[!include [banner](../includes/psa-now-project-operations.md)]

Ir divi veidi, kā programmā Project Service resursu piešķirt uzdevumam risinājumā Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervējiet resursu kā darba grupas dalībnieku un pēc tam to piešķiriet uzdevumam

Varat pievienot resursu projekta darba grupai un pēc tam piešķirt uzdevumus resursam projekta grafikā.

1. Cilnē **Darba grupas dalībnieks** pievienojiet jaunu darba grupas dalībnieku, atlasot vienumu **Jauns**. 

2. Tiek atvērts panelis **Darba grupas dalībnieku ātrā izveide**, kur varat atlasīt rezervējamā resursa vārdu un iestatīt lomu. 

    Atlasiet kādu no šīm piešķiršanas metodēm resursa rezervēšanai:

    - **Pilna noslodze**: izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā (no sākuma līdz beigu datumam).
    - **Noslodzes procentuāla vērtība**: izmantojot šo metodi, tiek rezervēta resursa noslodzes procentuālā vertība norādītajā laika posmā (no sākuma līdz beigu datumam).
    - Vienums **Sadalīt vienmērīgi pa stundām**: rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā.
    - **Pa stundām — sākotnējā slodze**: rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā.
    - **Nav** pievieno resursu darba grupai, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi.

3. Uzdevuma režģa **Plānot** atlasiet ikonu **Resurss** resursa šūnā un pēc tam sadaļā **Darba grupas dalībnieki** atlasiet darba grupas dalībnieku, ko tikko pievienojāt. 

> [!NOTE]
> Ņemiet vērā, ka resursam gan cilnē **Darba grupas dalībnieks**, gan cilnē **Saskaņošana** tiek rādītas rezervētās stundas un piešķirtās stundas. Stundu skaitam ir jābūt vienādam, tomēr tā var nebūt, jo rezervācijas un piešķīrumi nav cieši saistīti. Cilnē **Saskaņošana** tiek sniegta informācija, ja šie rādītāji atšķiras, piemēram, ja piešķirat resursam vairāk stundu, nekā esat tam rezervējis. Pēc tam varat veikt korekcijas šajā informācija, paplašinot resursa rezervācijas vai mainot piešķīrumu.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vispārēja darba grupas dalībnieka izveide, izmantojot uzdevumu piešķiri

Veidojot vispārēju darba grupas dalībnieku, piešķirot uzdevumu, izveidojat vietturi vai vispārēju resursu, kas raksturo nosauktā resursa īpašības, kuras jums nepieciešamas darbam ar uzdevumiem. Pēc tam jūs ģenerējat prasību (vai iesniedzat pieprasījumu, izmantojot prasību), kas tiek izmantota nosauktā resursa meklēšanai un rezervēšanai.

1. Uzdevuma režģī **Plānot** resursa šūnā atlasiet ikonu **Resurss**.

2. Ierakstiet nosaukumu, ko lietot kā viettura resursa nosaukumu. Piemēram, programmas vadītājs

3. Atlasiet vienumu **Izveidot** un pēc tam laukā **Projekta darba grupas dalībnieka ātrā izveide** iestatiet lomu vispārējam resursam.

4. Varat turpināt piešķirt uzdevumus šim viettura resursam, atlasot vienumu **Resursa atlase** uzdevumam. Tie ir uzskaitīti sadaļā **Darba grupas dalībnieki**.

5. Kad esat pabeidzis vispārējā resursa piešķiršanu, atlasiet vispārējo resursu cilnē **Darba grupa** un atlasiet **Izveidot prasību**, lai izveidotu resursa prasību vispārējam resursam.

6. Vispārejam resursam atlasiet **Rezervēt**. Pēc tam varat izmantot plānošanas paneli, lai atrastu un rezervētu reālu resursu. Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam.

7. Kad vispārējais resurss ir aizpildīts ar nosauktu resursu, vispārējais resurss tiek noņemts no darba grupas un vispārējam resursam piešķirtie uzdevumi tiek piešķirti nosauktajam resursu, kas izpildīja vispārējā resursa prasības.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nosaukta resursa piešķiršana no visu rezervējamo resursu saraksta

Varat izmantot meklēšanas lodziņu **Resursu atlasītājs**, lai meklētu visus rezervējamos resursus un piešķirtu tos uzdevumam.

Šādā veidā piešķirtie resursi tiek pievienoti darba grupai bez jebkādām rezervācijām. Tas ir līdzīgi kā pievienot darba grupas dalībnieku un atlasot Nav kā piešķiršanas metodi. Šis resurss cilnē **Darba grupa** un cilnē **Saskaņošana** tiek rādīti kā resursi, kuriem ir tikai piešķīrumi un rezervāciju trūkums. Ja vēlaties izmantot to pieejamību, rezervējiet tos.

1. Uzdevuma režģī **Plānot** resursa šūnā atlasiet ikonu **Resurss**.

2. Sāciet rakstīt nosaukumu. Sadaļā **Resursu atlasītājs** pie **Citi resursi** tiek rādīti nosaukuma meklēšanas rezultāti.

3. Sarakstā atlasiet resursu, kuru vēlaties piešķirt uzdevumam.

