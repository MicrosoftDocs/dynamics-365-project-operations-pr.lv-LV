---
title: Projektu līgumu virsraksta informācija
description: Šajā rakstā ir sniegta informācija par laukiem un informāciju par projektu līgumiem programmā Project Operations.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f648113f54257e2c303cb2729e282d70f818d838
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824918"
---
# <a name="header-details-for-project-contracts"></a>Projektu līgumu virsraksta informācija

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts sniedz informāciju par laukiem, kas attiecas uz visu projekta līgumu, ieskaitot iestatījumus, kas ietekmē visas līguma rindas. Ir iekļauta arī informācija par līgumu, kas ir apkopota visos projekta līguma apakšpunktos, lai vadītu KPI.

Nākamajā tabulā ir uzskaitīti līguma lauki projekta piedāvājumam, kas ir unikāli Dynamics 365 Project Operations vai kam ir dažas svarīgas darbības izmaiņas Dynamics 365 Sales pārdošanas līgumos.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Veidi | **Kopsavilkuma** cilne (paslēpta) | Šis ir opciju kopas lauks ar šādām opcijām:</br>- **Balstīts uz darbu** (pieejama tikai tad, ja ir instalēts Project Operations)</br>- **Balstīts uz vienumu** (pieejama tikai tad, ja ir instalēts Project Operations un Sales)</br>- **Balstīts uz pakalpojuma uzturēšanu** (pieejama, ja ir instalēts Dynamics 365 Field Service) | Projekta operācijās šī lauka vērtība noklusējumā ir **Balstīts uz darbu**, un līgums tiek klasificēts kā projekta līgums. Līgumam ir jābūt uz projektu balstītam, lai iespējotu visus projektam specifiskos paplašinājumus un funkcionalitāti. |
| Potenciāls klients | Cilne **Kopsavilkums** | Atsauce uz klienta uzņēmuma vai konta ierakstu. Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka. | Projekta līguma noklusējuma valūta, pamatojoties uz klienta valūtu. To var mainīt, pirms līgums ir saglabāts. |
| Konta pārvaldnieks | Cilne **Kopsavilkums** | Šī darījuma konta pārvaldnieka vārds. Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka. | Konta pārvaldnieks ir atbildīgs par attiecību ar klientu pārvaldīšanu līdz projekta pabeigšanai. Pamatojoties uz grāmatojamo resursu ierakstu, kas saistīts ar konta pārvaldnieku, līguma vienība neizpilda projekta līguma saistības. |
| Līgumslēdzēja vienība | Cilne **Kopsavilkums** | Organizācijas vienība, kas atbild par ar šo līgumu saistīto projektu nodrošināšanu. Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka. | Līgumslēdzēja struktūrvienība ir tā uzņēmuma nodaļa, kas izpilda projektus. Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas. |
| Produktu cenrādis | Cilne **Kopsavilkums** | Šis cenrādis tiek izmantots noklusētajām cenām uz produktu balstītās līgumu rindās. Nolaižamo opciju saraksts šim laukam rāda cenrādi sarakstu, kurā cenrāža valūta atbilst līgumā norādītajai valūtai. Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka. Projekta līgumā šis lauks ir noklusēts no konta ieraksta, bet to var mainīt. | Šai jomai nav nekādas pakārtotas atbilstības. |
| Valūta | Cilne **Kopsavilkums** | Valūta, kas izmantota, lai uzrādītu šī darījuma vērtību, un valūta, kurā klientam tiks izrakstīts rēķins. Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka. Projekta līgumā šis lauks ir noklusējums no konta ieraksta, bet to var mainīt. | Pēc tam, kad līgums ir saglabāts, šis lauks vairs nav rediģējams. Šo lauku izmanto, lai iestatītu produkta un projekta cenrāžus kā noklusējumu līgumā. Tiek izmantota tāda līguma valūta, kas atbilst cenrāža valūtai. |
| Nepārsniedzamais ierobežojums | Cilne **Kopsavilkums** | Šis lauks norāda norunāto gala vērtības maksimālo robežvērtību, kam klients ir piekritis šī darījuma ietvaros. | Maksimālā robežvērtība tiek aplēsta izpildes laikā un ir piemērojama visiem rindu vienumiem un projektiem, kas saistīti ar šo darījumu. |
| Pieprasītais piegādes datums | Cilne **Kopsavilkums** | Veidojot līgumu no projekta piedāvājuma, šis lauks tiek kopēts no projekta piedāvājuma atbilstošā lauka. | Šis datums tiek lietots kā rēķinu ģenerēšanas grafiku beigu datums. |

Projekta līguma cilnē **Līguma veiktspēja** ir pieejami šādi KPI: 

>[!NOTE]
>Visas summas cilnē **Līguma izpilde** ir izteiktas vides noklusējuma valūtā.

