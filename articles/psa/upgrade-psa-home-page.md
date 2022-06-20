---
title: Jaunināšanas sākumlapa
description: Šajā rakstā ir parādīts, kur atrast svarīgu informāciju par jaunajiem un mainītajiem līdzekļiem programmā Dynamics 365 Project Service Automation un procesu jaunināšanai uz jaunāko versiju.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5dcf41af31a60b952ce82c08e3c082490d59d4f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926647"
---
# <a name="upgrade-home-page"></a>Jaunināšanas sākumlapa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Jaunināšana no PSA versijas 2.x vai 1.x uz versiju 3.x

### <a name="new-instances"></a>Jaunas instances

No 2019. gada 17. maija, atlasot Project Service Automation jaunas instances nodrošināšanas laikā, versija 3.x tiek instalēta pēc noklusējuma.

### <a name="existing-instances"></a>Esošās instances

Iepriekš klienti, kam ir PSA versijas 2.x instance un kam tā bija jājaunina uz versiju 3.x, kas ir Apvienotā uz klienta interfeisa balstītā (UCI) PSA versija, bija jāsazinās ar Microsoft atbalsta dienestu un jāsniedz papildinformācija par savu instanci, lai atbalsts varētu palīdzēt veikt jaunināšanu uz versiju 3.x. No 2020. gada 1. marta klienti, kuriem ir instance ar PSA versiju 2.x un ir jājaunina uz versiju 3.x, varēs jaunināt savas instances tieši no administratora portāla bez vajadzības sazināties ar Microsoft atbalsta dienestu.  

> [!NOTE]
> PSA versija 3.x ietver būtiskas izmaiņas. Tā ir izveidota, izmantojot vienotā interfeisa struktūru, lai palīdzētu nodrošināt uzlabotu lietotāja pieredzi. Pārveidotajā lietojumprogrammā ir nodrošināts konsekvents, vienots lietotāja interfeiss (UI), kā arī reaģējošie noformējuma principi optimālai skatīšanai jebkāda izmēra ekrānā vai ierīcē. Lietojumprogrammā ir veiktas arī citas izmaiņas. Daži no izmainītajiem apgabaliem ietver cenu noteikšanu, rezervāciju un resursu piešķiršanu, laiku, izdevumus un apstiprinājumus.

Pirms jaunināšanas procesa sākšanas ieteicams izpildīt tālāk norādītos uzdevumus.

- Pārbaudiet, vai Dynamics 365 Field Service un Project Service Automation ir instalēti noteiktajā instancē. Ja ir instalēti abi risinājumi, jums ir jāplāno to jaunināšana, pirms atsākat regulāru instances lietošanu.
- Rūpīgi izlasiet tālāk sniegtos rakstus. Izpratne par izmaiņām versijās palīdzēs jums jaunināšanas procesā. Šajos rakstos ir sniegta informācija par galvenajām PSA izmaiņām, kā arī apsvērumi un ieteikumi, kā plānot jaunināšanu uz versiju 3.x.

    - [Kas jauns vai mainīts Project Service Automation 3. versijā](whats-new-changed-v3.md)
    - [Jaunināšanas apsvērumi – Project Service Automation versijas 2.x vai 1.x uz versiju 3.x](upgrade-v3.md)

- Jauniniet savu smilškastes instanci, lai novērtētu veiktās ieviešanas izmaiņas pirms ražošanas instances jaunināšanas.

Pēc tam, kad esat pārskatījis iepriekš minētos rakstus un esat gatavs jaunināšanai uz PSA versiju 3.x vai UCI versiju, iesniedziet pieprasījumu Microsoft atbalstam, lai jaunināšana būtu pieejama administrēšanas centrā. Pieprasījumā norādiet detalizētu informāciju par savu instanci.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Vecāku versiju PSA (PSA versija 2.x) no jauna izveidotajā instancē

No 2019. gada 17. maija visas jaunās instancēs UCI būs iekļauts kā noklusējuma klients. Attiecībā uz saskaņošanu ar šīm izmaiņām, PSA versija 3.x un Field Service versija 8.x tiks nodrošinātas pēc noklusējuma, jo šīs versijas ir paredzētas darbam ar UCI klientu.

Sākot ar 2020. gada 1. martu Dynamics PSA klienti vairs nevarēs izveidot jaunu vidi ar vecākām PSA versijām, piemēram, PSA versiju 2.x vai jaunāku. Jebkura jaunā vide būs pieejama tikai ar PSA versiju 3.x.

> [!NOTE]
> Lai varētu izmantot labākās iespējas, lietojot vecākas Field Service un PSA lietojumprogrammu versijas, pārejiet uz lapu **Sistēmas iestatījumi** un laukam **Izmantot tikai jauno vienoto interfeisu (ieteicams)** atlasiet **Nē**, jo šīs versijas nav paredzētas pareizai ielādēšanai UCI. Pēc UCI izslēgšanas varat atvērt un palaist šīs Field Service un PSA versijas, izmantojot veco tīmekļa klientu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
