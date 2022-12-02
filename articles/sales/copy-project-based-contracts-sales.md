---
title: Projektā balstītu līgumu kopēšana
description: Šajā rakstā ir sniegta informācija par projekta līgumu kopēšanu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410373"
---
# <a name="copy-project-based-contracts"></a>Projektā balstītu līgumu kopēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Varat ērti izveidot jaunus projekta līgumus, kopējot esošos līgumus kādā no diviem tālāk norādītajiem veidiem.

- Saraksta lapā **Projekta līgumi** atlasiet projekta līgumu un pēc tam atlasiet **Kopēt**.
- Detalizētas informācijas lapā **Projekta līgums** atlasiet **Kopēt**.

Abos gadījumos atveras dialoglodziņš, kurā var iestatīt kopētā līguma parametrus. Dialoglodziņā ir iekļauti tālāk norādītie lauki. Atkarībā no atlasītajām vērtībām kopēšanas process var mainīties.

| Kolonna | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| Tēma | Ievadiet mērķa līguma tēmu. Kad tiek atvērts dialoglodziņš, sistēma šajā laukā iestata avota līguma nosaukumu, bet tam ir pievienots vārds “kopija”. | Šim laukam nav lejupstraumes ietekmes. |
| klient | Atsauce uz klienta uzņēmuma vai konta ierakstu. Kad tiek atvērts dialoglodziņš, sistēma šajā laukā iestata avota līguma uzņēmumu. | Šis lauks ir līguma primārais klients. |
| Atbildīgais uzņēmums | Uzņēmums, kas ir atbildīgs par projektu īstenošanu, kas ir saistīti ar šo darījumu. Kad tiek atvērts dialoglodziņš, sistēma šajā laukā iestata avota līguma atbildīgo uzņēmumu. | Šis uzņēmums ir juridiskā persona, kas īstenos šo projektu pēc darījuma slēgšanas. Atbildīgā uzņēmuma valūtai ir jāatbilst līguma slēgšanas vienības valūtai. |
| Līgumslēdzēja vienība | Organizācijas struktūrvienība, kas ir atbildīga par projektu īstenošanu, kas ir saistīti ar šo darījumu. Kad tiek atvērts dialoglodziņš, sistēma šajā laukā iestata avota līguma slēgšanas vienību. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpilda projektus pēc darījuma slēgšanas. Katrai līgumslēdzēja vienībai ir valūta. Šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas. |
| Valūta | Valūta, kādā notiek šī piedāvājuma darījumi. Kad tiek atvērts dialoglodziņš, sistēma lauku iestata uz avota līguma valūtu. Valūtu var mainīt. Ja tas ir izveidots, lauks **Kopēt izcenojumu** vienmēr tiek iestatīts uz **Nē**, jo avota līguma cenrāži vairs nav būtiski. | Šī valūta tiek izmantota noklusējuma cenrāžos, lai ģenerētu finanšu aprēķinu līgumam un izrakstītu rēķinu klientam, kad darījums ir iegūts. |
| Pieprasītais piegādes datums | Klienta pieprasītais piegādes datums. | Šis datums tiek izmantots kā beigu datumu, kad izveidojat rēķinu izrakstīšanas datumus ar noteiktu biežumu. |
| Kopēt izcenojumu | Vērtība, kas norāda, vai līguma izcenojums ir jākopē no avota līguma. | Ja laukā ir iestatīta vērtība **Jā**, projekta un produktu cenrāža atsauces tiek kopētas no avota līguma uz mērķa līgumu. Ja iestatīta opcija **Nē**, tiek izmantoti noklusējuma cenrāži, pamatojoties uz jaunākajiem uzņēmuma cenrāžiem vai projekta parametriem. |

Ja dialoglodziņā atlasāt opciju **Labi**, sistēma izveido līguma kopiju, pamatojoties uz iestatītajām parametru vērtībām. Pēc tam tiek atvērts jaunais līgums.

Šī informācija **netiek** kopēta no avota līguma uz mērķa līgumu, jo tā ir specifiska katram līgumam:

- Rēķina izrakstīšanas grafiki
- Līguma un līguma rindas klienti
- Projekta atsauce projekta līguma rindās
- Klienta budžeta informācija

Līguma rindas projektiem un produktiem, līguma rindu informācijā ietvertie aprēķini un līguma līmeņa nepārsniedzamās vērtības tiek kopētas. Noklusējuma cenu un izmaksu likmju noklusējuma vērtības ir atkarīgas atlases laukā **Kopēt izcenojumu**, kas atrodams dialoglodziņā **Parametru kopēšana**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
