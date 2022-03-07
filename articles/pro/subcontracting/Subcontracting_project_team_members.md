---
title: Apakšuzņēmuma līgumu slēgšana projekta grupas dalībniekiem
description: Šajā tēmā ir paskaidrots, kā slēgt apakšlīgumus par projekta grupas dalībniekiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903054"
---
# <a name="subcontracting-project-team-members"></a>Apakšuzņēmuma līgumu slēgšana projekta grupas dalībniekiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Microsoft Dynamics 365 Project Operations varat izvēlēties slēgt apakšlīgumus par projekta grupas dalībniekiem bez personāla vai ar personālu.

- Projekta grupas dalībniekiem bez personāla ir piešķirts vispārējs resurss.
- Komandas dalībniekiem, kuriem ir piešķirts nosaukts resurss.

Saistot projekta grupas dalībnieku ar apakšuzņēmuma rindu, visi uzdevumi uzdevumiem, kas ir grupas dalībniekam, tiks atkārtoti izmaksāti, pamatojoties uz apakšuzņēmuma līgumam pievienoto iepirkuma cenrādi.  Lapas **Detalizēta informācija par projektu cilnē Novērtējumi** **atlasiet** **pogu Atjaunināt cenas,** lai skatītu atjauninātās cenas un/vai izmaksu sārņus, kas izriet no lēmuma par apakšuzņēmuma līgumu slēdzu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana projekta grupas dalībniekam bez darbinieku saimirgots
**Lapā Grupas dalībniekam ir** apakšuzņēmuma līgumu un apakšuzņēmuma rindu lauki, kas ļauj projekta vadītājam izteikt, kā viņš vēlas izmantot nepieciešamo jaudu no apakšuzņēmuma līguma. Lai slēgtu apakšlīgumus par projekta grupas dalībnieku kā vispārīgu resursu, rīkojieties šādi:

1.  Grupas dalībnieka detalizētas informācijas lapā izvēlieties apakšuzņēmuma **līgumu**.

2.  Varat atlasīt tikai apakšuzņēmuma līgumus ar **statusu Melnraksts** vai **Apstiprināts**. **Slēgtos** vai **Atceltos** apakšuzņēmuma līgumus nevar atlasīt. 

3.  **Pēc** apakšuzņēmuma līguma atlasīšanas tiek redzams lauks Apakšuzņēmuma rinda.

4.  Laukā **Apakšuzņēmuma rinda** var atlasīt tikai laika apakšuzņēmēja rindas. Nevar atlasīt izdevumu vai materiālu apakšuzņēmēju rindas.

5.  Projekta grupas dalībnieka ieraksta lomai jāatbilst lomai apakšuzņēmuma rindā. Tas nodrošina, ka projektā novērtētās lomas laiks ir tā pati loma, kas tiek iegādāta apakšuzņēmuma rindā. 

Ja vispārīgais grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu, **lauks Darbinieka tips** vispārīgās grupas dalībnieka rindā tiks atjaunināts uz **Līguma darbinieks un** **Apakšuzņēmuma līguma derīgums** tiks iestatīts uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana ar personāla projekta grupas dalībnieku
Tāpat kā vispārīgi vai darbinieki, arī komandas locekļi, kuriem ir personāla grupas dalībnieka statuss un kas nepieciešama projektam, var būt saistīts arī ar apakšuzņēmuma līgumu. Lai slēgtu apakšuzņēmuma līgumus par nosauktu projekta grupas dalībnieku, rīkojieties šādi:

1.  Pārliecinieties, vai nosauktais resurss ir iestatīts kā līguma darbinieka tips rezervējamam resursam. Pārliecinieties arī, vai **rezervējamā** resursa lauks Piegādātājs atbilst piegādātājam, kas atrodas jūsu atlasāmajā apakšuzņēmuma līguma laukā. 

2.  Apakšuzņēmuma līgumus var atlasīt tikai **melnraksta** vai **apstiprinātajā** statusā. **Slēgtos** vai **Atceltos** apakšuzņēmuma līgumus nevar atlasīt. 

3.  **Pēc** apakšuzņēmuma līguma atlasīšanas tiek redzams lauks Apakšuzņēmuma rinda.

4.  Laukā **Apakšuzņēmuma rinda** var atlasīt tikai laika apakšuzņēmēja rindas. Nevar atlasīt izdevumu vai materiālu apakšuzņēmēju rindas.

5.  Projekta grupas dalībnieka ieraksta lomai jāatbilst lomai apakšuzņēmuma rindā. Tas nodrošina, ka projektā novērtētās lomas laiks ir tā pati loma, kas tiek iegādāta apakšuzņēmuma rindā. 

Nosauktie projekta grupas dalībnieki, kas iestatīti kā rezervējamā resursa līgumdarbinieka **tips**, tiks rādīti ar apakšuzņēmuma līguma derīguma statusu **Nav** derīgs, ja tie nav saistīti ar apakšuzņēmuma līgumu. Ja nosaukts projekta grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu, **lauks Darbinieka tips grupas dalībnieka rindā tiks** atjaunināts uz Līguma darbinieks **un** **Apakšuzņēmuma līguma derīgums** tiks iestatīts uz **Derīgs**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
