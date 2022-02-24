---
title: Resursu lietojamības pārskats
description: Šajā tēmā ir sniegta informācija par resursu lietojumu risinājumā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401385"
---
# <a name="resource-utilization-overview"></a>Resursu lietojamības pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Resursiem var būt mērķa apmaksājamā izmantošana. Šī mērķa izmantošana tiek vai nu definēta kā atribūts resursa noklusējuma lomā, vai iestatīta atsevišķa rezervācijas resursa ierakstā. Izmantošanas aprēķini ir balstīti uz faktiskajām stundām, par kurām resursi ir paziņojuši, izmantojot apstiprinātos laika ierakstus.

Izmantošanas aprēķināšanai lieto šādas formulas:

  - Apmaksājamā izmantošana = Rēķinā iekļaujamās stundas ÷ Resursa noslodze
  - Neapmaksājamā izmantošana = Faktiskais laiks ar norēķinu tipa ID = Rēķinā neiekļaujams, Papildu vai Nav pieejams ÷ Resursa noslodze
  - Iekšējs = Faktiskais laiks bez pārdošanas līguma ÷ Resursa noslodze
  - Resursa noslodze = Resursa darba stundas – Ārpus biroja – Brīvdienas

Skatu **Resursa izmantojums** var atrast rūtī **Resursi**.

Katra režģa šūna norāda resursa apmaksājamās izmantošanas procentuālo vērtību periodā, piemēram, dienā, nedēļā vai mēnesī. Šūnu iekrāsošanai lieto šādas formulas:

  - **Zaļa**: rēķinā iekļaujamais lietojums >= resursa mērķa lietojums
  - **Dzeltena**: mērķa lietojums – 20 <= rēķinā iekļaujamais lietojums < mērķa lietojums
  - **Sarkana**: rēķinā iekļaujamais lietojums < mērķa lietojums – 20

Tā kā skats **Apmaksājamā izmantošana** ir atkarīgs no plānošanas paneļa, varat izmantot plānošanas paneļa filtrēšanas iespējas, lai filtrētu rezultātus.

Režģim ir jāiestata mērķa lietojums lomai vai atsevišķam resursam. Lai veiktu šo iestatīšanu, atveriet **Resursi** > **Resursu lomas**.

Turklāt katram rezervējamajam resursam ir jāpiešķir noklusējuma loma. Atveriet sadaļu **Resursi** > **Resursi**. Cilnē **Project Service** pārbaudiet, vai resursa loma ir definēta un vai laukā **Ir noklusējuma** ir iestatīta vērtība **Jā**. Varat pievienot papildu lomas, kurām iestatīta opcija **Ir noklusējuma** = **Nē**. Loma, kurai iestatīta opcija **Ir noklusējuma** = **Jā**, tiek izmantota, lai novērtētu resursa izmantojumu atbilstoši attiecīgās mērķim.

Cilnē **Project Service** resursam var iestatīt arī atsevišķu mērķa lietojumu. Šādā gadījumā lietojuma aprēķinā tiek izmantots mērķa lietojums, lai novērtētu resursa mērķi, nevis resursa noklusējuma lomas mērķi.

Resursa lietojums tiek rādīts tikai tad, ja šis resurss ir apstiprinājis rēķinā iekļaujamu laiku periodā, kas ir norādīts režģī.
