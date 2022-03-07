---
title: Apakšlīgumu galvenes informācija
description: Šajā tēmā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Project Operations apakšlīgumu galvenē.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501335"
---
# <a name="header-details-for-subcontracts"></a>Apakšlīgumu galvenes informācija

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Dynamics 365 Project Operations apakšlīgumu galvenē.

Tā kā projekta vadītājs plāno un izpilda projektus, viņš var nodarbināt apakšuzņēmējus un iegādāties produktus un pakalpojumus no piegādātājiem. Ja projekta vadītājam ir jāiegādājas produkti vai pakalpojumi, viņš var izveidot apakšlīgumu programmā Project Operations.

Lai izveidotu apakšlīgumu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un lapā **Apakšlīgums** atlasiet **Jauns**.
2. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

    Tālāk norādītajā tabulā ir sniegta informācija par laukiem **Apakšlīgumu galvenes** lapā.

    | Lauks | Apraksts |Funkcionālā ietekme |
    |---|------|---| 
    | Nosaukums/vārds, uzvārds | Apakšlīguma nosaukums. | Visos apakšuzņēmēja līguma nolaižamajos sarakstos apakšuzņēmēja līguma nosaukums tiek norādīts pirmajā kolonnā, lai palīdzētu jums identificēt apakšuzņēmēja līgumu. | 
    | Apraksts | Apakšlīgumā iegādāto pakalpojumu un produktu īss apraksts. | Nevienu |
    | Kreditors | Uzņēmuma nosaukums, no kura tiek iegādāti produkti un pakalpojumi. Šim uzņēmuma ierakstam ir attiecību tips **Pārdevējs** vai **Piegādātājs**. | Pamatojoties uz atlasīto piegādātāju, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:<br/> **• Valūta** </br> **• Cenrāži** </br> **• Maksājumu nosacījumi**</br> **• Maksājuma adrese**</br> **• Rēķina adrese**</br> **• Rēķina saņēmēja nosaukums/vārds** </br>**• Piegādātāja kontu vadītājs**|
    | Apakšuzņēmēja līguma datums | Datums, kad ir izveidots apakšuzņēmēja līgums. | Apakšuzņēmēja līgumu datums tiek izmantots, lai atlasītu pareizo cenrādi no cenrāžiem, kas ir pievienoti saistītajam piegādātājam, vai no projekta parametriem. |
    | Statusa iemesls | Apakšlīguma statuss. | Statuss nosaka, kur atrodas apakšuzņēmēja līgums biznesa procesā, un to var rediģēt. <br/>Vērtības ir šādas:<br>• **Melnraksts**: apakšuzņēmēja līgumu var rediģēt. Apakšuzņēmēja līgumus var rediģēt tikai ar statusu **Melnraksts**.<br/>• **Apstiprināts**: ar piegādātāju tiek pabeigts pārrunu process, un apakšuzņēmēja līgums tiek apstiprināts piegādei. <br/>• **Slēgts**: piegāde uz apakšuzņēmēja līgumu ir pabeigta.<br/>• **Atcelts**: apakšuzņēmēja līguma tika atcelts, un piegāde netiek plānota.  | 
    | Valūta | Valūta, kurā tiek iegādāti produkti un pakalpojumi. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta, bet to var mainīt. | Apakšuzņēmēja līguma valūta tiek izmantota, lai atlasītu pareizo cenrādi no cenrāžiem, kas ir pievienoti saistītajam piegādātājam, vai no projekta parametriem. Cenrādi citā valūtā nevar saistīt ar apakšuzņēmēja līgumu. Laika patēriņa, izmaksu un materiālu resursi, ko piegādātājs piegādā saskaņā ar šo apakšuzņēmēja līgumu, projektā tiek ierakstīti šajā valūtā. Pēc apakšuzņēmēja līguma ieraksta saglabāšanas apakšuzņēmēja līguma valūtu nevar mainīt.|
    | Līgumslēdzēja vienība | Uzņēmuma nodaļa, kas noslēdz pirkuma līgumu vai apakšlīgumu ar pārdevēju. | Nevienu |
    | Maksājumu nosacījumi | Maksājumu nosacījumi par piegādātāju rēķiniem, kas tiek izsniegti šajā apakšuzņēmēja līgumā. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājumu nosacījumi no apakšuzņēmēja līguma tiek kopēti uz visiem ar šo apakšuzņēmēja līgumu saistītajiem piegādātāja rēķiniem. Maksājumu nosacījumus var atjaunināt, ja apakšuzņēmēja līguma statuss ir **Melnraksts**. | 
    | Maksājuma adrese | Piegādātāja adrese, uz kuru ir jānosūta maksājumi. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājumu adrese no apakšuzņēmēja līguma tiek kopēta, kā maksājuma adrese visiem šī apakšuzņēmēja līguma izveidotajiem piegādātāja rēķiniem. Maksājumu adresi var atjaunināt, ja apakšuzņēmēja līguma statuss ir **Melnraksts**.|
    | Rēķina saņēmēja nosaukums/vārds | Tās personas vai nodaļas nosaukums pārdevēja uzņēmumā, kas nosūtīs rēķinu. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | **Rēķina saņēmēja nosaukums/vārds** vērtība no apakšuzņēmēja līguma tiek kopēta uz visiem ar šo apakšuzņēmēja līgumu saistītajiem piegādātāja rēķiniem. Šo lauku var atjaunināt, ja apakšuzņēmēja līguma statuss ir **Melnraksts**.|
    | Rēķina adrese | Adrese, kas tiek izmantota pārdevēja rēķinos. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Šī adrese ir adrese "rēķins no" piegādātāju rēķiniem, kas izveidoti šim apakšuzņēmēja līgumam. |
    | Starpsumma | Ja apakšuzņēmēja līgumā nav rindu, ievadiet pasūtījuma starpsummu pirms nodokļiem. Ja apakšlīgumā ir rindas, šis lauks ir tikai lasāms. Parādītā summa ir starpsumma no visām apakšuzņēmēja līguma rindām. | Nevienu |
    | Kopā nodokļi | Ja apakšuzņēmēja līgumā nav rindu, ievadiet šī apakšuzņēmēja līguma kopējo nodokļu summu. Ja apakšlīgumā ir rindas, šis lauks ir tikai lasāms. Parādītā summa ir kopējo nodokļu summa no visām apakšuzņēmēja līguma rindām. | Nevienu |
    | Kopsumma | Šajā aprēķinātajā laukā ir redzama apakšlīguma kopsumma pēc nodokļu iekļaušanas. | Nevienu |
    | Apstiprinātais datums | Datums, kad tika apstiprināts apakšuzņēmēja līgums. | Nevienu |
    | Pieprasīja | Pēc noklusējuma šajā laukā tiek iestatīts tā lietotāja vārds, kurš ir izveidojis šo apakšuzņēmēja līgumu. Tomēr apakšuzņēmēja līguma izveidotājs var mainīt vērtību, lai norādītu personu, kuras vārdā tiek izveidots šis apakšuzņēmēja līgums. | Nevienu |
    | Kreditoru kontu vadītājs | Pārdevēja uzņēmuma primārās kontaktpersonas vārds. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. Kā apakšuzņēmēja līguma piegādātāja konta vadītājs jūs varat atlasīt citu kontaktpersonu. | Jūs varat iestatīt e-pasta brīdinājumus, lai jūs informētu kontaktpersonu par to, kad cenu pārrunu rezultātā tiek veiktas apakšuzņēmēja līguma izmaiņas. |
