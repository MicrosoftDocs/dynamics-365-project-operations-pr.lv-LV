---
title: Apstiprinājuma atcelšana iepriekš apstiprinātiem ierakstiem
description: Šajā rakstā izskaidrots, kā projekta vadītājs var atcelt iepriekš apstiprinātu laika, izmaksu vai materiālu lietojuma ierakstu apstiprinājumu.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930465"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Apstiprinājuma atcelšana iepriekš apstiprinātiem ierakstiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta vadītājs vai apstiprinātājs, kurš ir iepriekš apstiprinājis laika, izmaksu vai materiālu lietojuma ierakstus, var atcelt šo ierakstu apstiprinājumu. 

Lai atceltu iepriekš apstiprināto laika vai izdevumu ierakstu apstiprinājumu, veiciet tālāk norādītās darbības.

1. Atveriet sadaļu **Projekti** \> **Mani darbi** \> **Apstiprinājumi**.
2. Saraksta lapā **Apstiprinājumi** tiek rādīti visi laika ieraksti, kas gaida apstiprinājumu. Mainiet skatu uz **Mani iepriekšējie apstiprinājumi**.
3. Atlasiet laika, izdevumu vai materiālu apstiprinājumus, ko atcelt. Darbību rūtī atlasiet **Atcelt apstiprinājumu**.
4. Parādītajā apstiprinājuma lodziņā atlasiet vienumu **Labi**, lai apstiprinātu darbību.

> [!IMPORTANT]
> Nevar atcelt iepriekš apstiprināta laika, izmaksu un materiālu lietojuma ieraksta apstiprinājumu, par ko klientam jau ir izrakstīts rēķins. Mēģinot to izdarīt, tiek parādīts ziņojums, ka apstiprinājumu nevar atcelt, jo par to jau ir izrakstīts rēķins. Šajā gadījumā apstiprinājumu var atcelt tikai tad, ja klientam sākotnējā rēķinā tiek izmantots labots rēķins, lai izsniegtu pilnu kredītu vai atmaksu.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Iepriekš apstiprināta ieraksta apstiprinājuma atcelšanas ietekme

Kad apstiprinājums tiek atcelts, tam ir gan operacionāla, gan finansiālā ietekme.

### <a name="operational-impact"></a>Operatīva ietekme

Ja ieraksta apstiprinājums ir atcelts, apstiprinājuma ieraksts tiek atzīmēts kā **Iesniegts**. Ieraksta statuss tiek mainīts uz **Iesniegts**. Šajā posmā projekta darba grupas dalībnieks var atsaukt ierakstu, iesniedzot atsaukšanas pieprasījumu.

Apstiprinātājs var mainīt **Daudzums, par ko izrakstīt rēķinu** un **Norēķinu tips** un pēc tam ierakstu apstiprināt vēlreiz.

### <a name="financial-impact"></a>Finansiālā ietekme

Ja ieraksta apstiprinājums ir atcelts, atbilstošās faktiskās vērtības izmaksām un pārdošanai tiek atjauninātas tālāk norādītajā veidā.

- Lauks **Korekcijas statuss** tiek atjaunināts uz **Koriģēts**.
- Lauks **Norēķinu statuss** tiek atjaunināts uz **Atcelts**.

Tālāk tiek izveidotas anulēšanas ievadnes tabulā Esošie. Lai izveidotu atgrieztos ierakstus, sistēma pārkopē lauka vērtības no sākotnējiem esošajiem. Vienīgās vērtības, kas nav pārkopētas, ir daudzuma vērtības. Šīs vērtības tiek atgrieztas. Atgrieztie esošie tiek izveidoti gan sadaļā **Izmaksas**, **gan Nerēķina pārdošana** esošajos izdevumos. Anulētajām faktiskajām vērtībām lauks **Korekcijas statuss** tiek iestatīts uz **Nekoriģējams** un lauks **Norēķinu statuss** tiek iestatīts uz **Atcelts**. Šo izmaiņu dēļ ierakstītie nepabeigtie tēriņi un ieņēmumi projektā vairs neveido summas, kuras šīs faktiskās vērtības pārstāv.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
