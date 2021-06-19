---
title: Darījumu kategoriju kā cenu noteikšanas dimensiju izmantošana
description: Šajā tēmā ir sniegta informācija par transakcijas kategorijas lauka izmantošanu kā cenu noteikšanas dimensiju.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d956545e1ad38fb09660f107e085f38d099c2207
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004450"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Darījumu kategoriju kā cenu noteikšanas dimensiju izmantošana


_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Šajā tēmā ir izskaidrots, kā izmantot lauku **Transakcijas kategorija** kā cenu noteikšanas dimensiju. 

## <a name="prerequisites"></a>Priekšnosacījumi
Pirms šajā tēmā aprakstīto procedūru veikšanas ir nepieciešams jauns organizācijas cenu dimensiju risinājums. Ja tas vēl nav izveidots, skatiet tēmu [Pielāgotu lauku un entītiju kā cenu noteikšanas dimensiju izveide](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Transakcijas kategorijas lauka pievienošana veidlapām un skatiem
Lai lauks **Transakcijas kategorija** būtu redzams cenu noteikšanas dimensijas risinājumā, šis lauks ir jāpievieno visām veidlapām un skatiem kā entītija.

Tālāk redzamajā tabulā ir uzskaitītas visas iebūvētās veidlapas un skati pēc entītijas. Turklāt jaunais lauks būs jāpievieno arī visām papildu veidlapām vai skatiem jūsu pielāgotajās entītijās.

|  Elements        | Veidlapas     |Skati        |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena| Informācija |- Aktīvu resursu kategoriju cenas<br> - Resursu kategorijas cenu saistītais |
|  Lomas cenas uzcenojums| Informācija|- Aktīvais lomas cenas uzcenojums<br>- Lomas cenas uzcenojuma saistītais |
|  Piedāvājuma rindas informācija|- Projekta informācija<br>- Projekta ātrā izveidošana| - Aktīva piedāvājuma rindas detalizēta informācija<br>- Apvienota piedāvājuma rindas detalizēta informācija<br>- Piedāvājuma rindas detalizētās informācijas saistītais |
|  Projekta līguma rindas informācija|- Projekta informācija<br>- Projekta ātrā izveidošana|- Līguma rindas apvienotā informācija<br>- Aktīvās līguma rindas informācija<br>- Līguma rindas papildinformācijas saistītais |
|  Projekta uzdevums|- Informācija<br>- Jauna veidlapa| &nbsp; |
|  Projekta grupas dalībnieks|- Informācija<br>- Jauna veidlapa|- Aktīvie projekta grupas dalībnieki<br>- Projekta darba grupas dalībnieki<br>- Projekta grupas dalībnieku saistītais |
|  Laika ieraksts|- Informācija<br>- Izveidot laika ierakstu|- Mani laika ieraksti pēc datuma<br>- Mani laika ieraksti šajā nedēļā<br>- Laika ieraksti apstiprināšanai|
|  Žurnāla rinda|- Informācija<br>- Ātrā izveide|- Aktīvās žurnāla rindas<br>- Žurnāla rindas saistītais|
|  Rēķina rindas informācija|- Informācija<br>- Ātrā izveide|- Aktīva rēķina rindas informācija<br>- Rēķinā iekļaujamas transakcijas<br>- Papildu rēķina transakcijas<br>- Rēķina rindas informācijas saistītais <br>- Rēķinā neiekļaujamas transakcijas|
|  Faktiski|- Informācija<br>- Aktīvās faktiskās vērtības| Faktiskais saistītais |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Transakcijas kategorijas lauka kā cenu noteikšanas dimensijas iestatīšana

1. Pārejiet uz **Iestatījumi** > **Parametri**. 
2. Lapā **Parametri**, cilnē **Uz summu balstītās cenu noteikšanas dimensijas** pārliecinieties, ka režģis parāda ierakstus entītijā **Cenu noteikšanas dimensijas**.
3. Pievienojiet **Transakcijas kategoriju** šim sarakstam un iestatiet laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Jā**.
4. Laukā **Dimensijas tips** atlasiet **Uz summu balstīts** un pēc tam atlasiet **Transakcijas kategorijas** prioritāti, kā tā ir saistīta ar izmaksām un pārdošanu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]