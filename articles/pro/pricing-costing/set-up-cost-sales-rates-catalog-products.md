---
title: Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite
description: Šajā tēmā ir sniegta informācija par izmaksu un pārdošanas likmju iestatīšanu preču katalogā.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176710"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Cenu iestatīšana preču kataloga vienumiem risinājumā Dynamics 365 Project Operations ir tāda pati kā Dynamics 365 Sales.

Tā kā produktus nevar novērtēt vai izmantot projektiem risinājumā Project Operations,, preču kataloga cenas nav jāiestata projekta cenrāžiem piedāvājumiem un līgumiem.

Preču kataloga cenas ir jāiestata piedāvājuma, līguma vai konta laukā **Produkta cena**. Neiestatiet preču kataloga cenas šo entītiju projektu cenrāžos. Projekta cenrādis ir pieejams tikai risinājumam Project Operations. Pastāv ar piedāvājumu saistīta biznesa loģika, kas kopē cenrāžus no piedāvājuma uz līgumu. Rezultāts ir līgumā noteiktais projekta cenrādis. Kopēšanas darbība var aizkavēt piedāvājuma veiksmīgu procesu, ja projekta cenrādis piedāvājumā kļūst pārāk liels. Produktu cenrāži netiek kopēti, lai izveidotu pielāgotus cenrāžus līgumos. Tas nozīmē, ka produktu cenrāži neietekmēs piedāvājuma veiksmīgu izpildi.
