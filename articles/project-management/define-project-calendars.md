---
title: Projekta kalendāru definēšana
description: Šajā tēmā ir sniegta informācija par to, kā projektam lietot kalendāra veidni, lai sekotu līdzi projekta grafikam.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487649"
---
# <a name="define-project-calendars"></a>Projekta kalendāru definēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Lai izveidotu un pārvaldītu projektu, projektam jālieto kalendāra veidne. Kalendāra veidne definē šādus projekta atribūtus:

- darba stundas, ieskaitot sākuma un beigu laiku;
- darba dienas;
- kalendāra izņēmumi, piemēram, brīvdienas.

Projektam lietotā kalendāra veidne ir organizācijas iestatījumos definētās kalendāra veidnes kopija.

> [!NOTE]
> Ja maināt kalendāra veidni, šīs izmaiņas netiek attiecinātas uz projekta darba laiku. Lai mainītu projekta darba laiku, jālieto jauna veidne.

Lai organizācijai izveidotu kalendāra veidni, ir divas galvenās prasības:

- definējiet veidnes vēlamo darba laiku, izmantojot jaunu vai esošu rezervējamu resursu;
- izveidojiet jaunu kalendāra veidni un saistiet to ar rezervējamo resursu.

**Veidnes darba laiku definēšana**

1. Atveriet sadaļu **Resursi** \> **Resursi.**
2. Izveidojiet jaunu resursu atsaucei kalendāra veidnē vai atlasiet esošu resursu.
3. Atlasiet resursa cilni **Darba stundas** un izpildiet sadaļā [Resursa darba stundu iestatīšana](/dynamics365/field-service/set-work-hours-resource) sniegtos norādījumus, lai konfigurētu kalendāra kārtulas.

**Jaunas kalendāra veidnes izveide**

1. Pārejiet uz **Iestatījumi** \> **Kalendāra veidne**.
2. Atlasiet **Jauns** un ievadiet nosaukumu, aprakstu un veidnes resursu.

> [!NOTE]
> Ja kalendārā ir atsauce uz resursu, ar šo kalendāra veidni tiek saistīta resursa kalendāra kopija. Ja tiek mainītas kopētās veidnes darba stundas, šīs izmaiņas netiek attiecinātas uz kalendāra veidni.

Tagad šo darba veidni varat sasaistīt ar projekta kalendāra veidni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

