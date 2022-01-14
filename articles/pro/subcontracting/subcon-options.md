---
title: Apakšuzņēmuma līgumu slēdzuma iespējas projekta grupas dalībniekiem
description: Šajā tēmā ir izskaidrotas apakšuzņēmuma līgumu slēdzuma opcijas projekta grupas dalībniekiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903715"
---
# <a name="subcontracting-options-for-project-team-members"></a>Apakšuzņēmuma līgumu slēdzuma iespējas projekta grupas dalībniekiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Microsoft Dynamics 365 Project Operations varat novērtēt vienam vai vairākiem projekta grupas dalībniekiem pieejamās apakšuzņēmuma līgumu slēdzināšanas opcijas. Pieejamās apakšuzņēmuma līgumu slēdzot opcijas, ļauj:

- Izveidot jaunu apakšuzņēmuma līgumu un/vai izveidot jaunas rindas esošam apakšuzņēmuma līgumam atlasītajiem projekta grupas dalībniekiem. 
- Rezervējiet pret jau esošu apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindu. 

Varat izvēlēties kādu no pieejamajām apakšuzņēmuma līgumu opcijām vispārējiem projekta grupas dalībniekiem vai izvēlēties kādu no projekta grupas dalībniekiem, kuriem ir piešķirts nosaukts resurss, kas ir līgumdarbinieks. 

Apakšuzņēmuma līgumu slēgšana nav pieejama:

- Projekta grupas dalībnieki, kuriem ir personāls ar darbinieku. 
- Projekta grupas dalībnieki, kas jau ir saistīti ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana projekta grupas dalībniekam bez darbinieku saimirgots

Lai pārskatītu un izvēlētos kādu no pieejamajām apakšuzņēmuma līgumu opcijām vispārējam vai darbiniekam bez darbinieku loka, rīkojieties šādi:

1. Atlasiet vienu vai vairākas projekta grupas dalībnieku ierakstus, kur resurss ir vispārējs resurss.
2. Pārliecinieties, vai neviens no atlasītajiem projekta grupas dalībnieku ierakstiem jau nav slēgts par apakšuzņēmuma līgumu. 
3. **Projekta grupas** dalībnieku apakšrežģī atlasiet Apakšnodaļas opcijas. Tiek **atvērts dialoglodziņš Apakšuzņēmuma līgumu** opcijas. 
4. Ja 1. darbībā atlasījāt tikai viena projekta grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
    - Izveidojiet jaunas apakšuzņēmuma rindas. 
    - Rezervēt pret esošu apakšuzņēmuma līgumu Ja 1. darbībā atlasījāt vairākus projekta grupas dalībnieku ierakstus, vienīgā pieejamā iespēja ir izveidot jaunas apakšuzņēmuma rindas.
5. Iespēja rezervēt pret esošu apakšuzņēmuma rindu ļauj atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu, pret kuru vēlaties rezervēt. Atlasot apakšuzņēmuma rindu, lai rezervētu noslodzi, ir jānodrošina, ka atlasītā apakšuzņēmuma rinda ir uz laiku un projekta grupas dalībniekam nepieciešamā loma atbilst lomai, kas iegādāta apakšuzņēmuma rindā.
6. Atlasot projekta grupas dalībniekiem izveidot jaunas apakšuzņēmēju rindas, sistēma ļauj atlasīt apakšuzņēmuma līgumu, kuru vēlaties izveidot šīs rindas. Apakšuzņēmuma līgumam, kurā vēlaties izveidot jaunas rindas, jābūt **statuss** Melnraksts. Izmantojot šo opciju, lai izveidotu jaunas apakšuzņēmuma rindas atlasītajiem projekta grupas dalībniekiem, sistēma katram projekta grupas dalībniekam izveidos vienu apakšuzņēmēja rindu. Loma, stundas un datumi tiek kopēti no projekta grupas dalībnieka uz katru izveidoto apakšuzņēmuma rindu. 
7. Ja vispārējs grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu, **lauks Darbinieka tips** vispārīgās grupas dalībnieka rindā tiks atjaunināts uz **Līguma darbinieks un līguma spēkā** **esamības** vērtība tiks iestatīta uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšuzņēmuma līgumu slēgšana ar personāla projekta grupas dalībnieku

