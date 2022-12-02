---
title: Noklusējuma cenrāži
description: Šajā rakstā ir sniegta informācija par noklusējuma pārdošanas un izmaksu cenrāžiem programmā Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410272"
---
# <a name="default-price-lists"></a>Noklusējuma cenrāži

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

## <a name="sales-price-lists"></a>Pārdošanas cenrāži

Katrā projekta piedāvājumā un līgumā Dynamics 365 Project Operations ir noklusējuma pārdošanas cenrādis. 

### <a name="price-list-default-on-project-quotes"></a>Cenrāža noklusējums projekta piedāvājumos
Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kurš cenrādis projekta piedāvājumam tiks izmantots pēc noklusējuma.

1. Sistēma apskata cenrāžus, kas ir pievienoti uzņēmuma projekta cenrāžiem. 
1. Ja uzņēmuma ierakstam nav pievienoti projekta cenrāži, sistēma apskata pārdošanas cenrāžus, kas pievienoti ar projekta parametriem un kas atbilst projekta piedāvājuma valūtai.
1. Pēc tam sistēma pārbauda to cenrāžu spēkā būšanas datumu, kas atbilst projekta piedāvājuma datumu diapazonam. Precīzāk — datumu, kurā tika izveidots piedāvājums.
1. Ja ir vairāki cenrāži, kas ir spēkā projekta piedāvājuma datumā, projekta piedāvājumā pēc noklusējuma tiek izmantoti visi cenrāži.
1. Ja projekta piedāvājumā attiecīgajā datumā nav spēkā neviens cenrādis, projekta piedāvājumā netiek pēc noklusējuma izmantots projekta cenrādis. Projekta piedāvājumā tiks parādīts brīdinājuma ziņojums. Ziņojumā ir norādīts, ka faktiskajiem datiem un aprēķiniem projektā netiks rādītas cenas, jo nav pievienotu projekta cenrāžu.

### <a name="price-list-default-on-project-contracts"></a>Cenrāža noklusējums projekta līgumos 
Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kurš cenrādis projekta līgumam tiks izmantots pēc noklusējuma.

1. Ja līgums ir izveidots no piedāvājuma, projekta cenrāži piedāvājumā tiek kopēti atsevišķi un pievienoti projekta līgumam.
1. Ja līgums ir izveidots no nulles, sistēma apskata cenrāžus, kas ir pievienoti uzņēmuma projekta cenrāžiem. Ja uzņēmuma ierakstam nav pievienoti projekta cenrāži, sistēma meklē pārdošanas cenrāžus, kas pievienoti ar projekta parametriem, kuri atbilst projekta līguma valūtai.
1. Pēc tam sistēma pārbauda to cenrāžu spēkā būšanas datumu, kas atbilst projekta līguma datumu diapazonam. Precīzāk — datumu, kurā tika izveidots līgums.
1. Ja ir vairāki cenrāži, kas ir spēkā līguma datumā, līgumā pēc noklusējuma tiek izmantoti visi cenrāži.
1. Ja līgumā attiecīgajā datumā nav spēkā neviens cenrādis, līgumā netiek pēc noklusējuma izmantoti projekta cenrāži. Līgumā tiks parādīts brīdinājuma ziņojums. Ziņojumā ir norādīts, ka faktiskajiem datiem un aprēķiniem projektā netiks rādītas cenas, jo nav pievienotu projekta cenrāžu.

## <a name="cost-price-lists"></a>Izmaksu cenrāži

Izmaksu cenrāži netiek pēc noklusējuma izmantoti nevienā Project Operators entītijā. Projekta izmaksām izmantojamā izmaksu cenrāža noteikšana vienmēr tiek veikta katrai transakcijai. Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kuru cenrādi izmantot projekta izmaksām.

