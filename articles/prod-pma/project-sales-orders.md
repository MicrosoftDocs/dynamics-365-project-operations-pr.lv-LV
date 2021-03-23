---
title: Projekta pārdošanas pasūtījumi laika un materiālu projektiem
description: Šajā tēmā izskaidrots, kā izveidot projektā balstītus pārdošanas pasūtījumus laika un materiālu projektiem.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289063"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projekta pārdošanas pasūtījumi laika un materiālu projektiem

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot pārdošanas pasūtījumu projektam. Pārdošanas pasūtījumus var izveidot vienīgi projektiem ar veidu **laiks un materiāli**.

Ja laika un materiālu projektam projekta līgumā ir vairāki finansējuma avoti, ir jāiespējo parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem** lapā **Projekta pārvaldības un uzskaites parametri**. 

> [!NOTE]
> - Atbalsts projekta pārdošanas pasūtījumiem ar vairākiem finansējuma avotiem ir pieejams sākot ar programmas laidienu 10.0.2 vai jaunāku.
> - Parametrs projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem iespējošanai tiks noņemts 2020. gada aprīļa laidiena vilnī, pēc kura šī funkcionalitāte būs iespējota vienmēr.

Projektā balstītus pārdošanas pasūtījumus varat izveidot divos veidos:

- Dodieties uz pašu projektu. Darbību rūtī atlasiet **Pārvaldīt > Elementu uzdevumi > Pārdošanas pasūtījums**. Projekta informācija pēc noklusējuma būs no projekta pārdošanas pasūtījuma. Ja projekta līgumam ir vairāk nekā viens finansējuma avots, būs nepieciešams atlasīt finansējuma avotu, lai iestatītu pārdošanas pasūtījuma klientu. Ja projektam ir tikai viens finansējuma avots, klients tiks iestatīts automātiski.
- Dodieties uz saraksta lapu **Visi pārdošanas pasūtījumi** un izveidojiet jaunu pārdošanas pasūtījumu. Pārdošanas pasūtījumam vajadzēs atlasīt projektu. Kad projekts ir atlasīts, klients tiks iestatīts no finansējuma avota vai arī vajadzēs atlasīt finansējuma avotu, ja projekta līgumam ir vairāki finansējuma avoti.



[!INCLUDE[footer-include](../includes/footer-banner.md)]