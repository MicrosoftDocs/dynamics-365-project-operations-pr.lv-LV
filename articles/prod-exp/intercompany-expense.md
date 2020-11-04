---
title: Starpuzņēmumu izdevumi
description: Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā. Šādā gadījumā var izmantot starpuzņēmumu izmaksu līdzekli, lai darbinieka izdevumus piešķirtu juridiskajai personai, kurai tika veikts darbs.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080595"
---
# <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

[!include [banner](../includes/banner.md)]

Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā. Šādā gadījumā var izmantot starpuzņēmumu izmaksu līdzekli, lai darbinieka izdevumus piešķirtu juridiskajai personai, kurai tika veikts darbs. Juridiska persona, kas nodarbina darba ņēmēju, tiek saukta par juridisku personu-aizdevēju. Juridiskā persona, kurai darba ņēmējs uzkrāj izdevumus, tiek saukta par aizņemošo juridisko personu. 

Lai darba ņēmējs varētu izveidot un iesniegt izdevumus darbam, kas tiek veikts citai juridiskai personai, juridiskajā personā-aizdevējā, lapā **Izdevumu pārvaldības parametri** atlasiet opciju **Atļaut starpuzņēmumu izmaksu rindas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Starpuzņēmumu izmaksu nodokļu grāmatošana

[!include [banner](../includes/banner.md)]

Ja vēlaties izmantot nodokļu grupas, kas saistītas ar (avota) juridisko personu-aizdevēju, nevis (galamērķa) juridisko personu-aizņēmēju savā izdevumu atskaitē, jums tā ir jākonfigurē virsgrāmatas PVN iestatīšanā. Ja virsgrāmatas parametrs **Juridiskā persona starpuzņēmumu nodokļu grāmatošanai** ir iestatīts kā **Avots** un **Lietot PVN nodokļu kārtulas** ir iestatīts uz **Nē** , tiks izmantota juridiskās personas-aizdevēja nodokļu kombinācija. Ja viens un tas pats parametrs ir iestatīts uz **Mērķis** , tiks izmantota juridiskās personas-aizņēmēja nodokļu kombinācija. Ja juridiskajām personām ASV parametrs ir iestatīts uz **Avots** , jaunajā lapā **Virsgrāmatas grāmatošanas grupas** ir jākonfigurē arī lauks **Pārdošanas nodokļa parāds**. Grāmatvedības programma izmantos šajā laukā ietverto informāciju, lai iegūtu ar nodokļiem saistītu uzskaites ierakstu.   
Darbība ir konsekventa izdevumu rindām, kas iegrāmatotas ar projektu vai bez tā.  
