---
title: Vispārējo resursu prasību izpilde
description: Šajā tēmā ir sniegta informācija par rezervācijas nosaukumu resursiem attiecībā uz vispārējo resursu prasībām.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897595"
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


