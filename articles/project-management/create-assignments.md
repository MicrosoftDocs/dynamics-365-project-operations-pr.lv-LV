---
title: Resursu piešķiru izveidošana
description: Šajā rakstā ir sniegta informācija par vispārīgu un nosauktu resursu piešķiru izveidi.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812003"
---
# <a name="create-resource-assignments"></a>Resursu piešķiru izveidošana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Resursu piešķire ir projekta darba grupas dalībnieka tieša saistība ar lapas mezgla uzdevumu. Šajā rakstā ir sniegta informācija par dažādajiem veidiem, kādos var piešķirt resursus.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vispārēja darba grupas dalībnieka izveide, izmantojot uzdevumu piešķiri


Izveidojot vispārēju darba grupas dalībnieku, izmantojot uzdevumu piešķiri, jūs izveidojat vietturi vai vispārēju resursu. Šis vispārīgais resurss apraksta tā nosauktā resursa īpašības, ar kuru galu galā vēlaties strādāt pie uzdevumiem. Pēc tam ģenerējat prasību vai iesniedzat pieprasījumu, izmantojot vajadzību, kas tiek izmantota, lai meklētu un rezervētu nosaukto resursu.

1. Uzdevuma režģī Plānot šūnā **Resurss** atlasiet ikonu Resurss.
2. Ierakstiet nosaukumu, kas kalpo kā viettura resursa nosaukums. Piemēram, programmas vadītājs
3. Atlasiet vienumu **Izveidot** un pēc tam laukā **Projekta darba grupas dalībnieka ātrā izveide** iestatiet lomu vispārējam resursam.
4. Pēc vajadzības piešķiriet uzdevumus šim viettura resursam, atlasot resursu vienumā **Resursa atlase** šim uzdevumam. Resursi ir uzskaitīti sadaļā **Darba grupas dalībnieki**.
5. Kad esat pabeidzis piešķirt vispārīgo resursu, cilnē Darba grupa **atlasiet vispārīgo resursu un pēc tam atlasiet** Ģenerēt vajadzību **,** lai izveidotu resursu vajadzību vispārējam resursam.
6. Vispārējam resursam atlasiet vienumu **Rezervēt** un pēc tam varat izmantot paneli Plānot, lai atrastu un rezervētu reālu resursu. Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam.
7. Kad vispārējais resurss ir pilnībā izpildīts ar nosauktu resursu, vispārējais resurss tiek noņemts no darba grupas. (Daļējas resursu prasības izpildes rezultātā netiks izveidota resursu piešķiršana.) Vispārīgā resursa uzdevumu piešķires tiek piešķirtas nosauktajam resursam, kas izpildīja vispārējā resursa resursu prasību.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nosaukta resursa piešķiršana no visu rezervējamo resursu saraksta

Varat izmantot meklēšanas lodziņu **Resursu atlasītājs**, lai meklētu visus aktīvos rezervējamos resursus un piešķirtu tos jebkuram lapas mezgla uzdevumam. Šādā veidā piešķirtie resursi tiek pievienoti darba grupai bez jebkādām rezervācijām. Tas ir līdzīgi kā pievienot darba grupas dalībnieku un atlasīt **Nav** kā piešķiršanas metodi. Šis resurss cilnēs **Darba grupa**, **Resursa piešķiršana** un **Saskaņošana** tiek rādīts kā resursi, kuriem ir tikai piešķīrumi un rezervāciju trūkums. Ja vēlaties izmantot to pieejamību, rezervējiet tos.

1. Uzdevumu režģī, panelī vai laika skalā pārejiet uz šūnu **Piešķirts**.
2. Meklēšanas lodziņā sāciet rakstīt vārdu. Sadaļā **Resursu atlasītājs** pie **Citi resursi** tiek rādīti nosaukuma meklēšanas rezultāti.
3. Atlasiet resursu, kuru vēlaties piešķirt uzdevumam, vai atlasiet resursa nosaukumu sadaļā **Citiem darba grupas resursi**.

