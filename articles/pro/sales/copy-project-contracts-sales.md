---
title: Projekta līgumu kopēšana — Lite
description: Šajā rakstā sniegta informācija par projektu līgumu kopēšanu projektu operācijās.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a1846af677f7cea3ec22fdba4408f2bbd7db8a3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932627"
---
# <a name="copy-project-contracts---lite"></a>Projekta līgumu kopēšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Varat ērti izveidot jaunus projekta līgumus, izveidojot esošo līgumu kopijas kādā no diviem tālāk norādītajiem veidiem. 

  - Saraksta lapā **Projekta līgumi** atlasiet projekta līgumu un pēc tam atlasiet **Kopēt**.
  - Detalizētas informācijas lapā **Projekta līgums** atlasiet **Kopēt**.

Tiks atvērta dialoga lapa, kurā varat atlasīt kopētā līguma parametrus. Dialogā ir iekļauti tālāk norādītie lauki. Atkarībā no dialogā atlasītajām vērtībām kopēšanas process var mainīties.

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Tēma | Ievadiet mērķa līguma tēmu. Kad tiek atvērts dialogs, sistēma šajā laukā iestata avota līguma nosaukumu, kam pievienots **-copy**. | Šim laukam nav lejupstraumes ietekmes. |
| Klients | Atsauce uz klienta uzņēmuma vai konta ierakstu. Kad tiek atvērts dialogs, sistēma šajā laukā ievada avota līguma uzņēmumu. | Šis lauks ir līguma primārais klients. |
| Līgumslēdzēja vienība | Organizācijas struktūrvienība, kas ir atbildīga vai ar šo darījumu saistīto projektu īstenošanu. Kad tiek atvērta dialoga lapa, sistēma to iestata uz avota līguma līgumslēdzēja vienību. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpilda projektus pēc darījuma slēgšanas. Katrai līgumslēdzēja vienībai ir valūta. Šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas. |
| Valūta | Valūta, kādā notiek šī piedāvājuma darījumi. Kad tiek atvērta dialoga lapa, sistēma laukā iestatīs uz avota līguma valūtu. Valūtu var mainīt. Ja tas ir izveidots, lauks **Kopēt izcenojumu** vienmēr tiek iestatīts uz **Nē**, jo avota līguma cenrāži vairs nav būtiski. | Valūta tiek izmantota noklusējuma cenrāžos, lai izveidotu finanšu aprēķinu līgumam un izrakstītu rēķinu klientam, kad darījums ir iegūts. |
| Pieprasītais piegādes datums | Klienta pieprasītais piegādes datums. | Šis datums tiek izmantots kā beigu datumu, kad izveidojat rēķinu izrakstīšanas datumus ar noteiktu biežumu. |
| Kopēt izcenojumu | Norāda, vai līguma izcenojums ir jākopē no avota līguma. | Ja laukā ir iestatīta vērtība **Jā**, projekta un produktu cenrāža atsauces tiek kopētas no avota uz mērķa līgumu. Ja ir atlasīta opcija **Nē**, cenrāžu noklusējuma vērtības tiek noteiktas, pamatojoties uz jaunākajiem uzņēmuma cenrāžiem vai projekta parametriem. |

Ja dialoga lapā atlasāt opciju **Labi**, sistēma izveido līguma kopiju, pamatojoties uz atlasītajiem parametriem. Tiek atvērts jaunais līgums.

Tālāk norādītā informācija netiek kopēta no **avota** uz **mērķa līgumu**.

  - Rēķina izrakstīšanas grafiki
  - Līguma un līguma rindas klienti
  - Projekta atsauce projekta līguma rindās
  - Klienta budžeta informācija

Šī informācija katram līgumam ir ļoti specifiska, tādēļ šie lauki un ieraksti netiek kopēti. Līguma rindas projektiem un produktiem, līguma rindu informācijā ietvertie aprēķini un līguma līmeņa nepārsniedzamā vērtības tiek kopētas. Cenu un izmaksu likmju noklusējuma vērtības ir atkarīgas atlases laukā **Kopēt izcenojumu**, kas atrodams dialoga lapā **Parametru kopēšana**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]