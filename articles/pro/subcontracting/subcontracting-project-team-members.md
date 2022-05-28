---
title: Apakšlīguma projekta grupas dalībnieki
description: Šajā tēmā paskaidrots, kā apakšuzņēmuma līgumi par projekta grupas dalībniekiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587855"
---
# <a name="subcontracting-project-team-members"></a>Apakšlīguma projekta grupas dalībnieki

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Microsoft Dynamics 365 Project Operations varat izvēlēties slēgt apakšlīgumus par projekta grupas dalībniekiem bez personāla vai darbiniekiem.

- Projekta grupas dalībniekiem, kuriem nav darbinieku, ir piešķirts vispārējs resurss.
- Komandas dalībniekiem ar personālu ir piešķirts nosaukts resurss.

Saistot projekta grupas dalībnieku ar apakšuzņēmuma rindu, visas piešķires uzdevumiem, kas ir grupas dalībniekam, tiks atkārtoti ģenerētas, pamatojoties uz iepirkuma cenrādi, kas pievienots apakšlīgumam.  **Lapas Detalizēta informācija** par **projektu cilnē Novērtējumi** atlasiet **pogu Atjaunināt cenas**, lai skatītu atjauninātās cenas un/vai izmaksas, kas izriet no lēmuma slēgt apakšuzņēmuma līgumus rezultātā. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšlīgumu slēgšana ar projekta grupas dalībnieku bez personāla
Lapā **Grupas dalībnieks detalizēta informācija** ir apakšuzņēmuma un apakšuzņēmuma rindu lauki, kas ļauj projekta vadītājam izteikt, kā viņš vēlas iegūt no apakšuzņēmuma nepieciešamo jaudu. Lai apakšuzņēmuma līgumu par projekta grupas dalībnieku noslēgtu apakšuzņēmuma līgumu kā vispārīgu resursu, rīkojieties šādi:

1.  Izvēlieties apakšuzņēmuma līgumu grupas dalībnieka detalizētās **informācijas** lapā.

2.  Varat atlasīt tikai apakšlīgumus ar **statusu Melnraksts** vai **Apstiprināts**. **Nevar atlasīt slēgtus** vai **atceltus** apakšlīgumus. 

3.  **Zemlīguma rindas** lauks kļūst redzams pēc apakšuzņēmuma atlasīšanas.

4.  Laukā **Apakšlīguma rinda** var atlasīt tikai uz laiku esošas apakšuzņēmuma rindas. Izdevumu vai materiālu apakšuzņēmuma rindas nevar atlasīt.

5.  Projekta grupas dalībnieka ieraksta lomai jāatbilst lomai apakšuzņēmuma rindā. Tas nodrošina, ka projektā novērtētās lomas laiks ir tā pati loma, kas tiek iegādāta apakšuzņēmuma līnijā. 

Ja vispārējs grupas dalībnieks ir saistīts ar apakšuzņēmuma un apakšuzņēmuma rindu, **lauks Darbinieka tips** vispārējā grupas dalībnieku rindā tiks atjaunināts uz **Līgumdarbinieks**, un **apakšuzņēmuma derīgums** tiks iestatīts uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšlīgumu slēgšana ar projekta grupas dalībnieku ar personālu
Tāpat kā vispārīgi vai bez personāla grupas locekļi, arī projektā nepieciešamās komandas locekļu personāla spējas var saistīt ar apakšuzņēmuma līgumu. Lai noslēgtu apakšlīgumu par nosauktu projekta grupas dalībnieku, rīkojieties šādi:

1.  Pārliecinieties, vai nosauktais resurss ir iestatīts kā līgumdarbinieka rezervējamā resursa tips. Pārliecinieties arī, vai **rezervējamā resursa lauks Piegādātājs** atbilst piegādātājam atlasītajā apakšuzņēmuma līgumā. 

2.  Apakšuzņēmuma līgumus var atlasīt tikai statusā Melnraksts **vai** **Apstiprināts**. **Nevar atlasīt slēgtus** vai **atceltus** apakšlīgumus. 

3.  **Zemlīguma rindas** lauks kļūst redzams pēc apakšuzņēmuma atlasīšanas.

4.  Laukā **Apakšlīguma rinda** var atlasīt tikai uz laiku esošas apakšuzņēmuma rindas. Izdevumu vai materiālu apakšuzņēmuma rindas nevar atlasīt.

5.  Projekta grupas dalībnieka ieraksta lomai jāatbilst lomai apakšuzņēmuma rindā. Tas nodrošina, ka projektā novērtētās lomas laiks ir tā pati loma, kas tiek iegādāta apakšuzņēmuma līnijā. 

Nosauktie projekta grupas dalībnieki, kas ir iestatīti kā līgumdarbinieka tips **rezervējamais resurss**, tiks parādīti ar apakšuzņēmuma derīguma statusu Nederīgs, **ja** tie nav saistīti ar apakšuzņēmuma līgumu. Ja nosaukts projekta grupas dalībnieks ir saistīts ar apakšuzņēmuma un apakšuzņēmuma rindu, **grupas dalībnieku rindas lauks Darbinieka tips** tiks atjaunināts uz **Līgumstrādnieks**, un **apakšuzņēmuma derīgums** tiks iestatīts uz **Derīgs**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
