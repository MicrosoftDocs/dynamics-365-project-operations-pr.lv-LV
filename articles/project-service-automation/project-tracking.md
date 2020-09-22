---
title: Projekta progress un izmaksu patēriņš
description: Šajā tēmā ir sniegta informācija par to, kā sekot līdzi projekta progresam un izmaksu patēriņam.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753544"
---
# <a name="project-progress-and-cost-consumption"></a>Projekta progress un izmaksu patēriņš

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nepieciešamība sekot līdzi grafika gaitai dažādās nozarēs atšķiras. Dažās nozarēs izsekošana notiek ļoti smalkā līmenī, turpretī citās nozarēs izsekošana tiek veikta augstākā līmenī. Šajā tēmā ir parādīts, kā veikt plānošanu, lai izpildītu jūsu organizācijas prasības.

## <a name="effort-tracking-view"></a>Piepūles izsekošanas skats

Skats **Piepūles izsekošana** seko līdzi grafikā iekļauto uzdevumu progresam. Tajā faktiskais piepūles stundu skaits, kas ir patērēts kādam uzdevumam, tiek salīdzināts ar šim uzdevumam plānoto piepūles stundu skaitu. Lai aprēķinātu izsekošanas metriku, programmatūrā PSA tiek izmantotas tālāk norādītās formulas.

- Progresa procentuālais daudzums = Līdz šim faktiski patērētā piepūle ÷ Uzdevumam plānotā piepūle 
- Novērtējums līdz pabeigšanai (ETC) = Plānotā piepūle - Līdz šim faktiski patērētā piepūle 
- Novērtējums pabeigšanas laikā (ETC) = Atlikusī piepūle + Līdz šim faktiski patērētā piepūle 
- Projektētā piepūles novirze = Plānotā piepūle - EAC

Programmatūrā PSA uzdevumam tiek rādīta projektētā piepūles novirze. Ja EAC ir lielāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems vairāk laika, nekā sākotnēji tika plānots. Tādēļ tas atpaliek no grafika. Ja EAC ir mazāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems mazāk laika, nekā sākotnēji tika plānots. Tādēļ tas apsteidz grafiku.

## <a name="re-projecting-effort"></a>Piepūles pārprojektēšana

Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses. Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo stāvokli. Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.

Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos.

- Pārlabot noklusējuma ETC ar jaunu uzdevumam faktiski atlikušās piepūles novērtējumu. 
- Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.

Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Piepūles pārprojektēšana kopsavilkuma uzdevumiem

Piepūli kopsavilkuma uzdevumiem vai konteinera uzdevumiem var pārprojektēt. Neatkarīgi no tā, vai lietotājs pārprojektēšanu veic, kopsavilkuma uzdevumiem izmantojot atlikušo piepūli vai progresa procentuālo daudzumu, sākas tālāk norādīto aprēķinu kopa.

- Uzdevumam tiek aprēķināts EAC, ETC un progresa procentuālais daudzums.
- Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējais EAC tika sadalīts uz uzdevumu.
- Tiek aprēķināts jaunais EAC uz katru no atsevišķajiem uzdevumiem līdz pat lapas mezgla uzdevumiem. 
- Ietekmētajiem pakārtotajiem uzdevumiem lejup pa lapas mezgliem tiek pārrēķināts to ETC un progresa procentuālais daudzums, pamatojoties uz EAC vērtību. Šādi uzdevumam tiek iegūta jauna piepūles novirzes projektēšana. 
- Tiek pārrēķināti kopsavilkuma uzdevumu EAC visiem uzdevumiem līdz saknes mezglam.

### <a name="cost-tracking-view"></a>Izmaksu izsekošanas skats 

Skatā **Izmaksu izsekošana** faktiskās izmaksas, kuras tika iztērētas uz uzdevumu, tiek salīdzinātas ar plānotajām uzdevuma izmaksām. 

> [!NOTE]
> Šajā skatā tiek rādītas tikai darbaspēka izmaksas, un nav iekļautas izmaksas no izdevumu tāmēm. 

Lai aprēķinātu izsekošanas metriku, programmatūrā PSA tiek izmantotas tālāk norādītās formulas.

- Patērēto izmaksu procentuālais daudzums = Līdz šim faktiski iztērētās izmaksas ÷ Uzdevumam plānotās izmaksas
- Izmaksas līdz pabeigšanai (CTC) = Plānotās izmaksas - Līdz šim faktiski iztērētās izmaksas
- EAC = CTC + Līdz šim faktiski iztērētās izmaksas
- Projektētā izmaksu novirze = Plānotās izmaksas - EAC

Uzdevumam tiek rādīta projektētā izmaksu novirze. Ja EAC ir lielāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās vairāk, nekā sākotnēji tika plānots. Tādēļ tam ir tendence pārsniegt budžetu. Ja EAC ir mazāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās mazāk, nekā sākotnēji tika plānots. Tādēļ tam ir tendence iekļauties budžetā.

## <a name="project-managers-re-projection-of-cost"></a>Projektu vadītāja veiktā izmaksu pārprojektēšana

Kad notiek piepūles pārprojektēšana, skatā **Izmaksu izsekošana** tiek pārrēķināts CTC, EAC, patērēto izmaksu procentuālais daudzums un projektētā izmaksu nobīde.

## <a name="project-status-summary"></a>Projekta noteikta kopsavilkums

Izsekošanas dati skatā **Piepūles izsekošana** un **Izmaksu izsekošana** rāda progresu un izmaksu patēriņu projekta saknes mezgla, kopsavilkuma uzdevumu un lapas mezgla uzdevumu līmeņos. Lapas **Projekta entītija** sadaļā **Statuss** tiek rādīts projekta līmeņa statusa kopsavilkums.

## <a name="status-summary-fields"></a>Statusa kopsavilkuma lauki

Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss. Tajā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku. Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu. Lauku **Statusa atjaunināšanas laiks** nevar rediģēt, un tā vērtība ir laikspiedols, kas norāda, kad statuss tika atjaunināts pēdējo reizi.

Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas datuma. Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šos laukus varat iestatīt uz **Apsteidz**. Ja grafika un izmaksu novirze saknes mezglam ir negatīva, varat tos iestatīt uz **Atpaliek**.
