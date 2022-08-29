---
title: Laika, izmaksu un materiālu izlietojuma reģistrēšana apakšlīguma komponentiem
description: Šajā rakstā ir paskaidrots, kā Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas reģistrēts projektos no apakšuzņēmuma līgumiem paredzētiem komponentiem Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261146"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laika, izdevumu un materiālu izmantošanas reģistrēšana projektos ar apakšuzņēmuma līgumiem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

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
