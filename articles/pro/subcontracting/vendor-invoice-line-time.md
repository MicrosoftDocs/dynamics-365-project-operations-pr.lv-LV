---
title: Kreditora rēķina rindas par laiku
description: Šajā rakstā ir paskaidrots, kā reģistrēt kreditoru rēķinu rindas par laika izmaksām, ko apakšuzņēmēji ir ieguldījuši.
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

Kreditora rēķinam korporācijā Microsoft Dynamics 365 Project Operations var būt kreditora rēķina rindas uz laiku. Projektu vadītāji var izmantot kreditoru rēķinu rindas uz laiku, lai reģistrētu apakšuzņēmēja laika izmaksas projektos.

Kreditora rēķina rindās uz laiku var būt vai nebūt atsauces uz apakšuzņēmuma līgumu rindiņu. Ja kreditora rēķina rindā par laiku ir atsauce uz apakšlīgumu, projektu vadītāji varēs saskaņot un pārbaudīt laiku, par kuru rēķins tiek izrakstīts, izmantojot kreditora rēķina rindu, ar laiku, ko reģistrējuši apakšuzņēmēji un ko projekta vadītāji ir apstiprinājuši projektā.

Šajā tabulā ir sniegta informācija par laukiem kreditoru rēķinu rindās uz laiku.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu identificēt. | Šis nosaukums tiks rādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss apraksts par pakalpojumiem, par kuriem kreditors izraksta rēķinus kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmuma līgums, uz kura sākotnēji tika pasūtīti pakalpojumi. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas rindas kreditora rēķinā pārmanto šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kurās ir atsauces uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līgumu līnija | Apakšuzņēmuma līnija, uz kuras tika pasūtīti pakalpojumi. To apakšlīgumu rindu saraksts, kuras var atlasīt, ir ierobežots līdz rindām atlasītajā apakšuzņēmuma līgumā. | Ja apakšuzņēmuma līgumu rinda ir atlasīta kreditora rēķina rindā uz laiku, lauka Projekts **,** Loma **un** Rezervējamais resurss **noklusējuma vērtības** tiek ievadītas no atbilstošajiem apakšlīguma rindas laukiem. Ja atlasītajā apakšuzņēmuma līguma rindiņā ir vērtības laukos **Projekts**, **Loma** un **Rezervējams** laukos, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks ierakstītas kreditora rēķina rindas faktiskās izmaksas. | Nevienu |
| Transakciju klase | Noklusējuma vērtība ir **"Laiks"**. | Vērtība **Laiks** norāda, ka kreditora rēķina rinda tiek izmantota, lai reģistrētu apakšuzņēmēja laika rēķina summu. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar laiku, ko reģistrē apakšuzņēmēju resursi jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma līguma rindiņu un šis lauks tiek atstāts tukšs, faktiskās izmaksas, ko izveido kreditora rēķina rinda, netiks saistītas ne ar vienu nesamaksātu pārdošanas faktisko vērtību. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, nevarēs izrakstīt rēķinus par izmaksām gala debitoram. |
| Loma | To apakšuzņēmuma līgumu resursu loma, par kuru laiku tiek izrakstīts rēķins. | Šis lauks norāda lomu, ko veic apakšuzņēmuma līguma resursi, kuru laiks tiek izrakstīts rēķinā ar kreditora rēķinu. |
| Rezervējamais resurss | Tā apakšuzņēmēja nosaukums, kura laiks tiek izrakstīts rēķinos. Rezervējama resursa izvēle nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar laiku, ko reģistrē jebkurš resurss, kas pieder kreditoram kreditora rēķina rindā. |
| Daudzums | Rēķina rindā ievadiet laika stundu skaitu, par kurām kreditors ir izrakstījis rēķinu. |Nevienu |
| Vienību grupa | Noklusējuma vērtība ir **Laika vienības grupa**, un to nevar mainīt. | Nevienu |
| Vienība | Noklusējuma vērtība ir stundu pamatvienība no laika vienības grupas. Šo vērtību var mainīt, lai iegādātos jebkurā laika vienības grupas vienībā, piemēram, dienā vai nedēļā. | Lomu un vienības vērtību kombinācija **tiks izmantota kā noklusējuma vai aprēķinātā vērtība laukam** Vienības cena **kreditora rēķina rindā.** **·** |
| Vienības cena | Noklusējuma vienības cenā tiek izmantota lomas **un** vienības **vērtību kombinācija** no projekta cenrāža, kas ir piemērojama kreditora rēķina rindas transakcijas datumam. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no vienības kreditora rēķina rindā, sistēma izmanto vienības konvertāciju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis tikai lasāmais lauks tiek aprēķināts kā *daudzuma*&times;*vienības cena*, ja vērtības tiek ievadītas gan laukā Daudzums **, gan** **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā varat ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopējā summa, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummu* + *pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
