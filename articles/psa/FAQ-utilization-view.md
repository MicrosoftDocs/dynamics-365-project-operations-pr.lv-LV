---
title: Skatīt rēķinā iekļaujamo resursu lietojumu
description: Šajā tēmā ir sniegta informācija par resursu lietojuma skatu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32dba5acd95c1d192556153240ebd51343112be53aa3db93e5e6f127c2d960e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007155"
---
# <a name="view-chargeable-utilization-for-resources"></a>Skatīt rēķinā iekļaujamo resursu lietojumu

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Lietojuma skats** lapā **Project Service resursu lietojums** rāda katram rezervējamam resursam piemērojamu lietojumu. Skata pamatā ir plānošanas panelis, tādēļ tajā ir atrodamas daudzas tās pašas funkcijas.

> ![Lietojuma skata ekrānuzņēmums.](media/FAQ-utilization-1.png)
 

Rēķinā iekļaujamā lietojuma aprēķinu veic šādi:

   Rēķinā iekļaujamais lietojums = (faktiskais rēķinā iekļaujamo stundu skaits)/resursa noslodze.

Šūnās ir norādīts aprēķinātais rēķinā iekļaujamais lietojums atlasītajam periodam (dienas, nedēļas vai mēneši).

Katras šūnas krāsa norāda resursa rēķinā iekļaujamo lietojumu salīdzinājumā ar to mērķa rēķinā iekļaujamo lietojumu. 

Mērķa lietojumu var iestatīt resursa noklusējuma lomai vai atsevišķam resursam. Aprēķinā vispirms tiek ņemta vērā atsevišķa resursa mērķa vērtība un pēc tam resursa noklusējuma loma.

## <a name="set-target-on-a-resource"></a>Mērķa iestatīšana resursā

1. Atveriet sadaļu **Resursi** \> **Resursi.** 
2. Atlasiet resursu, lai atvērtu ierakstu. 
3. Cilnē **Project Service** var iestatīt resursa mērķa izmantojumu.

> ![Ekrānuzņēmums, kurā redzama cilnes Project Service izmantošana, lai iestatītu mērķa lietojumu.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Mērķa lietojuma iestatīšana lomai

1. Dodieties uz **Resursi** \> **Resursu lomas**. 
2. Atlasiet lomu un pēc tam atveriet ierakstu. 
3. Iestatiet lomai mērķa lietojumu.

> ![Ekrānuzņēmums, kurā redzama resursu lomu izmantošana, lai iestatītu mērķa lietojumu.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Rēķinā iekļaujamo resursu lietojumu aprēķins

Lai aprēķinātu resursa rēķinā iekļaujamo lietojumu, ir nepieciešams veikt dažas priekšdarbības. 

### <a name="set-default-role-for-individual-resource"></a>Noklusējuma lomas iestatīšana atsevišķam resursam

Pirmkārt, mērķa lietojums ir jāiestata atsevišķam resursam vai resursu noklusējuma lomām. Ja mērķa vērtībām tiek izmantotas resursu lomas, katram atsevišķam resursam jābūt noklusējuma lomai. 

1. Lai to iestatītu, atveriet vienumu **Resursi** \> **Resursi**. 
2. Atlasiet resursu, atveriet ierakstu un pēc tam atlasiet cilni **Project Service**. 
3. Režģī **Resursu lomas** pārliecinieties, vai resursam ir viena loma un vai **Noklusējuma** iestatījums ir **Jā.**
 
### <a name="change-billing-type-for-resource-role"></a>Norēķinu tipa maiņa šai resursa lomai.

Resursu lomu norēķinu tipam jābūt **Rēķinā iekļaujams**. 

1. Dodieties uz **Resursi** \> **Resursu lomas**. 
2. Noklikšķiniet uz lomas, lai atvērtu ierakstu, un pēc tam iestatiet norēķinu tipa noklusējuma vērtību **Rēķinā iekļaujams**.

### <a name="set-working-hours-for-resource-role"></a>Darba stundu iestatīšana resursu lomai
 
Resursam ir jābūt darba stundām noslodzes aprēķinam. 

1. Atveriet sadaļu **Resursi** \> **Resursi.** 
2. Noklikšķiniet uz resursa, lai atvērtu ierakstu, un pēc tam noklikšķiniet uz **Rādīt darba stundas**. 
3. Varat veikt resursu saraksta lielapjoma atjaunināšanu, lietojot **Darba stundu veidne** skatā **Resursu saraksts**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Rēķinā iekļaujamo faktisko stundu traucējummeklēšana

Faktiskā rēķinā iekļaujamo stundu skaita avots ir entītija **Faktiskās vērtības**. Faktiskās vērtības, kurām norēķinu tips ir **Rēķinā iekļaujams**, tiek iekļautas aprēķinā, un tādēļ ir jābūt projektiem, kuros faktiskās vērtības tiek iekļautas rēķinā.

Ja rēķinā iekļaujamais lietojums nav redzams, var pārbaudīt šādus aspektus:

- Resursa noslodzei ir noteiktas darba stundas.
- Resursam ir atsevišķi noteikts mērķa lietojums, vai tam ir piešķirta noklusējuma loma. Lomai ir noteikts mērķa lietojums.
- Faktiskajām vērtībām norēķinu tips ir **Rēķinā iekļaujams** plānotajā lietojuma aprēķināšanas periodā. Tālāk skatiet dažus aspektus, kuri jāpārbauda, ja tiek rādītas faktiskās vērtības, kuru norēķinu tips nav Rēķinā iekļaujams:

  - Lomai, kas izmantota faktiskajai vērtība, noklusējuma norēķinu tips nav Rēķinā iekļaujams.
  - Projekta pamatojumam izmantotās projekta līguma rindas lomai ir atlasīts iestatījums Nav iekļaujams rēķinā.
  - Projektam nav saistītās līguma rindas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]