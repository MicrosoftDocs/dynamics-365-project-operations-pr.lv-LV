---
title: Cenu noteikšanas dimensiju izslēgšana
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensiju izslēgšanu.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004540"
---
# <a name="turning-off-a-pricing-dimension"></a>Cenu noteikšanas dimensiju izslēgšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Iespējams, ik pēc dažiem gadiem jums ir jāpārskata un jāatjaunina sava cenu noteikšanas stratēģija. Jūsu veiktajiem atjauninājumiem var būt nepieciešams izslēgt esošu cenas noteikšanas dimensiju un izveidot jaunu. Piemēram, iepriekš jūs noteicāt cenas, izmantojot **Lomu**, bet tagad esat izlēmis noteikt cenas, izmantojot **Darba pieredzi**. Tam var būt nepieciešams izslēgt **Lomu** kā cenas noteikšanas dimensiju un izveidot **Darba pieredzi** kā jaunu cenas noteikšanas dimensiju. 

Cenas noteikšanas dimensijas izslēgšanu, neatkarīgi no tā, vai tā ir iekļauta vai pielāgota, var izdarīt, iestatot Cenas noteikšanas dimensijas laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Nē**.

Tomēr, ja tas ir izdarīts, iespējams, saņemsit kļūdas ziņojumu, ka **Cenu noteikšanas dimensiju nevar atjaunināt vai dzēst, ja ir saistīti cenu ieraksti.**

![Biznesa procesa kļūda ir iespējama, izslēdzot cenas noteikšanas dimensiju](media/Business-Process-Error.png)

Šis kļūdas ziņojums norāda, ka pastāv cenu ieraksti, kas iepriekš tika iestatīti izslēgtai dimensijai. Visi **Lomas cenas** un **Lomas cenas uzcenojuma** ieraksti, kas norāda uz dimensiju, ir jādzēš, pirms dimensiju piemērojamību var iestatīt uz **Nē**. Šīs noteikums attiecas gan uz iekļautām cenu noteikšanas dimensijām, gan uz jebkurām pielāgotām cenu noteikšanas dimensijām, kuras, iespējams, esat izveidojis. Šīs pārbaudes iemesls – katram **Lomas cenas** ierakstam ir jābūt unikālai dimensiju kombinācijai. Piemēram, cenrādī ar nosaukumu **ASV izmaksu likmes 2018. gadā** ir šādas **Lomu cenu** rindas. 

| Standarta nosaukums         | Org. struktūrvienība    |Vienība   |Cenrādis  |Valūta  |
| -----------------------|-------------|-------|-------|----------|
| Sistēmas inženieris|Contoso US|stunda| 100|USD|
| Vecākais sistēmu inženieris|Contoso US|stunda| 150| USD|


Izslēdzot **Standarta nosaukumu** kā cenas noteikšanas dimensiju un kad cenas noteikšanas programma meklē noteiktu cenu, tā izmantos tikai **Org. struktūrvienības** vērtību no ievades konteksta. Ja ievades konteksta **Organizācijas struktūrvienība** ir Contoso US, rezultāts nebūs noteikts, jo abas rindas sakritīs. Lai izvairītos no šāda scenārija, veidojot **Lomu cenu** ierakstus, sistēma pārbauda, lai dimensiju kombinācija ir unikāla. Ja dimensija ir izslēgta pēc **Lomu cenu** izveides, šo ierobežojumu var pārkāpt. Tāpēc pirms dimensijas izslēgšanas ir jādzēš visas **Lomu cenu** un **Lomu cenu uzcenojumu** rindas, kurām ir šī dimensijas vērtība.


[!INCLUDE[footer-include](../includes/footer-banner.md)]