---
title: Kreditora rēķina rindas atskaites punktiem
description: Šajā tēmā paskaidrots, kā izveidot kreditora rēķina rindas starplīguma atskaites punktiem.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590631"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Kreditora rēķina rindas atskaites punktiem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditora rēķinā sistēmā Microsoft Dynamics 365 Project Operations var būt kreditora rēķina rindas atskaites punktiem, kas definēti apakšuzņēmuma rindā. Projektu vadītāji var izmantot kreditora rēķina rindas atskaites punktiem, lai reģistrētu to pakalpojumu izmaksas, kas tiek iepirkti kā starpposma izmaksas, kas radušās par pakalpojumiem vai produktiem, kuri tiek iepirkti projektam.

Kreditora rēķina rindām atskaites punktiem vienmēr jāatsaucas uz apakšuzņēmuma rindu, kurai ir fiksētas cenas norēķinu metode. Ja kreditora rēķina rinda atskaites punktiem atsaucas uz apakšuzņēmuma rindu, projektu vadītāji varēs saskaņot un pārbaudīt laika, izdevumu vai materiālu pamatizmaksas, kas atsaucas uz šo apakšuzņēmuma rindu, ar atskaites punktu, par kuru kreditors izraksta rēķinu.

Šajā tabulā ir sniegta informācija par atskaites punktu kreditoru rēķinu rindu laukiem.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu veikt identifikāciju. | Šis nosaukums tiks parādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss to pakalpojumu apraksts, par kuriem piegādātājs izraksta rēķinu kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmums, kurā pakalpojumi sākotnēji tika pasūtīti. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas kreditora rēķina rindas pārmantos šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kas atsaucas uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līnija | Apakšuzņēmuma līnija, kurā pakalpojumi tika pasūtīti. Atlasāmo apakšuzņēmuma rindu saraksts attiecas tikai uz atlasītā apakšlīguma rindām. | Ja kreditora rēķina rindā atskaites punktiem ir atlasīta apakšuzņēmuma rinda, **lauki Loma** un **Transakcija kategorija** un ar produktu saistītie lauki nav atbilstoši un nav pieejami. Lauki **Daudzums**, **Vienība** un **Vienību grupa** neattiecas arī uz atskaites punkta kreditora rēķina rindām. |
| Darījuma datums | Datums, kad projektā tiks reģistrētas kreditora rēķina rindas faktiskās izmaksas. | Nevienu |
| Transakciju klase | Atlasiet **Atskaites punkts**, lai ierakstītu kreditora rēķinu par pabeigtu atskaites punktu, kas tika definēts apakšuzņēmuma rindā. | Nevienu |
| Atskaites punkts | Atlasiet atskaites punktu, kas definēts saistītajā apakšuzņēmuma rindā, kas atzīmēta kā **gatava rēķinam**. | Apakšuzņēmuma rindas atskaites punktus, kuru statuss **ir Gatavs rēķinam**, var atlasīt kreditora rēķina rindā. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, par kuru tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar darbību klasi saistītajā apakšuzņēmuma rindā, kas tiek ierakstīta jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma rindu un šis lauks ir atstāts tukšs, faktiskās izmaksas, ko izveidojusi kreditora rēķina rinda, netiks saistītas ar neskaitāmām pārdošanas faktiskajām versijām. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, ka par izmaksām nevar izrakstīt rēķinus gala debitoram. |
| Atskaites punkta summa | Ievadiet atskaites punkta vērtību, kas definēta apakšuzņēmuma rindā, kura ir gatava rēķina izrakstīšanai. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *Atskaites punkta summa* + *PVN*. | Nevienu |

> [!NOTE]
> Kad tiek izveidota kreditora rēķina rinda, kas atsaucas uz apakšuzņēmuma rindas atskaites punktu, apakšlīguma atskaites punkta statuss tiek atjaunināts uz **izveidoto** kreditora rēķinu. Pēc tam, kad šis kreditora rēķins ir apstiprināts, apakšuzņēmuma rindas atskaites punkta statuss tiek atjaunināts uz **kreditora rēķina apstiprinājumu**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
