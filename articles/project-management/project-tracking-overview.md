---
title: Projekta izsekošanas pārskats
description: Šajā tēmā ir sniegta informācija par to, kā sekot līdzi projekta progresam un izmaksu patēriņam.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127367"
---
# <a name="project-tracking-overview"></a>Projekta izsekošanas pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Nepieciešamība sekot līdzi grafika gaitai dažādās nozarēs atšķiras. Dažās nozarēs izsekošana notiek ļoti smalkā līmenī, kamēr citās nozarēs izsekošana tiek veikta augstākā līmenī. Šajā tēmā ir parādīts, kā veikt plānošanu, lai izpildītu jūsu organizācijas prasības.

## <a name="effort-tracking-view"></a>Piepūles izsekošanas skats

Skats **Piepūles izsekošana** izseko uzdevumu progresu grafikā, salīdzinot faktiskās ieguldījuma stundas, kas tiek patērētas uzdevumam, ar plānotajām ieguldījuma stundām. Lai aprēķinātu izsekošanas metriku, programmatūrā Dynamics 365 Project Operations tiek izmantotas tālāk norādītās formulas.

- **Progresa procentuālā vērtība**: līdz šim veiktā piepūle + novērtējums beigu stadijā (EAC) 
- **Novērtējums līdz pabeigšanai (ETC)**: Plānotā piepūle – Līdz šim faktiski patērētā piepūle 
- **EAC**: Atlikusī piepūle + Līdz šim veiktā piepūle 
- **Projektētā piepūles novirze**: Plānotā piepūle – EAC

Programmatūrā Project Operations uzdevumam tiek rādīta projektētā piepūles novirze. Ja EAC ir lielāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs vairāk laika, nekā sākotnēji plānots, un tas atpaliek no grafika. Ja EAC ir mazāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs mazāk laika, nekā sākotnēji plānots, un tas ir pirms grafika.

## <a name="reprojecting-effort"></a>Piepūles pārprojektēšana

Projektu vadītāji bieži pārskata sākotnējās uzdevumu aplēses. Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu. Taču projektu vadītājiem nav ieteicams mainīt bāzlīnijas skaitļus. Iemesls ir tāds, ka projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.

Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos:

- Pārlabot noklusējuma ETC ar jaunu uzdevumam faktiski atlikušās piepūles novērtējumu. 
- Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.

Katra no šīm metodēm izraisa uzdevuma ETC, EAC, progresa procentuālā daudzuma pārrēķināšanu un uzdevumam projektētās piepūles novirzes pārrēķināšanu. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Piepūles pārprojektēšana kopsavilkuma uzdevumiem

Piepūli kopsavilkuma uzdevumiem vai konteinera uzdevumiem var pārprojektēt. Neatkarīgi no tā, vai lietotājs pārprojektēšanu veic, kopsavilkuma uzdevumiem izmantojot atlikušo piepūli vai progresa procentuālo daudzumu, sākas tālāk norādīto aprēķinu kopa.

- Uzdevumam tiek aprēķināts EAC, ETC un progresa procentuālais daudzums.
- Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējais EAC tika sadalīts uz uzdevumu.
- Tiek aprēķināts jaunais EAC katram atsevišķajam uzdevumam līdz pat lapas mezgla uzdevumiem. 
- Ietekmētajiem pakārtotajiem uzdevumiem lejup pa lapas mezgliem tiek pārrēķināts to ETC un progresa procentuālais daudzums, pamatojoties uz EAC vērtību. Šādi uzdevumam tiek iegūta jauna piepūles novirzes projektēšana. 
- Tiek pārrēķināti kopsavilkuma uzdevumu EAC visiem uzdevumiem līdz saknes mezglam.

### <a name="cost-tracking-view"></a>Izmaksu izsekošanas skats 

Skatā **Izmaksu izsekošana** faktiskās izmaksas, kuras tika iztērētas uz uzdevumu, tiek salīdzinātas ar plānotajām uzdevuma izmaksām. 

> [!NOTE]
> Šajā skatā tiek rādītas tikai darbaspēka izmaksas, un nav iekļautas izmaksas no izdevumu tāmēm. Lai aprēķinātu izsekošanas metriku, programmatūrā Project Operations tiek izmantotas tālāk norādītās formulas.

- **Patērēto izmaksu procentuālais daudzums**: Līdz šim faktiski iztērētās izmaksas ÷ Novērtētās izmaksas beigu stadijā
- **Izmaksas līdz pabeigšanai (CTC)**: Plānotās izmaksas – Līdz šim faktiski iztērētās izmaksas
- **EAC**: Atlikušās izmaksas + Līdz šim faktiski iztērētās izmaksas
- **Projektētā izmaksu novirze**: Plānotās izmaksas – EAC

Uzdevumam tiek rādīta projektētā izmaksu novirze. Ja EAC ir lielāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās vairāk, nekā sākotnēji tika plānots. Tādēļ tam ir tendence pārsniegt budžetu. Ja EAC ir mazāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās mazāk, nekā sākotnēji tika plānots. Tādēļ tam ir tendence iekļauties budžetā.

## <a name="project-managers-reprojection-of-cost"></a>Projektu vadītāja veiktā izmaksu pārprojektēšana

Kad notiek piepūles pārprojektēšana, skatā **Izmaksu izsekošana** tiek pārrēķināts CTC, EAC, patērēto izmaksu procentuālais daudzums un projektētā izmaksu nobīde.

## <a name="project-status-summary"></a>Projekta noteikta kopsavilkums

Izsekošanas dati skatā **Piepūles izsekošana** un **Izmaksu izsekošana** rāda progresu un izmaksu patēriņu projekta saknes mezgla, kopsavilkuma uzdevumu un lapas mezgla uzdevumu līmeņos. Lapas **Projekta entītija** sadaļā **Statuss** tiek rādīts projekta līmeņa statusa kopsavilkums.

## <a name="status-summary-fields"></a>Statusa kopsavilkuma lauki

Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss. Tajā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku. Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu. Lauku **Statusa atjaunināšanas laiks** nevar rediģēt, un tā vērtība ir laikspiedols, kas norāda, kad statuss tika atjaunināts pēdējo reizi.

Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas datuma. Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šos laukus varat iestatīt uz **Apsteidz**. Ja grafika un izmaksu novirze saknes mezglam ir negatīva, varat tos iestatīt uz **Atpaliek**.
