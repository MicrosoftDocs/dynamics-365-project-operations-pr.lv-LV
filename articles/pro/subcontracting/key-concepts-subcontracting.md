---
title: Galvenie jēdzieni apakšlīgumu slēgšanā
description: Šajā tēmā izskaidroti daži galvenie jēdzieni, kas attiecas uz apakšlīgumu slēgšanu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578120"
---
# <a name="key-concepts-in-subcontracting"></a>Galvenie jēdzieni apakšlīgumu slēgšanā

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā izskaidroti daži galvenie jēdzieni, kas ir jāzina pirms sākat lietot apakšlīgumu slēgšanas funkcionalitāti programmā Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Līgumslēdzēja vienība apakšsavienībā

Līgumslēdzēja vienība pārstāv to nodaļu vai praksi, kuras pārziņā ir iespējamā projekta nodrošināšana. Līgumslēdzēja vienība ir arī nodaļa, kas stājas līgumattiecībās ar piegādātāju.

## <a name="purchase-currency"></a>Pirkuma valūta

Programmā Project Operations pirkuma valūta ir valūta, kurā ir izveidots šis apakšlīgums. Tā ir arī valūta, kurā tiek reģistrētas apakšuzņēmēja projekta izmaksas. Pirkuma valūta var atšķirties no projekta valūtas, savukārt projekta valūta var atšķirties no pārdošanas valūtas.

## <a name="billing-methods-on-subcontract-lines"></a>Norēķinu metodes apakšlīguma rindās

Projektiem parasti ir fiksētas maksas un uz patēriņu balstīti līgumslēgšanas modeļi. Programmā Project Operations šīs norēķinu metodes tiek atbalstītas pārdošanas un pirksanas kontekstos. Norēķinu metodes pirkumiem darbojas tālāk aprakstītajā veidā.

- **Laiks un materiāli** — ja apakšlīguma rindā tiek izmantota norēķinu metode **Laiks un materiāli**, laika izmaksas projektā tiek ierakstītas, apašuzņēmējiem strādājot un reģistrējot laiku. Pēc tam šīs apakšuzņēmēju transakcijas tiek saskaņotas ar rindas elementiem pārdevēju rēķinos. Šajā modelī projekta vadītāji, kas izmanto programmu Project Operations, var saskaņot un pārbaudīt pārdevēja rēķina rindas ar reģistrēto un apstiprināto apakšuzņēmēju laiku. Kad pārbaude ir pabeigta, iepriekšējās izmaksu faktiskās vērtības, kas tika reģistrētas pēc apstiprināšanas, tiek anulētas, un projektā tiek izveidotas jaunas izmaksu faktiskās vērtības, par pamatu izmantojot pārdevēja rēķinu.
- **Fiksēta cena** — šajā fiksētas maksas līguma modelī pārdevēju rēķini ir balstīti uz fiksētiem atskaites punktiem. Tomēr apakšuzņēmēju resursi var arī reģistrēt laiku. Pēc tam šo laiku pārskata un apstiprina projekta vadītājs. Kad tas ir apstiprināts, Project Operations projektā izveido pagaidu faktiskās izmaksas. Pēc tam, kad pārdevējs ir nosūtījis rēķinu par atskaites punktu, projekta vadītājs var saskaņot iepriekš reģistrētās izmaksu faktiskās vērtības ar atskaites punktu. Kad pārbaude ir pabeigta, faktiskās izmaksu vērtības tiek anulētas, un tiek reģistrētas uz atskaites punktu balstītās izmaksas.

## <a name="project-price-lists-on-subcontracts"></a>Projekta cenrāži apakšlīgumos

Projekta cenrāži ir cenrāži, ko izmanto, lai iestatītu laika, izmaksu un citu ar projektiem saistītu komponentu pirkuma cenas. Var būt vairāki cenrāži, un katram no tiem var būt apakšlīgums ar savu spēkā stāšanās datumu programmā Project Operations. Programmā Project Operations netiek atbalstīta apakšlīgumu cenrāžu spēkā stāšanās datumu pārklāšanās.

## <a name="transaction-classes-on-subcontracts"></a>Transakciju klases apakšlīgumos

Project Operations atbalsta četru veidu transakciju klases:

- Laiks
- Izdevumi
- Materiāls
- Maksa

Pirkumu izmaksas var aprēķināt un tās var rasties tikai transakciju klasēs **Laiks**, **Izdevumi** un **Materiāli**. **Maksa** ir tikai ieņēmumu transakciju klase, un tā nav pieejama pirkšanas saturā.

## <a name="purchase-pricing-dimensions"></a>Pirkumu cenu noteikšanas dimensijas

Cenu noteikšanas dimensijas ļauj izlemt, kādi atribūti tiek izmantoti pirkuma cenas un laika transakciju noklusējuma iestatījumiem. Saistībā ar pirkšanu programmā Project Operations tiek atbalstītas tikai fiksētas dimensiju kopas pirkuma cenas un noklusējuma iestatīšanai. Pirkuma cenas un noklusējuma vērtības iestatīšanai apakšlīguma rindās un apakšlīguma laika transakcijās atribūti ir **Loma** un **Rezervējams resurss**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
