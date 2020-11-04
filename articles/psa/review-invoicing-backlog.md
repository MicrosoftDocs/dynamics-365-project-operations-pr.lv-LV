---
title: Nepabeigtās rēķinu izrakstīšanas pārskatīšana projektiem un projektu līgumiem
description: Šajā tēmā ir sniegta informācija par to, kā apskatīt laiku, izdevumus un produktu rezerves, un kā tās atzīmēt kā gatavus rēķina izrakstīšanai.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080653"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Nepabeigtās rēķinu izrakstīšanas pārskatīšana projektiem un projektu līgumiem

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kad transakcija ir sagatavota, lai izveidotu un apstrādātu rēķinu, transakcijai jābūt atzīmētai **Gatavs rēķina izrakstīšanai**. Šajā tēmā ir apraksti transakciju tipi, ko var izveidot.

## <a name="review-the-time-and-material-billing-backlog"></a>Nepabeigtās laika un materiālu rēķinu izrakstīšanas pārskatīšana

Kad projektam tiek iesniegts un apstiprināts laika vai izdevumu ieraksts, PSA izveido projekta faktiskās vērtības. Ja projekta un transakciju klases kombinācija ir kartēta uz līguma rindu laika un materiālu projektam, tad, apstiprinot ierakstu, tiek izveidotas divas faktiskās vērtības:

- Faktiskās izmaksas 
- Rēķinā neiekļautā faktiskā pārdošana

Rēķinā neiekļautā faktiskā pārdošana norāda nepabeigto rēķinu izrakstīšanu, un tās rēķinu izrakstīšanas statuss ir jāiestata kā **Gatavs rēķina izrakstīšanai**. Kad tiek izveidots projekta rēķins, rēķinā neiekļautā faktiskā pārdošana, kas atzīmēta kā **Gatavs rēķina izrakstīšanai** , tiek kopēta kā rēķina rindas informācija.

Lai pārskatītu nepabeigto rēķinu izrakstīšanu par laiku un materiāliem, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu**. Atlasiet visus rēķinos neiekļautos faktiskos pārdošanas datus, kas ir gatavi rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**. Šo faktisko datu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.

![Nepabeigtā rēķinu izrakstīšana par laiku un materiālu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Nepabeigto preču rēķinu izrakstīšanas pārskatīšana

Programmā PSA, ja projekta līgumam ir uz produktu balstītas līguma rindas, šīs rindas tiek ņemtas vērā rēķinu izrakstīšanai, kad projekta līgumam tiek izveidots rēķins. Jebkurš produkts, kuram ir līguma rindas, kas ir atzīmētas kā **Gatavs rēķina izrakstīšanai** , tiek kopēts uz projekta rēķinu kā projekta rēķina rindas.

Lai pārskatītu nepabeigto rēķinu izrakstīšanu par produktiem, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Nepabeigtā rēķinu izrakstīšana par produktiem**. Atlasiet visas uz produktu balstītās līguma rindas, kas ir gatavas rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**. Šo rindu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.

![Nepabeigtā rēķinu izrakstīšana par produktiem](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Rēķinu izrakstīšanas atskaites punktu pārskatīšana attiecībā uz fiksētas cenas līgumiem

Katrai projekta līguma rindai, kurai ir fiksētas cenas rēķina izrakstīšanas metode, ir jādefinē līguma atskaites punkti. Šos līguma atskaites punktus var iekļaut rēķinā tikai tad, ja tie ir atzīmēti kā **Gatavs rēķina izrakstīšanai**. 

Lai pārskatītu rēķinu izrakstīšanas atskaites punktus, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Fiksētas cenas atskaites punkti**. Atlasiet atskaites punktus, kas ir gatavi rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**. Šo atskaites punktu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.

![Fiksētas cenas atskaites punkti](media/FPBacklog.png)
