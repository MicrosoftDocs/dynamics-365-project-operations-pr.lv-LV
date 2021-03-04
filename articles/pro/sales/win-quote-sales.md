---
title: Piedāvājuma aizvēršana — Lite
description: Šajā tēmā ir sniegta informācija par piedāvājuma slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764873"
---
# <a name="close-a-quote---lite"></a>Piedāvājuma aizvēršana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu. Piedāvājuma melnrakstu var slēgt, jo Microsoft Dynamics 365 Project Operations neatbalsta aktivizēšanas un pārskatīšanas darbības.

## <a name="close-a-quote-as-won"></a>Iegūta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā iegūtu, statuss tiek iestatīts uz aizvērtu un statusa iemesls ir Iegūts. Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts, kurā ir ietverta piedāvājuma informācija. Tā kā slēgtu piedāvājumu nevar atvērt no jauna, jūsu izmaiņas apstiprinās apstiprinājuma dialoglodziņš.

Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu

Ja projekta laikam ir kādi faktiskie dati, kamēr tas joprojām ir pievienots projekta piedāvājumam, tiek ierakstītas tikai laika vai izdevumu izmaksas. Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas. Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi. Ja izmaksu faktiskās vērtības atsaucas uz laika un materiāla līguma rindu, atbilstošie rēķinā neiekļautie pārdošanas faktiskie dati tiek izveidoti laikam, kad piedāvājums ir slēgts un tiek izveidots projekta līgums. Ja izdevumu faktiskie dati atsaucas uz fiksētas cenas līguma rindu, programma beigs no jauna pārstrādāt izmaksu faktiskās vērtības, kuras balstīt dalīto norēķinu kārtulās projekta līguma klientiem.

## <a name="closing-a-quote-as-lost"></a>Zaudēta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā zaudētu, statuss tiek iestatīts uz Aizvērtu un statusa iemesls ir Zaudēts. Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms. Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.

Ja projekta piedāvājums, kas ir aizvērts kā Zaudēts attiecas uz projektu jebkurā no tā rindām, šo projektu arī atzīmē kā Slēgtu. Visas resursu rezervācijas no šīs dienas uz priekšu tiek atceltas.

> [!NOTE]
> Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.
