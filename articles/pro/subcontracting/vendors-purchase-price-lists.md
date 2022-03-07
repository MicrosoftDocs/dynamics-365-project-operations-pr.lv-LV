---
title: Pārdevēju un pirkumu cenrāžu pārvaldība programmā Project Operations
description: Šajā tēmā ir sniegta informācija, kas palīdzēs izveidot un uzturēt pārdevēju datus un pirkumu cenrāžus apakšlīgumu slēgšanai.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994150"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Pārdevēju un pirkumu cenrāžu pārvaldība programmā Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

## <a name="vendors-in-project-operations"></a>Pārdevēji programmā Project Operations

Programmā Microsoft Dynamics 365 Project Operations pārdevēju uzņēmumu attiecību tips ir **Pārdevējs** vai **Piegādātājs**. Apakšlīgumā kā pārdevēju varat izvēlēties tikai tādu uzņēmuma ierakstu, kuram ir viens no šiem attiecību tipiem.

Ar pārdevēja ierakstu var saistīt vienu vai vairākus pirkumu cenrāžus. Tomēr katram pirkumu cenrādim, kas ir saistīts ar pārdevēja ierakstu, jābūt spēkā atšķirīgam datumam. Programmā Project Operations netiek atbalstīta datumu pārklāšanās cenrāžiem.

Pēc noklusējuma pārdevēja ierakstam visiem pārdevējam izveidotajiem apakšlīgumiem tiek izmantoti tālāk uzskaitītie lauki un jēdzieni.

- Maksājumu nosacījumi
- Rēķina saņēmēja kontaktpersona
- Primārā kontaktpersona

    > [!NOTE]
    > Pēc noklusējuma pārdevēja primārā kontaktpersona tiek izmantota kā apakšlīguma pārdevēja uzņēmuma pārvaldītājs.

- Valūta
- Pašreizējā iepirkuma cenrāži

## <a name="purchase-price-lists-in-project-operations"></a>Iepirkumu cenrāži programmā Project Operations

Cenrādis, kur lauks **Konteksts** ir iestatīts kā **Pirkums**, tiek uzskatīts par pirkuma cenrādi. Pirkuma cenrāžus var definēt tā, lai attēlotu laika, izmaksu un materiālu iepirkuma cenu katalogu. Pirkuma cenrāži līdzinās izmaksu un pārdošanas cenrāžiem programmā Project Operations. Tālāk minētie jēdzieni attiecas uz pirkuma cenrāžiem tāpat kā uz izmaksu un pārdošanas cenrāžiem.

- **Datuma spēkā esamība** — pirkuma cenrāžiem ir datuma spēkā esamība. Datuma spēkā esamību norāda sākuma datuma un beigu datuma lauki katrā cenrādī. Laiks starp sākuma datumu un beigu datumu ir datuma spēkā esamības periods.
- **Valūta** — cenrāža galvenē norādītā valūta tiek izmantota kā valūta, kādā katalogā tiek norādītas darba cenas, izdevumu kategorijas un produkti.
- **Noklusējuma laika vienība** — noklusējuma laika vienība norāda darba cenas pirkumiem. Cenrāža laika vienības lauks tiek lietots tikai, lai norādītu noklusējuma vērtību. Šo vērtību var mainīt atsevišķu lomu cenu rindās.

Pirkuma cenrāžus var pievienot pārdevēju ierakstiem kā asociācijas, kas pazīstamas kā projekta cenrāži. Šie cenrāži tiek izmantoti, lai ievadītu noklusējuma cenas apakšlīguma rindās. Pēc noklusējuma, ja pārdevēja ierakstam tiek pievienoti vairāki pirkuma cenrāži, pārdevējam izveidotajiem apakšlīgumiem tiek izmantots jaunākais cenrādis. Pārdevēja ierakstiem var pievienot tikai tos cenrāžus, kur lauks **Konteksts** ir iestatīts kā **Pirkums**.

### <a name="subcontract-specific-purchase-price-lists"></a>Ar apakšlīgumu saistīti cenrāži

Pirkuma cenrāžus var arī pievienot apakšlīgumiem kā asociācijas, kas pazīstamas kā projekta cenrāži. Šie cenrāži tiek izmantoti, lai ievadītu noklusējuma cenas apakšlīguma rindās. Pēc noklusējuma, ja apakšlīgumam tiek pievienoti vairāki pirkuma cenrāži, katram no tiem ir jābūt atšķirīgai datumu spēkā esamībai. Programmā Project Operations netiek atbalstīti cenrāži, kuru datumu spēkā esamība pārklājas. Apakšlīgumiem var pievienot tikai tos cenrāžus, kur lauks **Konteksts** ir iestatīts kā **Pirkums**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]