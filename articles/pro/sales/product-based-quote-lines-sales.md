---
title: Produkta piedāvājuma rindas pārskats — Lite
description: Šajā tēmā ir sniegta informācija par darbu ar produkta piedāvājuma rindām.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369835"
---
# <a name="product-based-quote-lines-overview---lite"></a>Produkta piedāvājuma rindas pārskats — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Programmā Dynamics 365 Project Operations varat izveidot uz produktu balstītas piedāvājuma rindas. Uz produktu balstītas piedāvājuma rindas var būt manuāli pievienotas, vai tās var būt vienumi no produkti kataloga.

## <a name="product-catalog"></a>Preču katalogs

Katram produktam produktu katalogā ir noklusējuma vienība un vienību grupa. Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai kopīgi šie atribūti. 

Piemēram, uzņēmums pārdod abonementa licences dažādu veidu programmatūrai. Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.

- Lietotāju skaits
- Abonementa ilgums mēnešos

Lai uzturētu šāda tipa katalogu, izveidojiet produktu saimi, kuras nosaukums ir **Abonējama programmatūra**, un kā atribūtus pievienojiet lietotāju skaitu un abonementa ilgumu. Pēc tam varat pievienot atsevišķus produktus produktu saimei **Abonējama programmatūra**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Produktu kataloga vienumu pievienošana projekta piedāvājumam

Lapās **Projekta piedāvājums** un **Projekta līgums** ir sadaļas, kas paredzētas uz projektu balstītām rindām un uz produktu balstītām rindām. Attiecībā uz produkta rindām — piedāvājuma rindas vai projekta līguma rindas nolaižamajā sarakstā ir iekļauti visi produkti un vienības attiecīgajā produktu cenrādī. Varat arī pievienot produktus, kas neveido daļu no produktu cenrāža.

Turklāt varat atlasīt produktus no citiem cenrāžiem vai tieši no produktu kataloga. Ja produktus atlasāt tieši no kāda produktu kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis. Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz nulli (0).

Kad piedāvājuma rinda ir balstīta uz produktu katalogu, pārdošanas cenu varat pārlabot tieši piedāvājuma rindā. Piedāvājuma rinda laukā **Cenu noteikšana** ar divām pieejamām vērtībām:

- **Pārlabot izcenojumu**
- **Izmantot noklusējumu**

Ja atlasāt **Pārlabot izcenojumu**, noklusējuma cena netiek iestatīta. Tā vietā jums ir jāievada cena šim produktam piedāvājuma rindā. Ja atlasāt opciju **Lietot noklusējumu**, tiek izmantota noklusējuma pārdošanas cena, kā arī lauks ir slēgts rediģēšanai.

Piedāvājuma produktu rindās tiek ievadītas noklusējuma pārdošanas cenas. Pēc tam lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot izcenojumu**, lai jūs varētu rediģēt noteiktā cenu piedāvājuma rindās. Šī ir risinājumam Project Operations specifiska pārlabošana uz produkta rindu uzvedību programmā Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]