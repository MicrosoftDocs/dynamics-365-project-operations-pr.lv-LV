---
title: Produktu kataloga cenu noteikšana
description: Šajā tēmā ir sniegta informācija par to, kā programmatūrā Dynamics 365 Project Service Automation (PSA) darbojas produktu kataloga cenu noteikšana.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 59e05a55d41573b96785a2f41a7d5d822f6b515fb55edddea5ef1862b7694a1b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000180"
---
# <a name="product-catalog-pricing"></a>Produktu kataloga cenu noteikšana 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Cenrāžu un cenrāža elementu entītijas atbalsta produktu kataloga cenu noteikšanu. Vairumā gadījumu šī funkcionalitāte tiek izmantota uz katalogu balstītām rindām projektu piedāvājumos un projektu līgumos.

Uz projektu balstītām rindām pēc darījuma iegūšanas šo darījumu apzīmē līgums. Tā kā pirms darījuma iegūšanas parasti notiek pārrunu process, piedāvājumam pievienotais izcenojums vienmēr tiek kopēts uz jaunu cenrādi un pievienots šim līgumam. Šo jauno cenrādi nevar mainīt ārpus līguma darbības jomas. Šis ierobežojums palīdz aizsargāt likmju kartīti, par kuru tika panākta vienošanās, pret visām cenu izmaiņām, kas notiek galvenajā cenrādī.

Produkti ir jāiestata tā, lai produktu katalogā tiem būtu noklusējuma izmaksu un cenu saraksti. Šī saraksta cena, standarta izmaksas un pašreizējās izmaksas jums ir jāizmanto, lai konfigurētu noklusējuma izmaksas un saraksta cenas. Noklusējuma saraksta cenas piedāvājuma rindā vai projekta līguma rindā tiek izmantotas tikai tad, ja sistēma nevar atrast attiecīgā produkta cenrāža rindu piedāvājuma vai projekta līguma produktu cenrādī.

Produktu kataloga rindu izmaksu cenu starp piedāvājumiem var mainīt. Šī iespēja ir svarīga, jo, ja netiek veikta precīza izmaksu izsekošana, nevar noteikt operatīvo peļņu no projekta saistībām. Pēc noklusējuma kā izmaksu cena tiek izmantota produkta standarta cena. Taču piedāvājuma rindā noklusējuma izmaksu cenu var atjaunināt, ja šim piedāvājumam ir citāda izmaksu cena.

## <a name="price-list-items"></a>Cenrāža elementi

Produktus no produktu kataloga varat pievienot dažādiem cenrāžiem. Cenrāža rindas produktiem vienmēr atsaucas uz noteiktu vienību. Cenrāža elementos minēta produkta cenas noteikšanu var konfigurēt kā valūtas summu. Vai arī to var konfigurēt kā saraksta cenas, pašreizējo izmaksu vai standarta izmaksu funkciju.

PSA atbalsta dažādas noapaļošanas opcijas, kad cenas tiek konfigurētas kā saraksta cenas, standarta izmaksu vai pašreizējo izmaksu funkcija. Papildus vairāku cenu noteikšanas metožu un noapaļošanas opciju izmantošanai ir iespējams arī sasaistīt atlaižu sarakstus un cenrāža elementus. 

> ![Produktu no produktu kataloga pievienošana dažādiem cenrāžiem.](media/basic-guide-16.png)

Kad kādam piedāvājumam izveidojat jaunu pielāgotu cenrādi, lapā **Projekta piedāvājums** atlasot **Izveidot pielāgotu izcenojumu**, PSA izveido cenrāža kopiju un lauks **Entītija** jaunā cenrāža virsrakstā tiek iestatīts uz **Pārdošanas entītija**. Jaunā cenrāža nosaukumam tiek pievienots piedāvājuma nosaukums un laikspiedols. Jaunā cenrāža nosaukumu un piedāvājuma nosaukumu varat arī izmantot pielāgotās darbplūsmās, lai aktivizētu papildu pārskatīšanu un apstiprināšanu piedāvājumiem, kuros tiek izmantots pielāgots izcenojums.

 
## <a name="default-product-price-list"></a>Noklusējuma produktu cenrādis
Katram klienta ierakstam ir lauks **Noklusējuma cenrādis**, kur varat norādīt cenrādi, kurš atbilst šī klienta valūtai. Programmatūrā PSA šajā laukā noklusējuma vērtība netiek ievadīta automātiski. Ja ar noteiktu klientu pastāv pielāgota vienošanās par cenu noteikšanu, šo lauku varat izmantot, lai saistītu kādu cenrādi ar šo klientu.

Lai ievadītu noklusējuma produktu cenrāžus, iespējas, piedāvājuma un projekta līguma entītijas izmanto tālāk norādīto secību. Tāda pati secība tiek izmantota projektu cenrāžiem.

1.  Piedāvājums
2.  Iespēja
3.  Klients
4.  PSA globālie iestatījumi

Pēc noklusējuma piedāvājuma rindas laukā **Produkts** ir uzskaitīti visi aktīvie produkti, kas atrodas attiecīgā piedāvājuma produktu cenrādī. Ja kāds produkts ir deaktivizēts vai ja tas ir melnraksta produkts, tas nav iekļauts sarakstā pat tad, ja šis produkts ir cenrādī. 

Produktu kataloga rindas tiek pievienotas kā rēķina rindas pirmajā rēķinā, kurš tiek izveidots projekta līgumam. Melnraksta rēķinā šīs rēķina rindas var izdzēst. Tādā gadījumā rindas būs redzamas nākamajā rēķinā, līdz par tām ir izrakstīts rēķins vai līdz rēķins tiek nosūtīts klientam. Programmatūrā PSA produkta rēķina rindā nevar izrakstīt rēķinu par daļēju daudzumu. Kad tiek izrakstīts rēķins par produktu rindām no projekta līguma, tiek izveidotas faktiskās vērtības. Taču šīs faktiskās vērtības nav sasaistītas ar attiecīgo projekta entītiju. Citiem vārdiem sakot, uz produktu balstītās projekta līguma rindas ir neatkarīgas no jebkāda uz projektu balstītā lietojuma. PSA neseko līdzi materiālu patēriņam projektos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]