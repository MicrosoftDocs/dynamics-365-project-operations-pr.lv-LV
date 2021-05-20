---
title: Projekta iespēju pārvaldība
description: Šajā tēmā ir sniegta informācija par to, kā strādāt ar iespējām, kas ir saistītas ar projektiem.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948429"
---
# <a name="manage-project-based-opportunities"></a>Projekta iespēju pārvaldība

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Uzņēmumiem, kas strādā ar projektiem, piegādes operācijas parasti ir izvērstas vairākās valstīs un ģeogrāfiskajās atrašanās vietās. Projekta izpildes un piegādes izmaksas var mainīties atkarībā no tā, kāda ģeogrāfiskā vieta vai nodaļa pārvalda piegādi. Savukārt tas var ietekmēt darījuma uzcenojumu. Projekta pakalpojumu piegāde parasti ietver daudz cilvēkresursu nodaļas laika, ievērojamas izmaksas par ceļojumiem, materiālu izmaksas un citus izdevumus.

Projekta iespējas programmā ir Dynamics 365 Project Operations izstrādātas ar paplašinājumiem programmai Dynamics 365 Sales. Šajā tēmā ir sniegta detalizēta informācija par dažādiem laukiem un biznesa loģiku, kas ir iekļauta papildu funkcionalitātē un kas ir nepieciešama uzņēmumiem, kas strādā projektiem, lai pārvaldītu projektu iespējas.

## <a name="view-all-project-based-opportunities"></a>Visu projekta iespēju skatīšana

Visu projekta iespēju sarakstu var redzēt lapā **Iespēju saraksts**. 

1. Dodieties uz **Pārdošana** > **Iespējas**.
2. Izmantojiet **skatu pārslēdzēju**, lai atlasītu citus iespēju filtrētos skatus. Varat izveidot savus skatus, kuros ir pielāgoti filtrēšanas kritēriji, lai konfigurētu šos skatus un navigācijas opcijas.

Projekta iespējas var tikt izveidotas vai dzēstas šajā saraksta lapā vai detalizētās informācijas lapā.

## <a name="business-process-flow-for-project-based-deals"></a>Biznesa procesa plūsma projektu darījumiem

Project Operations projekta darījumiem atbalsta tālāk norādītās biznesa procesu plūsmas.

- Interesenta–iespējas biznesa process
- Iespējas pārdošanas process

### <a name="lead-to-opportunity-business-process"></a>Interesenta–iespējas biznesa process 
Interesenta–iespējas biznesa process atbalsta tālāk uzskaitītos posmus.

| Posms | Kartēta entītija | Funkcionalitāte |
| --- | --- | --- |
| Kvalificēt | Interesenti | Kvalificējiet interesentu, lai izveidotu uzņēmumu, kontaktpersonu un/vai iespēju. |
| Izstrādāt | Iespēja | Izstrādājiet iespēju, lai pievienotu papildinformāciju par attiecīgo darbu, galvenajām iesaistītajām personām un konkurenci. |
| Piedāvāt | Iespēja | Izstrādājiet priekšlikumu un saņemiet apstiprinājumu no iekšējās pārbaudes darba grupas. |
| Aizvēršana | Iespēja | Iegūstiet iespēju, lai noslēgtu darījumu. |

### <a name="opportunity-sales-process"></a>Iespējas pārdošanas process
Iespējas pārdošanas process risinājumā Project Operations ir iespēju pārdošanas procesa biznesa plūsmas paplašinājums pārdošanas lietojumprogrammā. Šis biznesa process ir izstrādāts, lai atbalstītu tālāk minētos projekta iespējas posmus.

| Posms | Kartēta entītija | Funkcionalitāte |
| --- | --- | --- |
| Kvalificēt | Iespēja | Kvalificējiet interesentu, lai izveidotu uzņēmumu, kontaktpersonu un/vai iespēju. |
| Piedāvāt | Piedāvājums | Izstrādājiet priekšlikumu, izmantojot projekta piedāvājumus, un saņemiet apstiprinājumu no iekšējās pārbaudes darba grupas. |
| Līgums | Projekta līgums | Iegūstiet piedāvājumu, lai izveidotu līgumu un sāktu projekta izpildi un piegādi. |
| Aizvēršana | Projekta līgums | Sekmīgi pabeidziet darbu un slēdziet projekta līgumu. |

> [!NOTE]
> Ja jūsu projekta darījums sākās ar interesentu, interesenta–iespējas biznesa process ir prioritārs.
>
> Ja jūsu projekta darījums sākās ar iespēju, iespējas pārdošanas process ir prioritārs.

Varat rediģēt produktu biznesa procesa plūsmu vai izveidot savas biznesa procesa plūsmas, lai izsekotu pārdošanas procesam. Papildinformāciju par biznesa procesu plūsmu skatiet rakstā [Biznesa procesu plūsmu pārskats](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]