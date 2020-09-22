---
title: Transakcijas kategorijas izmantošana kā cenu noteikšanas dimensiju
description: Šajā tēmā ir sniegta informācija par transakcijas kategorijas izmantošanu kā cenu noteikšanas dimensiju.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753556"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Transakcijas kategorijas izmantošana kā cenu noteikšanas dimensiju
Šajā tēmā ir sniegta informācija par transakcijas kategorijas izmantošanu kā cenu noteikšanas dimensiju. Pirms darba sākšanas, ja vēl neesat izveidojis cenas noteikšanas dimensijas risinājumu, jums būs jāizveido jauns. Ja jums jau ir cenas noteikšanas dimensijas risinājums, varat veikt izmaiņas šajā risinājumā. Ja savai organizācijai neesat izveidojis jaunu cenas noteikšanas dimensijas risinājumu, izpildiet procedūru tēmā [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Transakcijas kategorijas pievienošana veidlapām un skatiem
Lai padarītu transakcijas kategoriju redzamu lietotāja interfeisā (UI), izmantojot cenas noteikšanas dimensijas risinājumu, jums būs jāapskata visas galveno entītiju veidlapas un skati un šie lauki jāpievieno šo entītiju veidlapām un skatiem.
Tālāk sniegtajā tabulā ir pieejams visaptverošs iekļautu veidlapu un skatu saraksts, kas tiek parādīti pēc entītijas un kas ir jāatjaunina ar jaunajiem laukiem. Ja šo entītiju pielāgojumos ir papildu skati vai veidlapas, pievienojiet tiem arī jaunus laukus.

|  Entītija        | Veidlapas     |Skati        |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena|• Informācija |• Aktīvu resursu kategoriju cenas<br> • Ar resursu kategorijas cenu saistītais skats|
|  Lomas cenas uzcenojums|• Informācija|• Aktīvais lomas cenas uzcenojums<br>• Ar lomas cenas uzcenojumu saistītais skats|
|  Piedāvājuma rindas informācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Aktīva piedāvājuma rindas papildinformācija<br>Apvienota piedāvājuma rindas papildinformācija<br>Piedāvājuma rindas papildinformācijas saistītais skats|
|  Projekta līguma rindas papildinformācija|• Projekta informācija<br>• Projekta ātrā izveidošana|Līguma rindas apvienotā papildinformācija<br>Aktīvās līguma rindas papildinformācija<br>Līguma rindas papildinformācijas saistītais skats|
|  Projekta grupas dalībnieks|• Informācija<br>• Jauna veidlapa|• Aktīvie projekta darba grupas dalībnieki<br>• Projekta darba grupas dalībnieki<br>• Projekta grupas dalībnieku saistītais skats|
|  Laika ieraksts|• Informācija<br>• Laika ieraksta izveide|• Mani laika ieraksti pēc datuma<br>• Mani laika ieraksti šajā nedēļā<br>• Laika ieraksti apstiprināšanai|
|  Žurnāla rinda|• Informācija<br>• Ātrā izveide|• Aktīvās žurnāla rindas<br>• Žurnāla rindas saistītais skats|
|  Rēķina rindas informācija|• Informācija<br>• Ātrā izveide|• Aktīva rēķina rindas papildinformācija<br>• Rēķinā iekļaujamas darbības<br>• Papildu rēķina darbības<br>• Rēķina rindas papildinformācijas saistītais skats<br>• Rēķinā neiekļaujamas darbības|
|  Faktiski|• Informācija<br>• Aktīvās faktiskās vērtības|• Faktiskais saistītais skats|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Transakcijas kategorijas iestatīšana kā cenu noteikšanas dimensiju

1. Tīmekļa interfeisā pārejiet uz **Project Service** > **Iestatījumi** > **Parametri**. 
2. Lapā **Parametri**, cilnē **Uz summu balstītās cenu noteikšanas dimensijas** ņemiet vērā režģi, kas parāda ierakstus entītijā **Cenu noteikšanas dimensijas**.
3. Pievienojiet **Transakcijas kategoriju** šim sarakstam un iestatiet laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Jā**.
4. Laukā **Dimensijas tips** atlasiet **Uz summu balstīts** un pēc tam atlasiet **Transakcijas kategorijas** prioritāti, kas saistīta ar izmaksām un pārdošanu.
