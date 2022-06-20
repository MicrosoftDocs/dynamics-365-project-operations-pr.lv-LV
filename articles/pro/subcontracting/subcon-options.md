---
title: Apakšlīguma iespējas projekta grupas dalībniekiem
description: Šajā rakstā ir izskaidrotas apakšuzņēmuma līgumu opcijas projekta grupas dalībniekiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88a76ccf73a4b6cfa13a67b50130b007f244d831
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919793"
---
# <a name="subcontracting-options-for-project-team-members"></a>Apakšlīguma iespējas projekta grupas dalībniekiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Microsoft Dynamics 365 Project Operations var novērtēt apakšuzņēmuma līgumu opcijas, kas pieejamas vienam vai vairākiem projekta grupas dalībniekiem. Pieejamās apakšuzņēmuma līgumu opcijas ļauj:

- Izveidojiet jaunu apakšuzņēmuma līgumu un/vai izveidojiet jaunas rindas esošā apakšuzņēmuma līgumā atlasītajiem projekta grupas dalībniekiem. 
- Rezervēt jau esošai apakšuzņēmuma un apakšuzņēmuma līnijai. 

Varat izvēlēties kādu no pieejamajām apakšuzņēmuma līgumu opcijām vispārējiem projekta grupas dalībniekiem vai izvēlēties kādu no projekta grupas dalībniekiem, kuriem ir personāls ar nosauktu resursu, kas ir līgumdarbinieks. 

Apakšuzņēmuma līgumu slēgšanas iespējas nav pieejamas:

- Projekta komandas locekļi, kuros strādājis darbinieks. 
- Projekta grupas dalībnieki, kas jau ir saistīti ar apakšuzņēmuma un apakšuzņēmuma rindu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšlīgumu slēgšana ar projekta grupas dalībnieku bez personāla

Lai pārskatītu un izvēlētos kādu no pieejamajām apakšuzņēmuma līgumu opcijām vispārējam vai bez personāla esošam projekta grupas dalībniekam, rīkojieties šādi:

1. Atlasiet vienu vai vairākus projekta grupas dalībnieku ierakstus, kuros resurss ir vispārējs resurss.
2. Pārliecinieties, vai neviens no atlasītajiem projekta grupas dalībnieku ierakstiem jau nav noslēdzis apakšuzņēmuma līgumus. 
3. Projekta grupas dalībnieku apakšrežā atlasiet **Apakšuzņēmuma opcijas**. Tiek **atvērts dialoglodziņš Apakšuzņēmuma opciju** dialogs. 
4. Ja 1. darbībā atlasījāt tikai vienu projekta grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
    - Izveidojiet jaunas apakšuzņēmuma rindas. 
    - Rezervēt pret esošu apakšuzņēmuma līgumu Ja 1. darbībā atlasījāt vairākus projekta grupas dalībnieku ierakstus, tad vienīgā pieejamā iespēja ir izveidot jaunas apakšuzņēmuma rindas.
5. Iespēja rezervēt pret esošu apakšuzņēmuma rindu ļauj atlasīt apakšuzņēmuma un apakšuzņēmuma rindu, pret kuru vēlaties rezervēt. Izvēloties apakšuzņēmuma rindu rezerves noslodzei, pārliecinieties, vai atlasītā apakšuzņēmuma rinda ir paredzēta laikam un ka projekta grupas dalībniekam nepieciešamā loma atbilst apakšuzņēmuma rindā iegādātajai lomai.
6. Atlasot izveidot jaunas apakšuzņēmuma rindas projekta grupas dalībniekiem, sistēma ļauj atlasīt apakšuzņēmuma līgumu, kuru vēlaties izveidot šīs rindas. Apakšuzņēmuma līgumam, kuru atlasījāt, lai izveidotu jaunas rindas, jābūt melnraksta **statusā**. Izmantojot šo opciju, lai atlasītajiem projekta grupas dalībniekiem izveidotu jaunas apakšuzņēmuma rindas, sistēma katram projekta grupas dalībniekam uz laiku izveidos vienu apakšuzņēmuma rindu. Loma, stundas un datumi tiks kopēti no projekta grupas dalībnieka uz katru izveidoto apakšuzņēmuma rindu. 
7. Ja vispārējs grupas dalībnieks ir saistīts ar apakšuzņēmuma un apakšuzņēmuma rindu, **lauks Darbinieka tips** vispārīgajā grupas dalībnieku rindā tiks atjaunināts uz **Līgumdarbinieks** un **apakšuzņēmuma derīguma** vērtība tiks iestatīta kā **Derīga**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšlīgumu slēgšana ar projekta grupas dalībnieku ar personālu

