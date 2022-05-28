---
title: Kreditora rēķina rindas laikam
description: Šajā tēmā ir izskaidrots, kā reģistrēt kreditora rēķina rindas laika izmaksām, ko apakšuzņēmēji ir ieguldījuši.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597209"
---
# <a name="vendor-invoice-lines-for-time"></a>Kreditora rēķina rindas laikam

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditora rēķinā sistēmā Microsoft Dynamics 365 Project Operations var būt kreditora rēķina rindas laikam. Projektu vadītāji var laiku izmantot kreditora rēķina rindas, lai reģistrētu apakšuzņēmēja laika izmaksas projektos.

Kreditora rēķina rindas laikam var vai nevar atsaukties uz apakšuzņēmuma rindu uz laiku. Ja kreditora rēķina rinda laikam atsaucas uz apakšuzņēmuma līgumu, projektu vadītāji varēs saskaņot un pārbaudīt laiku, par kuru kreditora rēķina rinda izraksta rēķinu, ar laiku, ko reģistrē apakšuzņēmēji un apstiprina projekta vadītāji.

Šajā tabulā ir sniegta informācija par laukiem kreditora rēķina rindās laikam.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu veikt identifikāciju. | Šis nosaukums tiks parādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss to pakalpojumu apraksts, kuriem kreditors izraksta rēķinu kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmums, kurā pakalpojumi sākotnēji tika pasūtīti. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas kreditora rēķina rindas pārmantos šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kas atsaucas uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līnija | Apakšuzņēmuma līnija, kurā pakalpojumi tika pasūtīti. Atlasāmo apakšuzņēmuma rindu saraksts attiecas tikai uz atlasītā apakšlīguma rindām. | Ja kreditora rēķina rindā uz laiku ir atlasīta apakšuzņēmuma rinda, nolīguma vērtības **laukiem projekta**, **lomas** un **rezervējamā resursa** laukiem tiek ievadītas no atbilstošajiem apakšuzņēmuma rindas laukiem. Ja atlasītajai apakšuzņēmuma rindai ir vērtības **laukos Projekts**, **Loma** un **Rezervējams**, atbilstošo lauku vērtības kreditora rēķina rindā nevar atšķirties no šīm vērtībām. |
| Darījuma datums | Datums, kad projektā tiks reģistrētas kreditora rēķina rindas faktiskās izmaksas. | Nevienu |
| Transakciju klase | Noklusējuma vērtība ir **"Laiks"**. | Vērtība **Laiks** norāda, ka kreditora rēķina rinda tiek izmantota, lai reģistrētu apakšuzņēmēja laika rēķina summu. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, par kuru tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar laiku, ko apakšuzņēmēja resursi reģistrē jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma rindu un šis lauks ir atstāts tukšs, faktiskās izmaksas, ko izveidojusi kreditora rēķina rinda, netiks saistītas ar neskaitāmām pārdošanas faktiskajām versijām. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, ka par izmaksām nevar izrakstīt rēķinus gala debitoram. |
| Loma | Apakšuzņēmuma resursu loma, par kuru laiku tiek izrakstīts rēķins. | Šajā laukā ir norādīta loma, ko veic apakšuzņēmuma resursi, kuru rēķinā norādītais laiks kreditora rēķinā. |
| Rezervējamais resurss | Tā apakšuzņēmēja nosaukums, par kura laiku tiek izrakstīts rēķins. Rezervējamā resursa atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar laiku, ko reģistrē jebkurš resurss, kas pieder piegādātājam kreditora rēķina rindā. |
| Daudzums | Ievadiet laika stundu skaitu, par kurām kreditors rēķina rindā izraksta rēķinu. |Nevienu |
| Vienību grupa | Noklusējuma vērtība ir **laika vienību grupa**, un to nevar mainīt. | Nevienu |
| Vienība | Noklusējuma vērtība ir laika vienību grupas stundu pamatvienība. Šo vērtību var mainīt, lai iegādātos jebkurā laika vienību grupas vienībā, piemēram, dienā vai nedēļā. | Lomu un vienības vērtību kombinācija **tiks izmantota kā noklusētā vai aprēķinātā vērtība kreditora rēķina rindas laukam** Vienības cena **.** **·** |
| Vienības cena | Noklusējuma vienības cenā tiek izmantota lomas un **vienības** vērtību kombinācija **no** projekta cenrāža, kas attiecas uz kreditora rēķina rindas darbības datumu. | Ja piemērojamā projekta cenrāža cena ir iestatīta vienībā, kas atšķiras no piegādātāja rēķina rindas vienības, sistēma izmanto vienību konvertēšanu, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis lasāmais lauks tiek aprēķināts kā *Daudzuma*&times;*vienības cena*, ja vērtības ir ievadītas gan laukā Daudzums **,** gan **laukā Vienības cena.** Ja viens vai abi šie lauki ir tukši, šajā laukā var ievadīt vērtību. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *starpsummas* + *PVN*. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
