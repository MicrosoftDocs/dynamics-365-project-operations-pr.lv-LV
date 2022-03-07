---
title: Produktu cenrāži
description: Šajā tēmā sniegta informācija par cenu sarakstiem katalogu cenrāžos, ko izmanto projektu piedāvājumos un līgumos.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999235"
---
# <a name="product-price-lists"></a>Produktu cenrāži

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

 Programmā Project Operations **produktu cenrāži** un ar tiem saistītās cenrāža elementu entītijas atbalsta funkcionalitāti produktu cenu noteikšanai pēc produkta piedāvājuma un līguma rindām. Projektos lietotajiem produktiem tiek izmantoti projekta cenrāži ar cenrāža elementu ierakstiem. 

Produkti ir jāiestata tā, lai produktu katalogā tiem būtu noklusējuma izmaksu un cenu saraksti. Šī saraksta cena, standarta izmaksas un pašreizējās izmaksas ir jāizmanto, lai konfigurētu noklusējuma izmaksas un saraksta cenas. Noklusējuma saraksta cenas piedāvājuma rindā vai projekta līguma rindā tiek izmantotas tikai tad, ja sistēma nevar atrast attiecīgā produkta cenrāža rindu piedāvājuma vai projekta līguma produktu cenrādī.

Produktu kataloga rindu izmaksu cenu starp piedāvājumiem var mainīt. Šī iespēja ir svarīga, jo, ja netiek veikta precīza izmaksu izsekošana, nevar noteikt operatīvo peļņu no projekta saistībām. Pēc noklusējuma kā izmaksu cena tiek izmantota produkta standarta cena. Taču piedāvājuma rindā noklusējuma izmaksu cenu var atjaunināt, ja šim piedāvājumam ir citāda izmaksu cena.

## <a name="price-list-items"></a>Cenrāža elementi

Produktus no produktu kataloga varat pievienot dažādiem cenrāžiem. Cenrāža rindas produktiem vienmēr atsaucas uz noteiktu vienību. Cenrāža elementos minēta produkta cenas noteikšanu var konfigurēt kā valūtas summu. Vai arī to var konfigurēt kā saraksta cenas, pašreizējo izmaksu vai standarta izmaksu funkciju.

Cenu noteikšanas funkcionalitāte atbalsta dažādas noapaļošanas opcijas, kad produktu cenas tiek konfigurētas kā saraksta cenas, standarta izmaksu vai pašreizējo izmaksu funkcija. Papildus vairāku cenu noteikšanas metožu un noapaļošanas opciju izmantošanai ir iespējams arī sasaistīt atlaižu sarakstus un cenrāža elementus. 

 
## <a name="default-product-price-list"></a>Noklusējuma produktu cenrādis
Katram klienta ierakstam ir lauks **Noklusējuma cenrādis**, kur varat norādīt cenrādi, kurš atbilst šī klienta valūtai. Šajā laukā noklusējuma vērtība netiek ievadīta automātiski. Ja ar noteiktu klientu pastāv pielāgota vienošanās par cenu noteikšanu, šo lauku varat izmantot, lai saistītu kādu cenrādi ar šo klientu.

Lai ievadītu noklusējuma produktu cenrāžus, iespējas, piedāvājuma un projekta līguma entītijas izmanto tālāk norādīto secību. Tāda pati secība tiek izmantota projektu cenrāžiem.

1.  Piedāvājums
2.  Iespēja
3.  Klients
4.  Globālie iestatījumi 

Pēc noklusējuma piedāvājuma rindas laukā **Produkts** ir uzskaitīti visi aktīvie produkti, kas atrodas attiecīgā piedāvājuma produktu cenrādī. Ja kāds produkts ir deaktivizēts vai ja tas ir melnraksta produkts, tas nav iekļauts sarakstā pat tad, ja šis produkts ir cenrādī. 

Produktu kataloga rindas tiek pievienotas kā rēķina rindas pirmajā rēķinā, kurš tiek izveidots projekta līgumam. Melnraksta rēķinā šīs rēķina rindas var izdzēst. Tādā gadījumā rindas būs redzamas nākamajā rēķinā, līdz par tām ir izrakstīts rēķins vai līdz rēķins tiek nosūtīts klientam. Produkta rēķina rindā nevar izrakstīt rēķinu par daļēju daudzumu. Kad tiek izrakstīts rēķins par produktu rindām no projekta līguma, tiek izveidotas faktiskās vērtības. Taču šīs faktiskās vērtības nav sasaistītas ar attiecīgo projekta entītiju. Citiem vārdiem sakot, uz produktu balstītās projekta līguma rindas ir neatkarīgas no jebkāda uz projektu balstītā lietojuma. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
