---
title: Kreditora rēķina rindas par laiku
description: Šajā rakstā ir izskaidrots, kā ierakstīt piegādātāja rēķina rindas par laika izmaksām, ko ievada apakšuzņēmēji.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262022"
---
# <a name="vendor-invoice-lines-for-time"></a>Kreditora rēķina rindas par laiku

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Piegādātāja rēķinam programmā Microsoft Dynamics 365 Project Operations var būt piegādātāja rēķina rindas, kas paredzētas laikam. Projektu vadītāji var izmantot piegādātāja rēķina rindas, kas paredzētas laikam, lai projektos ierakstītu apakšuzņēmēja laika izmaksas.

Piegādātāja rēķina rindās, kas paredzētas laikam, var būt un var arī nebūt atsauce uz apakšlīguma rindu, kas paredzēta laikam. Ja piegādātāja rēķina rinda laikam satur atsauci uz apakšlīgumu, projektu vadītāji var saskaņot un pārbaudīt laiku, par kuru piegādātājs izraksta rēķinu rēķina rindā, salīdzinot ar laiku, ko ierakstījuši apakšuzņēmēji un apstiprinājuši projekta vadītāji.

Šajā tabulā ir informācija par piegādātāja rēķina rindām laikam.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Piegādātāja rēķina rindas nosaukums, lai atvieglotu identificēšanu. | Šis nosaukums tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, kas ir balstīti uz piegādātāja rēķina rindām. |
| Apraksts | Īss pakalpojumu apraksts, par kuriem piegādātājs izraksta rēķinu piegādātāja rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšlīgums, ar kuru pakalpojumi sākotnēji tika pasūtīti. | Ja piegādātāja rēķinam ir atlasīts apakšlīgums, visas rindas piegādātāja rēķinā pārmantos šo atlasi. Piegādātāja rēķinā nevar būt piegādātāja rēķina rindas, kam ir atsauce uz dažādiem apakšlīgumiem. |
| Apakšlīguma rinda | Apakšlīguma rinda, ar kuru pakalpojumi tika pasūtīti. Atlasāmo apakšlīguma rindu saraksts ir ierobežots līdz atlasītā apakšlīguma rindām. | Kad piegādātāja rēķina rindā laikam ir atlasīta apakšlīguma rinda, lauku **Projekts**, **Loma** un **Rezervējamais resurss** noklusējuma vērtības tiek ievadītas no atbilstošajiem apakšlīguma rindas laukiem. Ja atlasītajai apakšlīguma rindai ir vērtības laukos **Projekts**, **Loma** un **Rezervējams**, atbilstošo lauku vērtības piegādātāja rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kurā piegādātāja rēķina rindas faktiskās izmaksas tiek ierakstītas projektā. | Nevienu |
| Transakciju klase | Noklusējuma vērtība ir **"Laiks"**. | Vērtība **Laiks** norāda, ka piegādātāja rēķina rinda tiek izmantota, lai ierakstītu rēķina summu par apakšuzņēmēja laiku. |
| Project | Projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot piegādātāja rēķina rindu ar laiku, ko apakšuzņēmēja resursi ir ierakstījuši jebkurā projekta uzdevumā. Ja piegādātāja rēķina rindā nav atsauces uz apakšlīguma rindu un šis lauks ir atstāts tukšs, piegādātāja rēķina rindas izveidotās faktiskās izmaksas netiks saistītas ne ar kādām rēķinā neiekļautām faktiskajām pārdošanām. Šajā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, par izmaksām var nebūt iespējams izrakstīt rēķinu gala klientam. |
| Loma | To apakšuzņēmēju resursu loma, par kuru laiku tiek izrakstīts rēķins. | Šajā laukā ir norādīta loma, ko izpilda apakšlīguma resursi, par kuru laiku tiek izrakstīts rēķins piegādātāja rēķinā. |
| Rezervējamais resurss | Tā apakšuzņēmēja vārds, par kura laiku tiek izrakstīts rēķins. Rezervējamā resursa atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot piegādātāja rēķina rindu ar laiku, ko ieraksta jebkurš resurss, kurš pieder piegādātājam, piegādātāja rēķina rindā. |
| Daudzums | Ievadiet laika stundu skaitu, par ko piegādātājs izraksta rēķinu rēķina rindā. |Nevienu |
| Vienību grupa | Noklusējuma vērtība ir **Laika vienību grupa**, un to nevar mainīt. | Nevienu |
| Vienība | Noklusējuma vērtība ir stundu pamatvienība no laika vienību grupas. Šo vērtību var mainīt, lai iegādātos jebkuru laika vienību grupas vienību, piemēram, dienu vai nedēļu. | Vērtību **Loma** un **Vienība** kombinācija tiks izmantota kā noklusējuma vērtība vai aprēķinātā vērtība laukam **Vienības cena** apakšlīguma rēķina rindā. |
| Vienības cena | Vienības noklusējuma cenā tiek izmantota vērtību **Loma** un **Vienība** kombinācija no projekta cenrāža, kas ir piemērojams piegādātāja rēķina rindas transakcijas datumam. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no vienības piegādātāja rēķina rindā, sistēma izmanto vienības konversiju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis tikai lasāmais lauks tiek automātiski aprēķināts kā *Daudzums* &times; *Vienības cena*, ja vērtības ir ievadītas gan laukā **Daudzums**, gan laukā **Vienības cena**. Ja viens vai abi šie lauki ir tukši, tad tajos var ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Piegādātāja rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *Starpsumma* + *Pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
