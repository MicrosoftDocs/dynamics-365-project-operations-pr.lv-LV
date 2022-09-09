---
title: Kopējiet uz projektiem balstītus līgumus
description: Šajā rakstā ir sniegta informācija par projektu līgumu kopēšanu pakalpojumā Microsoft Dynamics 365 Project Operations.
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
# <a name="copy-project-based-contracts"></a>Kopējiet uz projektiem balstītus līgumus

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Varat viegli izveidot jaunus projektu līgumus, kopējot esošos līgumus vienā no diviem veidiem:

- **Saraksta lapā Projekta līgumi** atlasiet projekta līgumu un pēc tam atlasiet **Kopēt**.
- Detalizētas informācijas lapā **Projekta līgums** atlasiet **Kopēt**.

Abos gadījumos tiek parādīts dialoglodziņš, kurā var iestatīt kopētā līguma parametrus. Dialoglodziņā ir šādi lauki. Atkarībā no atlasītajām vērtībām kopēšanas process var mainīties.

| Kolonna | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| Tēma | Ievadiet mērķa līguma tēmu. Atverot dialoglodziņu, sistēma iestata lauku uz avota līguma nosaukumu, bet tam tiek pievienots vārds "kopija". | Šim laukam nav lejupstraumes ietekmes. |
| klient | Atsauce uz klienta uzņēmuma vai konta ierakstu. Kad dialoglodziņš ir atvērts, sistēma iestata lauku uz avota līguma kontu. | Šis lauks ir līguma primārais klients. |
| Atbildīgais uzņēmums | Uzņēmums, kas ir atbildīgs par ar šo darījumu saistīto projektu īstenošanu. Atverot dialoglodziņu, sistēma iestata lauku uz avota līguma īpašnieku uzņēmumu. | Īpašnieks uzņēmums ir juridiska persona, kas izpildīs projektu pēc darījuma slēgšanas. Piederošā uzņēmuma valūtai jāatbilst līgumslēdzējas vienības valūtai. |
| Līgumslēdzēja vienība | Organizācijas struktūrvienība, kas ir atbildīga par ar šo darījumu saistīto projektu īstenošanu. Kad dialoglodziņš ir atvērts, sistēma iestata lauku uz avota līguma līgumslēdzēju vienību. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpilda projektus pēc darījuma slēgšanas. Katrai līgumslēdzēja vienībai ir valūta. Šī valūta tiek izmantota, lai ziņotu par aplēstajām un faktiskajām izmaksām, kas radušās projekta laikā. |
| Valūta | Valūta, kādā notiek šī piedāvājuma darījumi. Kad dialoglodziņš ir atvērts, sistēma iestata lauku uz avota līguma valūtu. Valūtu var mainīt. Ja tā ir, lauks **Kopēt cenas** vienmēr tiek iestatīts uz **Nē**, jo avota līguma cenrāži vairs nav atbilstoši. | Šī valūta tiek izmantota noklusējuma cenrāžiem, lai līgumā ģenerētu finanšu aprēķinus un izrakstītu debitoram rēķinu, kad darījums ir laimēts. |
| Pieprasītais piegādes datums | Piegādes datums, ko pieprasa klients. | Šis datums tiek izmantots kā beigu datums, kad noteiktā frekvencē izveidojat rēķinu izrakstīšanas datumus. |
| Kopēt izcenojumu | Vērtība, kas norāda, vai līgumā noteiktās cenas ir jākopē no avota līguma. | Ja lauks ir iestatīts uz **Jā**, projekta un produktu cenrāža atsauces tiek kopētas no avota līguma uz mērķa līgumu. Ja tas ir iestatīts uz **Nē**, tiek izmantoti noklusējuma cenrāži, pamatojoties uz jaunākajiem cenrāžiem kontā vai projekta parametros. |

Ja dialoglodziņā atlasāt **Labi (OK**), sistēma izveido līguma kopiju, pamatojoties uz iestatītajām parametru vērtībām. Tad tiek atvērts jaunais līgums.

Tālāk norādītā informācija netiek **kopēta** no avota līguma uz mērķa līgumu, jo tā ir specifiska katram līgumam:

- Rēķina izrakstīšanas grafiki
- Līguma un līguma rindas klienti
- Projekta atsauce projekta līguma rindās
- Klienta budžeta informācija

Tiek kopētas līgumu rindas par projektiem un produktiem, aplēses līguma rindas detaļās un nepārsniegtas vērtības līguma līmenī. Noklusējuma cenu un izmaksu likmju ievadīšana ir atkarīga no izvēles **dialoglodziņa** Parametru **kopēšana laukā Kopēt cenas**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
