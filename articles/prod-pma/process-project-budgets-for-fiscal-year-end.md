---
title: Projekta budžeta pārcelšana finanšu gada beigās
description: Šis raksts sniedz inoformation par to, kā pārnest atlikušās budžeta summas uz nākamajiem gadiem un izveidot budžeta reģistra detaļas.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080577"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projekta budžeta pārcelšana finanšu gada beigās

[!include [banner](../includes/banner.md)]

Strādājot ar vairāku gadu projektu, finanšu gada beigās var būt atlikums budžetā. Atlikušās budžeta summas var pārcelt uz nākamo gadu un izveidot budžeta reģistra informāciju par summām saistītajos virsgrāmatas kontos. Lai pārnestu atlikušās summas, pārskatiet un analizējiet atlikušās budžeta summas.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Atlikušo budžeta summu pārskatīšana un analīze

Izpildiet tālāk aprakstītās darbības, lai pārskatītu gada beigu budžeta summas projektiem, bet neveiktu summas pārcelšanu.

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**. 
2. Lapas **Projekta budžeta pārcelšanas process** cilnē **Gada beigu opcijas** pārbaudiet, vai nav iespējota opcija **Pārcelt atlikušās projekta budžeta summas**.
3. Cilnes **Parametri** laukā **Projekta budžeta gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu. 
4. Laukā **Aktuālais finanšu gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu. 
5. Laukā **No prognozes modeļa** atlasiet **Atlikušais budžets**. 
6. Lai iekļautu projektus, kas atbilst atlasītajiem kritērijiem, bet kuriem nav atlikušā budžeta, atlasiet **Rādīt nulli atlikušo**.  
7. Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem, un pēc tam atlasiet **Apstrādāt**. 
8. Lai noformētu datu bāzes vaicājumu, kas ielādē noteiktu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.

Lai iegūtu papildinformāciju par noteiktu rindu rūtī, atlasiet rindu un pēc tam atlasiet opciju **Skatīt budžeta detaļas** vai **Skatīt kontus**.

## <a name="carry-forward-remaining-budget-amounts"></a>Paliekošo budžeta summu pārcelšana 

Apstrādājot atlikušās budžeta summas, var izveidot darbības virsgrāmatā tām summām, kuras tiek pārceltas. Lai izveidotu virsgrāmatas transakcijas, veiciet sadaļā [Budžeta summu pārcelšana un virsgrāmatas transakciju izveide](#carry-forward) norādītās darbības. 

> [!NOTE]
> Budžeta summas, kas tiek pārceltas, tiek pārvietotas uz budžeta modeli, kas ir atlasīts lapā **Budžeta modeļi** kā pārcēluma prognozes modelis.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budžeta summu pārcelšana un virsgrāmatas transakciju izveide

1.  Atlasiet **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**. 
2. Lapā **Projekta budžeta pārcelšanas process** atlasiet **Gada beigas** un pēc tam iespējojiet **Pārcelt atlikušās projekta budžeta summas** un **Izveidot budžeta reģistra ierakstus virsgrāmatā**. 
3. Cilnes **Parametri** lauku grupā **Projekta parametri** atlasiet tālāk norādītās darbības.

   - **Projekta budžeta gads** : atlasiet tā finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summas. 
   - **Peļņa un zaudējumi** : izveidojiet peļņas un zaudējumu transakciju virsgrāmatā. 
   -  **NP** : izveidojiet Nepabeigtie projekti (NP) transakcijas virsgrāmatā.
   -  **Alga** : izveidojiet algu sadalījuma transakcijas virsgrāmatā. 

5. Lauku grupā **Virsgrāmata** norādiet šādu informāciju: 

   - Laukā **Aktuālais finanšu gads** atlasiet finanšu gadu, uz kuru jāpārceļ atlikušās projektu budžeta summas.. Noklusējuma vērtība ir viens gads pēc vērtības laukā **Projekta budžeta gads**.
   -  Laukā **Pārcelšanas periods** atlasiet periodu, kuram vēlaties izveidot budžeta reģistra detalizētu informāciju virsgrāmatai. Parasti tas ir sākuma finanšu gada pirmais periods.

6. Lauku grupā **Kopēt no/uz** norādiet šādu informāciju:

   - Laukā **No prognozes modeļa** atlasiet projekta budžeta prognožu modeli, kas saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem. 
   - Laukā **Uz virsgrāmatas budžeta modeli** atlasiet virsgrāmatas budžeta modeli, kas saistīts ar budžeta summām, kuras vēlaties pārcelt uz virsgrāmatu. 
   -  Atlasiet **Pārsūtīt pārdošanas valūtu** , lai izmantotu projekta pārdošanas valūtu virsgrāmatas transakcijām, kas tiek izveidotas, pārsūtot projektu budžeta summas. Ja opcija nav atlasīta, darbības izmanto uzskaites valūtu. 
   -  Atlasiet **Rādīt nulli atlikušo** , lai iekļautu projektus, kuriem nav atlikušo budžeta summu, bet kuri atbilst citiem kritērijiem, kas atlasīti apakšējā rūtī redzamajos projektos.

7. Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem. Ja vēlaties izveidot datu bāzes vaicājumu, kas ielādē noteiktu projektu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.
8. Katram projektam, kuru vēlaties apstrādāt, atlasiet opciju projekta rindas sākumā.

    > [!TIP]
    > Lai atlasītu visus vai lielāko daļu projektu, atzīmējiet atlases rūtiņu augšējā augšējā kreisajā stūrī. Lai izslēgtu jebkura projekta apstrādi, noņemiet atzīmi šim projektam.

9. Lai pārceltu atlikušo budžeta summu atlasītajiem projektiem uz atlasīto finanšu gadu un izveidotu budžeta reģistra detaļas virsgrāmatā, atlasiet **Apstrādāt**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budžeta summu pārcelšana, neveidojot virsgrāmatas darbības

1. Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**.
2. Lapas **Projekta budžeta pārcelšanas process** laukā **Gada beigu opcijas** atlasiet opciju **Pārcelt atlikušās projekta budžeta summas**.
3. Grupas **Parametri** laukā **Projekta budžeta gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu.
4. Grupā **Kopēt no/uz** norādiet šādu informāciju:

   - Laukā **No prognozes modeļa** atlasiet projekta budžeta prognožu modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārcelt projektiem. 
   - Atlasiet **Rādīt nulli atlikušo** ,lai iekļautu projektus, kuriem nav atlikušo budžeta summu, bet kuri atbilst citiem atlasītajiem kritērijiem.
   - Grupā **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem. Lai noformētu datu bāzes vaicājumu, kas ielādē noteiktu projektu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.

5. Katram projektam, kuru vēlaties apstrādāt, atlasiet opciju projekta rindas sākumā. 
6. Atlasiet **Apstrādāt** , lai atlasītajiem projektiem pārceltu atlikušās budžeta summas atlasītajam finanšu gadam.



[!INCLUDE[footer-include](../includes/footer-banner.md)]