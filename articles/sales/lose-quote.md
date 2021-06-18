---
title: Projekta piedāvājumu kopēšana
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu kopēšanu Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e9009391d33c5dd5988ae65e13ca1ca1ec398bc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999095"
---
# <a name="copy-project-based-quotes"></a>Projekta piedāvājumu kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Jaunu Projekta piedāvājumu var viegli izveidot, nokopējot esošu piedāvājumu. 

- Lai kopētu Projekta piedāvājumu, saraksta lapā **Projekta piedāvājumi** vai detalizētās informācijas lapā **Projekta piedāvājums** atlasiet projekta piedāvājumu, ko vēlaties kopēt, un pēc tam atlasiet vienumu **Kopēt**.

Tiks atvērta dialoga lapa, kurā varat ievadīt kopijas parametrus. Tālāk sniegtajā tabulā ir uzskaitīti lauki, kas ir iekļauti dialoga lapā. Atkarībā no atlasītajām vērtībām kopēšanas process var mainīties.

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Tēma | Ievadiet mērķa piedāvājuma saistīto tēmu vai nosaukumu. Kad tiek atvērts dialogs, sistēma to iestata uz to avota piedāvājuma tēmu, kam pievienots **-copy**. | |
| Potenciāls klients | Atsauce uz klienta uzņēmuma vai konta ierakstu. Kad tiek atvērts dialogs, sistēma to iestata uz avota piedāvājuma uzņēmumu. | Šis lauks ir piedāvājuma primārais klients. |
| Līgumslēdzēja vienība | Organizācijas struktūrvienība, kas ir atbildīga vai ar šo darījumu saistītā/-o projekta/-u īstenošanu.
Kad tiek atvērts dialogs, sistēma to iestata uz avota piedāvājuma līgumslēdzēja vienību. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpildīs projektus pēc darījuma slēgšanas. Katrai līgumslēdzēja vienībai ir valūta. Šo valūtu lieto, lai ziņotu projekta izpildes laikā radušās prognozētās un faktiskās izmaksas. |
| Valūta | Šī ir valūta, kādā notiek šī piedāvājuma darījumi. Kad tiek atvērts dialogs, sistēma to iestata uz avota piedāvājuma valūtu. To var modificēt, un izmaiņu gadījumā lauks **Kopēt izcenojumu** vienmēr ir iestatīts uz **Nē**. Tas ir tādēļ, ka avota piedāvājuma cenrāži vairs nav attiecināmi. | Valūta tiek izmantota noklusējuma cenrādī, lai izveidotu finanšu aprēķinu piedāvājumam un vēlāk izrakstītu rēķinu klientam, kad darījums ir iegūts. |
| Pieprasītais piegādes datums | Tas ir klienta pieprasītais piegādes datums. | To izmanto kā beigu datumu, veidojot rēķinu izrakstīšanas datumus ar noteiktu biežumu. |
| Kopēt izcenojumu | Vērtība Jā/Nē norāda, vai piedāvājuma izcenojums ir jākopē no avota piedāvājuma. | Ja ir atlasīta opcija **Jā**, projekta cenrādis un produktu cenrāža atsauces tiek kopētas no avota piedāvājuma uz mērķa piedāvājumu. Ja ir atlasīta opcija **Nē**, cenrāžu noklusējuma vērtības tiek noteiktas, pamatojoties uz jaunākajiem cenrāžiem, kas tika iestatīti uzņēmuma vai projekta parametros. |

Ja dialoga lapā atlasāt opciju **Labi**, sistēma izveido projekta piedāvājuma kopiju, pamatojoties uz dialogā atlasītajiem parametriem. Tiek atvērts jaunais projekta piedāvājums. 

> [!NOTE]
> Tālāk norādītā informācija netiek kopēta no avota uz mērķa piedāvājumu.
>
> - Rēķina izrakstīšanas grafiki
> - Piedāvājuma un piedāvājuma rindas klienti
> - Projekta atsauce projekta piedāvājuma rindās — klienta budžeta informācija
>
>Šī informācija katram piedāvājumam ir ļoti specifiska, tādēļ šie lauki un ieraksti netiek kopēti. Piedāvājuma rindas projektiem un produktiem, piedāvājuma rindu informācijā ietvertie aprēķini un piedāvājuma līmeņa nepārsniedzamā vērtības tiek kopētas. Cenu un izmaksu likmju noklusējuma vērtības ir atkarīgas no opcijas **Kopēt izcenojumu** dialoga lapā **Kopijas parametri**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]