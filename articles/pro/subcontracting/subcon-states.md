---
title: Apakšlīguma statusa pārejas
description: Šajā rakstā ir izskaidrotas valsts pārejas apakšuzņēmuma līgumā korporācijā Microsoft Dynamics 365 Project Operations, kad apakšlīgums tiek izveidots, izpildīts un slēgts.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261284"
---
# <a name="state-transitions-on-a-subcontract"></a>Apakšlīguma statusa pārejas 

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā ir izskaidrotas valsts pārejas apakšuzņēmuma līgumā pakalpojumā Microsoft Dynamics 365 Project Operations. Katrs štats tiek pārstāvēts kā projekts, apstiprināts, slēgts vai atcelts. Šis attēls attēlo stāvokļa pārejas.

![Apakšuzņēmuma līgumu valsts modelis](../media/SubconStates.png)  

Šajā tabulā sniegts apraksts par to, ko katrs statuss pārstāv apakšuzņēmuma dzīves ciklā projekta darbībās.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Tas atspoguļo apakšuzņēmuma līguma sākotnējo stāvokli. Notiek sarunas ar pārdevēju. Līnijas un cenas var tikt mainītas. Apakšlīgumu šajā valstī var izmantot, lai novērtētu un personāla projekta vajadzības pēc resursiem un materiāliem. Uz to var atsaukties arī par laiku, izdevumiem un materiālu izmantošanu projektā. Apakšlīgumu šajā stāvoklī var rediģēt un izdzēst. | Apstiprināts |
| Apstiprināts | Tas ir apakšuzņēmuma līguma posms pēc tam, kad ir pabeigtas sarunas ar pārdevēju par cenu noteikšanu un iegādājamajām pozīcijām. Tomēr faktiskā materiālu piegāde un/vai darbs, izmantojot ar apakšlīgumiem saistītus resursus, joprojām turpinās. Apakšlīgumu šajā valstī var izmantot, lai novērtētu un personāla projekta vajadzības pēc resursiem un materiāliem. Uz to var atsaukties arī par laiku, izdevumiem un materiālu izmantošanu projektā. Apakšlīgumu šādā stāvoklī nevar rediģēt vai dzēst. Poga **Atcelt** ļauj atcelt apstiprinātu apakšlīgumu. Poga **Atkārtoti atvērt** ļauj atkārtoti atvērt apakšlīgumu, lai tas atkal nonāktu melnraksta **statusā**. Izmantojiet **pogu Aizvērt**, lai aizvērtu apstiprinātu apakšlīgumu. | Aizvērta <br> Atcelta <br> Melnraksts |
| Aizvērta | Tas ir apakšuzņēmuma līguma posms, kad ir pabeigta faktiskā materiālu piegāde un/vai darbs, izmantojot ar apakšuzņēmuma līgumu saistītus resursus. Apakšlīgumu šajā valstī vairs nevar izmantot, lai novērtētu un personāla projektu vajadzības pēc resursiem un materiāliem. Turklāt uz to vairs nevar atsaukties laikā, izdevumos un materiālajā lietojumā projektā. Apakšlīgumu šādā stāvoklī nevar rediģēt vai dzēst. | Nevienu |
| Atcelta | Tas ir apakšuzņēmuma līguma posms, kad vairs nav nepieciešama faktiska materiālu piegāde un/vai darbs, izmantojot resursus, par kuriem ir slēgti apakšlīgumi. Apakšlīgumu šajā valstī nevar izmantot, lai novērtētu un personāla projekta vajadzības pēc resursiem un materiāliem, kā arī to nevar atsaukties uz laiku, izdevumiem un materiālu izmantošanu projektā. Apakšlīgumu šādā stāvoklī nevar rediģēt vai dzēst. | Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
