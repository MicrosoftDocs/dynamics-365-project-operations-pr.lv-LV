---
title: Konfigurēt iekšējo projektu uzskaiti
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt uzskaites metodes Project Operations iekšējiem projektiem.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005535"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurēt iekšējo projektu uzskaiti

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Iekšējie projekti ļauj uzņēmumiem izsekot izmaksas, kas saistītas ar darbībām, par kurām klientam netiek izrakstīts rēķins. Iekšējo projektu piemēri ir šādi:

- Projekta, piemēram, mobilās programmas, izstrāde un izmaksu izsekošana saistībā ar izstrādi.
- Pirmspārdošanas laika un izdevumu pārvaldīšana. Šo pirmspārdošanas iekšējo projektu vēlāk var pārveidot par rēķinā iekļaujamu projektu, ja piedāvājums tiek iegūts.

Jebkurš projekts, kas nav saistīts ar līgumu, Dynamics 365 Project Operations tiek uzskatīts par iekšēju. Projekta izmaksu un ieņēmumu profili netiek izmantoti, lai noteiktu projekta uzskaites kārtulas. Iekšējās projekta izmaksas vienmēr tiek grāmatotas, izmantojot peļņas un zaudējumu principus. Grāmatojumu virsgrāmatas konti tiek definēti lapā **Virsgrāmatas publicēšanas iestatījumi**.

- Laika darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **algu sadalījuma** kontu.
- Izdevumu darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **ieskaita kontu izdevumiem**.
- Vienību transakcijas tiek grāmatotas, veicot konta **Izmaksas** debetēšanu un konta **Izmaksas — vienība** kreditēšanu.

Pēc darbību grāmatošanas projektā, ja projekts ir saistīts ar projekta līgumu, sistēma atceļ visus uzkrātos darījumus un izveido jaunus rēķinā iekļaujamus darījumus. Rēķinā iekļautie darījumi ievēro uzskaites kārtulas, kas definētas atbilstošajā projekta izmaksu un ieņēmumu profilā.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
