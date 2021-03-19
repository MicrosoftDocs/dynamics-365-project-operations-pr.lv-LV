---
title: Interesentu pārvaldība
description: Šajā tēmā ir sniegta informācija par projekta interesentu pārvaldību.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 526f2ab1fd186877f32a2d11bd92ee8c26a19139
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278067"
---
# <a name="manage-leads"></a>Interesentu pārvaldība

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Project Operations ļauj pārvaldīt un kvalificēt projekta interesentus. Interesentu pārvaldības process iekļauj darba interesentu izveidi un šo interesentu kvalificēšanu. 

## <a name="project-sales-leads"></a>Projekta pārdošanas interesenti

Sadaļas **Pārdošana** kreisajā navigācijas rūtī atveriet saraksta lapu **Interesenti**, lai skatītu sarakstu ar visiem interesentu ierakstiem sistēmā. Parādītais interesentu saraksts satur darba un cita veida interesentus, ko var izveidot, ja jums ir arī lietojumprogrammas Dynamics 365 Sales vai Dynamics 365 Field Service.

Varat izveidot filtrēto skatu, lai skatītu tikai projekta interesentus, izveidojot filtru ar vērtību **Tips**. Piemēram, varat atlasīt, lai parādītu tikai darba interesentus.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Jauna interesenta izveide projekta darījumam

Ja projekta interesents ir kvalificēts, tiek izveidota iespēja un uzņēmums. Projekta iespēja ir sākuma punkts pārdošanas veikšanas darbībām iespējas fāzē. Projekta iespējām ir unikālas funkcijas, kas nepieciešamas, lai pārdotu projekta darbu. Šīs funkcijas ir uzskaitītas tālāk.

- Norēķinu metodes Laiks un materiāli un Fiksēta cena
- Vairāki spēkā esoši cenrāži, kas paredzēti personāla vadībai, izdevumiem un materiāliem, kas ir saistīti ar projektiem

Lai kvalificēts interesents automātiski izveidotu iespēju, iestatiet atribūtu **Tips** uz **Balstīts uz darbu**, kad izveidojat interesentu. Ja izvēlaties citu tipu, interesents neveido projekta iespējas, ja tas ir kvalificēts. Ja projekta iespējas netiek izveidotas, projekta specifiskās funkcijas nav pieejamas lejupstraumes pārdošanas procesos.

Šajā tabulā ir iekļauta svarīga lauku informācija par interesentu, kā arī šo lauku lejupstraumes ietekme.
 
| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Tēma | Cilne Vispārīgi | Šim teksta laukam ir jāietver īss darījuma apraksts. | Interesenta tēma pēc noklusējuma tiks izmantota kā Iespējas tēma, kā arī Piedāvājuma un Projekta līguma nosaukums. |
| Veidi | Cilne Vispārīgi | Šajā opciju kopas laukā ir tālāk norādītās opcijas.</br>- Balstīts uz darbu (pieejams tikai tad, ja ir instalēts Project Operations)</br>- Balstīts uz vienumu (pieejams tikai tad, ja ir instalēts Project Operations un Sales)</br>- Opcijas, kuru pamatā ir servisa uzturēšana (pieejama, ja ir instalēts Field Service) | Ja šī lauka vērtība interesentam ir iestatīta uz **Balstīts uz darbu**, interesents ir kvalificēts, lai izveidotu projekta iespēju. Uz projektu balstītai iespējai ir nepieciešams iespējot visus projektam specifiskos paplašinājumus un funkcionalitāti šī darījuma lejupstraumes pārdošanas procesā. |
| Vārds | Cilne Vispārīgi | Paredzamā klienta kontaktpersonas vārds | Ja interesents ir kvalificēts, tiek izveidots uzņēmums, kontaktpersona un iespēja. Šeit iestatītā vērtība ir kontaktpersonas vārds. |
| Uzvārds | Cilne Vispārīgi | Paredzamā klienta kontaktpersonas uzvārds | Ja interesents ir kvalificēts, tiek izveidots uzņēmums, kontaktpersona un iespēja. Šeit iestatītā vērtība ir kontaktpersonas uzvārds. |
| Uzņēmums | Cilne Vispārīgi | Paredzamā klienta uzņēmuma nosaukums | Ja interesents ir kvalificēts, tiek izveidots uzņēmums, kontaktpersona un iespēja. Šeit iestatītā vērtība ir izveidotā uzņēmuma nosaukums. |
| Valūta | Detalizētas informācijas cilne | Paredzamā klienta valūta | Ja interesents ir kvalificēts, tiek izveidots uzņēmums, kontaktpersona un iespēja. Šeit iestatītā vērtība ir izveidotā uzņēmuma valūta. |

