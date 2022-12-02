---
title: Apakšlīguma iespējas projekta grupas dalībniekiem
description: Šajā rakstā izskaidrots apakšlīgumu izveides opcijas projekta darba grupas dalībniekiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522288"
---
# <a name="subcontracting-options-for-project-team-members"></a>Apakšlīguma iespējas projekta grupas dalībniekiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Programmā Microsoft Dynamics 365 Project Operations varat novērtēt vienam vai vairākiem projekta darba grupas dalībniekiem pieejamās apakšlīgumu izveides opcijas. Pieejamās apakšlīgumu izveides opcijas ļauj:

- izveidot jaunu apakšlīgumu un/vai izveidojiet jaunas rindas esošā apakšlīgumā atlasītajiem projekta darba grupas dalībniekiem; 
- rezervēt attiecībā pret jau esošu apakšlīgumu un apakšlīguma rindu. 

Varat izvēlēties no pieejamajām apakšlīgumu slēgšanas opcijām vispārīgiem projekta darba grupas dalībniekiem vai izvēlēties no projekta darba grupas dalībniekiem, kas ir iekļauti personālā, izmantojot nosauktu resursu, kurš ir līgumdarbinieks. 

Apakšlīgumu opcijas nav pieejamas:

- projekta darba grupas dalībniekiem, kas ir iekļauti personālā ar darbinieku; 
- projekta darba grupas dalībniekiem, kuri jau ir saistīti ar apakšlīgumu vai apakšlīguma rindu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Apakšlīguma izveide personālā neiekļautam projekta grupas dalībniekam

Lai pārskatītu un izvēlētos no pieejamajām apakšlīgumu slēgšanas opcijām attiecībā uz vispārēju vai personālā neiekļautu projekta darba grupas dalībnieku, veiciet tālāk norādītās darbības.

1. Atlasiet vienu vai vairākus projekta darba grupas dalībnieku ierakstus, kur resurss ir vispārējs resurss.
2. Pārliecinieties, ka nevienam no atlasītajiem projekta darba grupas dalībnieku ierakstiem vēl nav noslēgts apakšlīgums. 
3. Projekta darba grupas dalībnieku apakšrežģī atlasiet **Apakšlīguma opcijas**. Tiek atvērts dialoglodziņš **Apakšlīguma opcijas**. 
4. Ja 1. darbībā atlasījāt tikai vienu projekta darba grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
    - jaunu apakšlīguma rindu izveide; 
    - rezervēšana attiecībā pret esošu apakšlīgumu. Ja 1. darbībā atlasījāt vairākus projekta darba grupas dalībnieku ierakstus, vienīgā pieejamā opcija ir jaunu apakšlīguma rindu izveide.
5. Opcija rezervēt attiecībā pret esošu apakšlīguma rindu ļauj atlasīt apakšlīgumu un apakšlīguma rindu, attiecībā pret kuru vēlaties veikt rezervāciju. Atlasot apakšlīguma rindu noslodzes rezervēšanai, ir jānodrošina, ka atlasītā apakšlīguma rinda ir paredzēta laikam un ka projekta darba grupas dalībniekam nepieciešamā loma atbilst lomai, kas tika iegādāta apakšlīguma rindā.
6. Projekta darba grupas dalībniekiem atlasot jaunas apakšlīguma rindas, sistēma ļauj atlasīt apakšlīgumu, kuram vēlaties izveidot šīs rindas. Apakšlīgumam, ko atlasāt jaunu rindu izveidei, ir nepieciešams statuss **Melnraksts**. Izmantojot šo opciju, lai atlasītajiem projekta darba grupas dalībniekiem izveidotu jaunas apakšlīguma rindas, sistēma katram projekta darba grupas dalībniekam izveido vienu apakšlīguma rindu, kas paredzēta laikam. Loma, stundas un datumi tiek kopēti no projekta darba grupas dalībnieka uz katru izveidoto apakšlīguma rindu. 
7. Ja ar apakšlīgumu un apakšlīguma rindu tiek saistīts vispārējs darba grupas dalībnieks, lauks **Darbinieka tips** vispārējā darba grupas dalībnieka rindā tiek atjaunināts uz **Līgumdarbinieks**, un vērtība **Apakšuzņēmēja līguma derīgums** tiek iestatīta uz **Derīgs**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Apakšlīguma izveide personālā iekļautam projekta grupas dalībniekam

