---
title: Materiālu finanšu aprēķini projektiem
description: Šajā tēmā ir sniegta informācija par projekta materiālu definēšanu vai aprēķiniem.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1717abb8f37acb7ab5f4e24b9323b3d958b40b13d7da44c0bbfa88eea28b99ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992620"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Materiālu finanšu aprēķini projektiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations projekta vadītājiem ļauj definēt projekta materiālu izmaksas katram projektam vai uzdevumam. Katru materiālu aprēķinu var saistīt ar konkrētu projekta uzdevumu. Izmaksas tiek kategorizētas dažādās izmaksu kategorijās, kas tiek definētas organizācijas līmenī. Cenu noteikšana un izmaksu noteikšana katrai izmaksu kategorijai tiek definēts cenrādis. 

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
