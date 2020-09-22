---
title: Cenas noteikšanas dimensijas izslēgšana
description: Šajā tēmā ir parādīts, kā Project Service risinājumā iestatīt cenu noteikšanas dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753524"
---
# <a name="turn-off-a-pricing-dimension"></a>Cenas noteikšanas dimensijas izslēgšana

Iespējams, ik pēc dažiem gadiem jums ir jāpārskata un jāatjaunina sava cenu noteikšanas stratēģija. Jūsu veiktajiem atjauninājumiem var būt nepieciešams izslēgt esošu cenas noteikšanas dimensiju un izveidot jaunu. Piemēram, iepriekš jūs noteicāt cenas, izmantojot **Lomu**, bet tagad esat izlēmis noteikt cenas, izmantojot **Darba pieredzi**. Tam var būt nepieciešams izslēgt **Lomu** kā cenas noteikšanas dimensiju un izveidot **Darba pieredzi** kā jaunu cenas noteikšanas dimensiju. 

Cenas noteikšanas dimensijas izslēgšanu, neatkarīgi no tā, vai tā ir iekļauta vai pielāgota, var izdarīt, iestatot Cenas noteikšanas dimensijas laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Nē**.

Tomēr, to darot, var parādīties šāds kļūdas ziņojums.

![Biznesa procesa kļūda ir iespējama, izslēdzot cenas noteikšanas dimensiju](media/Business-Process-Error.png)


Šis kļūdas ziņojums norāda, ka pastāv cenu ieraksti, kas iepriekš tika iestatīti izslēgtai dimensijai. Visi **Lomas cenas** un **Lomas cenas uzcenojuma** ieraksti, kas norāda uz dimensiju, ir jādzēš, pirms dimensiju piemērojamību var iestatīt uz **Nē**. Šīs noteikums attiecas gan uz iekļautām cenu noteikšanas dimensijām, gan uz jebkurām pielāgotām cenu noteikšanas dimensijām, kuras, iespējams, esat izveidojis. Šīs pārbaudes iemesls – programmai Project Service ir ierobežojums, ka katram **Lomas cenas** ierakstam ir jābūt unikālai dimensiju kombinācijai. Piemēram, cenrādī ar nosaukumu **ASV izmaksu likmes 2018. gadā** ir šādas **Lomu cenu** rindas. 

| Standarta nosaukums         | Org. struktūrvienība    |Vienība   |Cena  |Valūta  |
| -----------------------|-------------|-------|-------|----------|
| Sistēmas inženieris|Contoso ASV|Hour| 100|USD|
| Vecākais sistēmu inženieris|Contoso ASV|Hour| 150| USD|


Izslēdzot **Standarta nosaukumu** kā cenas noteikšanas dimensiju un kad Project Service cenas noteikšanas programma meklē noteiktu cenu, tā izmantos tikai **Org. struktūrvienības** vērtību no ievades konteksta. Ja ievades konteksta **Organizācijas struktūrvienība** ir Contoso ASV, rezultāts nebūs noteikts, jo abas rindas sakritīs. Lai izvairītos no šāda scenārija, veidojot **Lomu cenu** ierakstus, programma Project Service pārbauda, lai dimensiju kombinācija ir unikāla. Ja dimensija ir izslēgta pēc **Lomu cenu** izveides, šo ierobežojumu var pārkāpt. Tāpēc pirms dimensijas izslēgšanas ir jādzēš visas **Lomu cenu** un **Lomu cenu uzcenojumu** rindas, kurām ir šī dimensijas vērtība.

