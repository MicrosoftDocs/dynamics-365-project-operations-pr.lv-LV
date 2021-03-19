---
title: Starpuzņēmumu izdevumi
description: Šajā tēmā sniegta informācija par to, kā izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271542"
---
# <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā. Varat izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs. Juridiska persona, kas nodarbina darba ņēmēju, tiek saukta par juridisku personu-aizdevēju. Juridiskā persona, kurai darba ņēmējs uzkrāj izdevumus, tiek saukta par aizņemošo juridisko personu. 

Lai darbinieks varētu izveidot un iesniegt starpuzņēmumu izdevumus, ir jāiespējo starpuzņēmumu izdevumu rindas. Aizdevuma juridiskajā entitījā lapā **Izdevumu pārvaldes parametri** atlasiet **Atļaut starpuzņēmumu izdevumu rindas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Starpuzņēmumu izmaksu nodokļu grāmatošana

[!include [banner](../includes/banner.md)]

Pirms varat izmantot nodokļu grupas, kuras jūsu izdevumu atskaitē ir saistītas ar aizdevuma (avota) juridisko entitīju, nevis aizņēmuma (mērķa) juridisko entitīju, ir jāiespējo funkcionalitāte Virsgrāmatas pārdošanas nodokļu iestatīšanas skatā. Ja parametrs **Juridiska entitīja starpuzņēmumu nodokļu izlikšanai** ir iestatīts uz **Avots** un **Piemērot pārdošanas nodokļu piemērošanas kārtulas** ir iestatīts uz **Nē**, tiek izmantota aizņēmuma juridiskās entitījas nodokļu kombinācija. Ja viens un tas pats parametrs ir iestatīts uz **Mērķis**, tiks izmantota juridiskās personas-aizņēmēja nodokļu kombinācija. Ja juridiskajām personām ASV parametrs ir iestatīts uz **Avots**, jaunajā lapā **Virsgrāmatas grāmatošanas grupas** ir jākonfigurē arī lauks **Pārdošanas nodokļa parāds**. Grāmatvedības programma izmantos šajā laukā ietverto informāciju, lai iegūtu ar nodokļiem saistītu uzskaites ierakstu.   
Darbība ir konsekventa izdevumu rindām, kas iegrāmatotas ar projektu vai bez tā.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]