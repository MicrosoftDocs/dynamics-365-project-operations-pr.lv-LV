---
title: Apakšlīgumu galvenes informācija
description: Šajā tēmā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Project Operations apakšlīgumu galvenē.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323650"
---
# <a name="header-details-for-subcontracts"></a>Apakšlīgumu galvenes informācija

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Dynamics 365 Project Operations apakšlīgumu galvenē.

Tā kā projekta vadītājs plāno un izpilda projektus, viņš var nodarbināt apakšuzņēmējus un iegādāties produktus un pakalpojumus no piegādātājiem. Ja projekta vadītājam ir jāiegādājas produkti vai pakalpojumi, viņš var izveidot apakšlīgumu programmā Project Operations.

Lai izveidotu apakšlīgumu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un lapā **Apakšlīgums** atlasiet **Jauns**.
2. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

    Tālāk redzamajā tabulā ir sniegta informācija par laukiem apakšlīgumu galvenes lapā.

    | **Lauks** | **Apraksts** |
    | --- | --- | 
    | Nosaukums/vārds, uzvārds | Apakšlīguma nosaukums. |
    | Apraksts | Apakšlīgumā iegādāto pakalpojumu un produktu īss apraksts. |
    | Kreditors | Uzņēmuma nosaukums, no kura tiek iegādāti produkti un pakalpojumi. Šim uzņēmuma ierakstam ir attiecību tips **Pārdevējs** vai **Piegādātājs**. |
    | Apakšuzņēmēja līguma datums | Apakšlīguma izveides datums. |
    | Statusa iemesls | Apakšlīguma statuss. |
    | Valūta | Produktu un pakalpojumu iegādes valūta. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma, bet to var mainīt. Projekta cenrāžiem, kas tiek izmantoti produktu un pakalpojumu cenu noteikšanai apakšlīgumā, ir jābūt šajā valūtā. Ar šo apakšlīgumu nevar saistīt cenrāžus citās valūtās. Šajā apakšlīgumā radušās produktu un pakalpojumu izmaksas tiek ierakstītas projektā šajā valūtā. |
    | Līgumslēdzēja vienība | Uzņēmuma nodaļa, kas noslēdz pirkuma līgumu vai apakšlīgumu ar pārdevēju. |
    | Maksājumu nosacījumi | Maksājumu nosacījumi, kas attiecas uz pārdevēju rēķiniem, kas tiek izdoti šim apakšlīgumam. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma ieraksta. |
    | Maksājuma adrese | Adrese, uz kurieni tiek nosūtīts maksājumi par pārdevēju rēķiniem. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma ieraksta. |
    | Rēķina saņēmēja nosaukums/vārds | Tās personas vai nodaļas nosaukums pārdevēja uzņēmumā, kas nosūtīs rēķinu. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma ieraksta un tiek izmantota kā primārās kontaktpersonas nosaukums pārdevēju rēķinos, kas izveidoti šim apakšlīgumam. |
    | Norēķinu adrese | No šī pārdevēja saņemtajos rēķinos izmantotā adrese. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma ieraksta. Šī adrese tiek izmantota arī kā rēķina nosūtīšanas adrese pārdevēju rēķinos, kas izveidoti šim apakšlīgumam. |
    | Starpsumma | Ja apakšlīgumā nav rindu, ievadiet vērtību šajā laukā, kas norāda pasūtījuma starpsummu pirms nodokļiem. Ja apakšlīgumā ir rindas, šis lauks ir tikai lasāms. Parādītā summa ir visu apakšlīguma rindu starpsumma. |
    | Kopā nodokļi | Ja apakšlīgumā nav rindu, ievadiet vērtību šajā laukā, kas norāda šī apakšlīguma nodokļu summu. Ja apakšlīgumā ir rindas, šis lauks ir tikai lasāms. Parādītā summa ir visu apakšlīguma rindu nodokļu summa. |
    | Kopsumma |  Šajā aprēķinātajā laukā ir redzama apakšlīguma kopsumma pēc nodokļu iekļaušanas.  |
    | Apstiprinātais datums | Apakšlīguma apstiprināšanas datums.  |
    | Pieprasīja | Šī lauka vērtība pēc noklusējuma tiek nodēvēta tā lietotāja vārdā, kas izveidojis šo apakšlīgumu. Apakšlīguma izveidotājs šo vērtību var mainīt, lai norādītu personu, kā vārdā tas veido apakšlīgumu.  |
    | Kreditoru kontu vadītājs | Pārdevēja uzņēmuma primārās kontaktpersonas vārds. Šī lauka vērtība pēc noklusējuma tiek izgūta no pārdevēja uzņēmuma ieraksta. Lietotājs šo lauka vērtību var mainīt, lai atlasītu citu kontaktpersonu kā apakšlīguma pārdevēja uzņēmuma vadītāju. Šī kontaktpersona var konfigurēt un nosūtīt e-pasta brīdinājumus un cenu apspriešanu. |