## <a name="qualify-a-new-project-based-lead"></a>Jauna projekta interesenta kvalificēšana

Interesenti, kuru vērtība **Tips** ir iestatīta uz **Balstīts uz darbu**, tiek saukti par projekta interesentiem. Ja projekta interesents ir kvalificēts, tiek izveidota tālāk norādītā informācija.

- Uzņēmums, kas izmanto lauku **Uzņēmums** no interesenta.
- Kontaktpersonas ieraksts, kas saistīts ar uzņēmumu, pamatojoties uz vērtībām interesenta laukos **Vārds** un **Uzvārds**.
- Projekta iespēja, kuras lauks **Tips** ir iestatīts kā **Balstīts uz darbu**.

Detalizētu informāciju par interesentu kvalificēšanu skatiet tēmā [Interesentu kvalificēšana vai pārvēršana](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Interesenta kvalifikācija un informācija par juridisko personu 

Kad izmantojat Project Operations, izmantojot izvietošanas režīmu, Project Operations scenārijiem, kas balstīti uz resursiem/nav balstīti uz krājumiem, katram klientam un iespējai jāiestata lauku kopa **Atbildīgais uzņēmums**. Atbildīgais uzņēmums ir juridiska persona jūsu organizācijā, kas atbildīga par projekta izpildi. Katram klientam vai uzņēmumam ar klienta attiecību tipu lauka vērtībai **Atbildīgais uzņēmums** ir jābūt iestatītai uz to juridisko personu, kas noslēdz līgumu un ved pārrunas ar šo klientu. Klients var būt piešķirts tikai vienai juridiskajai personai.

Kad interesents tiek kvalificēts, izveidotajiem klientu un iespēju ierakstiem lauku **Atbildīgais uzņēmums** iestata uz pašreizējā lietotāja rezervējamā resursa ieraksta uzņēmumu.

Ja pašreizējā lietotāja rezervējamā resursa ieraksts ir tukšs, klientu un iespēju ierakstiem pēc noklusējuma tiek izmantota lietotāja ieraksta vērtība laukā **Atbildīgais uzņēmums**.

## <a name="business-process-flow-for-project-based-deals"></a>Biznesa procesa plūsma projektu darījumiem

Project Operations projekta darījumiem atbalsta tālāk norādītās biznesa procesu plūsmas.

- Interesenta–iespējas biznesa process
- Iespējas pārdošanas process

Interesenta–iespējas biznesa process atbalsta tālāk uzskaitītos posmus.

| Posma nosaukums | Kartēta entītija | Funkcionalitāte |
| --- | --- | --- |
| Kvalificēt | Interesenti | Kvalificējiet interesentu, lai izveidotu uzņēmumu, kontaktpersonu un/vai iespēju. |
| Izstrādāt | Iespēja | Izstrādājiet iespēju, lai pievienotu papildinformāciju par attiecīgo darbu, galvenajām iesaistītajām personām un konkurenci. |
| Piedāvāt | Iespēja | Izstrādājiet priekšlikumu un saņemiet apstiprinājumu no iekšējās pārbaudes darba grupas. |
| Aizvēršana | Iespēja | Iegūstiet iespēju, lai noslēgtu darījumu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]