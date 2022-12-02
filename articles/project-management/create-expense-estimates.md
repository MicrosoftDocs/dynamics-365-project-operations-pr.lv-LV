---
title: Izdevumu finanšu aprēķini projektiem
description: Šajā rakstā ir sniegta informācija par to, kā definēt vai aprēķināt projekta izdevumus.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a29244a65dd88d3ba0f8333a63627bb0c068273
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925703"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Izdevumu finanšu aprēķini projektiem
_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations projekta vadītājiem ļauj definēt projekta izmaksas katram projektam vai uzdevumam. Katru izmaksu elementu var saistīt ar konkrētu projekta uzdevumu. Izmaksas tiek kategorizētas dažādās izmaksu kategorijās, kas tiek definētas organizācijas līmenī. Cenu noteikšana un izmaksu noteikšana katrai izmaksu kategorijai tiek definēts cenrādis. 

Lai apskatītu, pievienotu vai dzēstu projekta izdevumus, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz sadaļu **Projekti** un atlasiet projektu, ar kuru vēlaties strādāt.
2. Atlasiet cilni **Projekta aprēķini** un skatiet projekta izmaksu sarakstu.
3. Atlasiet **Jauni izdevumi**, lai pievienotu izdevumus. Varat arī atlasīt izmaksas, ko vēlaties dzēst, un pēc tam atlasīt vienumu **Dzēst izdevumus**.

Tālāk sniegtajā tabulā ir informācija par projekta rindas **Izdevumu aprēķins** laukiem. 

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Uzdevums | Projekta uzdevumu saraksts. Tas ietver kopsavilkuma un lapas mezgla uzdevumus. | Atlasot uzdevumu izdevumu novērtējuma rindai, uzdevumam tiks ietekmēti prognozētie izdevumi un prognozētie pārdošanas izdevumi. Ja šis lauks tiek atstāts tukšs, izmaksu aprēķins tiek izsekots un apkopots tikai projekta līmenī. |
| Kategorija | Transakciju kategoriju saraksts, kurām lietojumprogrammā ir piesaistītas izmaksu kategorijas. | Atlasot kategoriju, izmaksu tāmes rindā tiek vadīta cenu noteikšana un izmaksu noteikšana. |
| Sākuma datums | Prognozētais izmaksu sākuma datums. | Šim laukam nav lejupstraumes ietekmes. |
| Vienību grupa | Šī lauka noklusējuma vērtība tiek ņemta no vienību grupas, kas ir iestatīta kā noklusējums atlasītajai kategorijai. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Šim laukam nav lejupstraumes ietekmes. |
| Vienība | Šī lauka noklusējuma vērtība ir atlasītās kategorijas noklusējuma vienība. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Mainot vienību, tiek parādīts atšķirīga noklusējuma vienības cena un izmaksas. |
| Daudzums | Prognozējamo izdevumu apjoms. | Šim laukam nav lejupstraumes ietekmes. |
| Vienības izmaksas | Atlasītās kategorijas un vienības izmaksu kombinācija, kā tas ir iestatīts piemērojamajam izmaksu cenrādim. | Vienības izmaksas vienmēr tiek parādītas projekta izmaksu valūtā. |
| Vienības cena | Atlasītās kategorijas un vienības cenu kombinācija, kā tas ir iestatīts piemērojamajam pārdošanas cenrādim. | Vienības cena vienmēr tiek parādīta projekta pārdošanas valūtā. |
| Kopējās izmaksas | Izmaksu summa, kas tiek aprēķināta kā daudzuma \*vienības izmaksas.| Izmaksu summa vienmēr tiek parādīta projekta izmaksu valūtā. |
| Kopējie pārdošanas rādītāji | Pārdošanas summa, kas tiek aprēķināta kā daudzuma \*vienības cena. | Pārdošanas summa vienmēr tiek parādīta projekta pārdošanas valūtā. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
