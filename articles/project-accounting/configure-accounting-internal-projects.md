---
title: Konfigurēt iekšējo projektu uzskaiti
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt uzskaites metodes Project Operations iekšējiem projektiem.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287607"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurēt iekšējo projektu uzskaiti

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Iekšējie projekti ļauj uzņēmumiem izsekot izmaksas, kas saistītas ar darbībām, par kurām klientam netiek izrakstīts rēķins. Iekšējo projektu piemēri ir šādi:

- Projekta, piemēram, mobilās programmas, izstrāde un izmaksu izsekošana saistībā ar izstrādi.
- Pirmspārdošanas laika un izdevumu pārvaldīšana. Šo pirmspārdošanas iekšējo projektu vēlāk var pārveidot par rēķinā iekļaujamu projektu, ja piedāvājums tiek iegūts.

Jebkurš projekts, kas nav saistīts ar līgumu, Dynamics 365 Project Operations tiek uzskatīts par iekšēju. Projekta izmaksu un ieņēmumu profili netiek izmantoti, lai noteiktu projekta uzskaites kārtulas. Iekšējās projekta izmaksas vienmēr tiek grāmatotas, izmantojot peļņas un zaudējumu principus. Grāmatojumu virsgrāmatas konti tiek definēti lapā **Virsgrāmatas publicēšanas iestatījumi**.

- Laika darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **algu sadalījuma** kontu.
- Izdevumu darījumi tiek grāmatoti, debitējot **izmaksu** kontu un kreditējot **ieskaita kontu izdevumiem**.

Pēc darbību grāmatošanas projektā, ja projekts ir saistīts ar projekta līgumu, sistēma atceļ visus uzkrātos darījumus un izveido jaunus rēķinā iekļaujamus darījumus. Rēķinā iekļautie darījumi ievēro uzskaites kārtulas, kas definētas atbilstošajā projekta izmaksu un ieņēmumu profilā.




[!INCLUDE[footer-include](../includes/footer-banner.md)]