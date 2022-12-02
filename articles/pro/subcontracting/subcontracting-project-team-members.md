---
title: Apakšlīguma projekta grupas dalībnieki
description: Šajā rakstā izskaidrots, kā izveidot projekta darba grupas dalībnieku apakšlīgumus programmā Microsoft Dynamics 365 Project Operations.
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

Programmā Microsoft Dynamics 365 Project Operations varat izvēlēties izveidot apakšlīgumus projekta darba grupas dalībniekiem, kuri ietilpst vai neietilpst personālā.

- Projekta darba grupas dalībniekiem, kuri neietilpst personālā, tiek piešķirts vispārējs resurss.
- Darba grupas dalībniekiem, kuri ietilpst personālā, tiek piešķirts nosaukts resurss.

Saistot projekta darba grupas dalībnieku ar apakšlīguma rindu, visiem darba grupas dalībnieka uzdevumu piešķīrumiem tiks pārrēķinātas izmaksas, balstoties uz pirkumu cenrādi, kas pievienots apakšlīgumam.  Cilnē **Aprēķini**, kas atrodas lapā **Detalizēta informācija par projektu**, atlasiet pogu **Atjaunināt cenas**, lai skatītu atjaunināto izcenojumu un/vai izmaksas, kas rodas no lēmuma slēgt apakšlīgumu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšlīguma izveide personālā neiekļautam projekta grupas dalībniekam
Lapā **Darba grupas dalībnieka informācija** ir apakšlīguma un apakšlīguma rindu laiki, kuros projekta vadītājs var norādīt, kā vēlas piesaistīt nepieciešamo noslodzi no apakšlīguma. Lai projekta darba grupas dalībniekam izveidotu apakšlīgumu kā vispārējam resursam, izpildiet tālāk norādītās darbības.

1.  Lapā **Darba grupas dalībnieka informācija** izvēlieties apakšlīgumu.

2.  Var atlasīt tikai tos apakšlīgumus, kam ir statuss **Melnraksts** vai **Apstiprināts**. Apakšlīgumus ar statusu **Slēgts** vai **Atcelts** nevar atlasīt. 

3.  Pēc apakšlīguma atlasīšanas kļūst redzams lauks **Apakšlīguma rinda**.

4.  Laukā **Apakšlīguma rinda** var atlasīt tikai tās apakšlīguma rindas, kas paredzētas laikam. Izdevumiem vai materiāliem nevar atlasīt apakšlīguma rindas.

5.  Projekta darba grupas dalībnieka ieraksta lomai ir jāatbilst lomai apakšlīguma rindā. Tādējādi tiek nodrošināts, ka laiks lomai, kas tiek prognozēta projektā, ir tāds pats kā lomai, kas tiek iegādāta apakšlīguma rindā. 

Ja ar apakšlīgumu un apakšlīguma rindu tiek saistīts vispārējs darba grupas dalībnieks, lauks **Darbinieka tips** vispārējā darba grupas dalībnieka rindā tiek atjaunināts uz **Līgumdarbinieks**, un **Apakšuzņēmēja līguma derīgums** tiek iestatīts uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšlīguma izveide personālā iekļautam projekta grupas dalībniekam
Tāpat kā vispārīgie vai personālā neiekļautie darba grupas dalībnieki, arī personālā iekļauta darba grupas dalībnieka noslodzi, kas nepieciešama projektā, var saistīt ar apakšlīgumu. Lai izveidotu apakšlīgumu nosauktam projekta darba grupas dalībniekam, izpildiet tālāk norādītās darbības.

1.  Pārliecinieties, ka nosauktais resurss ir iestatīts kā rezervējama resursa tipa līgumdarbinieks. Turklāt pārliecinieties, vai rezervējamā resursa lauks **Piegādātājs** atbilst piegādātājam jūsu atlasītajā apakšlīgumā. 

2.  Var atlasīt tikai tos apakšlīgumus, kuri ir ar statusu **Melnraksts** vai **Apstiprināts**. Apakšlīgumus ar statusu **Slēgts** vai **Atcelts** nevar atlasīt. 

3.  Pēc apakšlīguma atlasīšanas kļūst redzams lauks **Apakšlīguma rinda**.

4.  Laukā **Apakšlīguma rinda** var atlasīt tikai tās apakšlīguma rindas, kas paredzētas laikam. Izdevumiem vai materiāliem nevar atlasīt apakšlīguma rindas.

5.  Projekta darba grupas dalībnieka ieraksta lomai ir jāatbilst lomai apakšlīguma rindā. Tādējādi tiek nodrošināts, ka laiks lomai, kas tiek prognozēta projektā, ir tāds pats kā lomai, kas tiek iegādāta apakšlīguma rindā. 

Nosaukti projekta darba grupas dalībnieki, kas ir iestatīti kā līgumdarbinieki ar tipu **Rezervējams resurss**, tiks rādīti ar apakšuzņēmēja līguma derīguma statusu **Nav derīgs**, ja tie nav saistīti ar apakšlīgumu. Ja ar apakšlīgumu un apakšlīguma rindu tiek saistīts nosaukts darba grupas dalībnieks, lauks **Darbinieka tips** darba grupas dalībnieka rindā tiek atjaunināts uz **Līgumdarbinieks**, un **Apakšuzņēmēja līguma derīgums** tiek iestatīts uz **Derīgs**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
