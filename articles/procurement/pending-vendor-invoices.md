---
title: Krājumos neesošu materiālu iegāde, izmantojot neapstiprinātu piegādātāju rēķinu
description: Šajā tēmā ir izskaidrots, kā ierakstīt neapstiprinātus piegādātāju rēķinus.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547298"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Krājumos neesošu materiālu iegāde, izmantojot neapstiprinātu piegādātāju rēķinu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Kad uzņēmums projekta vajadzībām veic krājumos neesošu materiālu iepirkumu, izmaksas var nekavējoties reģistrēt saistībā ar šo projektu. 

Piemēram, Contoso Robotics ASV veic aprīkojuma atjaunošanas projektu, un tam ir nepieciešamas programmatūras licences. Šīs licences tiek iegādātas no trešās puses piegādātāja.  Izmantojot Dynamics 365 Finance, kreditoru ierēdnis ieraksta neapstiprinātu piegādātāja rēķina dokumentu un pieskaita licences izmaksas tieši aprīkojuma atjaunošanas projektam. 

> [!IMPORTANT]
> Pirms šajā tēmā aprakstītās funkcionalitātes izmantošanas pārskatiet un lietojiet nepieciešamās konfigurācijas. Papildinformāciju skatiet sadaļā [Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu iespējošana](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Ar projektu saistīta neapstiprināta piegādātāja rēķina grāmatošana 

Neapstiprinātos piegādātāju rēķinus var ierakstīt lapā **Neapstiprinātie piegādātāju rēķini** (**Kreditori** > **Rēķini** > **Neapstiprinātie piegādātāju rēķini**). Lai grāmatotu ar projektu saistītu neapstiprinātu piegādātāja rēķinu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Kreditori** > **Rēķini** un atlasiet **Jauns**. 
2. Laukā **Rēķina konts** atlasiet piegādātāju un laukā **Numurs** ievadiet piegādātāja rēķina identifikatoru.
3. Pievienojiet piegādātāja rēķinam rindu un laukā **Vienuma numurs** atlasiet no piegādātāja iegādāto krājumos neesošo preci. 

    > [!NOTE]
    > Piegādātāja rēķina rindas, kas ir balstītas uz sagādes kategoriju, nevar ierakstīt attiecībā uz projektu. 
    
5. Pievienojiet iegādāto daudzumu. Sistēma aizpilda cenu par vienību, pamatojoties uz krājumos neesošo preču cenas konfigurāciju. 
6. Pārbaudiet kopējo summu un citu rindā nepieciešamo informāciju.
7. Rindas detalizētās informācijas cilnē **Projekts** atlasiet tā projekta ID, kurā šis vienums tiks ierakstīts.
8. Ja vēlaties, atlasiet darbības numuru un atjauniniet projekta kategoriju un rindas rekvizītu.
9. Grāmatojiet neapstiprināto piegādātāja rēķinu. Kad rēķins ir grāmatots, sistēma ieraksta:
    
    - piegādātāja bilances summu;
    - PVN summu.
    - Projekta izmaksas tiek ierakstītas sagādes integrācijas kontā.
    - Projekta faktisko izmaksu transakcija programmā Dataverse.  Šī transakcija tiek apstrādāta tālāk, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Grāmatojot šo žurnālu, summa tiek pārvietota no sagādes integrācijas konta uz projekta izmaksu kontu. 
    - Pirkumi, par kuriem projekta klientam tiek izrakstīti rēķini, izmantojot laika un materiālu norēķinu metodi. Turklāt rēķinā neiekļautajām pārdošanas transakcijām tiek izveidoti pirkumi programmā Dataverse. Preču cenrādis programmā Dataverse tiek izmantots pārdošanas cenām un daudzumiem rēķinā neiekļautajām pārdošanas transakcijām.
