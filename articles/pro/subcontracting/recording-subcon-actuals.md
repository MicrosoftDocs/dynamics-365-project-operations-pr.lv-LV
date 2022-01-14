---
title: Laika, izdevumu un materiālu izmantošanas reģistrēšana apakšuzņēmēju komponentiem
description: Šajā tēmā ir paskaidrots, kā korporācija Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas ierakstīts projektos no apakšuzņēmēju komponentiem Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903711"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laika, izdevumu un materiālu izmantošanas reģistrēšana projektos apakšuzņēmēju komponentiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir paskaidrots, kā korporācija Microsoft izseko laiku, izdevumus un materiālu lietojumu, kas ierakstīts projektos no apakšuzņēmēju komponentiem Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projektu apakšuzņēmēja laika izmaksas
Projekta operācijās līgumdarbinieki var reģistrēt projektu laiku līdzīgi kā darbinieki. Ievadot laiku projektiem un/vai projekta uzdevumiem, līgumdarbinieks var atlasīt noteiktu apakšuzņēmuma līgumu un apakšuzņēmuma rindu.

Kad līgumdarbinieku iesniegtais laiks ir apstiprināts, projekta izmaksas tiek reģistrētas, izmantojot vienības pašizmaksas likmi, kas šim līgumdarbinieku resursam ir iestatīta **apakšuzņēmuma** līguma pirkšanas cenrāža sadaļā Lomu cenas.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektu apakšuzņēmēju izdevumu izmaksas
Ievadot izdevumus, kas radušies saistībā ar projektiem, izdevumu ierakstā var atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu. 

Kad šis izdevumu ieraksts ir iesniegts un apstiprināts, izdevumu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības pašizmaksu, kas iestatīta šai darbības kategorijai **apakšuzņēmuma** līguma pirkšanas cenrāža sadaļā Kategoriju cenas.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektu apakšuzņēmēju materiālu izmaksas
Ievadot materiālu lietojumu projektos, materiālu lietojuma žurnālā var atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu. Kad materiālu izmantošanas žurnāls ir iesniegts un apstiprināts, materiālu izmaksas tiek reģistrētas projektā, pamatojoties uz vienības pašizmaksu, kas šai precei ir iestatīta **apakšuzņēmēju** cenrāža sadaļā Cenrādis.

Materiālu lietojumu var ierakstīt arī projektu rakstīšanas produktiem. Šāda veida materiālu lietojumu var saistīt arī ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu. Ierakstot materiālu lietojumu ierakstāmiem produktiem, ir jāievada ierakstāmā produkta vienības pašizmaksa. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
