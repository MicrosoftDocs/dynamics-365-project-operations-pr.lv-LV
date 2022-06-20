---
title: Kreditoru rēķinu rindas izdevumu kategorijām
description: Šajā rakstā paskaidrots, kā reģistrēt kreditora rēķina rindas izdevumu kategorijām.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925895"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Kreditoru rēķinu rindas izdevumu kategorijām

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditora rēķinā sistēmā Microsoft Dynamics 365 Project Operations var būt kreditora rēķina rindas izdevumu kategorijām. Projektu vadītāji var izmantot kreditoru rēķinu rindas izdevumu kategorijām, lai reģistrētu to pakalpojumu izmaksas, kas iepirkti kā izdevumu kategorijas.

Kreditora rēķina rindas izdevumu kategorijām var vai nevar atsaukties uz apakšuzņēmuma rindu izdevumu kategorijām. Ja kreditora rēķina rinda izdevumu kategorijām atsaucas uz apakšuzņēmuma līgumu, projektu vadītāji varēs saskaņot un pārbaudīt izdevumus, par kuriem kreditora rēķina rinda izraksta rēķinu, ar izdevumiem, kas reģistrēti šajās izdevumu kategorijās un ko projekta vadītāji ir apstiprinājuši projektā.

Šajā tabulā ir sniegta informācija par kreditoru rēķinu rindu laukiem izdevumu kategorijām.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu veikt identifikāciju. | Šis nosaukums tiks parādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss to pakalpojumu apraksts, kuriem kreditors izraksta rēķinu kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmums, kurā pakalpojumi sākotnēji tika pasūtīti. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas kreditora rēķina rindas pārmantos šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kas atsaucas uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līnija | Apakšuzņēmuma līnija, kurā pakalpojumi tika pasūtīti. Atlasāmo apakšuzņēmuma rindu saraksts attiecas tikai uz atlasītā apakšlīguma rindām. | Ja kreditora rēķina rindā izdevumu kategorijām ir atlasīta apakšuzņēmuma rinda, noklusētās vērtības **laukiem Projekts**, **Uzdevums** un **Darbība tiek** ievadītas no atbilstošajiem zemlīguma rindas laukiem. Ja atlasītajai apakšuzņēmuma rindai ir vērtības **laukos Projekts**, **Projekta uzdevums** un **Transakcija**, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks reģistrētas kreditora rēķina rindas faktiskās izmaksas. |Nevienu |
| Transakciju klase | Atlasiet **Izdevumi**, lai reģistrētu kreditora rēķinu izdevumu kategorijai. | Vērtība **Izdevumi** norāda, ka kreditora rēķina rinda tiek izmantota, lai reģistrētu rēķina summu pakalpojumiem, kas iepirkti kā izdevumu kategorijas. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, par kuru tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar izdevumiem, kas ierakstīti jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma rindu un šis lauks ir atstāts tukšs, faktiskās izmaksas, ko izveidojusi kreditora rēķina rinda, netiks saistītas ar neskaitāmām pārdošanas faktiskajām versijām. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, ka par izmaksām nevar izrakstīt rēķinus gala debitoram. |
| Transakciju kategorija | Darbību kategorija, kurai tiek izrakstīts rēķins. Atlasītajai darbību kategorijai ir jāizveido atbilstoša izdevumu kategorija. | Darbību kategorijas un vienības vērtību kombinācija **tiks izmantota kā noklusētā vai aprēķinātā vērtība kreditora rēķina rindas laukam** Vienības cena **.** **·** |
| Daudzums | Ievadiet daudzumu, par kuru piegādātājs rēķina rindā izraksta rēķinu. |Nevienu|
| Vienību grupa | Noklusējuma vērtība tiek ievadīta, pamatojoties uz atlasītās darbību kategorijas vienību grupu. | Nevienu |
| Vienība | Noklusējuma vērtība ir atlasītās vienību grupas pamatvienība. Šo vērtību var mainīt, lai iegādātos jebkurā vienību grupas vienībā. | Darbību kategorijas un vienības vērtību kombinācija **tiks izmantota kā noklusētā vai aprēķinātā vērtība kreditora rēķina rindas laukam** Vienības cena **.** **·** |
| Vienības cena | Noklusējuma vienības cenā tiek izmantota projekta cenrāža transakciju **kategorijas** un **vienības** vērtību kombinācija, kas attiecas uz kreditora rēķina rindas darbības datumu. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no piegādātāja rēķina rindas vienības, sistēma izmanto vienību konvertēšanu, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis lasāmais lauks tiek aprēķināts kā *Daudzuma*&times;*vienības cena*, ja vērtības ir ievadītas gan laukā Daudzums **,** gan **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā var ievadīt vērtību.| Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummas* + *PVN*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
