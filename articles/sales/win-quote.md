---
title: Piedāvājuma slēgšana
description: Šajā tēmā ir sniegta informācija par piedāvājumu slēgšanu programmā Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993430"
---
# <a name="close-a-quote"></a>Piedāvājuma slēgšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu. Tā kā Microsoft Dynamics 365 Project Operations piedāvājumu funkcijas Aktivizēt un Pārskatīt netiek atbalstītas, varat aizvērt piedāvājuma melnrakstu.

## <a name="close-a-quote-as-won"></a>Iegūta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā iegūtu, piedāvājumam tiks iestatīts statuss **Slēgts** un statusa iemesls **Iegūts**. Slēdzot piedāvājumu, tas kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts ar visu piedāvājuma informāciju. Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.

No projekta piedāvājuma izveidotais projekta līgums ir pieejams arī Project Operations modulī Projekta pārvaldība un grāmatvedība. Ja projekta līgums nav kartēts uz projektu jebkurā no tā rindām, šis projekta līgums tiek padarīts pieejams kā neaktīvs projekta līgums un kļūst aktīvs, tiklīdz projekts tiek kartēts uz vismaz vienu no tā līguma rindām.

Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu

Ja projektā ir reģistrēti faktiskie laika dati, kamēr tas joprojām ir pievienots piedāvājuma melnrakstam, tiek reģistrētas tikai laika izmaksas vai izdevumi. Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas. Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi. Ja faktiskajās izmaksās ir atsauce uz laika un materiālu līguma rindu, sistēma automātiski izveidos atbilstošos rēķinā neiekļautos pārdošanas faktiskos datus, kad tiks slēgts piedāvājums un tiks izveidots projekta līgums. Ja faktiskajās izmaksās ir atsauce uz fiksētas cenas līguma rindu, lietojumprogramma pārtrauks faktisko izmaksu atkārtotu apstrādi, pamatojoties uz projekta līguma klientu sadalīšanas norēķinu kārtulām.

Visi atkārtoti apstrādātie faktiskie dati ir pieejami projekta grāmatvedim modulī Projekta pārvaldība un grāmatvedība, lai tos pārskatītu, atjauninātu un grāmatotu virsgrāmatā. 

## <a name="close-a-quote-as-lost"></a>Zaudēta piedāvājuma slēgšana

Slēdzot projekta piedāvājumu kā zaudētu, piedāvājums tiks slēgts ar statusu **Slēgts** un statusa iemeslu **Zaudēts**. Slēdzot piedāvājumu, tas kļūst tikai lasāms. Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.

Ja projekta piedāvājuma, kas ir slēgts kā zaudēts, jebkurā rindā ir atsauce uz kādu projektu, arī šis projekts tiek atzīmēts arī kā slēgts, kā arī tiek atceltas visas turpmākās resursu rezervācijas.

> [!NOTE]
> Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]