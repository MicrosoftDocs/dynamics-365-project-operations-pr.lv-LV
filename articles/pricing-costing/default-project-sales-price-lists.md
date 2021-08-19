---
title: Noklusējuma cenrāži
description: Šajā tēmā ir sniegta informācija par noklusējuma pārdošanas un izmaksu cenrāžiem programmā Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5e38e2f0b553b789956c6d73d481ab0ed2ce3a77815e7cf8c058a0b4666c558
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989875"
---
# <a name="default-price-lists"></a>Noklusējuma cenrāži

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

## <a name="sales-price-lists"></a>Pārdošanas cenrāži

Katrā projekta piedāvājumā un līgumā Dynamics 365 Project Operations ir noklusējuma pārdošanas cenrādis. 

### <a name="price-list-default-on-project-quotes"></a>Cenrāža noklusējums projekta piedāvājumos
Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kurš cenrādis projekta piedāvājumam tiks izmantots pēc noklusējuma.

1. Sistēma apskata cenrāžus, kas ir pievienoti uzņēmuma projekta cenrāžiem. 
2. Ja uzņēmuma ierakstam ir pievienoti projekta cenrāži, sistēma apskata pārdošanas cenrāžus, kas pievienoti ar projekta parametriem un kas atbilst projekta piedāvājuma valūtai.
3. Pēc tam sistēma pārbauda to cenrāžu spēkā būšanas datumu, kas atbilst projekta piedāvājuma datumu diapazonam. Precīzāk — datumu, kurā tika izveidots piedāvājums.
4. Ja ir vairāki cenrāži, kas ir spēkā projekta piedāvājuma datumā, projekta piedāvājumā pēc noklusējuma tiek izmantoti visi cenrāži.
5. Ja projekta piedāvājumā attiecīgajā datumā nav spēkā neviens cenrādis, projekta piedāvājumā netiek pēc noklusējuma izmantots projekta cenrādis. Projekta piedāvājumā tiks parādīts brīdinājuma ziņojums. Ziņojumā ir norādīts, ka faktiskajiem datiem un aprēķiniem projektā netiks rādītas cenas, jo nav pievienotu projekta cenrāžu.

### <a name="price-list-default-on-project-contracts"></a>Cenrāža noklusējums projekta līgumos 
Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kurš cenrādis projekta līgumam tiks izmantots pēc noklusējuma.

1. Ja līgums ir izveidots no piedāvājuma, projekta cenrāži piedāvājumā tiek kopēti atsevišķi un pievienoti projekta līgumam.
2. Ja līgums ir izveidots no nulles, sistēma apskata cenrāžus, kas ir pievienoti uzņēmuma projekta cenrāžiem. Ja uzņēmuma ierakstam nav pievienoti projekta cenrāži, sistēma meklē pārdošanas cenrāžus, kas pievienoti ar projekta parametriem, kuri atbilst projekta līguma valūtai.
4. Pēc tam sistēma pārbauda to cenrāžu spēkā būšanas datumu, kas atbilst projekta līguma datumu diapazonam. Precīzāk — datumu, kurā tika izveidots līgums.
5. Ja ir vairāki cenrāži, kas ir spēkā līguma datumā, līgumā pēc noklusējuma tiek izmantoti visi cenrāži.
6. Ja līgumā attiecīgajā datumā nav spēkā neviens cenrādis, līgumā netiek pēc noklusējuma izmantoti projekta cenrāži. Līgumā tiks parādīts brīdinājuma ziņojums. Ziņojumā ir norādīts, ka faktiskajiem datiem un aprēķiniem projektā netiks rādītas cenas, jo nav pievienotu projekta cenrāžu.

## <a name="cost-price-lists"></a>Izmaksu cenrāži

Izmaksu cenrāži netiek pēc noklusējuma izmantoti nevienā Project Operators entītijā. Projekta izmaksām izmantojamā izmaksu cenrāža noteikšana vienmēr tiek veikta attiecīgajā momentā. Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kuru cenrādi izmantot projekta izmaksām.

1. Vispirms sistēma apskata cenrāžus, kas ir pievienoti projekta līgumslēdzējas organizācijas struktūrvienībai.
2. Pēc tam sistēma apskata to cenrāžu spēkā būšanas datumus, kas atbilst ienākošā novērtējuma vai faktiskajās rindas datumam. Šādā gadījumā *novērtējuma rinda* attiecas uz visiem trim novērtējuma kontekstiem programmā Project Operations.

    - Projekta tāmes rinda
    - Piedāvājuma rindas informācija
    - Līguma rindas detaļas
  
3. Ja ir vairāki cenrāži, kas ir spēkā attiecībā uz ienākošo budžetu vai faktiskajiem datumiem, tiek atlasīts cenrādis, kas izveidots visnesenāk.
4. Ja projekta līgumslēdzēja organizācijas struktūrvienībai nav neviena pievienota cenrāža, sistēma apskata izdevumu cenrāžus, kas pievienoti projekta parametriem un atbilst projekta valūtai.
5. Pēc tam sistēma apskata to cenrāžu spēkā būšanas datumus, kas atbilst ienākošā novērtējuma vai faktiskajās rindas datumam. 
6. Ja ir vairāki cenrāži, kas ir spēkā attiecībā uz ienākošo budžetu vai faktiskajiem datumiem, tiek atlasīts cenrādis, kas izveidots visnesenāk.
7. Ja projekta parametriem nav pievienotu izmaksu cenrāžu ar atbilstošu valūtu un spēkā būšanas datumu, sistēma pēc noklusējuma iestata izmaksu likmi uz nulli (0) ienākošajā tāmē vai faktiskajā rindā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]