---
title: Kreditora rēķina rindas precēm
description: Šajā tēmā ir izskaidrots, kā reģistrēt piegādātāju rēķinu rindas precēm un izmantot dažādus laukus, lai reģistrētu preču iepirkumus no piegādātājiem.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599187"
---
# <a name="vendor-invoice-lines-for-products"></a>Kreditora rēķina rindas precēm

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditora rēķinā sistēmā Microsoft Dynamics 365 Project Operations var būt kreditora rēķina rindas precēm (sauktas arī par materiāliem). Projektu vadītāji var izmantot kreditoru rēķinu rindas precēm, lai reģistrētu projektos iegādāto preču izmaksas.

Kreditora rēķina rindas precēm var vai nevar atsaukties uz materiālu apakšuzņēmuma rindu. Ja kreditora rēķina rinda precēm atsaucas uz apakšuzņēmuma līgumu, projektu vadītāji varēs saskaņot un pārbaudīt preces, par kurām kreditora rēķina rinda izraksta rēķinu, salīdzinot ar iegādāto preču izmantošanu, kuras reģistrējuši un apstiprinājuši projektu vadītāji.

Šajā tabulā ir sniegta informācija par preču kreditora rēķina rindu laukiem.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu veikt identifikāciju. | Šis nosaukums tiks parādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss to preču apraksts, kurām kreditors izraksta rēķinu kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmums, kurā produkti sākotnēji tika pasūtīti. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas kreditora rēķina rindas pārmantos šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kas atsaucas uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līnija | Apakšuzņēmuma līnija, kurā preces tika pasūtītas. Atlasāmo apakšuzņēmuma rindu saraksts attiecas tikai uz atlasītā apakšlīguma rindām. | Ja preču kreditora rēķina rindā ir atlasīta apakšuzņēmuma rinda, lauku Projekts **,** Uzdevums **un** Prece **noklusētās vērtības** tiek ievadītas no atbilstošajiem zemlīguma rindas laukiem. Ja atlasītajai apakšuzņēmuma rindai ir vērtības **laukos Projekts**, **Uzdevums** un **Produkts**, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks reģistrētas kreditora rēķina rindas faktiskās izmaksas. | Nevienu|
| Transakciju klase | Kad precēm ir izrakstīts rēķins, šis lauks jāiestata uz **Materiāls**. | Vērtība **Materiāls** norāda, ka kreditora rēķina rinda tiek izmantota, lai reģistrētu iepirkto materiālu rēķina summu. |
| Project | Tā projekta nosaukums, kurā tika izmantotas preces, par kurām tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, kurā tika izmantotas preces, par kurām tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar iepirkto preci, kas tiek izmantota jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma rindu un šis lauks ir atstāts tukšs, faktiskās izmaksas, ko izveidojusi kreditora rēķina rinda, netiks saistītas ar neskaitāmām pārdošanas faktiskajām versijām. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, izmaksas nevarēs izrakstīt gala debitoram. |
| Atlasīt produktu | Atlasiet, vai prece, par kuru tiek izrakstīts rēķins, ir esoša prece no kataloga vai ierakstāmā prece. | Noklusējuma vērtība tiek ievadīta no apakšuzņēmuma rindas, kad ir atlasīta apakšuzņēmuma līguma rinda. |
| Produkts | Atlasiet preci no kataloga. Ja produkts ir ierakstāms produkts, ievadiet produkta nosaukumu. | Šis lauks tiek izmantots, lai ievadītu esošo preču noklusējuma iepirkuma cenas. |
| Daudzums | Ievadiet materiālu daudzumu, par kuru piegādātājs izraksta rēķinu šajā rēķina rindā. | Nevienu |
| Vienību grupa | Atlasiet vienības vienību grupu, kurā ir izteikts daudzums, par kuru tiek izrakstīts rēķins. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai samaksātu jebkurā atlasītās vienību grupas vienībā. | Produkta un vienības vērtību kombinācija **tiks izmantota kā kreditora rēķina rindas lauka Vienības cena** noklusējuma vai aprēķinātā vērtība **.** **·** |
| Vienības cena | Noklusētajā vienības cenā tiek izmantota projekta cenrāža produktu **un** vienību **vērtību kombinācija**, kas attiecas uz kreditora rēķina rindas darbības datumu. | Nevienu |
| Starpsumma | Šis lasāmais lauks tiek aprēķināts kā *Daudzuma*&times;*vienības cena*, ja vērtības ir ievadītas gan laukā Daudzums **,** gan **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā var ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummas* + *PVN*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