| Kolonna | Atrašanās vieta | Apraksts |
| --- | --- | --- |
| Līguma vērtība | Kopējais līgums | Projekta līguma kopējā vērtība.|
| Rēķinā norādītā summa | Kopējais līgums | Visu to rēķinu vērtību summa, kas ir atbilstoši šim līgumam.|
| Radušās izmaksas | Kopējais līgums | Visu to izmaksu faktisko datu summa, kas pieteiktas visos projektos, kuri ir kartēti uz līgumu. |
| Bruto peļņa | Kopējais līgums | Samaksātā summa — izmaksas, kas nav saistītas ar datumu/rēķinu summu |
| Paredzamā peļņa | Kopējais līgums | (Līguma vērtība — prognozētās izmaksas)/līguma valueEstimated izmaksas = visu paredzamo izmaksu summa, kas ir kartētas uz šo līgumu.|
| Līguma vērtība | Projektu līnijas | Līguma rindas vērtība. |
| Rēķinā norādītā summa | Projektu līnijas | Fiksētas cenas līguma rindai: kopsumma visiem rēķinu pārdošanas atskaites punktu faktiskaijiem datiem attiecībā pret šo līguma rindu dažādiem rēķiniem, kas izveidoti šim līgumam. Laika un materiālu līguma rindai: summa no visām apmaksājamām pārdošanas izmaksām šajā līguma rindā dažādos rēķinos, kas izveidoti šim līgumam. |
| Radušās izmaksas | Projektu līnijas | Visu to izmaksu faktisko datu summa, kas pieteiktas visos projektos, kuri ir kartēti uz līgumu. |
| Bruto peļņa | Projektu līnijas | (Samaksātā summa — izmaksas, kas nav saistītas ar datumu) / rēķinu summu |
| Paredzamā peļņa | Projektu līnijas | (Līguma rindas summa bāzes valūtā — līguma rindas prognozējamās izmaksas pamatvalūtā) / līguma rindu summa pamatvalūtā |
| Radušās izmaksas | Projekta rindas detalizētā informācija | Laiks: summa, kas ierakstīta izmaksu faktiskajā attiecībā uz šo lomu projektā, kas kartēts uz līguma rindu. Izmaksas: summa no visiem izmaksu izmaksu faktiskaijiem datiem, kas reģistrēti šai kategorijai projektā, kas kartēts uz līguma rindu. |
| Reģistrētais daudzums | Projekta rindas detalizētā informācija | Laiks: summa, kas ierakstīta izmaksu faktiskajā attiecībā uz šo lomu projektā, kas kartēts uz līguma rindu. Izmaksas: visi šīs izdevumu kategorijas daudzumi uz projekta izdevumu izmaksu aktuāļiem ir kartēti uz šo līguma rindu. |
| Rēķinā norādītā summa | Projekta rindas detalizētā informācija | Fiksētas cenas līguma rindai šis lauks tiek atstāts tukšs detalizācijas līmenī un ir redzams tikai līguma rindu līmenī. Attiecībā uz laika un materiālu līguma rindu aprēķini tiek pabeigti detalizētās informācijas līmenī. Detalizētā informācija rāda summu, kas attiecas uz visām rēķina ieņēmumu rindām atbilstoši šai līguma rindai, par kuru ir jāmaksā. |
| Rēķinā norādītais daudzums | Projekta rindas detalizētā informācija | Fiksētas cenas līguma rindai šis lauks tiek atstāts tukšs detalizācijas līmenī un ir redzams tikai līguma rindu līmenī. Laika un materiālu līguma rindai aprēķini tiek veikti detalizētas informācijas līmenī par laiku un izdevumiem. Laiks: stundu summa visās šīs lomas rēķinā norādītajās ieņēmumu pozīcijās attiecībā pret šo līguma rindu, kas ir apmaksājama. Izmaksas: visi šīs izdevumu kategorijas daudzumi uz projekta izdevumu izmaksu aktuāļiem ir kartēti uz šo līguma rindu. |
| Līguma vērtība | Produktu līnijas | Šīs uz produktu balstītās līguma rindas vērtība. |
| Rēķinā norādītā summa | Produktu līnijas | Summa visās rēķina rindās šajā uz produktu balstītajā līguma rindā dažādos rēķinos, kas izveidoti šim līgumam. |
| Radušās izmaksas | Produktu līnijas | Visu uz produktu balstītajā līguma rindā reģistrēto izmaksu faktisko datu summa. |
| Bruto peļņa | Projektu līnijas | Samaksātā summa — izmaksas, kas nav saistītas ar datumu/rēķinu summu |
| Paredzamā peļņa | Produktu līnijas | (Līguma rindas vērtība — līguma rindas prognozējamās izmaksas) / līguma rindas vērtība |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
