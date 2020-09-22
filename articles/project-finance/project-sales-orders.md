---
title: Projekta pārdošanas pasūtījumi laika un materiālu projektiem
description: Šajā tēmā izskaidrots, kā izveidot projektā balstītus pārdošanas pasūtījumus laika un materiālu projektiem.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753440"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projekta pārdošanas pasūtījumi laika un materiālu projektiem

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šajā tēmā aprakstīts, kā izveidot pārdošanas pasūtījumu projektam. Pārdošanas pasūtījumus var izveidot vienīgi projektiem ar veidu **laiks un materiāli**.

Ja laika un materiālu projektam projekta līgumā ir vairāki finansējuma avoti, ir jāiespējo parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem** lapā **Projekta pārvaldības un uzskaites parametri**. 

> [!NOTE]
> - Atbalsts projekta pārdošanas pasūtījumiem ar vairākiem finansējuma avotiem ir pieejams sākot ar programmas laidienu 10.0.2 vai jaunāku.
> - Parametrs projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem iespējošanai tiks noņemts 2020. gada aprīļa laidiena vilnī, pēc kura šī funkcionalitāte būs iespējota vienmēr.

Projektā balstītus pārdošanas pasūtījumus varat izveidot divos veidos:

- Dodieties uz pašu projektu. Darbību rūtī atlasiet **Pārvaldīt > Elementu uzdevumi > Pārdošanas pasūtījums**. Projekta informācija pēc noklusējuma būs no projekta pārdošanas pasūtījuma. Ja projekta līgumam ir vairāk nekā viens finansējuma avots, būs nepieciešams atlasīt finansējuma avotu, lai iestatītu pārdošanas pasūtījuma klientu. Ja projektam ir tikai viens finansējuma avots, klients tiks iestatīts automātiski.
- Dodieties uz saraksta lapu **Visi pārdošanas pasūtījumi** un izveidojiet jaunu pārdošanas pasūtījumu. Pārdošanas pasūtījumam vajadzēs atlasīt projektu. Kad projekts ir atlasīts, klients tiks iestatīts no finansējuma avota vai arī vajadzēs atlasīt finansējuma avotu, ja projekta līgumam ir vairāki finansējuma avoti.

