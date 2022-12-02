---
title: Apakšlīguma statusa pārejas
description: Šajā rakstā ir izskaidrotas stāvokļa pārejas apakšlīgumā programmā Microsoft Dynamics 365 Project Operations, kamēr apakšlīgums tiek izveidots, izpildīts un slēgts.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522940"
---
# <a name="state-transitions-on-a-subcontract"></a>Apakšlīguma statusa pārejas 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā rakstā ir izskaidrotas stāvokļa pārejas apakšlīgumā programmā Microsoft Dynamics 365 Project Operations. Katrs stāvoklis tiek norādīts kā melnraksts, apstiprināts, slēgts vai atcelts. Tālāk sniegtajā attēlā ir parādītas stāvokļa pārejas.

![Apakšlīguma stāvokļa modelis](../media/SubconStates.png)  

Tālāk redzamajā tabulā ir sniegts apraksts par to, ko katrs stāvoklis atspoguļo apakšlīguma dzīves cikla laikā programmā Project Operations.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Tas atspoguļo apakšlīguma sākotnējo stāvokli. Notiek sarunas ar piegādātāju. Rindas un cenas var tikt modificētas. Šajā stāvoklī apakšlīgumu var izmantot, lai novērtētu un nokomplektētu projekta prasības resursiem un materiāliem. Tam var izveidot atsauci arī uz laiku, izdevumiem un materiālu lietojumu projektā. Šajā stāvoklī apakšlīgumu var rediģēt un dzēst. | Apstiprināts |
| Apstiprināts | Tas atspoguļo apakšlīguma posmu pēc pārrunām ar piegādātāju par izcenojumu un rindu vienumu iegādes pabeigšanas. Tomēr faktiskā materiālu un/vai darba nodrošināšana, ko veic apakšlīguma resursi, vēl turpinās. Šajā stāvoklī apakšlīgumu var izmantot, lai novērtētu un nokomplektētu projekta prasības resursiem un materiāliem. Tam var izveidot atsauci arī uz laiku, izdevumiem un materiālu lietojumu projektā. Šajā stāvoklī apakšlīgumu nevar rediģēt vai dzēst. Izmantojot pogu **Atcelt**, varat atcelt apstiprinātu apakšlīgumu. Izmantojot pogu **Atkārtoti atvērt**, varat atkārtoti atvērt apakšlīgumu, lai atgrieztu to statusā **Melnraksts**. Lai aizvērtu apstiprinātu apakšlīgumu, izmantojiet pogu **Aizvērt**. | Aizvērta <br> Atcelta <br> Melnraksts |
| Aizvērta | Tas atspoguļo apakšlīguma posmu, kad ir pabeigta materiālu un/vai darba faktiskā nodrošināšana, ko veic apakšlīguma resursi. Šajā stāvoklī apakšlīgumu vairs nevar izmantot, lai novērtētu un nokomplektētu projekta prasības resursiem un materiāliem. Turklāt tam vairs nevar izveidot atsauci uz laiku, izdevumiem un materiālu lietojumu projektā. Šajā stāvoklī apakšlīgumu nevar rediģēt vai dzēst. | Nevienu |
| Atcelta | Tas atspoguļo apakšlīguma posmu, kad materiālu un/vai darba faktiskā nodrošināšana, ko veic apakšlīguma resursi, vairs nav nepieciešama. Šajā stāvoklī apakšlīgumu nevar izmantot, lai novērtētu un nokomplektētu projekta prasības resursiem un materiāliem, kā arī tam nevar izveidot atsauci uz laiku, izdevumiem un materiālu lietojumu projektā. Šajā stāvoklī apakšlīgumu nevar rediģēt vai dzēst. | Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
