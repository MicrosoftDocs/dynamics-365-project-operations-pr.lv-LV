---
title: Starpuzņēmumu izdevumi
description: Šajā tēmā sniegta informācija par to, kā izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001215"
---
# <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā. Varat izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs. Juridiska persona, kas nodarbina darba ņēmēju, tiek saukta par juridisku personu-aizdevēju. Juridiskā persona, kurai darba ņēmējs uzkrāj izdevumus, tiek saukta par aizņemošo juridisko personu. 

Lai darbinieks varētu izveidot un iesniegt starpuzņēmumu izdevumus, ir jāiespējo starpuzņēmumu izdevumu rindas. Aizdevuma juridiskajā entitījā lapā **Izdevumu pārvaldes parametri** atlasiet **Atļaut starpuzņēmumu izdevumu rindas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Starpuzņēmumu izmaksu nodokļu grāmatošana

[!include [banner](../includes/banner.md)]

Pirms varat izmantot nodokļu grupas, kuras jūsu izdevumu atskaitē ir saistītas ar aizdevuma (avota) juridisko entitīju, nevis aizņēmuma (mērķa) juridisko entitīju, ir jāiespējo funkcionalitāte Virsgrāmatas pārdošanas nodokļu iestatīšanas skatā. Ja parametrs **Juridiska entitīja starpuzņēmumu nodokļu izlikšanai** ir iestatīts uz **Avots** un **Piemērot pārdošanas nodokļu piemērošanas kārtulas** ir iestatīts uz **Nē**, tiek izmantota aizņēmuma juridiskās entitījas nodokļu kombinācija. Ja viens un tas pats parametrs ir iestatīts uz **Mērķis**, tiks izmantota juridiskās personas-aizņēmēja nodokļu kombinācija. Ja juridiskajām personām ASV parametrs ir iestatīts uz **Avots**, jaunajā lapā **Virsgrāmatas grāmatošanas grupas** ir jākonfigurē arī lauks **Pārdošanas nodokļa parāds**. Grāmatvedības programma izmantos šajā laukā ietverto informāciju, lai iegūtu ar nodokļiem saistītu uzskaites ierakstu.   
Darbība ir konsekventa izdevumu rindām, kas iegrāmatotas ar projektu vai bez tā.  

## <a name="new-expense-expression-builder"></a>Jauns izmaksu izteiksmju veidotājs

Jaunais izmaksu izteiksmju veidotājs risina problēmas, kas saistītas ar starpuzņēmumu izdevumu scenārijiem, kuros tiek izmantoti projekti. Šis līdzeklis nodrošina, ka, veidojot starpuzņēmumu izdevumus, izdevumu politika tiek pareizi validēta attiecībā pret izdevumu rindā atlasīto projektu un ka izdevumu pārskatu var veiksmīgi iesniegt.

Lai izdevumu izteiksmju veidotājs darbotos, šim līdzeklim ir jābūt ieslēgtam. Turklāt ir jāiestata tāda izmaksu politika, kurai ir projekta ID.

Ja izdevumu rindā jau konfigurējāt politikas, kas validē projekta ID, šīs politikas ir jāatceļ. Pēc tam varat ieslēgt līdzekli un atkārtoti konfigurēt politikas.

Lai ieslēgtu šo līdzekli, veiciet tālāk minētās darbības.

1. Atveriet sadaļu **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Sarakstā atlasiet **Jauns izmaksu izteiksmju veidotājs, lai risinātu problēmas, kas saistītas ar starpuzņēmumu izdevumu scenārijiem, kuros tiek izmantoti projekti**. Pēc tam atlasiet **Iespējot tūlīt**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
