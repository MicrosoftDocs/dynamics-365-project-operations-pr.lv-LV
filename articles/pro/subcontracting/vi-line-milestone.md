---
title: Kreditora rēķina rindas par atskaites punktiem
description: Šajā rakstā ir izskaidrots, kā apakšlīgumā izveidot atskaites punktu rēķina rindas.
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

Piegādātāja rēķinam programmā Microsoft Dynamics 365 Project Operations var būt piegādātāja rēķina rindas atskaites punktiem, kas ir definēti apakšlīguma rindā. Projektu vadītāji var izmantot piegādātāju rēķinu rindas par atskaites punktiem, lai reģistrētu izmaksas par pakalpojumiem, kas tiek iegādāti kā uz atskaites punktiem balstītas izmaksas, kuras rodas saistībā ar projektam iegādātajiem pakalpojumiem vai produktiem.

Piegādātāja rēķina rindās atskaites punktiem vienmēr ir jābūt atsaucei uz apakšlīguma rindu, kam ir fiksētas cenas norēķinu metode. Kad piegādātāja rēķina rinda atskaites punktiem satur atsauci uz apakšlīguma rindu, projektu vadītāji var saskaņot un pārbaudīt laika, izdevumu vai materiālu pamata izmaksas, uz ko attiecas šīs apakšlīguma rindas atsauce, salīdzinot ar atskaites punktu, par kuru izraksta rēķinu piegādātājs.

Šajā tabulā ir informācija par piegādātāja rēķina rindām atskaites punktiem.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Piegādātāja rēķina rindas nosaukums, lai atvieglotu identificēšanu. | Šis nosaukums tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, kas ir balstīti uz piegādātāja rēķina rindām. |
| Apraksts | Īss pakalpojumu apraksts, par kuriem piegādātājs izraksta rēķinu piegādātāja rēķina rindā. | Nevienu |
| Apakšuzņēmēja līgums | Apakšlīgums, ar kuru pakalpojumi sākotnēji tika pasūtīti. | Ja piegādātāja rēķinam ir atlasīts apakšlīgums, visas rindas piegādātāja rēķinā pārmantos šo atlasi. Piegādātāja rēķinā nevar būt piegādātāja rēķina rindas, kam ir atsauce uz dažādiem apakšlīgumiem. |
| Apakšlīguma rinda | Apakšlīguma rinda, ar kuru pakalpojumi tika pasūtīti. Atlasāmo apakšlīguma rindu saraksts ir ierobežots līdz atlasītā apakšlīguma rindām. | Ja piegādātāja rēķina rindā atskaites punktiem tiek atlasīta apakšlīguma rinda, lauki **Loma** un **Transakcijas kategorija**, kā arī ar produktiem saistītie lauki nav būtiski un nav pieejami. Arī lauki **Daudzums**, **Vienība** un **Vienību grupa** nav būtiski uz atskaites punktiem balstītām piegādātāja rēķina rindām. |
| Darījuma datums | Datums, kurā piegādātāja rēķina rindas faktiskās izmaksas tiek ierakstītas projektā. | Nevienu |
| Transakciju klase | Atlasiet **Atskaites punkts**, lai ierakstītu pārdevēja rēķinu par pabeigtu atskaites punktu, kas tika definēts apakšlīguma rindā. | Nevienu |
| Atskaites punkts | Atlasiet atskaites punktu, kas ir definēts saistītajā apakšlīguma rindā, kas atzīmēta kā **Gatavs rēķina izrakstīšanai**. | Apakšlīguma rindas atskaites punktus, kuriem ir statuss **Gatavs rēķina izrakstīšanai**, var atlasīt piegādātāja rēķina rindā. |
| Project | Projekta nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. | Šis lauks ir obligāts, un to nevar atstāt tukšu. |
| Uzdevums | Projekta uzdevuma nosaukums, kurā tika izmantoti pakalpojumi, par kuriem tiek izrakstīts rēķins. Šis lauks ir pieejams tikai tad, ja ir atlasīts projekts. Projekta uzdevuma atlase nav obligāta. | Ja šis lauks ir atstāts tukšs, projekta vadītājs var saskaņot piegādātāja rēķina rindu ar transakciju klasi saistītajā apakšlīguma rindā, kas tiek ierakstīta jebkurā projekta uzdevumā. Ja piegādātāja rēķina rindā nav atsauces uz apakšlīguma rindu un šis lauks ir atstāts tukšs, piegādātāja rēķina rindas izveidotās faktiskās izmaksas netiks saistītas ne ar kādām rēķinā neiekļautām faktiskajām pārdošanām. Šajā gadījumā, ja ir iestatīti uz uzdevumiem balstīti norēķini, par izmaksām var nebūt iespējams izrakstīt rēķinu gala klientam. |
| Atskaites punkta summa | Ievadiet atskaites punkta vērtību, kas ir definēta apakšlīguma rindā, kas ir gatava rēķina izrakstīšanai. | Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. | Nevienu |
| Kopsumma | Piegādātāja rēķina rindas kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā *Atskaites punkta summa* + *Pārdošanas nodokļi*. | Nevienu |

> [!NOTE]
> Veidojot piegādātāja rēķina rindu ar atsauci uz apakšlīguma rindas atskaites punktu, apakšlīguma atskaites punkta statuss tiek atjaunināts uz **Izveidots piegādātāja rēķins**. Pēc tam, kad šis piegādātāja rēķins ir apstiprināts, apakšlīguma rindas atskaites punkta statuss tiek atjaunināts uz **Piegādātāja rēķins apstiprināts**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
