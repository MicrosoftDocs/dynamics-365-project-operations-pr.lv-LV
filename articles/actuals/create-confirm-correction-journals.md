---
title: Korekciju žurnālu izveide un apstiprināšana
description: Šajā rakstā ir sniegta informācija par to, kā izveidot un apstiprināt labojumu žurnālu.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928073"
---
# <a name="create-and-confirm-correction-journals"></a>Korekciju žurnālu izveide un apstiprināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dažreiz laiks vai izdevumu ieraksts var būt ievadīts nepareizi. Piemēram, konsultants var atlasīt nepareizu datumu, kad izveido laika ierakstu, vai arī var atlasīt nepareizo projektu, ievadot izdevumus. Ja konsultants nevar atjaunināt iesniegtos ierakstus, aizmugursistēmas administrators var tieši labot projekta faktiskos datus.

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

 
## <a name="correct-approved-expense-entries"></a>Apstiprinātu izdevumu ierakstu labošana

Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus izdevumu ierakstus. 

1. Apgabala **Pārdošana** sadaļas **Transakcijas** kreisās puses navigācijas rūtī atlasiet **Apstiprinātie izdevumi**.

2. Sarakstā **Apstiprinātie izdevumi** atlasiet koriģējamo projektu un pēc tam atlasiet **Labot ierakstus**. Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Izdevumu korekcija**. 

3. Lapā **Jauns žurnāls** ievadiet labojuma **Aprakstu** un sadaļas **Jaunas vērtības izdevumiem** cilnē **Izdevumu korekcija** atlasiet tos datu laukus, ko vēlaties labot atlasītajām izdevumu rindām. Piemēram, varat piešķirt izdevumus citam vienumam **Projekts** vai labot vienumus **Izdevumu kategorija**, **Izdevumu datums** vai **Rezervējams resurss**.

4. Atlasiet **Priekšskatīt**. Dialoglodziņā atlasiet **Labi**. 

5. Pārbaudiet cilnē **Žurnāla rindas** veiktos labojumus. Varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem izdevumu ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.

6. Ja labotās vērtības tiek parādītas, kā paredzēts, atlasiet **Apstiprināt**. Dialoglodziņā atlasiet **Labi**. Ja vērtības netiek rādītas, kā paredzēts, atlasiet **Atcelt**, lai atgrieztos sarakstā **Apstiprinātie izdevumi**. Atkārtojiet 2.–5. darbību. 

7. Kad apstiprināsiet labojumu žurnālu, atgriezieties atjauninātajā projektā vai projektos, lai skatītu veiktās izmaiņas.

8. Cilnes **Faktiskās vērtības** projekta lapā pārskatiet sarakstu **Faktiskais saistītais skats**. Tiek parādīti sākotnējie ieraksti un labotie ieraksti.


## <a name="correct-approved-material-usage-logs"></a>Apstiprinātu materiālu lietojuma žurnālu labošana

Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus materiālu lietojuma žurnāla ierakstus.

1. Apgabala **Pārdošana** sadaļas **Transakcijas** kreisās puses navigācijas rūtī atlasiet **Faktiskie dati**.

2. Sarakstā **Faktiskie dati** izmantojiet kolonnu filtrus, lai atlasītu transakciju klasi **Materiāls**, lai tiktu rādīti tikai materiālu faktiskie dati. Izmantojiet citus kolonnu filtrus, lai papildus ierobežotu parādītos faktiskos datus. Kad varat atrast vēlamo faktisko datu kopu, atlasiet faktiskos datus un pēc tam atlasiet **Labot ierakstus**. Automātiski tiek izveidots jauns labojumu žurnāls, un tiek piešķirts tips **Materiālu korekcija**.

3. Lapas **Jauns žurnāls** laukā **Apraksts** ievadiet korekcijas aprakstu. Pēc tam cilnes **Materiālu korekcija** sadaļā **Jaunas vērtības materiāliem** atlasiet datu laukus, lai tos labotu atlasītajām materiālu rindām. Piemēram, varat piešķirt materiālu citam projektam vai labot produktu, materiālu datumu vai apakšlīgumu.

4. Atlasiet **Priekšskatīt**. Pēc tam dialoglodziņā atlasiet **Labi**.

5. Cilnē **Žurnāla rindas** pārbaudiet labojumus. Varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem materiālu ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.

6. Ja labotās vērtības tiek parādītas, kā paredzēts, atlasiet **Apstiprināt**. Pēc tam dialoglodziņā atlasiet **Labi**. Ja vērtības nav tādas, kā paredzēts, atlasiet **Atcelt**, lai atgrieztos sarakstā **Faktiskie dati**. Pēc tam atkārtojiet 2.–5. darbību.

7. Kad apstiprināsiet labojumu žurnālu, atgriezieties atjauninātajā projektā vai projektos, lai skatītu veiktās izmaiņas.

8. Cilnes **Faktiskās vērtības** projekta lapā pārskatiet sarakstu **Faktiskais saistītais skats**. Tiek parādīti sākotnējie ieraksti un labotie ieraksti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