Tāpat kā vispārīgi vai darbinieki, varat arī skatīt apakšuzņēmuma līgumu slēgšanas iespējas projekta grupas dalībniekam, kurā ir personāls, ja vien komandas darbinieks ir līgumdarbinieks. Lai pārskatītu un izvēlētos kādu no pieejamajām apakšuzņēmuma līgumu opcijām personālam vai nosauktam projekta grupas dalībniekam, rīkojieties šādi:

1. Atlasiet vienu vai vairākas projekta grupas dalībnieku ierakstus, kur resurss ir nosaukts līgumdarbinieks.
2. Pārliecinieties, vai neviens no atlasītajiem projekta grupas dalībnieku ierakstiem jau nav slēgts par apakšuzņēmuma līgumu. 
3. **Projekta grupas** dalībnieku apakšrežģī atlasiet Apakšnodaļas opcijas. Tiek **atvērts dialoglodziņš Apakšuzņēmuma līgumu** opcijas. 
4. Ja 1. darbībā atlasījāt tikai viena projekta grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
      - Izveidojiet jaunas apakšuzņēmuma rindas.
      - Rezervējiet pret esošu apakšuzņēmuma līgumu.
  Ja 1. darbībā atlasījāt vairākus projekta grupas dalībnieku ierakstus, vienīgā pieejamā iespēja ir izveidot jaunas apakšuzņēmuma rindas.
5. Iespēja rezervēt pret esošu apakšuzņēmuma rindu ļauj atlasīt apakšuzņēmuma līgumu un apakšuzņēmuma rindu, pret kuru vēlaties rezervēt. Izvēloties apakšuzņēmuma rindu, lai rezervētu noslodzi, jums jānodrošina:
      - Atlasītā apakšuzņēmuma līguma rinda ir paredzēta laikam. 
      - Projekta grupas dalībniekam nepieciešamā loma atbilst lomai, kas iegādāta apakšuzņēmuma rindā. 
      - Kreditors, ar kuru ir saistīts līguma darbinieks, ir tāds pats kā apakšuzņēmēja kreditors.
6. Atlasot projekta grupas dalībniekiem izveidot jaunas apakšuzņēmēju rindas, sistēma ļauj atlasīt apakšuzņēmuma līgumu, kuru vēlaties izveidot šīs rindas. Izmantojot šo opciju, pārliecinieties, ka kreditors, kuram pieder līguma darbinieks, ir tāds pats kā apakšuzņēmēja piegādātājs. 
7. Apakšuzņēmuma līgumam, kurā vēlaties izveidot jaunas rindas, jābūt **statuss** Melnraksts. Izmantojot šo opciju, lai izveidotu jaunas apakšuzņēmuma rindas atlasītajiem projekta grupas dalībniekiem, sistēma katram projekta grupas dalībniekam izveidos vienu apakšuzņēmēja rindu. Loma, stundas un datumi tiek kopēti no projekta grupas dalībnieka uz katru izveidoto apakšuzņēmuma rindu.  
8. Ja nosauktais grupas dalībnieks ir saistīts ar apakšuzņēmuma līgumu un apakšuzņēmuma rindu, **lauks Darbinieka tips** nosauktā komandas dalībnieka rindā tiks atjaunināts uz **Līguma darbinieks un līguma spēkā** **esamības** vērtība tiks iestatīta uz **Derīgs**.

## <a name="re-costing-subcontractor-assignments"></a>Apakšuzņēmēju uzdevumu pārdalīšana

Ja projekta grupas dalībnieks (vispārīgs vai nosaukts) ir saistīts ar apakšuzņēmuma līnijām, izmantojot **dialogu Apakšuzņēmuma līgumu** opcijas, visas piešķires uzdevumiem, kas ir grupas dalībniekam, tiks atkārtoti izstādītas, pamatojoties uz apakšuzņēmuma līgumam pievienoto iepirkuma cenrādi. Lapas **Detalizēta informācija par projektu cilnē Novērtējumi** **atlasiet** **pogu Atjaunināt cenas,** lai skatītu atjauninātās cenas un/vai izmaksu sārņus, kas izriet no lēmuma par apakšuzņēmuma līgumu slēdzu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
