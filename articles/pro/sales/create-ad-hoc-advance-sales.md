---
title: Ad hoc avansa izveide līgumā
description: Šajā tēmā ir sniegta informācija par līguma avansa izveidi pēc nepieciešamības.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 790a0281f72eff5f241d11da025b5b4af643a567
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596009"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Ad hoc avansa izveide līgumā

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Microsoft Dynamics 365 Project Operations atbalsta rēķinu izrakstīšanas scenārijus, kuros ir iesaistīti priekšapmaksas un avansa maksājumi. Process, lai izmantotu **Avansus**, lietojot **Project Operations**, ir līdzīgs **Honorāra** līgumiem. 

Izpildiet tālāk aprakstītās darbības, lai klientam izrakstītu avansa rēķinu.

1. Atveriet lapu **Projekta līgums** un pēc tam atlasiet cilni **Avansi un honorāri**.
2. Apakšrežģī, kurā ir uzskaitīti visi iepriekš ierakstītie avansa maksājumi un priekšapmaksas, atlasiet **+ Jauns projekta līguma honorārs**. 

    Tiek atvērta **Ātrās izveides** veidlapa, lai ierakstītu priekšapmaksu vai avansu.
    
3. Tālāk esošajā tabulā ir uzskaitīti avansa reģistrēšanas lauki un apsvērumi, kas jāņem vērā, izveidojot jaunus.

    | Lauks | Apraksts | Lejupstraumes ietekme |
    | --- | --- | --- |
    | **Projekta līguma klients** | Šajā laukā ir norādīts, kuram līgumā paredzētajam klientam tiks izrakstīts rēķins par šo avansu. | Ja līgumā ir vairāki klienti un katram no tiem vēlaties izrakstīt rēķinu par noteiktu honorāru vai avansa summu, izveidojiet avansu katram klientam atsevišķi. |
    | **Apraksts** | Avansa mērķa vai laika apraksts, lai palīdzētu identificēt šo avansu. | Šis apraksts tiek parādīts šī avansa rēķina rindā. |
    | **Summa** | Priekšapmaksas vai avansa summa. | Šī summa tiek parādīta šī avansa rēķina rindā. |
    | **Rēķina datums** | Datums, kurā klientam tiek izrakstīts rēķins par avansu. | Šis ir automātiskā rēķina izveides procesa datums, kad šim avansam tika izveidota rēķina rinda. |
    | **Rēķina statuss** | Tas ir opciju iestatījums, kas norāda, vai šis avanss ir pievienots šī klienta rēķina melnrakstam. Iespējamās vērtības.</br>- **Nav gatavs rēķina izrakstīšanai**</br>- **Gatavs rēķina izrakstīšanai** | Kad avansa maksājums vai priekšapmaksa ir atzīmēta kā **Gatava rēķina izrakstīšanai**, tas tiek pievienots kā rindas laiks rēķina melnrakstā. Tikai pilnīgi izrakstīts avanss var tikt izmantots, lai sasaistītu projekta izmaksas nākamajam rēķina periodam. |

4. Ātrās izveides dialoglodziņā atlasiet **Saglabāt un aizvērt**, lai ierakstītu avansu vai priekšapmaksu.
