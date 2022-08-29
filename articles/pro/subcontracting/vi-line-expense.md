---
title: Kreditoru rēķinu rindas izdevumu kategorijām
description: Šajā rakstā ir paskaidrots, kā ierakstīt kreditoru rēķinu rindas izdevumu kategorijām.
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

Kreditora rēķinā korporācijā Microsoft Dynamics 365 Project Operations var būt kreditoru rēķinu rindas izdevumu kategorijām. Projektu vadītāji var izmantot kreditoru rēķinu rindas izdevumu kategorijām, lai reģistrētu to pakalpojumu izmaksas, kas tiek iepirkti kā izdevumu kategorijas.

Kreditoru rēķinu rindās izdevumu kategorijām var būt vai nebūt atsauces uz apakšuzņēmuma līgumu rindu izdevumu kategorijām. Ja izdevumu kategoriju kreditora rēķina rindā ir atsauce uz apakšlīgumu, projektu vadītāji varēs saskaņot un pārbaudīt izdevumus, par kuriem rēķins tiek izrakstīts, izmantojot kreditora rēķina rindu, ar izdevumiem, kas ir ierakstīti šajās izdevumu kategorijās un kurus projekta vadītāji ir apstiprinājuši projektā.

Šajā tabulā ir sniegta informācija par laukiem kreditoru rēķinu rindās izdevumu kategorijām.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu identificēt. | Šis nosaukums tiks rādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss apraksts par pakalpojumiem, par kuriem kreditors izraksta rēķinus kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmuma līgums, uz kura sākotnēji tika pasūtīti pakalpojumi. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas rindas kreditora rēķinā pārmanto šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kurās ir atsauces uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līgumu līnija | Apakšuzņēmuma līnija, uz kuras tika pasūtīti pakalpojumi. To apakšlīgumu rindu saraksts, kuras var atlasīt, ir ierobežots līdz rindām atlasītajā apakšuzņēmuma līgumā. | Ja apakšuzņēmuma līgumu rinda ir atlasīta kreditora rēķina rindā izdevumu kategorijām, no atbilstošajiem apakšlīguma rindas laukiem tiek ievadītas **lauku Projekts**, **Uzdevums** un **Transakcija** noklusējuma vērtības laukiem. Ja atlasītajai apakšlīguma rindai ir vērtības laukos **Projekts**, **Uzdevums Projekts** un **Transakcija**, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks ierakstītas kreditora rēķina rindas faktiskās izmaksas. |Nevienu |
| Transakciju klase | Atlasiet **Izdevumi**, lai ierakstītu kreditora rēķinu izdevumu kategorijai. | Vērtība **Izdevumi** norāda, ka kreditora rēķina rinda tiek izmantota, lai ierakstītu rēķina summu par pakalpojumiem, kas tika iegādāti kā izdevumu kategorijas. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar izdevumiem, kas tiek ierakstīti jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma līguma rindiņu un šis lauks tiek atstāts tukšs, faktiskās izmaksas, ko izveido kreditora rēķina rinda, netiks saistītas ne ar vienu nesamaksātu pārdošanas faktisko vērtību. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, nevarēs izrakstīt rēķinus par izmaksām gala debitoram. |
| Transakciju kategorija | Transakciju kategorija, par kuru tiek izrakstīts rēķins. Atlasītajai transakciju kategorijai ir jāizveido atbilstoša izdevumu kategorija. | Transakciju kategorijas **un** **Vienības** vērtību kombinācija tiks izmantota kā noklusējuma vai aprēķinātā vērtība laukam **Vienības cena** kreditora rēķina rindā. |
| Daudzums | Rēķina rindā ievadiet daudzumu, par kuru kreditors ir izrakstījis rēķinu. |Nevienu|
| Vienību grupa | Noklusējuma vērtība tiek ievadīta, pamatojoties uz atlasītās transakciju kategorijas vienību grupu. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai iegādātos jebkurā vienības grupas vienībā. | Transakciju kategorijas **un** **Vienības** vērtību kombinācija tiks izmantota kā noklusējuma vai aprēķinātā vērtība laukam **Vienības cena** kreditora rēķina rindā. |
| Vienības cena | Noklusējuma vienības cenā tiek izmantota transakciju kategorijas **un** **vienības** vērtību kombinācija no projekta cenrāža, kas ir piemērojama kreditora rēķina rindas transakcijas datumam. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no vienības kreditora rēķina rindā, sistēma izmanto vienības konvertāciju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis tikai lasāmais lauks tiek aprēķināts kā *daudzuma*&times;*vienības cena*, ja vērtības tiek ievadītas gan laukā Daudzums **, gan** **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā varat ievadīt vērtību.| Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopējā summa, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummu* + *pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
