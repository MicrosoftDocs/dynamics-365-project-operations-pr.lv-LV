---
title: Projekta posmi
description: Šajā tēmā sniegta informācija par projekta posmiem, kas ir pieejami Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea8b74813e8a51930a03571eab0d962e14f66a8fd6cb978d3435570a01ce5c5d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003064"
---
# <a name="project-stages"></a>Projekta posmi

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta posmi ir izstrādāti, lai atspoguļotu projekta statusu tā norises laikā. Pielāgojumus var izmantot, lai automātiski atjauninātu posmus ar biznesa procesa plūsmām, Power Automate vai spraudņu paplašinājumiem.

Biznesa procesa plūsmā ir definēti šādi posmi:

- Izveidot:
- Piedāvājums
- Plāns
- Piegādāt
- Pabeigts
- Aizvēršana 

## <a name="new"></a>Izveidot:

Kad veidojat projektu, šī projekta posms tiek iestatīts uz **Jauns**. Ja projekts tika izveidots no veidnes, tam var būt grafika, tāmes un darba grupas dati. Pretējā gadījumā tās ir vispārīgas projekta aprises, un atlikušie komponenti ir jāievada.

## <a name="quote"></a>Piedāvājums

Kad projektu saistāt ar piedāvājumu vai kad projektu izveidojat no piedāvājuma, projekta posms tiek iestatīts uz **Piedāvājums** un tiek atjaunināti arī prognozētie sākuma un beigu datumi. Kamēr projekts ir posmā **Piedāvājums**, lapas **Projekta entītija** cilnē **Pārdošana** tiek rādīta detalizēta informācija par šo piedāvājumu.

## <a name="plan"></a>Plāns

Kad iegūstat piedāvājumu, kurš ir saistīts ar projektu, un kad šis projekts tiek pārvietots uz fāzi **Līgums**, projekta posms tiek atjaunināts uz **Plāns**. Kamēr projekts ir posmā **Plāns**, lapā **Projekta entītija** tiek rādīta detalizēta informācija par šo līgumu.

## <a name="deliver"></a>Sniegt

Kad projekta plāns ir pabeigts un esat gatavs sākt pašu projektu, projektu vadītājam ir jāatjaunina projekta posms uz **Sniegt**, lai parādītu, ka projekts ir sācies.

## <a name="complete"></a>Pabeigts 

Kad darbs pie projekta ir pabeigts, projektu vadītājs var atjaunināt posmu uz **Pabeigts**. Atjauninot projekta posmu uz **Pabeigts**, projektu vadītājs norāda, ka darbs ir 100-procentīgi pabeigts, bet projekts tiek paturēts atvērts, lai varētu ierakstīt visus gaidošos laika vai izdevumu ierakstus.

## <a name="close"></a>Aizvērt

Kad visas transakcijas projektam ir ierakstītas, projektu vadītājs var atjaunināt posmu uz **Aizvērt**. Šajā brīdī nekādas transakcijas vairs nevar ierakstīt, un projekts ir iestatīts uz tikai lasāmu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]