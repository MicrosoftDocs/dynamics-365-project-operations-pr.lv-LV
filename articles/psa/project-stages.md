---
title: Projekta posmu tipi
description: Šajā rakstā ir sniegta informācija par projekta posmiem.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d772acce152b08c7986739ac557818e6f97d0fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919069"
---
# <a name="project-stage-types"></a>Projekta posmu tipi 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta posmi ir izstrādāti, lai atspoguļotu projekta statusu tā norises laikā. Pielāgojumus var izmantot, lai automātiski atjauninātu posmus ar biznesa procesa plūsmām, Power Automate vai spraudņu paplašinājumiem.

Noklusējuma BPF ir definēti šādi posmi:

- Jaunas
- Piedāvājums
- Plāns
- Sniegt
- Pabeigts
- Aizvērt 

## <a name="new"></a>Jauns

Kad veidojat projektu, šī projekta posms tiek iestatīts uz **Jauns**. Ja projekts tika izveidots no veidnes, tam var būt grafika, tāmes un darba grupas dati. Pretējā gadījumā tas ir tikai vispārīgas projekta aprises, un atlikušie komponenti ir jāievada.

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
