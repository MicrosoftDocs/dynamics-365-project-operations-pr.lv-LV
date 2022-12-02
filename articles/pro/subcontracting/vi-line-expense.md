---
title: Kreditoru rēķinu rindas izdevumu kategorijām
description: Šajā rakstā izskaidrots, kā ierakstīt piegādātāja rēķina rindas izdevumu kategorijām.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261692"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Kreditoru rēķinu rindas izdevumu kategorijām

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Piegādātāja rēķinam programmā Microsoft Dynamics 365 Project Operations var būt piegādātāja rēķina rindas, kas paredzētas izdevumu kategorijām. Projekta vadītāji var izmantot piegādātāja rēķina rindas izdevumu kategorijām, lai ierakstītu pakalpojumu izmaksas, kas tiek iegādātas kā izdevumu kategorijas.

Piegādātāja rēķina rindās, kas paredzētas izdevumu kategorijām, var būt un var arī nebūt atsauce uz apakšlīguma rindu, kas paredzēta izdevumu kategorijām. Ja piegādātāja rēķina rinda izdevumu kategorijām satur atsauci uz apakšlīgumu, projektu vadītāji var saskaņot un pārbaudīt izdevumus, par kuriem piegādātājs izraksta rēķinu rēķina rindā, salīdzinot ar izdevumiem, ko šajās izdevumu kategorijās projektā ierakstījuši un apstiprinājuši projekta vadītāji.

Šajā tabulā ir informācija par piegādātāja rēķina rindām izdevumu kategorijām.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Piegādātāja rēķina rindas nosaukums, lai atvieglotu identificēšanu. | Šis nosaukums tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, kas ir balstīti uz piegādātāja rēķina rindām. |
| Apraksts | Īss pakalpojumu apraksts, par kuriem piegādātājs izraksta rēķinu piegādātāja rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšlīgums, ar kuru pakalpojumi sākotnēji tika pasūtīti. | Ja piegādātāja rēķinam ir atlasīts apakšlīgums, visas rindas piegādātāja rēķinā pārmantos šo atlasi. Piegādātāja rēķinā nevar būt piegādātāja rēķina rindas, kam ir atsauce uz dažādiem apakšlīgumiem. |
| Apakšlīguma rinda | Apakšlīguma rinda, ar kuru pakalpojumi tika pasūtīti. Atlasāmo apakšlīguma rindu saraksts ir ierobežots līdz atlasītā apakšlīguma rindām. | Kad piegādātāja rēķina rindā izdevumu kategorijām ir atlasīta apakšlīguma rinda, lauku **Projekts**, **Uzdevums** un **Transakciju kategorija** noklusējuma vērtības tiek ievadītas no atbilstošajiem apakšlīguma rindas laukiem. Ja atlasītajai apakšlīguma rindai ir vērtības laukos **Projekts**, **Projekta uzdevums** un **Transakciju kategorija**, atbilstošo lauku vērtības piegādātāja rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kurā piegādātāja rēķina rindas faktiskās izmaksas tiek ierakstītas projektā. |Nevienu |
| Transakciju klase | Atlasiet **Izdevumi**, lai ierakstītu piegādātāja rēķinu izdevumu kategorijai. | Vērtība **Izdevumi** norāda, ka piegādātāja rēķina rinda tiek izmantota, lai ierakstītu rēķina summu par pakalpojumiem, kas tika iegādāti kā izdevumu kategorijas. |
| Project | Projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot piegādātāja rēķina rindu ar izdevumiem, kas ir ierakstīti jebkurā projekta uzdevumā. Ja piegādātāja rēķina rindā nav atsauces uz apakšlīguma rindu un šis lauks ir atstāts tukšs, piegādātāja rēķina rindas izveidotās faktiskās izmaksas netiks saistītas ne ar kādām rēķinā neiekļautām faktiskajām pārdošanām. Šajā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, par izmaksām var nebūt iespējams izrakstīt rēķinu gala klientam. |
| Transakciju kategorija | Transakciju kategorija, par kuru tiek izrakstīts rēķins. Atlasītajai transakciju kategorijai ir jāizveido atbilstoša izdevumu kategorija. | Vērtību **Transakciju kategorija** un **Vienība** kombinācija tiks izmantota kā noklusējuma vērtība vai aprēķinātā vērtība laukam **Vienības cena** apakšlīguma rēķina rindā. |
| Daudzums | Ievadiet daudzumu, par ko piegādātājs izrakstījis rēķinu rēķina rindā. |Nevienu|
| Vienību grupa | Noklusējuma vērtība tiek ievadīta, pamatojoties uz atlasītās transakciju kategorijas vienību grupu. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai iepirktu jebkurā vienību grupas vienībā. | Vērtību **Transakciju kategorija** un **Vienība** kombinācija tiks izmantota kā noklusējuma vērtība vai aprēķinātā vērtība laukam **Vienības cena** apakšlīguma rēķina rindā. |
| Vienības cena | Vienības noklusējuma cenā tiek izmantota vērtību **Transakciju kategorija** un **Vienība** kombinācija no projekta cenrāža, kas ir piemērojams piegādātāja rēķina rindas transakcijas datumam. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no vienības piegādātāja rēķina rindā, sistēma izmanto vienības konversiju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis tikai lasāmais lauks tiek automātiski aprēķināts kā *Daudzums* &times; *Vienības cena*, ja vērtības ir ievadītas gan laukā **Daudzums**, gan laukā **Vienības cena**. Ja viens vai abi šie lauki ir tukši, tad tajos var ievadīt vērtību.| Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Piegādātāja rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *Starpsumma* + *Pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
