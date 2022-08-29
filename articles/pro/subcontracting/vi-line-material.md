---
title: Kreditora rēķina rindas par produktiem
description: Šajā rakstā ir paskaidrots, kā reģistrēt preču kreditoru rēķinu rindas un izmantot dažādus laukus, lai reģistrētu preču pirkumus no kreditoriem.
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

Kreditora rēķinā korporācijā Microsoft Dynamics 365 Project Operations var būt kreditoru rēķinu rindas par produktiem (sauktiem arī par materiāliem). Projektu vadītāji var izmantot kreditoru rēķinu rindas precēm, lai reģistrētu projektos iegādāto preču izmaksas.

Kreditoru rēķinu rindās par precēm var būt vai nebūt atsauces uz apakšuzņēmuma līgumu rindu par materiāliem. Ja preču kreditora rēķina rindā ir atsauces uz apakšlīgumu, projektu vadītāji varēs saskaņot un pārbaudīt preces, par kurām rēķins tiek izrakstīts, izmantojot kreditora rēķina rindu, pret iegādāto preču izmantošanu, kuras ir reģistrējuši un apstiprinājuši projektu vadītāji.

Šajā tabulā ir sniegta informācija par laukiem preču kreditoru rēķinu rindās.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu identificēt. | Šis nosaukums tiks rādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss apraksts par precēm, par kurām kreditors ir izrakstījis rēķinus kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšlīgums, uz kura preces sākotnēji tika pasūtītas. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas rindas kreditora rēķinā pārmanto šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kurās ir atsauces uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līgumu līnija | Apakšuzņēmuma līnija, uz kuras tika pasūtīti produkti. To apakšlīgumu rindu saraksts, kuras var atlasīt, ir ierobežots līdz rindām atlasītajā apakšuzņēmuma līgumā. | Ja apakšuzņēmuma līgumu rinda ir atlasīta preču kreditora rēķina rindā, apakšuzņēmuma līguma rindas atbilstošajos laukos tiek ievadītas **lauku Projekts**, **Uzdevums** un **Produkts** noklusējuma vērtības. Ja atlasītajai apakšuzņēmuma līgumu rindai ir vērtības laukos **Projekts**, **Uzdevums** un **Produkts**, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks ierakstītas kreditora rēķina rindas faktiskās izmaksas. | Nevienu|
| Transakciju klase | Kad rēķins par produktiem tiek izrakstīts, šim laukam ir jābūt iestatītam uz **Materiāls**. | Vērtība **Materiāls** norāda, ka kreditora rēķina rinda tiek izmantota, lai reģistrētu rēķina summu par iegādātajiem materiāliem. |
| Project | Tā projekta nosaukums, kurā tika izmantoti rēķini par produktiem, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, kurā tika izmantotas preces, par kurām tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar iegādāto preci, kas tiek izmantota jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma līguma rindiņu un šis lauks tiek atstāts tukšs, faktiskās izmaksas, ko izveido kreditora rēķina rinda, netiks saistītas ne ar vienu nesamaksātu pārdošanas faktisko vērtību. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, rēķinus par izmaksām nevarēs izrakstīt gala debitoram. |
| Atlasīt produktu | Atlasiet, vai prece, par kuru tiek izrakstīts rēķins, ir esoša prece no kataloga vai ierakstāma prece. | Noklusējuma vērtība tiek ievadīta no apakšuzņēmuma līguma rindas, kad ir atlasīta apakšuzņēmuma līguma rindiņa. |
| Produkts | Atlasiet produktu no kataloga. Ja produkts ir ierakstāms produkts, ievadiet produkta nosaukumu. | Šis lauks tiek izmantots, lai ievadītu esošo preču noklusējuma pirkšanas cenas. |
| Daudzums | Ievadiet materiāla daudzumu, par kuru kreditors ir izrakstījis rēķinu šajā rēķina rindā. | Nevienu |
| Vienību grupa | Atlasiet vienības vienību grupu, kurā ir izteikts rēķins par daudzumu, par kuru tiek izrakstīts rēķins. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai samaksātu jebkurā atlasītās vienības grupas vienībā. | Vērtības Produkts **un** **Vienība** kombinācija tiks izmantota kā noklusējuma vai aprēķinātā vērtība laukam **Vienības cena** kreditora rēķina rindā. |
| Vienības cena | Noklusējuma vienības cenā tiek izmantota produkta **un** vienības **vērtību kombinācija** no projekta cenrāža, kas ir piemērojama kreditora rēķina rindas transakcijas datumam. | Nevienu |
| Starpsumma | Šis tikai lasāmais lauks tiek aprēķināts kā *daudzuma*&times;*vienības cena*, ja vērtības tiek ievadītas gan laukā Daudzums **, gan** **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā varat ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopējā summa, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummu* + *pārdošanas nodoklis*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
