---
title: Kopsavilkuma informācija par projekta piedāvājumu
description: Šajā tēmā ir sniegta informācija par iestatījumiem un informāciju, kas attiecas uz projekta piedāvājumiem un ietekmē tos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde5305f179e9a4454bf97c44f1ebdf9986dd43
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908355"
---
# <a name="summary-information-on-a-project-quote"></a>Kopsavilkuma informācija par projekta piedāvājumu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Šajā rakstā izskaidrota informācija, kas attiecas uz projekta piedāvājumu. Tajā ir iekļauti iestatījumi, kas ietekmē visas piedāvājuma rindas, un informācija par piedāvājumu, kas ir apkopota visos rindas vienumos, lai vadītu projekta piedāvājuma KPI.

Tālāk sniegtajā tabulā ir uzskaitīti tie kopsavilkuma informācijas lauki projekta piedāvājumā, kas ir unikāli Dynamics 365 Project Operations vai kuriem ir dažas būtiskas izmaiņas darbībā atšķirībā no Dynamics 365 Sales piedāvājumiem.

| **Lauks** | **Atrašanās vieta** | **Atbilstība, mērķis un norādes** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Veidi | Kopsavilkuma cilne (slēpta) | Šajā opciju kopas laukā ir tālāk norādītās opcijas.</br>- Balstīts uz darbu (pieejams tikai tad, ja ir instalēts Project Operations)</br>- Balstīts uz vienumu (pieejams tikai tad, ja ir instalēts Project Operations un Sales)</br>- Opcijas, kuru pamatā ir servisa uzturēšana (pieejama, ja ir instalēts risinājums Dynamics 365 Field Service) | Ja izmantojat lietojumprogrammu Project Operations, šī lauka vērtība automātiski tiek uzstādīta uz **Balstīts uz darbu**. Šādi piedāvājums tiek klasificēts kā projekta piedāvājums. Piedāvājumam ir jābūt projekta piedāvājumam, lai iespējotu visus projektam specifiskos paplašinājumus un funkcionalitāti. |
| Atbildīgais uzņēmums | Kopsavilkums | Juridiskā persona, kas uzskaitīs izmaksas un ieņēmumus, kas uzkrājas no šī projekta vai projektiem, kas saistīti ar šo piedāvājumu. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Atbildīgais uzņēmums ir pielīdzināms juridiskās personas jēdzienam Project Operations modulī **Projekta pārvaldība un grāmatvedība**. Visas izmaksas un ieņēmumi, kas uzkrājušies no šī projekta, tiks ieskaitīti atbildīgā uzņēmuma virsgrāmatā. |
| Potenciāls klients | Kopsavilkuma cilne | Atsauce uz klienta uzņēmuma vai konta ierakstu. Projekta piedāvājumā atsaucei ir jāiestata derīgs klients kā klients piedāvājuma atbildīgajā uzņēmumā. Atbildīgais uzņēmums parāda sarakstu ar juridiskajām personām, un tās ir iestatītas Project Operations modulī **Projekta pārvaldība un grāmatvedība**. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Projekta piedāvājuma valūta tiek iestatīta pēc noklusējuma, pamatojoties uz klienta valūtu. Tomēr to var mainīt, pirms piedāvājums ir saglabāts. |
| Konta pārvaldnieks | Kopsavilkuma cilne | Šī darījuma konta pārvaldnieka vārds. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Konta pārvaldnieks ir atbildīgs par attiecību ar klientu pārvaldīšanu līdz projekta pabeigšanai. Pamatojoties uz rezervējamā resursa ierakstu, kas saistīts ar konta pārvaldnieku, līgumslēdzēja vienība pēc noklusējuma balstās uz projekta piedāvājumu.|
| Līgumslēdzēja vienība | Kopsavilkuma cilne | Organizācijas struktūrvienība, kas ir atbildīga par projekta vai ar šo piedāvājumu saistīto projektu īstenošanu. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpilda projektus pēc darījuma slēgšanas. Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta izpildes laikā radušās prognozētās un faktiskās izmaksas. |
| Produktu cenrādis | Kopsavilkuma cilne | Šis ir cenrādis, ko izmanto cenu noteikšanai pēc noklusējuma produktu piedāvājumu rindās. Šī lauka opciju sarakstā ir redzams saraksts ar cenrāžiem, kur cenrāža valūta atbilst piedāvājuma valūtai. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. Šis iespējas lauks pēc noklusējuma tiek ņemts no uzņēmuma ieraksta, bet to var mainīt. | Kad piedāvājums ir iegūts, lauka vērtība tiek pārkopēta uz izveidoto projekta līguma rindu. |
| Valūta | Kopsavilkuma cilne | Tas norāda valūtu, kas tiks izmantota, lai ziņotu šī darījuma vērtību. Tā ir arī valūta, kurā klientam tiek izrakstīts rēķins, ja darījums tiek iegūts. Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. Šis iespējas lauks pēc noklusējuma tiek ņemts no uzņēmuma ieraksta, bet lietotājs to var mainīt.  | Pēc tam, kad piedāvājums ir saglabāts, šis lauks vairs nav rediģējams. To izmanto, lai iestatītu produkta un projekta cenrāžus kā noklusējumu piedāvājumā. Tiek izmantota tāda piedāvājuma valūta, kas atbilst cenrāža valūtai. |
| Nepārsniedzamais ierobežojums | Kopsavilkuma cilne | Tas norāda norunāto gala vērtības maksimālo robežvērtību, kam klients piekrīt šī darījuma ietvaros. | Šī maksimālā robežvērtība tiek aplēsta izpildes laikā un ir piemērojama visiem rindu vienumiem un projektiem, kas saistīti ar šo darījumu. |
| Pieprasītais piegādes datums | Kopsavilkuma cilne | Ja piedāvājums ir izveidots no iespējas, šis lauks tiek kopēts no atbilstošā iespējas lauka. | Šis datums tiek lietots kā rēķinu ģenerēšanas grafiku beigu datums. |

Tālāk ir norādītas cilnes un KPI, kas ir pieejami projekta piedāvājumā un ir unikālas risinājumā Project Operations vai kam ir dažas būtiskas darbības izmaiņas, salīdzinājumā ar piedāvājumiem programmā Sales.

| **Lauks** | **Atrašanās vieta** | **Atbilstība, mērķis un norādes** |
| --- | --- | --- |
| Ienesīguma analīze | Cilne piedāvājumā | Cilnē ir redzamas šādas metrikas:</br>- Kopējās rēķinā iekļaujamās izmaksas</br></br>- Kopējās rēķinā neiekļaujamās izmaksas</br>- Kopējie ieņēmumi</br>- Kopējie ieņēmumi (pamatvalūtā)</br>- Bruto peļņa</br>- Koriģētā bruto peļņa|
| Salīdzinājums ar klienta vēlmju robežām | Cilne piedāvājumā | Šajā cilnē ir redzamas šādas metrikas:</br>- Prognozējamā pabeigšana</br>- Pieprasītā pabeigšana</br>- Klienta budžets</br>- Piedāvātā vērtība |
| Piedāvājuma analīze | Cilne piedāvājumā | Šajā cilnē ir apkopota informācija par projekta piedāvājuma galvenajiem KPI</br>- Salīdzinājumā ar klientu vēlmēm attiecībā uz budžetu un grafiku</br>- Bruto peļņa</br>- Koriģētā bruto peļņa |
