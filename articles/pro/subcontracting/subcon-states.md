---
title: Apakšlīguma statusa pārejas
description: Šajā rakstā ir izskaidrotas statusu pārejas uz apakšuzņēmuma līgumu programmā Microsoft Dynamics 365 Project Operations, jo apakšuzņēmuma līgums ir izveidots, izpildīts un slēgts.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919747"
---
# <a name="state-transitions-on-a-subcontract"></a>Apakšlīguma statusa pārejas 

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā ir izskaidrotas statusu pārejas uz apakšuzņēmuma līgumu programmā Microsoft Dynamics 365 Project Operations. Katrs statuss tiek attēlots kā melnraksts, apstiprināts, slēgts vai atcelts. Šis attēls attēlo statusu pārejas.

![Apakšuzņēmuma stāvokļa modelis](../media/SubconStates.png)  

Šajā tabulā sniegts apraksts par to, ko katrs statuss pārstāv apakšuzņēmuma dzīves ciklā projekta darbībās.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Tas atspoguļo apakšuzņēmuma sākotnējo stāvokli. Notiek sarunas ar kreditoru. Rindas un cenas tiek mainītas. Apakšlīgumu šajā stāvoklī var izmantot, lai novērtētu un personāla projekta prasības attiecībā uz resursiem un materiāliem. Uz to var atsaukties arī uz projekta laiku, izdevumiem un materiālu lietojumu. Apakšuzņēmuma līgumu šajā stāvoklī var rediģēt un dzēst. | Apstiprināts |
| Apstiprināts | Tas atspoguļo apakšlīguma stadiju pēc tam, kad sarunas ar kreditoru par cenām un iegādājamajiem rindas krājumiem ir pabeigtas. Tomēr materiālu un/vai darba faktiskā piegāde, izmantojot apakšuzņēmēju resursus, joprojām turpinās. Apakšlīgumu šajā stāvoklī var izmantot, lai novērtētu un personāla projekta prasības attiecībā uz resursiem un materiāliem. Uz to var atsaukties arī uz projekta laiku, izdevumiem un materiālu lietojumu. Apakšuzņēmuma līgumu šādā stāvoklī nevar rediģēt vai dzēst. Poga **Atcelt** ļauj atcelt apstiprinātu apakšuzņēmuma līgumu. **Poga Atkārtoti atvērt** ļauj atkārtoti atvērt apakšuzņēmuma līgumu, lai tas atgrieztos melnraksta **statusā**. **Izmantojiet pogu Aizvērt**, lai aizvērtu apstiprinātu apakšuzņēmuma līgumu. | Aizvērta <br> Atcelta <br> Melnraksts |
| Aizvērta | Tas ir apakšlīguma posms, kad ir pabeigta materiālu un/vai darba faktiskā piegāde ar apakšuzņēmēju resursiem. Apakšuzņēmuma līgumu šajā stāvoklī vairs nevar izmantot, lai novērtētu un pieprasītu personāla projektus resursiem un materiāliem. Tāpat uz to vairs nevar atsaukties uz projekta laiku, izdevumiem un materiālu lietojumu. Apakšuzņēmuma līgumu šādā stāvoklī nevar rediģēt vai dzēst. | Nevienu |
| Atcelta | Tas ir apakšlīguma posms, kad vairs nav nepieciešama faktiska materiālu piegāde un/vai darbs ar apakšuzņēmēju resursiem. Apakšlīgumu šajā stāvoklī nevar izmantot, lai novērtētu un personāla projekta prasības resursiem un materiāliem, kā arī nevar atsaukties uz projekta laiku, izdevumiem un materiālu izmantošanu. Apakšuzņēmuma līgumu šādā stāvoklī nevar rediģēt vai dzēst. | Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
