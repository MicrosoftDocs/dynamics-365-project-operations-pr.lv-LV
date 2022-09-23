---
title: Apakšlīguma projekta grupas dalībnieki
description: Šajā rakstā ir paskaidrots, kā slēgt apakšlīgumus par projekta grupas dalībniekiem pakalpojumā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522805"
---
# <a name="subcontracting-project-team-members"></a>Apakšlīguma projekta grupas dalībnieki

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Korporācijā Microsoft Dynamics 365 Project Operations varat izvēlēties slēgt apakšlīgumus par projekta grupas dalībniekiem bez personāla vai ar personālu.

- Projekta grupas dalībniekiem, kuriem nav darbinieku, ir piešķirts vispārējs resurss.
- Komandas locekļiem, kuriem ir personāls, ir piešķirts nosaukts resurss.

Saistot projekta grupas dalībnieku ar apakšuzņēmuma līgumu rindu, visi uzdevumi uzdevumiem, kas ir darba grupas dalībniekam, tiks atsaukti, pamatojoties uz pirkuma cenrādi, kas pievienots apakšlīgumam.  **Lapas Detalizēta informācija par** projektu cilnē Aplēses **atlasiet** **pogu Atjaunināt cenas**, lai skatītu atjauninātās cenas un/vai izmaksu segumus, kas izriet no lēmuma slēgt apakšuzņēmuma līgumu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana projekta komandas loceklim bez personāla
Komandas **dalībnieka informācijas** lapā ir apakšuzņēmuma līgumu un apakšlīgumu līniju lauki, kas ļauj projekta vadītājam izteikt, kā viņš vēlētos iegūt nepieciešamo jaudu no apakšuzņēmuma līguma. Lai slēgtu apakšlīgumu par projekta grupas dalībnieku kā vispārīgu resursu, rīkojieties šādi:

1.  Izvēlieties apakšlīgumu **komandas dalībnieka informācijas** lapā.

2.  Varat atlasīt tikai apakšlīgumus ar **statusu Melnraksts** vai **Apstiprināts**. **Nevar atlasīt slēgtus** vai **atceltus** apakšuzņēmuma līgumus. 

3.  Apakšlīguma rindas **lauks** kļūst redzams pēc apakšuzņēmuma līguma atlasīšanas.

4.  **Laukā Apakšlīguma rindiņa** varat atlasīt tikai tās apakšuzņēmuma līgumu rindas, kas ir paredzētas laika gaitā. Jūs nevarat atlasīt apakšlīgumu rindas izdevumiem vai materiāliem.

5.  Projekta komandas locekļa ieraksta lomai ir jāatbilst lomai apakšuzņēmuma līgumu līnijā. Tas nodrošina, ka laiks, kas tiek veltīts projektam, ir tā pati loma, kas tiek iegādāta apakšuzņēmuma līguma līnijā. 

Ja vispārējs darba grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindu, **lauks Nodarbinātā tips** vispārīgajā komandas dalībnieku rindā tiks atjaunināts uz **Līgumdarbinieks**, un **apakšuzņēmuma līguma derīgums** tiks iestatīts uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana projekta komandas loceklim ar personālu
Tāpat kā vispārīgi vai bez personāla komandas locekļi, arī projektā nepieciešamās komandas locekļa spējas var būt saistītas ar apakšlīgumu. Lai slēgtu apakšlīgumu ar noteiktu projekta grupas dalībnieku, rīkojieties šādi:

1.  Pārliecinieties, vai nosauktais resurss ir iestatīts kā līgumstrādnieka tips rezervējamam resursam. Pārliecinieties arī, vai rezervējamā resursa lauks **Kreditors** atbilst kreditoram atlasītajā apakšuzņēmuma līgumā. 

2.  Apakšuzņēmuma līgumus var atlasīt tikai formātā Melnraksts **vai** **Apstiprināts**. **Nevar atlasīt slēgtus** vai **atceltus** apakšuzņēmuma līgumus. 

3.  Apakšlīguma rindas **lauks** kļūst redzams pēc apakšuzņēmuma līguma atlasīšanas.

4.  **Laukā Apakšlīguma rindiņa** varat atlasīt tikai tās apakšuzņēmuma līgumu rindas, kas ir paredzētas laika gaitā. Jūs nevarat atlasīt apakšlīgumu rindas izdevumiem vai materiāliem.

5.  Projekta komandas locekļa ieraksta lomai ir jāatbilst lomai apakšuzņēmuma līgumu līnijā. Tas nodrošina, ka laiks, kas tiek veltīts projektam, ir tā pati loma, kas tiek iegādāta apakšuzņēmuma līguma līnijā. 

Nosauktajiem projekta grupas dalībniekiem, kuri ir iestatīti kā līgumstrādnieka **tips Rezervējams resurss**, tiks parādīts apakšlīguma derīguma statuss Nav **derīgs**, ja tie nav saistīti ar apakšlīgumu. Ja nosaukts projekta grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindu, **lauks Nodarbinātā tips** grupas dalībnieku rindā tiek atjaunināts uz **Līgumdarbinieks**, un **apakšlīguma spēkā esamība** tiks iestatīta uz **Derīgs**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
