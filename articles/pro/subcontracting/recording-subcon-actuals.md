---
title: Laika, izmaksu un materiālu izlietojuma reģistrēšana apakšlīguma komponentiem
description: Šajā rakstā paskaidrots, kā korporācija Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas reģistrēts projektos no apakšuzņēmēju komponentiem Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927659"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laika, izdevumu un materiālu izmantošanas reģistrēšana projektos apakšuzņēmēju komponentiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā paskaidrots, kā korporācija Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas reģistrēts projektos no apakšuzņēmēju komponentiem Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Apakšuzņēmēja laika izmaksas projektos
Projektu operācijās līgumdarbinieki var ierakstīt projektu laiku līdzīgi kā darbinieki. Ievadot projektu un/vai projekta uzdevumu laiku, līgumdarbinieks var atlasīt noteiktu apakšuzņēmuma un apakšuzņēmuma rindu.

Kad līgumdarbinieku iesniegtais laiks ir apstiprināts, projekta izmaksas tiek reģistrētas, izmantojot vienības izmaksu likmi, kas šim līgumdarbinieka resursam ir iestatīta **apakšlīguma iepirkuma cenrāža sadaļā Lomas cenas**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Apakšuzņēmēju izdevumu izmaksas par projektiem
Ievadot izdevumus, kas radušies projektos, izdevumu ierakstā var atlasīt apakšuzņēmuma un apakšuzņēmuma rindu. 

Kad šis izdevumu ieraksts ir iesniegts un apstiprināts, izdevumu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības pašizmaksu, kas šai darbību kategorijai ir iestatīta **apakšuzņēmēja iepirkuma cenrāža sadaļā Kategoriju cenas**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Izmaksas par apakšuzņēmēju materiāliem par projektiem
Ievadot materiālu patēriņu projektos, materiālu lietojuma žurnālā var atlasīt apakšuzņēmuma un apakšuzņēmuma rindu. Kad materiālu lietojuma žurnāls ir iesniegts un apstiprināts, materiālu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības pašizmaksu, kas šai precei ir iestatīta **apakšuzņēmuma cenrāža cenrāža sadaļā Cenrāža preces**.

Materiālu izmantošanu var reģistrēt arī projektu rakstīšanas produktiem. Šāda veida materiālu izmantošanu var saistīt arī ar apakšuzņēmuma un apakšuzņēmuma rindu. Ierakstot materiālu lietojumu rakstīšanas produktiem, jāievada ieraksta produkta vienības pašizmaksa. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
