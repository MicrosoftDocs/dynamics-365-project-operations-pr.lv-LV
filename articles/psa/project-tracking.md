---
title: Projekta norise un izmaksu patēriņš
description: Šajā rakstā ir sniegta informācija par projekta progresa un izmaksu patēriņa izsekošanu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: afcac5e6fbb7ed8a5a5f7f5876c6035b59eebcc2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921771"
---
# <a name="project-progress-and-cost-consumption"></a>Projekta norise un izmaksu patēriņš

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nepieciešamība sekot līdzi grafika gaitai dažādās nozarēs atšķiras. Dažās nozarēs izsekošana notiek ļoti smalkā līmenī, turpretī citās nozarēs izsekošana tiek veikta augstākā līmenī. Šajā rakstā ir parādīts, kā ieplānot, lai izpildītu organizācijas prasības.

## <a name="effort-tracking-view"></a>Piepūles izsekošanas skats

Skats **Piepūles izsekošana** seko līdzi grafikā iekļauto uzdevumu progresam. Tas salīdzina uzdevuma laikā pavadītās darba stundas ar plānotajām piepūles stundām. Lai aprēķinātu izsekošanas metriku, programmatūrā Project Service Automation tiek izmantotas tālāk norādītās formulas.

Sākotnēji uzdevuma izveides brīdī: plānotās izmaksas tiek iestatītas kā novērtētās izmaksas beigu stadijā. Kad faktiskās vērtības ir ierakstītas uzdevumā, izsekošanas skatā par piepūli tiek veikti tālāk norādītie aprēķini.

- Progresa procentuālā vērtība = līdz šim veiktā piepūle + novērtējums beigu stadijā (EAC) 
- Novērtējums līdz pabeigšanai (ETC) = novērtējums beigu stadijā (EAC) − līdz šim veiktā piepūle 
- EAC = atlikusī piepūle + līdz šim veiktā piepūle 
- Projektētā piepūles novirze = Plānotā piepūle - EAC

Programmatūrā Project Service Automation uzdevumam tiek rādīta projektētā piepūles novirze. Ja EAC ir lielāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems vairāk laika, nekā sākotnēji tika plānots. Tādēļ tas atpaliek no grafika. Ja EAC ir mazāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems mazāk laika, nekā sākotnēji tika plānots. Tādēļ tas apsteidz grafiku.

## <a name="reprojecting-effort"></a>Piepūles pārprojektēšana

Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses. Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu. Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.

Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos:

- Pārlabot noklusējuma ETC ar jaunu uzdevumam faktiski atlikušās piepūles novērtējumu. 
- Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.

Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Piepūles pārprojektēšana kopsavilkuma uzdevumiem

Piepūli kopsavilkuma uzdevumiem vai konteinera uzdevumiem var pārprojektēt. Neatkarīgi no tā, vai lietotājs pārprojektēšanu veic, kopsavilkuma uzdevumiem izmantojot atlikušo piepūli vai progresa procentuālo daudzumu, sākas tālāk norādīto aprēķinu kopa.

- Uzdevumam tiek aprēķināts EAC, ETC un progresa procentuālais daudzums.
- Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējais EAC tika sadalīts uz uzdevumu.
- Tiek aprēķināts jaunais EAC katram atsevišķajam uzdevumam līdz pat lapas mezgla uzdevumiem. 
- Ietekmētajiem pakārtotajiem uzdevumiem lejup pa lapas mezgliem tiek pārrēķināts to ETC un progresa procentuālais daudzums, pamatojoties uz EAC vērtību. Šādi uzdevumam tiek iegūta jauna piepūles novirzes projektēšana. 
- Tiek pārrēķināti kopsavilkuma uzdevumu EAC visiem uzdevumiem līdz saknes mezglam.

### <a name="cost-tracking-view"></a>Izmaksu izsekošanas skats 

Skatā **Izmaksu izsekošana** faktiskās izmaksas, kuras tika iztērētas uzdevumam, tiek salīdzinātas ar plānotajām izmaksām. 

> [!NOTE]
> Šajā skatā tiek rādītas tikai darbaspēka izmaksas, un nav iekļautas izmaksas no izdevumu tāmēm. 

Lai aprēķinātu izsekošanas metriku, programmatūrā Project Service Automation tiek izmantotas tālāk norādītās formulas.

Kad uzdevums ir izveidots, plānotās izmaksas ir vienādas ar novērtētajām izmaksām beigu stadijā. Pēc tam, kad faktiskās vērtības ir ierakstītas uzdevumā, **Izsekošanas** skatā par izmaksām tiek veikti tālāk norādītie aprēķini.

 - Patērēto izmaksu procentuālais daudzums = līdz šim faktiski iztērētās izmaksas ÷ novērtētās izmaksas uzdevumam beigu stadijā
 - Izmaksas līdz pabeigšanai (CTC) = novērtētās izmaksas - līdz šim faktiski iztērētās izmaksas
 - Izmaksas beigu stadijā = CTC + līdz šim faktiski iztērētās izmaksas
 - Plānotā izmaksu novirze = plānotās izmaksas − novērtētās izmaksas beigu stadijā

Uzdevumam tiek rādīta projektētā izmaksu novirze. Ja novērtētās izmaksas beigu stadijā ir lielākas par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās vairāk, nekā sākotnēji tika plānots. Tādēļ tam ir tendence pārsniegt budžetu. Ja novērtētās izmaksas beigu stadijā ir mazākas par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās mazāk, nekā sākotnēji tika plānots, un tā tendences ir mazākas par budžetu.

## <a name="project-managers-reprojection-of-cost"></a>Projektu vadītāja veiktā izmaksu pārprojektēšana

Kad notiek piepūles pārprojektēšana, skatā **Izmaksu izsekošana** tiek pārrēķināts CTC, novērtētās izmaksas beigu stadijā, patērēto izmaksu procentuālais daudzums un projektētā izmaksu novirze.

## <a name="project-status-summary"></a>Projekta noteikta kopsavilkums

Izsekošanas dati skatā **Piepūles izsekošana** un **Izmaksu izsekošana** rāda progresu un izmaksu patēriņu projekta saknes mezgla, kopsavilkuma uzdevumu un lapas mezgla uzdevumu līmeņos. Lapas **Projekta entītija** sadaļā **Statuss** tiek rādīts projekta līmeņa statusa kopsavilkums.

## <a name="status-summary-fields"></a>Statusa kopsavilkuma lauki

Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss. Tajā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku. Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu. Lauku **Statusa atjaunināšanas laiks** nevar rediģēt, un tā vērtība ir laikspiedols, kas norāda, kad statuss tika atjaunināts pēdējo reizi.

Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas datuma. Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šos laukus varat iestatīt uz **Apsteidz**. Ja grafika un izmaksu novirze saknes mezglam ir negatīva, varat tos iestatīt uz **Atpaliek**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