Tāpat kā vispārīgi vai komandas locekļi bez personāla, varat arī skatīt apakšuzņēmuma līgumu slēgšanas iespējas projekta komandas loceklim ar personālu, ja vien komandas loceklis ar personālu ir līgumdarbinieks. Lai pārskatītu un izvēlētos kādu no pieejamajām apakšuzņēmuma līgumu opcijām projekta grupas dalībniekam ar personālu vai vārdā, rīkojieties šādi:

1. Atlasiet vienu vai vairākus projekta grupas dalībnieku ierakstus, kuros resurss ir nosaukts līgumdarbinieks.
2. Pārliecinieties, vai neviens no atlasītajiem projekta grupas dalībnieku ierakstiem jau nav noslēdzis apakšuzņēmuma līgumus. 
3. Projekta grupas dalībnieku apakšrežā atlasiet **Apakšuzņēmuma opcijas**. Tiek **atvērts dialoglodziņš Apakšuzņēmuma opciju** dialogs. 
4. Ja 1. darbībā atlasījāt tikai vienu projekta grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
      - Izveidojiet jaunas apakšuzņēmuma rindas.
      - Rezervēt esošam apakšuzņēmuma līgumam.
  Ja 1. darbībā atlasījāt vairākus projekta grupas dalībnieku ierakstus, vienīgā pieejamā opcija ir izveidot jaunas apakšuzņēmuma rindas.
5. Iespēja rezervēt pret esošu apakšuzņēmuma rindu ļauj atlasīt apakšuzņēmuma un apakšuzņēmuma rindu, pret kuru vēlaties rezervēt. Izvēloties apakšuzņēmuma rindu, lai rezervētu noslodzi, jums jāpārliecinās:
      - Atlasītā apakšuzņēmuma rinda ir uz laiku. 
      - Loma, kas nepieciešama projekta grupas dalībniekam, atbilst lomai, kas tika iegādāta apakšuzņēmuma līgumā. 
      - Kreditors, ar kuru ir saistīts līguma darbinieks, ir tāds pats kā kreditors apakšlīgumā.
6. Atlasot izveidot jaunas apakšuzņēmuma rindas projekta grupas dalībniekiem, sistēma ļauj atlasīt apakšuzņēmuma līgumu, kuru vēlaties izveidot šīs rindas. Izmantojot šo opciju, pārliecinieties, vai piegādātājs, kuram pieder līguma darbinieks, ir tāds pats kā piegādātājs apakšuzņēmuma līgumā. 
7. Apakšuzņēmuma līgumam, kuru atlasījāt, lai izveidotu jaunas rindas, jābūt melnraksta **statusā**. Izmantojot šo opciju, lai atlasītajiem projekta grupas dalībniekiem izveidotu jaunas apakšuzņēmuma rindas, sistēma katram projekta grupas dalībniekam uz laiku izveidos vienu apakšuzņēmuma rindu. Loma, stundas un datumi tiks kopēti no projekta grupas dalībnieka uz katru izveidoto apakšuzņēmuma rindu.  
8. Ja nosaukts grupas dalībnieks ir saistīts ar apakšuzņēmuma un apakšuzņēmuma rindu, **lauks Darbinieka tips** norādītajā grupas dalībnieku rindā tiks atjaunināts uz **Līgumdarbinieks** un **apakšuzņēmēja derīguma** vērtība tiks iestatīta kā **Derīga**.

## <a name="re-costing-subcontractor-assignments"></a>Apakšuzņēmēju uzdevumu pārvērtēšana

Ja projekta grupas dalībnieks (vispārīgs vai nosaukts) ir saistīts ar apakšuzņēmuma līnijām, izmantojot **dialoglodziņu Apakšuzņēmuma opcijas**, visas piešķires uzdevumiem, kas ir grupas dalībniekam, tiks izmaksātas atkārtoti, pamatojoties uz apakšuzņēmuma līgumam pievienoto pirkšanas cenrādi. **Lapas Detalizēta informācija** par **projektu cilnē Novērtējumi** atlasiet **pogu Atjaunināt cenas**, lai skatītu atjauninātās cenas un/vai izmaksas, kas izriet no lēmuma slēgt apakšuzņēmuma līgumus rezultātā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
