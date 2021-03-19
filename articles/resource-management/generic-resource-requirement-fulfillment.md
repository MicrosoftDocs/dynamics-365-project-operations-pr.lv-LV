---
title: Vispārējo resursu prasību izpilde
description: Šajā tēmā ir sniegta informācija par to, kā rezervēt nosaukumu resursus attiecībā uz vispārējo resursu prasībām.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279597"
---
# <a name="generic-resource-requirement-fulfillment"></a>Vispārējo resursu prasību izpilde

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Varat rezervēt nosauktu resursu, lai aizstātu vispārējo resursu, kam ir nepieciešama resursa prasība.

1. Lapā **Projekti** atlasiet cilni **Darba grupa**.
2. Atlasiet vispārējo resursu, kam sarakstā ir resursu prasības, un pēc tam atlasiet **Rezervēt**. Vai arī atveriet resursu prasības pēc tam atlasiet **Rezervēt**.
3. Lapā **Plānošanas palīgs** atlasiet nosauktu resursu, lai grāmatotu savu projekta darba grupu, un pēc tam atlasiet **Rezervēt**.

Kad rezervēšana ir pabeigta un izpildīta ar nosauktu resursu, vispārējais resurss tiek aizstāts ar nosaukto resursu.

Plāna piešķires tiek atjauninātas, izmantojot arī nosaukto resursu.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Vispārēja resursa izpilde ar vairākiem nosauktiem resursiem
Prasības attiecībā uz vispārējo resursu ar vairākiem nosauktiem resursiem izpilde ir līdzīga viena nosaukta resursa piešķiršanai. Piemēram, ir uzdevums, kura ilgums ir piecas dienas un 120 stundu ilga darba intensitāte. Šo uzdevumu nevar izpildīt viens resurss, kas darbojas tipiskā astoņu stundu dienā vairāk nekā piecu dienu nedēļā. 

Šī prasība attiecas uz 120 stundām robotikas inženierijā piecu dienu laikā, kas ir 24 stundas diennaktī.

Tas ir piemērs, kad ir nepieciešami vairāki resursi, lai izpildītu vispārējo resursu pieprasījumu. Lai izpildītu prasību, jums jārezervē vairāki resursi.

Galvenā atšķirība šajā scenārijā ir tāda, ka vispārējais resurss paliek uzdevumam piešķirtajā darba grupā un rezervētie resursa darba grupas dalībnieki netiek piešķirti kā šīs pozīcijas daļa. Projekta vadītājs var piešķirt darbu atbilstoši nosauktajiem resursiem. Skats **Saskaņošana** var palīdzēt projekta vadītājam sadalīt rezervācijas vairākos resursos uz uzdevumu piešķirēm. Tas netiek darīts automātiski, jo jebkurš scenārijs, kas ir sarežģītāks par iepriekš minēto vienkāršo piemēru, piemēram, ja jums ir vairāku uzdevumu kopums, kas veido šo prasību, vai aktivitāte ir jāuzņemas sistēmai, lai jūs to varētu izmantot kā projekta vadītājs. Tā kā sistēma nevar saprast nolūku, pieņēmumi, iespējams, būs citādi, nekā paredzēts, un radīsies nepareizs vai neparedzams rezultāts. Prognozējamais rezultāts ir tāds, ka vispārējais resurss paliek piešķirts, kamēr projekta vadītājs apzināti neveido uzdevumus ar skata **Saskaņošana** palīdzību.




[!INCLUDE[footer-include](../includes/footer-banner.md)]