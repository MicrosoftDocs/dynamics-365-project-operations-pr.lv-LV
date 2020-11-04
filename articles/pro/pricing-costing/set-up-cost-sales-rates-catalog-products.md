---
title: Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem
description: Šajā tēmā ir sniegta informācija par izmaksu un pārdošanas likmju iestatīšanu preču katalogā.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080511"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Cenu iestatīšana preču kataloga vienumiem risinājumā Dynamics 365 Project Operations ir tāda pati kā Dynamics 365 Sales.

Tā kā produktus nevar novērtēt vai izmantot projektiem risinājumā Project Operations,, preču kataloga cenas nav jāiestata projekta cenrāžiem piedāvājumiem un līgumiem.

Preču kataloga cenas ir jāiestata piedāvājuma, līguma vai konta laukā **Produkta cena**. Neiestatiet preču kataloga cenas šo entītiju projektu cenrāžos. Projekta cenrādis ir pieejams tikai risinājumam Project Operations. Pastāv ar piedāvājumu saistīta biznesa loģika, kas kopē cenrāžus no piedāvājuma uz līgumu. Rezultāts ir līgumā noteiktais projekta cenrādis. Kopēšanas darbība var aizkavēt piedāvājuma veiksmīgu procesu, ja projekta cenrādis piedāvājumā kļūst pārāk liels. Produktu cenrāži netiek kopēti, lai izveidotu pielāgotus cenrāžus līgumos. Tas nozīmē, ka produktu cenrāži neietekmēs piedāvājuma veiksmīgu izpildi.
