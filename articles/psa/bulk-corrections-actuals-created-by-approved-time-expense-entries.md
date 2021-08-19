---
title: Ar apstiprinātiem laika un izdevumu ierakstiem izveidoto faktisko ierakstu lielapjoma korekcija
description: Šajā tēmā ir paskaidrots, kā administrators var veikt vienu vai vairākus iepriekš apstiprinātu laika vai izdevumu ierakstu labojumus, ja norēķini nav pabeigti.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 88706946e5c5c59be996640f4c7b37e958c1cf1d9fd14c72c0c6dc854a77dab4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995410"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Ar apstiprinātiem laika un izdevumu ierakstiem izveidoto faktisko ierakstu lielapjoma korekcija

[!include [banner](../includes/psa-now-project-operations.md)]

Dažreiz laiks vai izdevumu ieraksts var būt ievadīts nepareizi. Piemēram, konsultants var atlasīt nepareizu datumu, kad tiek izveidots laika ieraksts, vai arī var apmainīt vietām skaitļus, kad tiek ievadīti izdevumi. Ja konsultants nevar koriģēt iesniegtos ierakstus, administrators var tieši labot projekta ierakstu.

Lai izpildītu šajā tēmā aprakstītās procedūras, jums ir nepieciešamas administratora atļaujas.

## <a name="correct-approved-time-entries"></a>Apstiprinātu laika ierakstu labošana     

Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus projekta laika ierakstus.

1. Apgabalā **Pārdošana** atlasiet **Transakcijas** un pēc tam atlasiet **Apstiprinātais laiks**. 

2. Sarakstā **Apstiprinātais laiks** atrodiet un atlasiet vienu vai vairākus koriģējamos apstiprinātos laika ierakstus. Lai atrastu saistītos ierakstus, varat izmantot filtru. Piemēram, varat filtrēt pēc projekta ID un atlasīt visus apstiprinātos laika ierakstus ar attiecīgo projekta ID.

3. Atlasiet **Labot ierakstus**. Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Laika korekcija**. Atlasītie ieraksti tiek pievienoti žurnālam. 

4. Lapā **Jaunais žurnāls** ievadiet labojumu žurnāla **Aprakstu** un pēc tam atlasiet cilni **Laika ierakstu korekcijas**.  
5. Sadaļā **Jaunas vērtības laika ierakstiem** atjauniniet laukus ar pareizo informāciju, ja nepieciešams. Piemēram, var mainīt piešķirto projektu vai rezervējamo resursu.

6. Atlasiet **Priekšskatīt**. Dialoglodziņā atlasiet **Labi**. Cilnē **Žurnāla rindas** varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem laika ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas. Ja ir jāveic papildu labojumi, atkārtojiet 5. un 6. darbību. 

> [!NOTE]
> Visiem koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības laika ierakstiem**.

7. Ja labojumi tiek parādīti, kā paredzēts, atlasiet **Apstiprināt**. Dialoglodziņā atlasiet **Labi**.

8. Atgriezieties apgabalā **Pārdošana**, atlasiet lapu **Projekti** un pēc tam atveriet projektu, kura laika ierakstus tikko labojāt. 

9. Lapas **Projekti** cilnē **Faktiskās vērtības** skatiet veiktās izmaiņas. 

> [!NOTE]
> Ja cilne **Faktiskās vērtības** nav redzama, atlasiet **Saistīts** > **Faktiskās vērtības**.  

10. Sarakstā **Faktiskais saistītais skats** ir redzams, ka joprojām tiek parādīti apvērstie sākotnējie laika ieraksti, kā arī atbilstošie koriģētie laika ieraksti. 

Piemēram, tālāk redzamajā grafikā ir divi rindas elementi ar daudzumu 8,00, kam ir debets kolonnā Summa. Turklāt ir divi rindas elementi ar daudzumu 8,00, kam ir kredīta summas kolonnā Summa. Šīs korekcijas ienes daudzumu nulle.

![Faktiskais saistīto skatu saraksts.](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Apstiprinātu izdevumu ierakstu labošana

Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus izdevumu ierakstus. 

1. Apgabala **Pārdošana** sadaļas **Transakcijas** kreisās puses navigācijas rūtī atlasiet **Apstiprinātie izdevumi**.

2. Sarakstā **Apstiprinātie izdevumi** atlasiet koriģējamo projektu un pēc tam atlasiet **Labot ierakstus**. Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Izdevumu korekcija**. 

3. Lapā **Jauns žurnāls** ievadiet labojuma **Aprakstu** un sadaļas **Jaunas vērtības izdevumiem** cilnē **Izdevumu korekcija** atlasiet tos datu laukus, ko vēlaties labot atlasītajām izdevumu rindām. Piemēram, varat piešķirt izdevumus citam vienumam **Projekts** vai labot vienumus **Izdevumu kategorija**, **Izdevumu datums** vai **Rezervējams resurss**.

4. Atlasiet **Priekšskatīt**. Dialoglodziņā atlasiet **Labi**. 

5. Pārbaudiet cilnē **Žurnāla rindas** veiktos labojumus. Varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem izdevumu ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.

6. Ja labotās vērtības tiek parādītas, kā paredzēts, atlasiet **Apstiprināt**. Dialoglodziņā atlasiet **Labi**. Ja vērtības netiek rādītas, kā paredzēts, atlasiet **Atcelt**, lai atgrieztos sarakstā **Apstiprinātie izdevumi**. Atkārtojiet 2.–5. darbību. 

> [!NOTE]
> Koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības izdevumiem**.

7. Kad apstiprināsiet labojumu žurnālu, pārejiet atpakaļ uz atjaunināto projektu vai projektiem, lai skatītu veiktās izmaiņas.  

8. Cilnes **Faktiskās vērtības** projekta lapā pārskatiet skatu **Faktiskais saistītais skats**. Tiek parādīti sākotnējie ieraksti un labotie ieraksti. Tālāk redzamajā attēlā ir parādītas izdevumu ieraksta sākotnējās summas un atbilstošās koriģētās izmaksu ierakstu summas. 

![Izdevumu ieraksta sākotnējās summas.](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]