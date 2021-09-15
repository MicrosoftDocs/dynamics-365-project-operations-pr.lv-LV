---
title: Apakšlīgumu izveide 2021. oktobrī — agrīnās piekļuves laidiens
description: Šajā tēmā ir sniegts pārskats par apakšlīgumu slēgšanas iespējām programmā Project Operations, kas ir daļa no 2021. gada oktobra agrīnās piekļuves laidiena.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383704"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Apakšlīgumu izveide 2021. oktobrī — agrīnās piekļuves laidiens

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir sniegts pārskats par apakšlīgumu slēgšanas iespējām programmā Dynamics 365 Project Operations, kas ir daļa no 2021. gada oktobra agrīnās piekļuves laidiena. Šī līdzekļu kopa nav gatava ražošanai vai tiešsaistes videi, tādēļ šie līdzekļi saglabāsies agrīnās piekļuves laidienā, līdz tiks izlaista pilnā līdzekļu kopa. Stingri ieteicams neizmantot apakšlīgumu slēgšanas līdzekļu kopu tiešsaistes ražošanas scenārijiem, kamēr nav noņemts priekšskatījuma reklāmkarogs. 

Šajā sarakstā ir sniegts apraksts par to, kas pašlaik ir pieejams 2021. gada oktobra agrīnās piekļuves laidienā.

1. Projekta vadītājs izveido apakšlīgumu ar pārdevēju. Pēc noklusējuma apakšlīgumam tiek izmantoti pārdevēja ierakstam pievienotie cenrāži. Pārdevēja uzņēmuma attiecību tips ir **Pārdevējs** vai **Piegādātājs**.

2. Projekta vadītājs var norādīt visus pirkumus kā apakšlīguma rindas elementus. Apakšlīguma rindas var būt laiks, izmaksas vai produkti. Apakšlīguma rindas transakciju klase nosaka, kam šī rinda ir paredzēta.

3. Pārdevēja uzņēmuma pārvaldnieks un projekta vadītājs var atkārtoti veikt darbības apakšlīgumā. Cenu noteikšanu var pielāgot apakšlīgumam pievienotajos pirkumu cenrāžos.

4. Šajā posmā vai vēlāk procesā, ja apakšlīguma rinda paredzēta laikam, pārdevēja uzņēmuma pārvaldnieks saista pārdevēja kontaktpersonas ar katru apakšlīguma rindu. Šī saistība nodrošina informāciju projekta vadītājam, kurš strādā pie apakšlīguma izveides. Kad pārdevēja kontaktpersona ir saistīta ar apakšlīguma rindu, sistēma automātiski izveido rezervējamu resursu no kontaktpersonas, ja rezervējamais resurss vēl nepastāv.

5. Katras apakšlīguma rindas norēķinu metode var būt **Fiksēta cena** vai **Laiks un materiāli**. Fiksētas cenas apakšlīgumu rindām tiek iestatīts uz atskaites punktu balstīts rēķinu grafiks.

Pārējās pārskatā izklāstītās biznesa procesa plūsmas darbības apakšlīgumu slēgšanai pašlaik nav pieejamas. Pievienojot jaunu funkcionalitāti, šī tēma tiks atjaunināta. 

Tālāk redzamajā ilustrācijā parādīts Apakšlīgumu slēgšanas agrīnās piekļuves laidiens pretstatā biznesa procesam no sākuma līdz beigām.

![Apakšlīgumu slēgšanas procesa plūsma](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Uz daudzumu balstītu un uz darbu balstītu apakšlīgumu rindu agrīnās piekļuves laidiens
2021. gada oktobra agrīnās piekļuves laidienā tiek atbalstītas tikai uz daudzumu balstītās apakšlīguma rindas. Tas nozīmē, ka apakšlīguma rindu var izmantot, lai no pārdevēja iegādātos laiku, izdevumus vai materiālus, bet ne visu darba kopumu. Tas nozīmē arī to, ka apakšlīguma rindā pirkto daudzumu (laika vienības, izmaksas vai materiālu daudzumu), var izmantot jebkurā sistēmas projektā.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
