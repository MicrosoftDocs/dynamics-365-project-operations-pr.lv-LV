---
title: Darba stundu veidnes izveide
description: Šajā tēmā ir aprakstīts, kā izveidot darba stundu veidni programmā Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987400"
---
# <a name="create-a-work-hours-template-project-service"></a>Darba stundu veidnes izveide (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Atlasiet resursa cilni **Darba stundas** un izpildiet sadaļā [Resursa darba stundu iestatīšana](/dynamics365/field-service/set-work-hours-resource.md) sniegtos norādījumus, lai konfigurētu kalendāra kārtulas.

**Jaunas kalendāra veidnes izveide**

1. Pārejiet uz **Iestatījumi** \> **Kalendāra veidne**.
2. Atlasiet **Jauns** un ievadiet nosaukumu, aprakstu un veidnes resursu.


> [!NOTE]
> Ja kalendārā ir atsauce uz resursu, ar šo kalendāra veidni tiek saistīta resursa kalendāra kopija. Ja tiek mainītas kopētās veidnes darba stundas, šīs izmaiņas netiek attiecinātas uz kalendāra veidni.


### <a name="see-also"></a>Skatiet arī  
 [Resursu iestatīšana](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
