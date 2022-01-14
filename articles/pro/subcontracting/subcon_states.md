---
title: Valsts pārejas uz apakšuzņēmuma līgumu projekta operācijās
description: Šajā tēmā ir izskaidrotas valsts pārejas uz apakšuzņēmuma līgumu programmā Dynamics 365 Project Operations Microsoft, jo apakšuzņēmuma līgums tiek izveidots, izpildīts un slēgts.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903050"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Valsts pārejas uz apakšuzņēmuma līgumu projekta operācijās

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir izskaidrotas stāvokļa pārejas uz apakšuzņēmuma līgumu programmā Microsoft Dynamics 365 Project Operations. Katra valsts tiek attēlota kā melnraksts, apstiprināts, slēgts vai atcelts. Šajā attēlā ir attēlotas stāvokļa pārejas.

![Apakšuzņēmuma stāvokļa modelis](../media/SubconStates.png)  

Šajā tabulā ir sniegts apraksts par to, ko katrs štats pārstāv projekta operāciju apakšuzņēmuma līguma dzīves ciklā.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Tas atspoguļo apakšuzņēmuma līguma sākotnējo stāvokli. Notiek sarunas ar pārdevēju. Līnijas un cenas var tikt pārveidotas. Apakšuzņēmuma līgumu šajā stāvoklī var izmantot, lai novērtētu un personāla projekta prasības resursiem un materiāliem. Uz to var atsaukties arī laikā, izdevumos un materiālu izmantošanā projektā. Apakšuzņēmuma līgumu šajā stāvoklī var rediģēt un dzēst. | Apstiprināts |
| Apstiprināts | Tas ir apakšuzņēmuma līguma posms pēc tam, kad sarunas ar piegādātāju par cenu noteikšanu un rindu krājumiem, kas tiek iegādātas, ir pabeigtas. Tomēr materiālu un/vai darbu faktiskā piegāde ar apakšuzņēmēju resursiem joprojām turpinās. Apakšuzņēmuma līgumu šajā stāvoklī var izmantot, lai novērtētu un personāla projekta prasības resursiem un materiāliem. Uz to var atsaukties arī laikā, izdevumos un materiālu izmantošanā projektā. Apakšuzņēmuma līgumu šajā stāvoklī nevar rediģēt vai dzēst. **Poga Atcelt ļauj atcelt apstiprinātu** apakšuzņēmuma līgumu. **Poga Atkārtota atvēršana ļauj atkārtoti atvērt** apakšuzņēmuma līgumu, lai to atkal iemestu **melnraksta** statusā. Izmantojiet **pogu** Aizvērt, lai aizvērtu apstiprinātu apakšuzņēmuma līgumu. | Aizvērta <br> Atcelta <br> Melnraksts |
| Aizvērta | Tas ir apakšuzņēmuma līguma posms, kad ir pabeigta materiālu faktiskā piegāde un/vai darbs ar apakšuzņēmēju resursiem. Apakšuzņēmuma līgumu šajā valstī vairs nevar izmantot, lai novērtētu un personāla projektu prasības attiecībā uz resursiem un materiāliem. Arī uz to vairs nevar atsaukties laikā, izdevumos un materiālu izmantošanā projektā. Apakšuzņēmuma līgumu šajā stāvoklī nevar rediģēt vai dzēst. | Nevienu |
| Atcelta | Tas ir apakšuzņēmuma līguma posms, kad materiālu un/vai darba faktiska piegāde ar apakšuzņēmēju resursiem vairs nav nepieciešama. Apakšlīgumu šajā stāvoklī nevar izmantot, lai novērtētu un personāla projekta prasības resursiem un materiāliem, kā arī nevar atsaukties uz projekta laiku, izdevumiem un materiālu izmantošanu. Apakšuzņēmuma līgumu šajā stāvoklī nevar rediģēt vai dzēst. | Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
