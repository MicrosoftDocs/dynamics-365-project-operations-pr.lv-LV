---
title: Projekta ieguldījuma izsekošana
description: Šajā tēmā ir sniegta informācija par to, kā sekot līdzi projekta ieguldījumam un darba norisei.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710949"
---
# <a name="project-effort-tracking"></a>Projekta ieguldījuma izsekošana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Nepieciešamība sekot līdzi grafika gaitai dažādās nozarēs atšķiras. Dažās nozarēs izsekošana notiek ļoti smalkā līmenī, kamēr citās nozarēs izsekošana tiek veikta augstākā līmenī. Šajā tēmā ir parādīts, kā veikt plānošanu, lai izpildītu jūsu organizācijas prasības.

## <a name="effort-tracking-view"></a>Piepūles izsekošanas skats

Skats **Piepūles izsekošana** izseko uzdevumu progresu grafikā, salīdzinot faktiskās ieguldījuma stundas, kas tiek patērētas uzdevumam, ar plānotajām ieguldījuma stundām. Dynamics 365 Project Operations, lai aprēķinātu izsekošanas metriku, programmatūrā, izmanto tālāk norādītās formulas.

- **Progresa procentuālā vērtība**: līdz šim veiktā piepūle + novērtējums beigu stadijā (EAC) 
- **Atlikušais ieguldījums**: galīgā ieguldījuma novērtējums – faktiskais ieguldījums līdz konkrētajam datumam 
- **EAC**: Atlikusī piepūle + Līdz šim veiktā piepūle 
- **Projektētā piepūles novirze**: Plānotā piepūle – EAC

Programmatūrā Project Operations uzdevumam tiek rādīta projektētā piepūles novirze. Ja EAC ir lielāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs vairāk laika, nekā sākotnēji plānots, un tas atpaliek no grafika. Ja EAC ir mazāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs mazāk laika, nekā sākotnēji plānots, un tas ir pirms grafika.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Ieguldījuma pārplānošana lapas mezgla uzdevumos

Projektu vadītāji bieži pārskata sākotnējās uzdevumu aplēses. Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu. Tomēr projekta vadītājiem nav ieteicams mainīt plānotā ieguldījuma datus. Tas ir tāpēc, ka projekta plānotais ieguldījums ir projekta grafika un izmaksu aprēķina patiesās informācijas avots, kā arī visi projekta dalībnieki ir tam piekrituši.

Projekta vadītājs var pārplānot ieguldījumu kopsavilkuma uzdevumos, atjauninot **atlikušā ieguldījuma** noklusējuma vērtību ar jaunu aprēķinu. Šādas atjaunināšanas rezultātā tiek pārrēķināts uzdevuma galīgais ieguldījuma novērtējums, norises procentuālā daļa un paredzamā ieguldījuma novirze. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Piepūles pārprojektēšana kopsavilkuma uzdevumiem

Piepūli kopsavilkuma uzdevumiem vai konteinera uzdevumiem var pārprojektēt. Projektu vadītāji var atjaunināt kopsavilkuma uzdevumu atlikušo ieguldījumu. Atjauninot atlikušo ieguldījumu, lietojumprogrammā tiek aktivizēta šāda aprēķinu kopa:

- Uzdevumam tiek aprēķināts EAC un progresa procentuālais daudzums.
- Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējais EAC tika sadalīts uz uzdevumu.
- Tiek aprēķināts jaunais EAC katram atsevišķajam uzdevumam līdz pat lapas mezgla uzdevumiem. 
- Ietekmētajiem pakārtotajiem uzdevumiem lejup pa lapas mezgliem tiek pārrēķināts to atlikušais ieguldījums un progresa procentuālais daudzums, pamatojoties uz EAC vērtību. Šādi uzdevumam tiek iegūta jauna piepūles novirzes projektēšana. 
- Tiek pārrēķināti kopsavilkuma uzdevumu EAC visiem uzdevumiem līdz saknes mezglam.


## <a name="project-status-summary"></a>Projekta noteikta kopsavilkums

Izsekošanas dati skatā **Piepūles izsekošana** un **Izmaksu izsekošana** rāda progresu un izmaksu patēriņu projekta saknes mezgla, kopsavilkuma uzdevumu un lapas mezgla uzdevumu līmeņos. Lapas **Projekta entītija** sadaļā **Statuss** tiek rādīts projekta līmeņa statusa kopsavilkums.

## <a name="status-summary-fields"></a>Statusa kopsavilkuma lauki

Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss. Tajā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku. Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu. Lauku **Statusa atjaunināšanas laiks** nevar rediģēt, un tā vērtība ir laikspiedols, kas norāda, kad statuss tika atjaunināts pēdējo reizi.

Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas datuma. Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šos laukus varat iestatīt uz **Apsteidz**. Ja grafika un izmaksu novirze saknes mezglam ir negatīva, varat tos iestatīt uz **Atpaliek**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
