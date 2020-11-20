---
title: Jaunināšanas sākumlapa
description: Šajā tēmā parādīts, kur meklēt svarīgu informāciju par jaunām un izmainītām funkcijām programmā Dynamics 365 Project Service Automation, kā arī par procesu jaunināšanai uz jaunāko versiju.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121767"
---
# <a name="upgrade-home-page"></a>Jaunināšanas sākumlapa

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Jaunināšana no PSA versijas 2.x vai 1.x uz versiju 3.x

### <a name="new-instances"></a>Jaunas instances

No 2019. gada 17. maija, atlasot Project Service Automation jaunas instances nodrošināšanas laikā, versija 3.x tiek instalēta pēc noklusējuma.

### <a name="existing-instances"></a>Esošās instances

Iepriekš klienti, kam ir PSA versijas 2.x instance un kam tā jājaunina uz versiju 3.x, kas ir Apvienotā uz klienta interfeisa balstītā (UCI) PSA versija, bija jāsazinās ar Microsoft atbalsta dienestu un jāsniedz papildinformācija par savu instanci, lai atbalsts varētu palīdzēt veikt jaunināšanu uz versiju 3.x. Sākot ar 2020. gada 1. martu klienti, kam ir PSA versijas 2.x instance un kam tā jājaunina uz versiju 3.x, varēs jaunināt savas instances tieši no administratora portāla, un viņiem nebūs jāsazinās ar Microsoft atbalsta dienestu.  

> [!NOTE]
> PSA versija 3.x ietver būtiskas izmaiņas. Tā ir izveidota, izmantojot vienotā interfeisa struktūru, lai palīdzētu nodrošināt uzlabotu lietotāja pieredzi. Pārveidotajā lietojumprogrammā ir nodrošināts konsekvents, vienots lietotāja interfeiss (UI), kā arī reaģējošie noformējuma principi optimālai skatīšanai jebkāda izmēra ekrānā vai ierīcē. Lietojumprogrammā ir veiktas arī citas izmaiņas. Daži no izmainītajiem apgabaliem ietver cenu noteikšanu, rezervāciju un resursu piešķiršanu, laiku, izdevumus un apstiprinājumus.

Pirms jaunināšanas procesa sākšanas ieteicams izpildīt tālāk norādītos uzdevumus.

- Pārbaudiet, vai Dynamics 365 Field Service un Project Service Automation ir instalēti noteiktajā instancē. Ja ir instalēti abi risinājumi, jums ir jāplāno to jaunināšana, pirms atsākat regulāru instances lietošanu.
- Rūpīgi pārskatiet tālāk norādītās tēmas. Izpratne par izmaiņām versijās palīdzēs jums jaunināšanas procesā. Šīs tēmas sniedz informāciju par lielākajām izmaiņām programmā PSA kopā ar apsvērumiem un ieteikumiem, lai plānotu jaunināšanu uz versiju 3. x.

    - [Kas jauns vai mainīts Project Service Automation 3. versijā](whats-new-changed-v3.md)
    - [Jaunināšanas apsvērumi – Project Service Automation versijas 2.x vai 1.x uz versiju 3.x](upgrade-v3.md)

- Jauniniet savu smilškastes instanci, lai novērtētu veiktās ieviešanas izmaiņas pirms ražošanas instances jaunināšanas.

Pēc tam, kad būsit pārskatījis jau iepriekš minētās tēmas un esat gatavs veikt jaunināšanu uz PSA versiju 3.x vai uz UCI balstītu versiju, iesniedziet pieprasījumu Microsoft atbalstam, lai padarītu jaunināšanu pieejamu no administratora centra. Pieprasījumā norādiet detalizētu informāciju par savu instanci.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Vecāku versiju PSA (PSA versija 2.x) no jauna izveidotajā instancē

No 2019. gada 17. maija visas jaunās instancēs UCI būs iekļauts kā noklusējuma klients. Attiecībā uz saskaņošanu ar šīm izmaiņām, PSA versija 3.x un Field Service versija 8.x tiks nodrošinātas pēc noklusējuma, jo šīs versijas ir paredzētas darbam ar UCI klientu.

Sākot ar 2020. gada 1. martu Dynamics PSA klienti vairs nevarēs izveidot jaunas vides, izmantojot vecākas PSA versijas, piemēram, PSA versiju 2.x vai vecāku. Jebkura jaunā vide būs pieejama tikai ar PSA versiju 3.x.

> [!NOTE]
> Lai varētu izmantot labākās iespējas, lietojot vecākas Field Service un PSA lietojumprogrammu versijas, pārejiet uz lapu **Sistēmas iestatījumi** un laukam **Izmantot tikai jauno vienoto interfeisu (ieteicams)** atlasiet **Nē**, jo šīs versijas nav paredzētas pareizai ielādēšanai UCI. Pēc UCI izslēgšanas varat atvērt un palaist šīs Field Service un PSA versijas, izmantojot veco tīmekļa klientu. 
