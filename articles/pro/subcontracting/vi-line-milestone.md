---
title: Kreditora rēķina rindas par atskaites punktiem
description: Šajā rakstā ir paskaidrots, kā izveidot kreditoru rēķinu rindas atskaites punktiem apakšuzņēmuma līgumā.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261037"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Kreditora rēķina rindas par atskaites punktiem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditora rēķinā korporācijā Microsoft Dynamics 365 Project Operations var būt kreditoru rēķinu rindas atskaites punktiem, kas ir definēti apakšuzņēmuma līguma rindā. Projektu vadītāji var izmantot kreditoru rēķinu rindas atskaites punktiem, lai reģistrētu to pakalpojumu izmaksas, kas tiek iepirkti kā uz atskaites punktu balstītas izmaksas, kuras rodas par pakalpojumiem vai precēm, kas tiek iepirktas projektam.

Kreditoru rēķinu rindās atskaites punktiem vienmēr ir jāatsaucas uz apakšuzņēmuma līgumu rindu, kurai ir fiksētas cenas norēķinu metode. Kad atskaites punktu kreditora rēķina rindā ir atsauce uz apakšuzņēmuma līgumu rindu, projektu vadītāji varēs saskaņot un pārbaudīt laika, izdevumu vai materiālu, kuros ir atsauce uz šo apakšuzņēmuma līgumu, pamatā esošās izmaksas attiecībā pret atskaites punktu, par kuru kreditors ir izrakstījis rēķinu.

Nākamajā tabulā ir sniegta informācija par laukiem kreditoru rēķinu rindās atskaites punktiem.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina rindas nosaukums, lai palīdzētu identificēt. | Šis nosaukums tiks rādīts kā pirmā kolonna visās uzmeklēšanas reizēs, kuru pamatā ir kreditora rēķina rindas. |
| Apraksts | Īss apraksts par pakalpojumiem, par kuriem kreditors ir izrakstījis rēķinus kreditora rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšuzņēmuma līgums, uz kura sākotnēji tika pasūtīti pakalpojumi. | Ja kreditora rēķinam ir atlasīts apakšlīgums, visas rindas kreditora rēķinā pārmanto šo atlasi. Kreditora rēķinā nevar būt kreditora rēķina rindas, kurās ir atsauces uz dažādiem apakšuzņēmuma līgumiem. |
| Apakšuzņēmuma līgumu līnija | Apakšuzņēmuma līnija, uz kuras tika pasūtīti pakalpojumi. To apakšlīgumu rindu saraksts, kuras var atlasīt, ir ierobežots līdz rindām atlasītajā apakšuzņēmuma līgumā. | Ja atskaites punktiem kreditora rēķina rindā ir atlasīta apakšuzņēmuma līguma rinda, **lauki Lomu** un **transakciju kategorija** un ar precēm saistītie lauki nav būtiski un nav pieejami. Lauki **Daudzums**, **Vienība** un **Vienība** arī neattiecas uz atskaites punktu balstītām kreditoru rēķinu rindām. |
| Darījuma datums | Datums, kad projektā tiks ierakstītas kreditora rēķina rindas faktiskās izmaksas. | Nevienu |
| Transakciju klase | Atlasiet **Atskaites punkts**, lai ierakstītu kreditora rēķinu par pabeigtu atskaites punktu, kas tika definēts apakšuzņēmuma līguma rindiņā. | Nevienu |
| Atskaites punkts | Atlasiet atskaites punktu, kas ir definēts saistītajā apakšlīguma rindiņā, kas ir atzīmēta kā **Gatavs rēķinam**. | Apakšuzņēmuma līgumu rindu atskaites punktus, kuru statuss **ir Gatavs rēķinam**, var atlasīt kreditora rēķina rindā. |
| Project | Tā projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Tā projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot kreditora rēķina rindu ar transakciju klasi saistītajā apakšlīguma rindā, kas tiek ierakstīta jebkurā projekta uzdevumā. Ja kreditora rēķina rindā nav atsauces uz apakšuzņēmuma līguma rindiņu un šis lauks tiek atstāts tukšs, faktiskās izmaksas, ko izveido kreditora rēķina rinda, netiks saistītas ne ar vienu nesamaksātu pārdošanas faktisko vērtību. Šādā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, iespējams, nevarēs izrakstīt rēķinus par izmaksām gala debitoram. |
| Atskaites punkta summa | Ievadiet atskaites punkta vērtību, kas ir definēta apakšuzņēmuma līgumu rindā, kura ir gatava rēķināšanai. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Kreditora rēķina rindas kopējā summa, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *atskaites punkta summa* + *PĀRDOŠANAS NODOKLIS*. | Nevienu |

> [!NOTE]
> Kad tiek izveidota kreditora rēķina rinda, kas atsaucas uz apakšuzņēmuma līgumu rindas atskaites punktu, apakšuzņēmuma atskaites punkta statuss tiek atjaunināts uz **Izveidots** kreditora rēķins. Pēc tam, kad šis kreditora rēķins ir apstiprināts, apakšuzņēmuma līguma rindas atskaites punkta statuss tiek atjaunināts uz **Apstiprināts** kreditora rēķins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
