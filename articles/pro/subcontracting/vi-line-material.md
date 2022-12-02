---
title: Kreditora rēķina rindas par produktiem
description: Šajā rakstā paskaidrots, kā reģistrēt piegādātāja rēķina rindas un izmantot dažādos laukus, lai reģistrētu produktu pirkumus no piegādātājiem.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261568"
---
# <a name="vendor-invoice-lines-for-products"></a>Kreditora rēķina rindas par produktiem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Piegādātāja rēķinam programmā Microsoft Dynamics 365 Project Operations būt piegādātāja rēķina rindas produktiem (tos dēvē arī par materiāliem). Projektu vadītāji var izmantot piegādātāja rēķina rindas, kas paredzētas produktiem, lai projektos ierakstītu iegādāto produktu izmaksas.

Piegādātāja rēķina rindās, kas paredzētas produktiem, var būt un var arī nebūt atsauce uz apakšlīguma rindu, kas paredzēta materiāliem. Ja piegādātāja rēķina rinda produktiem satur atsauci uz apakšlīgumu, projektu vadītāji var saskaņot un pārbaudīt produktus, par kuriem piegādātājs izraksta rēķinu rēķina rindā, salīdzinot ar iegādāto produktu lietojumu, ko ierakstījuši un apstiprinājuši projekta vadītāji.

Šajā tabulā ir informācija par piegādātāja rēķina rindām produktiem.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Piegādātāja rēķina rindas nosaukums, lai atvieglotu identificēšanu. | Šis nosaukums tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, kas ir balstīti uz piegādātāja rēķina rindām. |
| Apraksts | Īss produktu apraksts, par kuriem piegādātājs izraksta rēķinu piegādātāja rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšlīgums, ar kuru produkti sākotnēji tika pasūtīti. | Ja piegādātāja rēķinam ir atlasīts apakšlīgums, visas rindas piegādātāja rēķinā pārmantos šo atlasi. Piegādātāja rēķinā nevar būt piegādātāja rēķina rindas, kam ir atsauce uz dažādiem apakšlīgumiem. |
| Apakšlīguma rinda | Apakšlīguma rinda, ar kuru produkti tika pasūtīti. Atlasāmo apakšlīguma rindu saraksts ir ierobežots līdz atlasītā apakšlīguma rindām. | Kad piegādātāja rēķina rindā produktiem ir atlasīta apakšlīguma rinda, lauku **Projekts**, **Uzdevums** un **Produkts** noklusējuma vērtības tiek ievadītas no atbilstošajiem apakšlīguma rindas laukiem. Ja atlasītajai apakšlīguma rindai ir vērtības laukos **Projekts**, **Uzdevums** un **Produkts**, atbilstošo lauku vērtības piegādātāja rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kurā piegādātāja rēķina rindas faktiskās izmaksas tiek ierakstītas projektā. | Nevienu|
| Transakciju klase | Kad par produktiem tiek izrakstīts rēķins, šim laukam jāiestata vērtība **Materiāls**. | Vērtība **Materiāls** norāda, ka piegādātāja rēķina rinda tiek izmantota, lai ierakstītu rēķina summu par iegādātajiem materiāliem. |
| Project | Projekta nosaukums, kurā tika izmantoti produkti, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Projekta uzdevuma nosaukums, kurā tika izmantoti produkti, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot piegādātāja rēķina rindu ar iegādāto produktu, kas tiek izmantots jebkurā projekta uzdevumā. Ja piegādātāja rēķina rindā nav atsauces uz apakšlīguma rindu un šis lauks ir atstāts tukšs, piegādātāja rēķina rindas izveidotās faktiskās izmaksas netiks saistītas ne ar kādām rēķinā neiekļautām faktiskajām pārdošanām. Šajā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, par izmaksām nebūs iespējams izrakstīt rēķinu gala klientam. |
| Atlasīt produktu | Norādiet, vai produkts, par ko tiek izrakstīts rēķins, ir esošs produkts preču katalogā, vai arī tas ir ierakstāms produkts. | Kad ir atlasīta apakšlīguma rinda, noklusējuma vērtība tiek ievadīta no apakšlīguma rindas. |
| Produkts | Izvēlieties produktu no kataloga. Ja produkts ir ierakstāms produkts, ievadiet produkta nosaukumu. | Šo lauku izmanto, lai ievadītu esošo produktu noklusējuma iegādes cenas. |
| Daudzums | Ievadiet materiālu daudzumu, par ko piegādātājs izrakstījis rēķinu šajā rēķina rindā. | Nevienu |
| Vienību grupa | Atlasiet vienības grupu vienībā, kurā ir iekļauts daudzums, par ko ir izrakstīts rēķins. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai apmaksātu jebkuru atlasītās vienību grupas vienību. | Vērtību **Produkts** un **Vienība** kombinācija tiks izmantota kā noklusējuma vērtība vai aprēķinātā vērtība laukam **Vienības cena** apakšlīguma rēķina rindā. |
| Vienības cena | Vienības noklusējuma cenā tiek izmantota vērtību **Produkts** un **Vienība** kombinācija no projekta cenrāža, kas ir piemērojams piegādātāja rēķina rindas transakcijas datumam. | Nevienu |
| Starpsumma | Šis tikai lasāmais lauks tiek automātiski aprēķināts kā *Daudzums* &times; *Vienības cena*, ja vērtības ir ievadītas gan laukā **Daudzums**, gan laukā **Vienības cena**. Ja viens vai abi šie lauki ir tukši, tad tajos var ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Piegādātāja rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *Starpsumma* + *Pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
