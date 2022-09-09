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
1. Ja konta ierakstam nav pievienoti projekta cenrāži, sistēma aplūko pārdošanas cenrāžus, kas pievienoti projekta parametriem, kuri atbilst projekta piedāvājuma valūtai.
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

Izmaksu cenrāži netiek pēc noklusējuma izmantoti nevienā Project Operators entītijā. Izmaksu cenrāža noteikšana, ko izmantot projekta izmaksām, vienmēr tiek veikta, pamatojoties uz katru darījumu. Sistēma pabeidz tālāk norādīto procesu, lai noteiktu, kuru cenrādi izmantot projekta izmaksām.

1. Sistēma aplūko cenrāžus, kas pievienoti projekta līgumslēdzējas organizācijas vienībai.
1. Pēc tam sistēma aplūko to cenrāžu datuma efektivitāti, kas atbilst ienākošā aplēses konteksta datumam vai faktiskajam kontekstam.

    - *Aplēses konteksts* attiecas uz jebkuru no trim projekta operāciju aplēses kontekstiem:

        - Projekta tāmes rinda
        - Piedāvājuma rindas informācija
        - Līguma rindas detaļas

    - *Faktiskais konteksts* attiecas uz jebkuru no trim faktisko datu avotiem project operations:

       - Manuāli izveidotas ierakstu žurnāla rindas vai korekcijas žurnāla rindas, kas izveidotas labojumu žurnālā
       - Žurnāla rindas, kas tiek izveidotas laika, izdevumu vai materiālu lietojuma žurnālu iesniegšanas laikā
       - Rēķina rindas detaļas

    Kad Project Operations atbilst ienākošās žurnāla rindas vai rēķina rindas datuma *efektivitātei faktiskajā kontekstā*, tiek izmantots lauks Transakcijas **datums**.

    - Ja ienākošā aplēses konteksta vai faktiskā konteksta datumā ir spēkā vairāki cenrāži, tiek atlasīts pēdējais izveidotais cenrādis.
    - Ja projekta līgumorganizācijas struktūrvienībai nav pievienoti cenrāži, sistēma izskata izmaksu cenrāžus, kas ir pievienoti projekta parametriem, kuri atbilst projekta valūtai.

## <a name="enable-multi-currency-cost-price-list"></a>Iespējot cenu sarakstu vairākās valūtās

Šo iestatījumu var atrast sadaļā **Iestatījumu** \> **parametri.** Noklusējuma vērtība ir **Nē**.

Ja šis iestatījums ir iespējots (tas ir, vērtība ir iestatīta uz **Jā**), sistēma darbojas šādi:

- Tas ļauj izmaksu cenrāžus jebkurā valūtā saistīt ar organizācijas struktūrvienību. Piemēram, izmaksu cenrādi EUR valūtā var pievienot organizācijas struktūrvienībai USD valūtā. Sistēma turpinās validēt, vai izmaksu cenrāžiem, kas ir pievienoti organizācijas struktūrvienībai, nav datuma efektivitātes, kas pārklājas.
- Tas apstiprina, ka izmaksu cenrāžiem, kas ir pievienoti projekta parametriem, nav pārklāšanās datuma efektivitātes, pat ja tiem ir dažādas valūtas. Šī darbība atšķiras no noklusējuma uzvedības (tas ir, darbības, kad vērtība ir iestatīta uz **Nē**). Noklusējuma darbībā tiek validēti tikai tie izmaksu cenrāži, kuros ir **viena un tā pati** valūta, lai nodrošinātu nepārklājas datuma efektivitāti.
- Ienākošās transakcijas kontekstā tas nosaka izmaksu cenrādi, pamatojoties tikai uz datuma ietekmi. Šī darbība atšķiras no noklusējuma darbības, kad sistēma atlasa izmaksu cenrādi, kas atbilst gan projekta valūtai, gan datuma efektivitātei.

Šo uzvedības izmaiņu dēļ Project Operations klienti varēs uzturēt globālu izmaksu cenrādi, kas būs svarīgs visam uzņēmumam. Viņiem nevajadzēs būt cenrāžiem katrā operāciju valūtā. Globālajam cenrādim būs datuma efektivitāte, un tas ļaus iestatīt izmaksu likmes jebkurā valūtā konkrētai cenu dimensiju vērtību kombinācijai. Izmaksu cenrāža valūta tiek izmantota tikai, lai ievadītu noklusējuma vērtības, kad **tiek izveidoti lomu cenu**, **kategoriju cenu** un **cenrāža** vienumu ieraksti. Tas netiks izmantots, lai noteiktu cenrādi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
