---
title: Laika, izmaksu un materiālu izlietojuma reģistrēšana apakšlīguma komponentiem
description: Šajā rakstā ir paskaidrots, kā Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas reģistrēts projektos no apakšuzņēmuma līgumiem paredzētiem komponentiem Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laika, izdevumu un materiālu izmantošanas reģistrēšana projektos ar apakšuzņēmuma līgumiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā rakstā ir paskaidrots, kā Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas reģistrēts projektos no apakšuzņēmuma līgumiem paredzētiem komponentiem Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Apakšuzņēmēja laika izmaksas projektos
Programmā Project Operations līgumdarbinieki var ierakstīt laiku projektos līdzīgi kā darbinieki. Ievadot laiku projektiem un/vai projekta uzdevumiem, līgumdarbinieks var izvēlēties konkrētu apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindu.

Kad līgumdarbinieku iesniegtais laiks ir apstiprināts, projekta izmaksas tiek reģistrētas, izmantojot vienības izmaksu likmi, kas šim līgumdarbinieka resursam **ir iestatīta apakšuzņēmuma līguma iepirkuma cenrāža pirkuma cenrāža sadaļā Lomu cenas**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Izmaksas par apakšuzņēmuma līgumiem par izdevumiem par projektiem
Ievadot izdevumus, kas radušies saistībā ar projektiem, izdevumu ierakstā varat izvēlēties apakšlīgumu un apakšlīguma rindu. 

Kad šis izdevumu ieraksts ir iesniegts un apstiprināts, izdevumu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības izmaksām, kas ir iestatītas šai transakciju kategorijai **apakšuzņēmuma pirkuma cenrāža sadaļā Kategorijas cenas**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Izmaksas par materiāliem, par kuriem noslēgti apakšlīgumi par projektiem
Ievadot materiālu izmantošanu projektos, materiālu izmantošanas žurnālā varat atlasīt apakšlīgumu un apakšuzņēmuma līgumu līniju. Kad materiālu izmantošanas žurnāls ir iesniegts un apstiprināts, materiālu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības izmaksām, kas šim produktam **ir** iestatītas apakšuzņēmuma cenrāža cenu saraksta sadaļā.

Materiālu izmantošanu var reģistrēt arī projektu rakstīšanai. Šāda veida materiālu izmantošanu var saistīt arī ar apakšuzņēmuma līgumu un apakšlīgumu līniju. Reģistrējot materiālu lietojumu rakstīšanas produktiem, jums jāievada ierakstāmā produkta vienas vienības izmaksas. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
