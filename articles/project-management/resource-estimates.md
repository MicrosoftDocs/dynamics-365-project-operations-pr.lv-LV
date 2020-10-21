---
title: Resursu aprēķini
description: Šajā tēmā ir sniegta informācija par to, kā programmā Project Operations tiek veikti resursu aprēķini.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928586"
---
# <a name="resource-estimates"></a>Resursu aprēķini

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Resursu aprēķini tiek iegūti no laika sadalījuma ieguldījuma, kas tiek definēts darba sadalījuma struktūrā kopā ar piemērojamajām izcenojuma dimensijām. Parasti aprēķins ir **likme/st. par katru komu x stundas.** Katra resursa laika sadalījuma ieguldījums tiek glabāts resursu piešķires ierakstā. Izcenojums tiek glabāts iepriekš definētā cenrādī. Vienību pārvēršana tiek veikta, pamatojoties uz piemērojamo cenrādi.

![Resursu aprēķini](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Noklusējuma izmaksas un izmaksu valūta

Izmaksas tiek iestatītas uz noklusējumu no organizācijas vienības.

## <a name="default-bill-rate-and-sales-currency"></a>Noklusējuma rēķina likme un pārdošanas valūta

Pārdošanas cenas tiek lietotas vienreiz katram darījumam. Pārdošanas cenrāža noklusējuma hierarhija ir šāda:

1. Organizācija
2. Klients
3. Piedāvājums/līgums
