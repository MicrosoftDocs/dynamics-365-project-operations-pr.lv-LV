---
title: Produktu līgumu rindu kompleksu vienību pārvaldīšana — Lite
description: Šajā tēmā ir sniegta informācija par to, kā atbalstīt uz abonementu balstītu produktu pārdošanu.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177385"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Produktu līgumu rindu kompleksu vienību pārvaldīšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, Dynamics 365 Project Operations izmanto daudzuma koeficientus. Uz abonēšanu balstītiem produktiem daudzums līgumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.

Abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī. Pārdošanas procesa laikā cena līguma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents. Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits. Daudzums, kas tiek izmantots līguma rindas summas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.

Lai atbalstītu šāda tipa pārdošanu, Project Operations atbalsta *daudzuma koeficientu* jēdzienu. Daudzuma faktori izmanto produktu atribūtus. Kad kādam produktam konfigurējat konkrētus rekvizītus, jūs varat atzīmēt šo rekvizītu apakškopu vai visus rekvizītus kā daudzuma faktorus.

Project Operations pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips. Kad prece ar konfigurētu daudzuma koeficientu tiek pievienota līguma rindai, lauks **Daudzums** kļūst tikai lasāms. Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, Project Operations aprēķina līguma rindas daudzumu.

Programmatūrā Dynamics 365 Sales varētu būt, piemēram, tālāk norādītie rekvizīti.

- **Lietotāju skaits**: lietotāju skaits.
- **Mēnešu skaits**: abonēšanas mēnešu skaits.
- **Produkta SKU** : produkta krājumu uzturēšanas vienība (SKU).

Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** var atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus.

Lai no produkta rekvizītiem izveidotu daudzuma koeficientus, izpildiet tālāk norādītās darbības.

1. Līdzeklī **Project Operations** atlasiet **Pārdošana — produkti**.
2. Atveriet produktu, kuram ir nepieciešams iestatīt daudzuma koeficientus. Pārliecinieties, vai produktam jau ir iestatīti rekvizīti.
3. Lapā **Projekta informācija** atlasiet cilni **Daudzuma koeficienti**.
4. Apakšrežģī atlasiet **+ Jauns lauka aprēķins**.
5. Ievadiet **Daudzuma koeficienta** nosaukumu un atlasiet rekvizīta vērtību, kas ir kartēta uz lauka aprēķinu.
6. Saglabāt un aizvērt formu.
7. Atkārtojiet 2.–6. darbību visiem rekvizītiem, kas kopā veido produkta līguma rindai atbilstošo daudzumu.

Ja ir iestatīti daudzuma koeficienti, tad, kad lietotājs veido līguma rindu šim produktam, līguma rindas daudzums ir slēgts. Pēc tam daudzums tiek aprēķināts kā šīs līguma rindas rekvizītu vērtību produkts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]