## <a name="editing-resource-assignment-contours"></a>Resursu piešķiršanas kontūru rediģēšana

Pēc noklusējuma, kad resursi tiek piešķirti uzdevumam grafikā, to centieni tiek lineāri sadalīti katram resursam, pamatojoties uz šī resursa darba stundām un projekta grafika režīmu. Projektu vadītājs var izmantot resursu piešķiršanas režģi, lai precizētu piepūles aprēķinus katram resursam, kas ir piešķirts vienam vai vairākiem uzdevumiem dažādās laika skalās. Šis līdzeklis palīdz projektu vadītājiem sagatavot precīzākus izmaksu un pārdošanas aprēķinus, kuru pamatā ir resursu piešķiršanas kontūras, kas tiek ģenerētas, kad resurss tiek piešķirts uzdevumam. Turklāt projektu vadītāji var vieglāk atspoguļot resursu pieprasījumu, kas nepieciešams, lai izveidotu pieprasījumu resursu prasībās.

### <a name="navigation"></a>Navigācija

Lai piekļūtu kontūru rediģēšanas režģim, projekta vadītājs vispirms atlasa cilni Uzdevumi projekta galvenajā lapā un pēc tam atlasa **cilni** Uzdevumi **·** .

![Cilne Uzdevumi projekta galvenās lapas cilnē Uzdevumi.](media/AssignmentGrid.png)

Režģis atbalsta divas grupēšanas metodes: **grupa pēc resursa** un **grupa pēc uzdevuma**. Atšķirībā no režģa skata kolonnas nav konfigurējamas. Vienīgās redzamās kolonnas ir **Piešķirts**, Uzdevuma nosaukums, Uzdevuma **sākums**, **·** **Piešķires pabeigšana** un **Uzdevuma piepūle.**

Kad režģis sākotnēji tiek atveidots, tas sākas ar agrāko uzdevuma kontūru. Ja jūsu grafikā nav nevienas piešķires, kas ir piepūlējusies, režģis būs tukšs un neko neatveidos.

![Tukšs piešķires režģis.](media/emptyassignmentgrid.png)

Ja vēlaties skatīt kontūras un dažādas laika skalas, ir pieejams arī tikai lasāms resursu piešķiršanas režģis un resursu saskaņošanas režģis.

### <a name="resource-calendars"></a>Resursu kalendāri

Iespēju rediģēt kontūru konkrētai dienai nosaka resursa darba dienas, kā tas atspoguļots to kalendārā. Ja šūna ir atspējota noteiktam resursam, šim resursam šajā periodā nav darba dienu.

Resursa kontūras var pārsniegt piešķirtā uzdevuma pašreizējo sākuma un beigu datumu. Ja kontūra tiek atjaunināta tā, lai tā būtu pēc uzdevuma pēdējā beigu datuma vai agrākā uzdevuma sākuma datuma, uzdevuma beigu datums vai sākuma datums tiks attiecīgi mainīts. Tomēr, ja kontūra tiek atjaunināta tā, ka tā ir vecāka par tāda uzdevuma sākuma datumu, kas ir saistīts ar priekšgājēju, atjauninājums neizdosies, jo uzdevums aktivizēs uzdevuma sākšanu pirms tā priekšgājēja pabeigšanas, un šī darbība pašlaik netiek atbalstīta.

### <a name="co-authoring"></a>Koprediģēšana

Resursu piešķiršanas režģa izmaiņas tiek automātiski atspoguļotas visos saistītajos skatos, tostarp diagrammas, laika grafika, paneļa un režģa skatos. Ja projektu vienlaikus pārskata vairāki lietotāji, visas viena lietotāja veiktās izmaiņas tiks atspoguļotas režģī. Savukārt visas resursu piešķiršanas režģī veiktās izmaiņas tiks rādītas visiem pārējiem lietotājiem, kuri skata projektu tajā pašā sesijā.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