Tāpat kā vispārējiem vai personālā neiekļautiem darba grupas dalībniekiem, varat skatīt arī personālā iekļautu projekta darba grupas dalībnieku apakšlīgumu slēgšanas opcijas, kamēr vien personālā iekļautais darba grupas dalībnieks ir līgumdarbinieks. Lai pārskatītu un izvēlētos no pieejamajām apakšlīgumu slēgšanas opcijām attiecībā uz personālā iekļautu vai nosauktu projekta darba grupas dalībnieku, veiciet tālāk norādītās darbības.

1. Atlasiet vienu vai vairākus projekta darba grupas dalībnieku ierakstus, kur resurss ir nosaukts līgumdarbinieks.
2. Pārliecinieties, ka nevienam no atlasītajiem projekta darba grupas dalībnieku ierakstiem vēl nav noslēgts apakšlīgums. 
3. Projekta darba grupas dalībnieku apakšrežģī atlasiet **Apakšlīguma opcijas**. Tiek atvērts dialoglodziņš **Apakšlīguma opcijas**. 
4. Ja 1. darbībā atlasījāt tikai vienu projekta darba grupas dalībnieka ierakstu, būs pieejamas šādas opcijas:
      - jaunu apakšlīguma rindu izveide;
      - rezervēšana attiecībā pret esošu apakšlīgumu.
  Ja 1. darbībā atlasījāt vairākus projekta darba grupas dalībnieku ierakstus, vienīgā pieejamā opcija ir jaunu apakšlīguma rindu izveide.
5. Opcija rezervēt attiecībā pret esošu apakšlīguma rindu ļauj atlasīt apakšlīgumu un apakšlīguma rindu, attiecībā pret kuru vēlaties veikt rezervāciju. Atlasot apakšlīguma rindu noslodzes rezervēšanai, ir jānodrošina tālāk norādītie nosacījumi.
      - Atlasītā apakšlīguma rinda ir paredzēta laikam. 
      - Projekta darba grupas dalībniekam nepieciešamā loma atbilst lomai, kas tika iegādāta apakšlīguma rindā. 
      - Piegādātājs, ar kuru ir saistīts līgumdarbinieks, ir tas pats kā piegādātājs apakšlīgumā.
6. Projekta darba grupas dalībniekiem atlasot jaunas apakšlīguma rindas, sistēma ļauj atlasīt apakšlīgumu, kuram vēlaties izveidot šīs rindas. Ar šo opciju jums jānodrošina, ka piegādātājs, kuram pieder līgumdarbinieks, ir tas pats kā piegādātājs apakšlīgumā. 
7. Apakšlīgumam, ko atlasāt jaunu rindu izveidei, ir nepieciešams statuss **Melnraksts**. Izmantojot šo opciju, lai atlasītajiem projekta darba grupas dalībniekiem izveidotu jaunas apakšlīguma rindas, sistēma katram projekta darba grupas dalībniekam izveido vienu apakšlīguma rindu, kas paredzēta laikam. Loma, stundas un datumi tiek kopēti no projekta darba grupas dalībnieka uz katru izveidoto apakšlīguma rindu.  
8. Ja ar apakšlīgumu un apakšlīguma rindu tiek saistīts nosaukts darba grupas dalībnieks, lauks **Darbinieka tips** nosauktā darba grupas dalībnieka rindā tiek atjaunināts uz **Līgumdarbinieks**, un vērtība **Apakšuzņēmēja līguma derīgums** tiek iestatīta uz **Derīgs**.

## <a name="re-costing-subcontractor-assignments"></a>Apakšlīguma piešķīrumu izmaksu pārrēķināšana

Saistot projekta darba grupas dalībnieku (vispārēju vai nosauktu) ar apakšlīguma rindām, izmantojot dialoglodziņu **Apakšlīguma opcijas**, visiem darba grupas dalībnieka uzdevumu piešķīrumiem tiks pārrēķinātas izmaksas, balstoties uz pirkumu cenrādi, kas pievienots apakšlīgumam. Cilnē **Aprēķini**, kas atrodas lapā **Detalizēta informācija par projektu**, atlasiet pogu **Atjaunināt cenas**, lai skatītu atjaunināto izcenojumu un/vai izmaksas, kas rodas no lēmuma slēgt apakšlīgumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