1. Sistēma apskata cenrāžus, kas ir pievienoti projekta līgumslēdzējas organizācijas struktūrvienībai.
1. Pēc tam sistēma apskata to cenrāžu spēkā būšanas datumus, kas atbilst ienākošā novērtējuma konteksta vai faktisko datu konteksta datumam.

    - *Novērtējuma konteksts* attiecas uz jebkuru no trim novērtējuma kontekstiem programmā Project Operations.

        - Projekta tāmes rinda
        - Piedāvājuma rindas informācija
        - Līguma rindas detaļas

    - *Faktisko datu konteksts* attiecas uz jebkuru no trim faktisko datu avotiem programmā Project Operations.

       - Ierakstu žurnāla rindas, kas ir izveidotas manuāli, vai korekciju žurnāla rindas, kas izveidotas korekciju žurnālā
       - Žurnāla rindas, kas izveidotas laika, izdevumu vai materiālu lietojuma žurnālu iesniegšanas laikā
       - Rēķina rindas detaļas

    Kad programma Project Operations salīdzina ienākošās žurnāla rindas vai rēķina rindas informācijas spēkā esamības datumu *faktisko datu kontekstā*, tā izmanto lauku **Transakcijas datums**.

    - Ja vairāki cenrāži ir spēkā ienākošā attiecībā uz novērtējuma kontekstu vai faktisko datu kontekstu, tiek atlasīts cenrādis, kas izveidots visnesenāk.
    - Ja projekta līgumslēdzēja organizācijas struktūrvienībai nav neviena pievienota cenrāža, sistēma apskata izdevumu cenrāžus, kas pievienoti projekta parametriem un atbilst projekta valūtai.

## <a name="enable-multi-currency-cost-price-list"></a>Iespējot cenu sarakstu vairākās valūtās

Šo iestatījumu var atrast sadaļā **Iestatījumi** \> **Parametri**. Noklusējuma vērtība ir **Nē**.

Ja šis iestatījums ir iespējots (tas ir, vērtība ir iestatīta uz **Jā**), sistēma darbojas, kā aprakstīts tālāk.

- Tā ļauj ar organizācijas vienību saistīt izmaksu cenrādi jebkurā valūtā. Piemēram, izmaksu cenrādis EUR valūtā var tikt pievienots organizācijas vienībai ar USD valūtu. Sistēma turpinās apstiprināt, ka izmaksu cenrāžiem, kas tiek pievienoti organizācijas vienībai, nepārklājas spēkā esamības datumi.
- Tā apstiprina, ka projekta parametriem pievienoto izmaksu cenrāžu spēkā esamības datumi nepārklājas pat tad, ja tiem ir dažādas valūtas. Šī uzvedība atšķiras no noklusējuma uzvedības (tas ir, kad vērtība ir iestatīta uz **Nē**). Noklusējuma uzvedības gadījumā spēkā esamības datumu nepārklāšanās tiek apstiprināta tikai tiem izmaksu cenrāžiem, kuriem ir **viena un tā pati** valūta.
- Ienākošas transakcijas kontekstā tā nosaka izmaksu cenrādi, pamatojoties tikai uz spēkā esamība datumu. Šī uzvedība atšķiras no noklusējuma uzvedības, kad sistēma atlasa izmaksu cenrādi, kas atbilst gan projekta valūtai, gan spēkā esamības datumam.

Šo uzvedības izmaiņu dēļ Project Operations klienti varēs uzturēt globālo izmaksu cenrādi, kas būs nepieciešams visam uzņēmumam. Viņiem nebūs nepieciešams cenrādis katrā operāciju valūtā. Globālajam cenrādim ir spēkā esamības datums, un tas ļauj iestatīt izmaksu likmes jebkurā valūtā noteiktai cenu noteikšanas dimensijas vērtību kombinācijai. Izmaksu cenrāža valūta tiek izmantota tikai noklusējuma vērtību ievadīšanai, kad tiek izveidoti vienumu ieraksti **Lomu cenas**, **Kategoriju cenas** un **Cenrādis**. Tā netiks izmantota cenrāža noteikšanai.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
