---
title: Konfigurēt iekšējo projektu uzskaiti
description: Šajā rakstā ir sniegta informācija par to, kā iestatīt uzskaites metodes Project Operations iekšējiem projektiem.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919471"
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
