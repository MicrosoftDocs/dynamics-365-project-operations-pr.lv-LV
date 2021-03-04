---
title: Iespējas iestatījumi — Lite
description: Šajā tēmā ir sniegta informācija par projektu darījumiem un projekta iespēju rindām.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c34817181b75b1b0079974f536e4d7b032ae87dd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181055"
---
# <a name="opportunity-header---lite"></a>Iespēju galvene — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Iespējas galvenē ietverta vispārējā informācija par projekta darījumu, kas attiecas uz visām rindām projekta iespējā.

Projekta iespējas risinājumā Dynamics 365 Project Operations ir iespēju paplašinājumi risinājumā Dynamics 365 Sales. Šie paplašinājumi nodrošina papildu funkcionalitāti, kas ir specifiska un nepieciešama projekta iespējām. Šajos paplašinājumos var būt jauni lauki un lentes darbības, kas pieejamas projekta iespējās. Iespējams, daži lauki, funkcijas un noklusējuma loģika, kas ir pieejama programmā Sales, nav pieejama risinājumā Project Operations.

Tālāk sniegtajā tabulā ir iekļauti projekta iespējas lauki, kas ir unikāli risinājumā Project Operations vai kuriem ir dažas svarīgas darbības izmaiņas, salīdzinot ar iespējām risinājumā Sales.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Veidi | Cilne Vispārīgi (slēpta) | Šajā opciju kopas laukā ir tālāk norādītās opcijas.</br>- Balstīts uz darbu (pieejams tikai ar Project Operations)</br>- Balstīts uz vienumu (pieejams tikai tad, ja ir instalēts Project Operations un Sales)</br>- Opcijas, kuru pamatā ir servisa uzturēšana (pieejama, ja ir instalēts Field Service) | Ja izmantojat Project Operations, šī lauka vērtība automātiski tiek uzstādīta uz **Balstīts uz darbu**, kas klasificē iespēju kā balstītu uz projektu. Iespējai jābūt balstītai uz projektu, lai iespējotu visus projektam specifiskos paplašinājumus un funkcionalitāti šī darījuma lejupstraumes pārdošanas procesā. |
| Kontaktinformācija | Cilne Vispārīgi | Atsauce uz klienta primāro kontaktpersonu šim darījumam. | |
| Konts | Cilne Vispārīgi | Atsauce uz klienta uzņēmuma vai konta ierakstu. | |
| Konta pārvaldnieks | Cilne Vispārīgi | Šī projekta iespējas konta pārvaldnieka vārds. | Konta pārvaldnieks ir atbildīgs par attiecību ar klientu pārvaldīšanu līdz projekta pabeigšanai. Pamatojoties uz rezervējamā resursa ierakstu, kas saistīts ar konta pārvaldnieku, līgumslēdzēja vienība ir noklusējuma vērtība. |
| Līgumslēdzēja vienība | Cilne Vispārīgi | Organizācijas struktūrvienība, kas ir atbildīga par projekta vai ar šo darījumu saistīto projektu īstenošanu. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas pabeidz projektu(-us) pēc darījuma slēgšanas. Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas. |

Informāciju par pārējiem laukiem un sadaļām iespējas cilnē **Kopsavilkums** skatiet tēmā [Iespējas izveide vai rediģēšana (Sales un Pārdošanas centrmezgls)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]