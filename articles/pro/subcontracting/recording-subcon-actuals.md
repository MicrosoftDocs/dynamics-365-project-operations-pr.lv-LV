---
title: Laika, izmaksu un materiālu izlietojuma reģistrēšana apakšlīguma komponentiem
description: Šajā rakstā izskaidrots, kā korporācija Microsoft izseko projektiem ierakstīto laiku, izdevumus un materiālu izlietojumu no apakšvadītajiem komponentiem Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522523"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laika, izmaksu un materiālu izlietojuma reģistrēšana projektiem ar apakšlīguma komponentiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā rakstā izskaidrots, kā korporācija Microsoft izseko projektiem ierakstīto laiku, izdevumus un materiālu izlietojumu no apakšvadītajiem komponentiem Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Izmaksas par apakšuzņēmēja laiku, kas veltīts projektiem
Project Operations ietvaros līguma darbinieki projektos var ierakstīt laiku līdzīgi kā pastāvīgie darbinieki. Ievadot laiku par projektiem un/vai projektu uzdevumiem, līgumdarbinieks var atlasīt īpašu apakšlīgumu un apakšlīguma rindu.

Kad līgumdarbinieku iesniegtais laiks ir apstiprināts, projekta izmaksas tiek reģistrētas, izmantojot vienības izmaksu likmi, kas tiek iestatīt līgumdarbinieka resursam apakšlīguma pirkuma cenrāža sadaļā **Lomu cenas**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Apakšuzņēmēju izdevumu par projektiem aprēķini
Ja tiek ievadītas projektu ietvaros radušās izmaksas, varat izdevumu ierakstā atlasīt apakšlīgumu un apakšlīguma rindu. 

Kad ir iesniegts un apstiprināts izdevumu ieraksts, izdevumu izmaksas tiek reģistrētas projektā, pamatojoties vienības izmaksās, kas iestatītas attiecīgajai transakcijas kategorijai apakšlīguma pirkuma cenrāža sadaļā **Kategoriju cenas**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Apakšuzņēmēju projektos izmantot materiālu aprēķini
Ja tiek ievadītas projektu ietvaros radies materiālu lietojums, varat materiālu lietojuma žurnālā atlasīt apakšlīgumu un apakšlīguma rindu. Kad ir iesniegts un apstiprināts materiālu lietojuma žurnāls, materiālu izmaksas tiek reģistrētas projektā, pamatojoties vienības izmaksās, kas tiek attiecīgajam produktam iestatītas apakšlīguma cenrāža sadaļā **Cenrāža vienības**.

Materiālu lietojumu tāpat var reģistrēt ierakstītiem projekta produktiem. Šā tipa materiālu lietojumu var arī saistīt ar apakšlīgumu un apakšlīguma rindu. Reģistrējot materiālu lietojumu ierakstītiem produktiem, ir jāievada ierakstītā produkta vienības izmaksas. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
