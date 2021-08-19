---
title: Sarežģītu vienību, piemēram, viena lietotāja, pārvaldība, uz vienu mēnesi produktu piedāvājuma rindām — Lite
description: Šajā tēmā ir sniegta informācija par sarežģītu vienību pārvaldību produktu piedāvājumu rindām.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d53dde1d3b2705c5b0283f989d0e2eebfdcb5a0eb5f91cf4bf48e9c07aba79d1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989785"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Sarežģītu vienību, piemēram, viena lietotāja, pārvaldība, uz vienu mēnesi produktu piedāvājuma rindām — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Dynamics 365 Project Operations, lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, izmanto daudzuma koeficientus. Uz abonēšanu balstītiem produktiem daudzums piedāvājumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.

Parasti abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī. Pārdošanas procesa laikā cena piedāvājuma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents. Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits. Daudzums, kas tiek izmantots piedāvājuma rindas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.

Lai atbalstītu šāda tipa pārdošanu, Project Operations ieviesa daudzuma koeficientu jēdzienu. Daudzuma koeficienti izmanto produkta atribūtus programmā Dynamics 365. Kad kādam produktam konfigurējat konkrētus rekvizītus, Project Operations ļauj jums atzīmēt apakškopu vai visus rekvizītus kā daudzuma faktorus.

Project Operations pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips. Kad pievienojat produktu ar daudzuma koeficientiem piedāvājuma rindai, lauks **Daudzums** kļūst tikai lasāms. Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, Project Operations aprēķināta piedāvājuma rindas daudzumu.

Programmatūrā Dynamics 365 Sales varētu būt, piemēram, tālāk norādītie rekvizīti.

- **Lietotāju skaits**: Lietotāju skaits
- **Mēnešu skaits**: Abonēšanas mēnešu skaits
- **Produkta SKU**

Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** varat atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus.

Lai no produkta rekvizītiem izveidotu daudzuma koeficientus, veiciet tālāk minētās darbības.

1. Project Operations kreisajā navigācijas rūtī pārejiet uz **Sales** > **Products**.
2. Atveriet produktu, kuram nepieciešams konfigurēt daudzuma koeficientus. Pārliecinieties, vai produktam ir jau konfigurēti rekvizīti.
3. Produkta lapā **Projekta informācija** atlasiet **Daudzuma koeficienti**.
4. Apakšrežģī atlasiet **+ Jauns lauka aprēķins**.
5. Ievadiet daudzuma koeficienta nosaukumu un atlasiet rekvizīta vērtību, kas ir kartēta uz lauka aprēķinu.
6. Saglabāt un aizvērt formu. Atkārtojiet šīs darbības visiem rekvizītiem, kas jāizmanto produkta piedāvājuma rindas daudzuma aprēķināšanai.

Kad produktam tiek izveidota produkta piedāvājuma rinda, piedāvājuma rindas daudzums tiek slēgts. Daudzums tiek aprēķināts kā to rekvizītu vērtību reizinājums, kas ievadīts šajā piedāvājuma rindā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]