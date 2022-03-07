---
title: Izveidot jaunu projektu
description: Šajā tēmā ir sniegta informācija par to, kā izveidot jaunu projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985960"
---
# <a name="create-a-new-project"></a>Izveidot jaunu projektu

[!include [banner](../includes/banner.md)]

Lai izveidotu jaunu projektu, izpildiet tālāk aprakstītās darbības.

1. Lapā **Projektu pārvaldība** atlasiet **Jauns projekts** un ievadiet šādas vērtības:

    - **Projekta veids:** Laiks un materiāls
    - **Projekta nosaukums:** XYZ Jaunināšanas fāze 2
    - **Projekta grupa:** TM\_WIP
    - **Projekta līguma ID:** 00000002

2. Atlasiet **Izveidot projektu**.

## <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1. Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēja ierakstu, kuram iepriekš iestatījāt kompetences, un atveriet darba ņēmēja ierakstu.
2. Darbību rūts cilnes **Projekts** grupā **Kompetences** atlasiet **Piešķirt projektus**.
3. Lapas **Resursu validācijas projekta piešķire** cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet projektu **XYZ Jaunināšanas fāze 2**.
4. Rūtī **Atlikušie projekti** atlasiet projektu un pēc tam atlasiet bulttaustiņu, lai to pievienotu rūtij **Atlasītie projekti**.

Varat arī pēc nepieciešamības resursam piešķirt kategorijas. Kategorijas veids ir vai nu **Izmaksas** vai **Ieņēmumi**. Kategorijas veidu nosaka jūsu organizācija. Ja resursam netiek piešķirtas kategorijas, Finance uzmeklē noklusējuma kategoriju izmaksu un ieņēmumu stundu cenām.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu raksturlielumu iestatīšana

Projekta vadītājs var izmantot projekta resursu funkcionalitāti, lai izveidotu projektam nepieciešamās lomas. Lomas var izmantot, ja apstiprinātie resursi joprojām nav zināmi, kad resursi tiek rezervēti. Lomas var īslaicīgi rezervēt kā plānotos resursu, lai varat turpināt projekta plānošanas posmus.

[![Lomas piemērs.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** uzņēmums Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kam ir apstiprināts projekta darba plāns. Jaunākais projekta vadītājs joprojām izpilda projekta tvērumu. Resursu pārvaldnieks pašlaik identificē konkrētus resursus, kuri tiks rezervēti darbam projektā. Projekta būtiskā rakstura dēļ projekta sponsors pieprasīja Vecāko projekta pārvaldnieku kā vienu no lomām. Resursu pārvaldniekam ir jāiegūst jaunais resurss un jādefinē loma sistēmā gadījumā, ja jaunākajam projekta pārvaldniekam projekta plānošanas laikā ir nepieciešama resursa informācija.

Tālāk minētajās darbībās parādīts, kā resursu pārvaldnieks var iestatīt vecākā projekta vadītāja lomu un ar to saistīt resursa raksturlielumus. Pēc tam lomu var izmantot, lai meklētu pieejamos resursus, kuri atbilst nepieciešamajām resursu kompetencēm.

1. Lapā **Lomu iestatīšana** atlasiet **Jauna** un ievadiet šādas vērtības:

    - **Lomas ID:** Vecākais projekta vadītājs
    - **Apraksts:** Vecākais projekta vadītājs

2. Atlasiet **Izveidot**.
3. Atlasiet lomu **Vecākais projekta vadītājs** un pēc tam atlasiet **Konfigurēt raksturlielumus**.
4. Laukā **Raksturlielumu veids** atlasiet **Prasme**.
5. Laukā **Pieejamie raksturlielumi** ievadiet meklējamo prasmi.
6. Laukā **Raksturlieluma veids** atlasiet **Sertifikāts**.
7. Laukā **Pieejamie raksturlielumi** ievadiet meklējamo sertifikāta veidu.

## <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1. Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.
2. Cilnē **Projekta komanda un plānošana** atlasiet **Pievienot**.
3. Laukā **Loma** atlasiet **Darba grupas dalībnieks**.
4. Atlasiet **Rezervēt no kalendāra**.
5. Lapā **Resursu pieejamība** atlasiet **Skatīt iestatījumus**.
6. Lapā **Pielāgot skata iestatījumus** ievadiet šādas vērtības:

    - **Datu diapazona skata formāts:** Diena
    - **Rādīt pieejamības aprakstus:** Jā
    - **Rādīt atlikušo noslodzi:** Jā

7. Resursu sarakstā atlasiet resursu.
8. Atlasiet **Stingrā rezervācija** un **Pilnā noslodze**.

## <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu, projekta vai resursa pārvaldnieki var sīkāk skatīt resursus, kurus var rezervēt projektam. Noklusējuma lomu varat saistīt ar esošu resursu vai nesen iegūtu resursu. Piemēram, kad tika nolīgts Daniels, viņam bija pieredze un prasmes biznesa analītiķa lomas pildīšanai. Resursu pārvaldnieks šo lomu piešķīra kā Daniela noklusējuma lomu. Tāpēc resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam ar projektiem.

Resursa rezervācijas laikā projektu pārvaldnieki var filtrēt darbam ar projektiem pieejamos lomu resursus. Šo informāciju viņi var izmantot kā vienu kritēriju, resursu izpildes laikā veicot daudzkritēriju lēmumu analīzi. Viņi var arī pievienot filtram citus resursa raksturlielumus, lai meklētu resursus, kam ir īpašas prasmes, izglītība un pieredze attiecībā uz konkrēto projektu.

**Scenārijs:** Tika sākts apstiprināts projekts, un projekta plānošanas posmā vecākā projekta vadītāja loma tika rezervēta kā plānots resurss. Resursu pārvaldnieks tagad ir ieguvis resursu, lai izpildītu vecākā projekta vadītāja lomu.

1. Lapā **Resursu saraksts** atlasiet **Daniels Goldšmits**.
2. Lapā **Resursa loma** atlasiet **Jauna** un ievadiet šādas vērtības:

    - **Stājas spēka:** Ievadiet pašreizējo datumu.
    - **Derīguma beigu datums:** Ievadiet **Nekad**.
    - **Loma:** Ievadiet **Vecākais projekta vadītājs**.

3. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
4. Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]