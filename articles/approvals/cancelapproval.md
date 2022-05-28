---
title: Atcelt iepriekš apstiprinātu ierakstu apstiprināšanu
description: Šajā tēmā paskaidrots, kā projektu vadītājs var atcelt iepriekš apstiprinātā laika, izdevumu vai materiālu lietojuma ierakstu apstiprināšanu.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584789"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Atcelt iepriekš apstiprinātu ierakstu apstiprināšanu

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta vadītājs vai apstiprinātājs, kas iepriekš ir apstiprinājis laika, izdevumu vai materiālu lietojuma ierakstus, var atcelt šo ierakstu apstiprināšanu. 

Veiciet šīs darbības, lai atceltu iepriekš apstiprināta laika, izdevumu vai materiālu lietojuma ieraksta apstiprinājumu.

1. Atveriet sadaļu **Projekti** \> **Mani darbi** \> **Apstiprinājumi**.
2. Lapā **Apstiprinājumu saraksts tiek rādīti** visi laika ieraksti, kas gaida apstiprinājumu. Mainīt skatu uz **Mani iepriekšējie apstiprinājumi**.
3. Atlasiet atcelšanas laiku, izdevumus vai materiālu apstiprinājumus. Pēc tam darbību rūtī atlasiet **Atcelt apstiprinājumu**.
4. Parādītajā apstiprinājuma ziņojuma lodziņā atlasiet **Labi**, lai apstiprinātu operāciju.

> [!IMPORTANT]
> Nevar atcelt iepriekš apstiprināta laika, izdevumu un materiālu lietojuma ieraksta apstiprināšanu, par kuru klientam jau ir izrakstīts rēķins. Ja mēģināt, tiek parādīts ziņojums, kurā norādīts, ka apstiprinājumu nevar atcelt, jo tam jau ir izrakstīts rēķins. Šādā gadījumā apstiprinājumu var atcelt tikai tad, ja tiek izmantots koriģējošs rēķins, lai izsniegtu klientam pilnu kredītu vai atmaksu sākotnējā rēķinā.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Iepriekš apstiprināta ieraksta apstiprinājuma anulēšanas ietekme

Kad apstiprinājums tiek atcelts, tam ir gan operacionāla, gan finansiālā ietekme.

### <a name="operational-impact"></a>Operatīva ietekme

Ja ieraksta apstiprinājums tiek atcelts, apstiprinājuma ieraksts tiek atzīmēts kā **iesniegts**. Ieraksta statuss tiek mainīts uz **Iesniegts**. Šajā posmā projekta komandas loceklis var atsaukt ierakstu, neiesniedzot atsaukšanas pieprasījumu.

Apstiprinātājs var mainīt apmaksājamā **daudzuma** un **norēķinu tipa** vērtības un pēc tam vēlreiz apstiprināt ierakstu.

### <a name="financial-impact"></a>Finansiālā ietekme

Ja ieraksta apstiprinājums tiek atcelts, atbilstošās izmaksas un pārdošanas faktiskās vērtības tiek atjauninātas šādā veidā:

- Lauks **Korekcijas statuss** tiek atjaunināts uz **Koriģēts**.
- Lauks **Norēķinu statuss** tiek atjaunināts uz **Atcelts**.

Tālāk tiek izveidotas anulēšanas ievadnes tabulā Esošie. Lai izveidotu atgrieztos ierakstus, sistēma pārkopē lauka vērtības no sākotnējiem esošajiem. Vienīgās vērtības, kas nav pārkopētas, ir daudzuma vērtības. Šīs vērtības tiek atgrieztas. Atgrieztie esošie tiek izveidoti gan sadaļā **Izmaksas**, **gan Nerēķina pārdošana** esošajos izdevumos. Anulētajām faktiskajām vērtībām lauks **Korekcijas statuss** tiek iestatīts uz **Nekoriģējams** un lauks **Norēķinu statuss** tiek iestatīts uz **Atcelts**. Šo izmaiņu dēļ ierakstītie nepabeigtie tēriņi un ieņēmumi projektā vairs neveido summas, kuras šīs faktiskās vērtības pārstāv.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
