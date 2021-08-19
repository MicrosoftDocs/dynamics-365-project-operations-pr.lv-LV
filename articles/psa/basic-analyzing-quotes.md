---
title: Projekta piedāvājumu analīze
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu analīzi.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b50f419d2c13cff4914f4b589c8d7ad9099c8734834d75f8d17104d2db40049b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002835"
---
# <a name="analysis-of-project-quotes"></a>Projekta piedāvājumu analīze

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizē projekta piedāvājumus, lai novērtētu ienesīgumu. Programma analizē arī to, cik labi piedāvājums atbilst klienta vēlmēm attiecībā uz piegādes datumu vai izpildes datumu, kā arī budžetu.

## <a name="profitability-analysis"></a>Ienesīguma analīze

Project Service Automation analizē ienesīgumu, izmantojot bruto peļņu un koriģēto bruto peļņu.

- Bruto peļņas tiek aprēķinātas, izmantojot tālāk norādīto formulu.

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Koriģētā bruto peļņa tiek aprēķināta, izmantojot tālāk norādīto formulu.

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Ja bruto peļņas un koriģētās bruto peļņas vērtības ievērojami atšķiras, liela daļa darba piedāvājumā ir klasificēta kā rēķinā neiekļaujama.

## <a name="analysis-of-customer-expectations"></a>Klientu vēlmju analīze

Varat analizēt piedāvājumus un ģenerēt klientu vēlmju diagrammas attiecībā uz grafiku un budžetu, ja tālāk esošajos laukos ievadāt vērtības.

- Lauks **Pieprasītais piegādes datums** piedāvājuma virsrakstā.
- Katras piedāvājuma rindas lauks **Klienta budžets** (uz projektu balstītām rindām un uz preci balstītām rindām).

Klienta vēlmju analīze par grafiku tiek veikta, salīdzinot piedāvājuma rindu detaļu vēlāko beigu datumu ar pieprasīto piegādes datumu visās piedāvājuma rindās.

Klienta vēlmju analīze par budžetu tiek veikta, salīdzinot klienta kopējā budžeta summu ar piedāvāto summu visās piedāvājuma rindās.


[!INCLUDE[footer-include](../includes/footer-banner.md)]