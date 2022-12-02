---
title: Krājumos neesošu materiālu vai iepirkuma kategoriju iegāde, izmantojot neapstiprinātu piegādātāju rēķinu
description: Šajā rakstā ir izskaidrots, kā ierakstīt neapstiprinātus piegādātāju rēķinus.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922001"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Krājumos neesošu materiālu vai iepirkuma kategoriju iegāde, izmantojot neapstiprinātu piegādātāju rēķinu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Kad uzņēmums projekta vajadzībām veic krājumos neesošu materiālu vai iepirkumu kategoriju iepirkumu, izmaksas var nekavējoties reģistrēt saistībā ar šo projektu. 

Piemēram, Contoso Robotics ASV veic aprīkojuma atjaunošanas projektu, un tam ir nepieciešamas programmatūras licences. Šīs licences tiek iegādātas no trešās puses piegādātāja.  Izmantojot Dynamics 365 Finance, kreditoru ierēdnis ieraksta neapstiprinātu piegādātāja rēķina dokumentu un pieskaita licences izmaksas tieši aprīkojuma atjaunošanas projektam. 

> [!IMPORTANT]
> Pirms šajā rakstā aprakstītās funkcionalitātes izmantošanas pārskatiet un lietojiet nepieciešamās konfigurācijas. Papildinformāciju skatiet sadaļā [Krājumā neesošu materiālu un neapmaksātu piegādātāju rēķinu iespējošana](configure-materials-nonstocked.md) un [Iepirkuma kategoriju lietošana ar projekta pirkuma pasūtījumiem un neapmaksātiem piegādātāju rēķiniem](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Ar projektu saistīta neapstiprināta piegādātāja rēķina grāmatošana 

Neapstiprinātos piegādātāju rēķinus var ierakstīt lapā **Neapstiprinātie piegādātāju rēķini** (**Kreditori** > **Rēķini** > **Neapstiprinātie piegādātāju rēķini**). Lai grāmatotu ar projektu saistītu neapstiprinātu piegādātāja rēķinu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Kreditori** > **Rēķini** un atlasiet **Jauns**. 
1. Laukā **Rēķina konts** atlasiet piegādātāju un laukā **Numurs** ievadiet piegādātāja rēķina identifikatoru.
1. Pievienojiet piegādātāja rēķinam rindu un laukā **Vienuma numurs** atlasiet no piegādātāja iegādāto krājumos neesošo preci. Varat arī laukā **Iepirkuma kategorija** atlastīt no piegādātāja iegādātā iepirkuma kategoriju.   
1. Pievienojiet iegādāto daudzumu. Sistēma aizpilda cenu par vienību, pamatojoties uz krājumos neesošo preču cenas konfigurāciju. 
1. Pārbaudiet kopējo summu un citu rindā nepieciešamo informāciju.
1. Rindas detalizētās informācijas cilnē **Projekts** atlasiet tā projekta ID, kurā šis vienums tiks ierakstīts.
1. Ja vēlaties, atlasiet darbības numuru un atjauniniet projekta kategoriju un rindas rekvizītu.
1. Grāmatojiet neapstiprināto piegādātāja rēķinu. Pēc rēķina iegrāmatošanas sistēma reģistrē tālāk uzskaitīto informāciju:
    
    - piegādātāja bilances summu;
    - PVN summu.
    - Projekta izmaksas tiek ierakstītas sagādes integrācijas kontā.
    - Projekta faktisko izmaksu transakcija programmā Dataverse.  Šī transakcija tiek apstrādāta tālāk, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Grāmatojot šo žurnālu, summa tiek pārvietota no sagādes integrācijas konta uz projekta izmaksu kontu. 
    - Pirkumi, par kuriem projekta klientam tiek izrakstīti rēķini, izmantojot laika un materiālu norēķinu metodi. Turklāt rēķinā neiekļautajām pārdošanas transakcijām tiek izveidoti pirkumi programmā Dataverse. Preču cenrādis programmā Dataverse tiek izmantots pārdošanas cenām un daudzumiem rēķinā neiekļautajām pārdošanas transakcijām.
