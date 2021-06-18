---
title: Kopsavilkuma informācija par projekta piedāvājumu — Lite
description: Šajā tēmā ir sniegta informācija par iestatījumiem un informāciju, kas attiecas uz projekta piedāvājumiem un ietekmē tos. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad549513c70ccf935e4dfdc17123be09ad737c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994325"
---
# <a name="header-details-for-project-quotes"></a>Projektu piedāvājumu virsraksta informācija

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā izskaidrota informācija, kas attiecas uz projekta piedāvājumu. Tajā ir iekļauti iestatījumi, kas ietekmē visas piedāvājuma rindas, un informācija par piedāvājumu, kas ir apkopota visos rindas vienumos, lai vadītu projekta piedāvājuma KPI.

Nākamajā tabulā ir uzskaitīti kopsavilkuma informācijas lauki projekta piedāvājumam, kas ir unikāli vai kam ir dažas svarīgas darbības izmaiņas Dynamics 365 Project Operations Dynamics 365 Sales piedāvājumos.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Veidi | Kopsavilkuma cilne (slēpta) | Šajā opciju kopas laukā ir tālāk norādītās opcijas.</br>- Balstīts uz darbu (pieejams tikai tad, ja ir instalēts Project Operations)</br>- Balstīts uz vienumu (pieejams tikai tad, ja ir instalēts Project Operations un Sales)</br>- Opcijas, kuru pamatā ir servisa uzturēšana (pieejama, ja ir instalēts risinājums Dynamics 365 Field Service) | Ja izmantojat lietojumprogrammu Project Operations, šī lauka vērtība automātiski tiek uzstādīta uz **Balstīts uz darbu**. Šādi piedāvājums tiek klasificēts kā projekta piedāvājums. Piedāvājumam ir jābūt projekta piedāvājumam, lai iespējotu visus projektam specifiskos paplašinājumus un funkcionalitāti. |
| Potenciāls klients | Kopsavilkuma cilne | Atsauce uz klienta uzņēmuma vai konta ierakstu. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Projekta piedāvājuma valūta tiek iestatīta pēc noklusējuma, pamatojoties uz klienta valūtu. Tomēr to var mainīt, pirms piedāvājums ir saglabāts. |
| Konta pārvaldnieks | Kopsavilkuma cilne | Šī darījuma konta pārvaldnieka vārds. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Konta pārvaldnieks ir atbildīgs par attiecību ar klientu pārvaldīšanu līdz projekta pabeigšanai. Pamatojoties uz rezervējamā resursa ierakstu, kas saistīts ar konta pārvaldnieku, līgumslēdzēja vienība pēc noklusējuma balstās uz projekta piedāvājumu. |
| Līgumslēdzēja vienība | Kopsavilkuma cilne | Organizācijas struktūrvienība, kas ir atbildīga par projekta vai ar šo piedāvājumu saistīto projektu īstenošanu. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpilda projektus pēc darījuma slēgšanas. Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta izpildes laikā radušās prognozētās un faktiskās izmaksas. |
| Produktu cenrādis | Kopsavilkuma cilne | Šis ir cenrādis, ko izmanto cenu noteikšanai pēc noklusējuma produktu piedāvājumu rindās. Šī lauka opciju sarakstā ir redzams saraksts ar cenrāžiem, kur cenrāža valūta atbilst piedāvājuma valūtai. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. Šis iespējas lauks pēc noklusējuma tiek ņemts no uzņēmuma ieraksta, bet to var mainīt. | Kad piedāvājums ir iegūts, lauka vērtība tiek pārkopēta uz izveidoto projekta līguma rindu. |
| Valūta | Kopsavilkuma cilne | Tas norāda valūtu, kas tiks izmantota, lai ziņotu šī darījuma vērtību. Tā ir arī valūta, kurā klientam tiek izrakstīts rēķins, ja darījums tiek iegūts. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. Šis iespējas lauks pēc noklusējuma tiek ņemts no uzņēmuma ieraksta, bet lietotājs to var mainīt. | Pēc tam, kad piedāvājums ir saglabāts, šis lauks vairs nav rediģējams. To izmanto, lai iestatītu produkta un projekta cenrāžus kā noklusējumu piedāvājumā. Tiek izmantota tāda piedāvājuma valūta, kas atbilst cenrāža valūtai. |
| Nepārsniedzamais ierobežojums | Kopsavilkuma cilne | Tas norāda norunāto gala vērtības maksimālo robežvērtību, kam klients piekrīt šī darījuma ietvaros. | Šī maksimālā robežvērtība tiek aplēsta izpildes laikā un ir piemērojama visiem rindu vienumiem un projektiem, kas saistīti ar šo darījumu. |
| Pieprasītais piegādes datums | Kopsavilkuma cilne | Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Šis datums tiek lietots kā rēķinu ģenerēšanas grafiku beigu datums. |

Tālāk ir norādītas cilnes un KPI, kas ir pieejami projekta piedāvājumā un ir unikālas risinājumā Project Operations vai kam ir dažas būtiskas darbības izmaiņas, salīdzinājumā ar piedāvājumiem programmā Sales.

| **Lauks** | **Atrašanās vieta** | **Apraksts** |
| --- | --- | --- |
| Ienesīguma analīze | Cilne piedāvājumā | Cilnē ir redzamas šādas metrikas:</br>- Kopējās rēķinā iekļaujamās izmaksas</br></br>- Kopējās rēķinā neiekļaujamās izmaksas</br>- Kopējie ieņēmumi</br>- Kopējie ieņēmumi (pamatvalūtā)</br>- Bruto peļņa</br>- Koriģētā bruto peļņa|
| Salīdzinājums ar klienta vēlmju robežām | Cilne piedāvājumā | Šajā cilnē ir redzamas šādas metrikas:</br>- Prognozējamā pabeigšana</br>- Pieprasītā pabeigšana</br>- Klienta budžets</br>- Piedāvātā vērtība |
| Piedāvājuma analīze | Cilne piedāvājumā | Šajā cilnē ir apkopota informācija par projekta piedāvājuma galvenajiem KPI</br>- Salīdzinājumā ar klientu vēlmēm attiecībā uz budžetu un grafiku</br>- Bruto peļņa</br>- Koriģētā bruto peļņa |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
