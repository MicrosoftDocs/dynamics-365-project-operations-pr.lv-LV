---
title: Resursu prasības ir redzamas resursiem.
description: Šajā rakstā ir sniegta informācija par nosaukto resursu rezervēšanu vispārējai resursu prasībai.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916251"
---
# <a name="book-named-resources-from-resource-requirements"></a>Resursu prasības ir redzamas resursiem.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Varat rezervēt nosauktu resursu, lai aizstātu vispārējo resursu, kam ir nepieciešama resursa prasība.

1. Project Service Automation (PSA) lapā **Projekti** noklikšķiniet uz cilnes **Darba grupa**.
2. Atlasiet vispārējo resursu, kam sarakstā ir resursu prasības, un pēc tam noklikšķiniet uz **Rezervēt**. Vai arī atveriet resursu prasības pēc tam noklikšķiniet uz **Rezervēt**.


![Vispārēja darba grupas dalībnieka rezervēšana.](media/RM-how-to-14.png)


3. Lapā **Plānošanas palīgs** atlasiet nosauktu resursu, lai grāmatotu savu projekta darba grupu, un pēc tam noklikšķiniet uz **Rezervēt**.

![Vispārēja darba grupas locekļa rezervēšana, izmantojot plānošanas palīgu.](media/RM-how-to-15.png)

Kad rezervēšana ir pabeigta un izpildīta ar nosauktu resursu, vispārējais resurss tiek aizstāts ar nosaukto resursu.

![Nosauktais darba grupas dalībnieks, kas aizstāj vispārējo darba grupas dalībnieku.](media/RM-how-to-16.png)

Plāna piešķires tiek atjauninātas, izmantojot arī nosaukto resursu.

![Projekta uzdevumiem piešķirtais nosauktais darba grupas dalībnieks.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Vispārēja resursa izpilde ar vairākiem nosauktiem resursiem
Prasības attiecībā uz vispārējo resursu ar vairākiem nosauktiem resursiem izpilde ir līdzīga viena nosaukta resursa piešķiršanai. Piemēram, ir uzdevums, kura ilgums ir piecas dienas un 120 stundu ilga darba intensitāte. Šo uzdevumu nevar izpildīt viens resurss, kas darbojas tipiskā astoņu stundu dienā vairāk nekā piecu dienu nedēļā. 

![Uzdevums, kam nepieciešamas 120 stundu ilgs darbs piecu dienu laikā.](media/RM-how-to-21.png)

Šī prasība attiecas uz 120 stundām robotikas inženierijā piecu dienu laikā, kas ir 24 stundas diennaktī.

![Dienas prasības.](media/RM-how-to-22.png)

Tas ir piemērs, kad ir nepieciešami vairāki resursi, lai izpildītu vispārējo resursu pieprasījumu. Lai izpildītu prasību, jums jārezervē vairāki resursi.

![Lai izpildītu prasību, ir jārezervē vairāki resursi.](media/RM-how-to-23.png)

Galvenā atšķirība šajā scenārijā ir tāda, ka vispārējais resurss paliek uzdevumam piešķirtajā darba grupā un rezervētie resursa darba grupas dalībnieki netiek piešķirti kā šīs pozīcijas daļa. Projekta vadītājs var piešķirt darbu atbilstoši nosauktajiem resursiem. Skats **Saskaņošana** var palīdzēt projekta vadītājam sadalīt rezervācijas vairākos resursos uz uzdevumu piešķirēm. Tas netiek darīts automātiski, jo jebkurš scenārijs, kas ir sarežģītāks par iepriekš minēto vienkāršo piemēru, piemēram, ja jums ir vairāku uzdevumu kopums, kas veido šo prasību, aktivitāte ir jāuzņemas sistēmai, lai jūs to varētu izmantot kā projekta vadītājs. Tā kā sistēma nevar saprast nolūku, pastāv iespēja, ka pieņēmumi būs citādi, nekā paredzēts, radīsies nepareizs vai neparedzams rezultāts. Prognozējamais rezultāts ir tāds, ka vispārējais resurss paliek piešķirts, kamēr projekta vadītājs apzināti neveido uzdevumus ar skata **Saskaņošana** palīdzību.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
