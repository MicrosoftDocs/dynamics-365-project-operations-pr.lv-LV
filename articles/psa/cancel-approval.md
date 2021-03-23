---
title: Iepriekš apstiprināto laika un izdevumu ierakstu atcelšana
description: Šajā tēmā ir sniegta informācija par to, kā atcelt apstiprinātu projekta laiku un izmaksu darbību.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290863"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Iepriekš apstiprināto laika vai izdevumu ierakstu atcelšana

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Jaunākajā Dynamics 365 Project Service Automation versijā apstiprinātāji var atcelt iepriekš apstiprinātos laika vai izdevumu ierakstus.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Iepriekš apstiprinātā laika vai izdevuma ieraksta atcelšana

Lai atceltu iepriekš apstiprināto laika vai izdevumu ievadi, veiciet tālāk norādītās darbības.

1. Atveriet sadaļu **Projekti** \> **Mani darbi** \> **Apstiprinājumi**.
2. Lapas **Apstiprinājumi** sarakstā mainiet skatu uz **Mani jaunākie apstiprinājumi.** Tiek parādīts iepriekš apstiprināto laika un izdevumu ierakstu saraksts.
3. Atlasiet vienu vai vairākus ierakstus un pēc tam atlasiet **Atcelt apstiprinājumu**. Tiek parādīts brīdinājuma ziņojums.
4. Lai atceltu lejupielādi, atlasiet **Labi**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Laika atcelšanas un izdevumu ieraksta apstiprinājuma ietekme

Kad apstiprinājums tiek atcelts, tam ir gan operacionāla, gan finansiālā ietekme.

### <a name="operational-impact"></a>Operacionāla ietekme

Kad apstiprinājums ir atcelts, operacionālajā pusē ieraksta statuss tiek atiestatīts uz **Melnraksts** un apstiprinājums vairs netiek rādīts skatā **Mani jaunākie apstiprinājumi**. Tā vietā atceltā apstiprināšana tiek parādīta vai nu skata **Apstiprinājuma laika ieraksti**, vai skata **Apstiprinājuma izdevumu ieraksti** atkarībā no tā, vai tas ir laika ieraksts vai izdevumu ieraksts. Turklāt saistītā laika vai izdevumu ieraksta statuss tiek mainīts uz **Iesniegts**, lai saistītais ieraksts atbilstu apstiprinājumam, kura statuss ir **Melnraksts.**

Kā apstiprinātājs var rediģēt dažus apstiprinājuma laukus, kam statuss ir **Melnraksts**. Šajos laukos ir iekļauti skati **Norēķinu veids** un **Apmaksas stundas laika ierakstiem**. Pēc izmaiņu veikšanas varat vēlreiz apstiprināt ieraksta apstiprināšanu. Varat arī noraidīt ierakstu. Ja noraidāt laika ieraksta apstiprinājumu, ieraksta statuss tiek mainīts uz **Atgriezts.** Ja noraidāt izdevumu ievadi, ieraksta statuss tiek mainīts uz **Atgriezts**. Funkcionāli gan atgrieztie, gan noraidītie ieraksti izturēsies vienādi ar ierakstu, kura statuss ir **Melnraksts**. Projekta darba grupas dalībnieks var veikt jebkādas nepieciešamās izmaiņas ierakstā un pēc tam to atkārtoti iesniegt apstiprināšanai vai dzēst pavisam.

### <a name="financial-impact"></a>Finansiālā ietekme

Projekts tiek ietekmēts arī finansiāli, kad apstiprinājums ir atcelts. Pirmkārt, atbilstošās izmaksu un pārdošanas faktiskās vērtības tiek atjauninātas šādā veidā:

- Pielāgošanas statuss ir iestatīts uz **Pielāgots**.
- Pielāgošanas statuss ir iestatīts uz **Atcelts**.

Tālāk tiek izveidotas anulēšanas ievadnes tabulā Esošie. Lai izveidotu atgrieztos ierakstus, sistēma pārkopē lauka vērtības no sākotnējiem esošajiem. Vienīgās vērtības, kas nav pārkopētas, ir daudzuma vērtības. Šīs vērtības tiek atgrieztas. Atgrieztie esošie tiek izveidoti gan sadaļā **Izmaksas**, **gan Nerēķina pārdošana** esošajos izdevumos. Atgriezto esošo lauks **Pielāgojuma statuss** ir iestatīts uz **Nav pielāgojams** un norēķinu statuss ir iestatīts uz **Atcelts**.

Pēc šo izmaiņu veikšanas summa, kas tiek ierakstīta kā projektā patērētā summa un projektā gūtie ieņēmumi, kļūs lielāka par to summu, ko veido šie faktiskie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]