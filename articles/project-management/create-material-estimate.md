---
title: Materiālu finanšu aprēķini projektiem
description: Šajā rakstā sniegta informācija par projektu materiālu definēšanu vai aplēšanu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925711"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Materiālu finanšu aprēķini projektiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations projekta vadītājiem ļauj definēt projekta materiālu izmaksas katram projektam vai uzdevumam. Katru materiālu aprēķinu var saistīt ar konkrētu projekta uzdevumu. Projektos izmantotie materiāli var būt rakstāmie produkti vai produkti no preču kataloga. Katrai produkta un vienības kombinācijai cenu var definēt projekta pārdošanas cenrāžos un projekta izmaksu cenrāžos.  

Lai skatītu, pievienotu vai dzēstu projekta materiālu aprēķinu, veiciet tālāk norādītās darbības.

1. Atveriet **Projekti** un atlasiet projektu, kuru vēlaties atjaunināt.
2. Cilnē **Materiālu aprēķini** skatiet projekta materiālu aprēķinu sarakstu.
3. Atlasiet **Jauns materiālu aprēķins**, lai izveidotu jaunu materiālu aprēķinu. Vai atlasiet materiālu aprēķinu, ko dzēst, un pēc tam atlasiet **Dzēst materiālu aprēķinu**.

Tālāk sniegtajā tabulā ir informācija par projekta rindas **Materiālu aprēķina rinda** laukiem. 

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Uzdevums | Projekta uzdevumu saraksts. Tas ietver kopsavilkuma un lapas mezgla uzdevumus. | Atlasot uzdevumu materiālu aprēķinu rindai, tiek ietekmētas uzdevuma prognozētās materiālu izmaksas un prognozētie materiālie pārdošanas apjomi. Ja šis lauks ir tukšs, materiālu aprēķins tiek izsekots un apkopots tikai projekta līmenī. |
| Atlasīt produktu |  Varat norādīt, vai šī aprēķina rinda ir esošam (kataloga) produktam vai ierakstāmam produktam. | Šis lauks nosaka, vai kataloga produkts ir atlasīts vai ierakstāms. |
| Produkts | Produkta ID no produktu kataloga. Kad atlasāt produkta ID, lauka **Atlasīt produktu** vērtība automātiski tiek atjaunināta uz **Esošs produkts**. ID tiek izmantots, lai no cenrāža izgūtu izmaksu un pārdošanas cenas. | Šim laukam nav lejupstraumes ietekmes. |
| Ierakstāmā produkta apraksts | Teksta lauks, ko rakstīt produkta nosaukumā. Šis lauks ir jāizmanto, ja laukam **Atlasīt produktu** tiek atlasīts **Ierakstāms**.| Šim laukam nav lejupstraumes ietekmes. |
| Sākuma datums | Paredzamais datums, kurā materiāli tiks izmantoti. | Šim laukam nav lejupstraumes ietekmes. |
| Vienību grupa | Šī lauka noklusējuma vērtība tiek ņemta no noklusējuma vienību grupas kataloga produktam. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Šim laukam nav lejupstraumes ietekmes. |
| Vienība | Šī lauka vērtība ir atlasītā produkta noklusējuma vienība. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Mainot vienību, tiek parādīts atšķirīga noklusējuma vienības cena un izmaksas. |
| Daudzums | Projektā izmantojamais produkta prognozētais daudzums. | Šim laukam nav lejupstraumes ietekmes. |
| Vienības izmaksas | Atlasītā produkta vienības izmaksas un vienību kombinācija, kā tas ir iestatīts piemērojamajam izmaksu cenrādim. | Vienības izmaksas vienmēr tiek parādītas projekta izmaksu valūtā. Ja cenrāža produktam un vienības iestatījumiem cenrādī nav iestatītu vienības izmaksu, vienības izmaksas pēc noklusējuma būs 0,00. |
| Vienības cena | Atlasītā produkta un vienības cenu kombinācija, kā tas ir iestatīts piemērojamajam pārdošanas cenrādim. | Vienības cena vienmēr tiek parādīta projekta pārdošanas valūtā. Ja cenrāža produktam un vienības iestatījumiem cenrādī nav iestatītu vienības cenu, vienības cena pēc noklusējuma būs 0,00.|
| Kopējās izmaksas | Izmaksu summa, kas tiek aprēķināta kā daudzuma \*vienības izmaksas.| Izmaksu summa vienmēr tiek parādīta projekta izmaksu valūtā. |
| Kopējie pārdošanas rādītāji | Pārdošanas summa, kas tiek aprēķināta kā daudzuma \*vienības cena. | Pārdošanas summa vienmēr tiek parādīta projekta pārdošanas valūtā. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
