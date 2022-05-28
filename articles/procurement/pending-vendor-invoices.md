---
title: Neuzkrātu materiālu vai sagādes kategoriju pirkšana, izmantojot neizlemtu kreditora rēķinu
description: Šajā tēmā ir izskaidrots, kā ierakstīt neapstiprinātus piegādātāju rēķinus.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612666"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Neuzkrātu materiālu vai sagādes kategoriju pirkšana, izmantojot neizlemtu kreditora rēķinu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Tā kā uzņēmums projektam iepērk neuzkrātus materiālus vai iepirkuma kategorijas, izmaksas var nekavējoties reģistrēt, salīdzinot ar projektu. 

Piemēram, Contoso Robotics ASV veic aprīkojuma atjaunošanas projektu, un tam ir nepieciešamas programmatūras licences. Šīs licences tiek iegādātas no trešās puses piegādātāja.  Izmantojot Dynamics 365 Finance, kreditoru darbinieks reģistrē gaidošo piegādātāja rēķina dokumentu un saista licences izmaksas tieši ar aprīkojuma atjaunošanas projektu. 

> [!IMPORTANT]
> Pirms šajā tēmā aprakstītās funkcionalitātes izmantošanas pārskatiet un lietojiet nepieciešamās konfigurācijas. Plašāku informāciju skatiet Enabling [non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md) and [Use procurement categories with project purchase orders and pending vendor invoices](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Ar projektu saistīta neapstiprināta piegādātāja rēķina grāmatošana 

Neapstiprinātos piegādātāju rēķinus var ierakstīt lapā **Neapstiprinātie piegādātāju rēķini** (**Kreditori** > **Rēķini** > **Neapstiprinātie piegādātāju rēķini**). Lai grāmatotu ar projektu saistītu neapstiprinātu piegādātāja rēķinu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Kreditoru** > **rēķini** un atlasiet **Jauns**. 
1. Laukā **Rēķina konts** atlasiet piegādātāju un pēc tam **laukā Numurs** ievadiet kreditora rēķina identifikāciju.
1. Pievienojiet rindu kreditora rēķinam un pēc tam **laukā Preces numurs** atlasiet neuzkrāto preci, kas iegādāta no piegādātāja. **Vai arī laukā Iepirkuma kategorija** atlasiet sagādes kategoriju, kas iegādāta no kreditora.   
1. Pievienojiet iepirkto daudzumu. Sistēma aizpilda vienības cenu, pamatojoties uz neuzkrāto krājumu cenu konfigurāciju. 
1. Pārbaudiet kopējo summu un citu rindā nepieciešamo informāciju.
1. Rindas detaļās **cilnē Projekts** atlasiet tā projekta ID, kurā šis vienums tiks ierakstīts.
1. Neobligāti: atlasiet aktivitātes numuru un atjauniniet projekta kategoriju un rindas rekvizītu.
1. Grāmatojiet gaidošo kreditora rēķinu. Grāmatojot rēķinu, sistēma reģistrē šādu informāciju:
    
    - piegādātāja bilances summu;
    - PVN summu.
    - Projekta izmaksas tiek ierakstītas sagādes integrācijas kontā.
    - Projekta faktisko izmaksu transakcija programmā Dataverse.  Šī transakcija tiek apstrādāta tālāk, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Grāmatojot šo žurnālu, summa tiek pārvietota no sagādes integrācijas konta uz projekta izmaksu kontu. 
    - Pirkumi, par kuriem projekta klientam tiek izrakstīti rēķini, izmantojot laika un materiālu norēķinu metodi. Turklāt rēķinā neiekļautajām pārdošanas transakcijām tiek izveidoti pirkumi programmā Dataverse. Preču cenrādis programmā Dataverse tiek izmantots pārdošanas cenām un daudzumiem rēķinā neiekļautajām pārdošanas transakcijām.
