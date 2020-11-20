---
title: Piedāvājuma aizvēršana — Lite
description: Šajā tēmā ir sniegta informācija par piedāvājuma slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175720"
---
# <a name="close-a-quote---lite"></a>Piedāvājuma aizvēršana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu. Programmā Microsoft Dynamics 365 Project Operations netiek atbalstītas piedāvājumu aktivizēšanas un pārskatīšanas operācijas, tāpēc var slēgt piedāvājuma melnrakstu.

## <a name="close-a-quote-as-won"></a>Iegūta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā iegūtu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Iegūts. Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts, kurā ir ietverta piedāvājuma informācija. Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms izmaiņu veikšanas tiek parādīts apstiprinājuma dialogs, jo slēgtu piedāvājumu vairs nevar atvērt un izmaiņas ir neatgriezeniskas.

Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu

Ja projektā ir reģistrēti faktiskie laika dati, kamēr tas joprojām ir pievienots piedāvājuma melnrakstam, tiek reģistrētas tikai laika izmaksas vai izdevumi. Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas. Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi. Ja faktiskajās izmaksās ir atsauce uz laika un materiālu līguma rindu, sistēma automātiski izveidos atbilstošos rēķinā neiekļautos pārdošanas faktiskos datus, kad tiks slēgts piedāvājums un tiks izveidots projekta līgums. Ja faktiskajās izmaksās ir atsauce uz fiksētas cenas līguma rindu, lietojumprogramma pārtrauks faktisko izmaksu atkārtotu apstrādi, pamatojoties uz projekta līguma klientu sadalīšanas norēķinu kārtulām.

## <a name="closing-a-quote-as-lost"></a>Zaudēta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā zaudētu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Zaudēts. Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms. Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.

Ja projekta piedāvājuma, kas ir slēgts kā zaudēts, jebkurā rindā ir atsauce uz kādu projektu, arī šis projekts tiek atzīmēts arī kā slēgts, kā arī tiek atceltas visas turpmākās resursu rezervācijas.

> [!NOTE]
> Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.
