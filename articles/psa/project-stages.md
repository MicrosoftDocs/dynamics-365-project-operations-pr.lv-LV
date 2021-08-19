---
title: Projekta posmu tipi
description: Šajā tēmā ir sniegta informācija par projekta posmiem.
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
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996895"
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