---
title: Projekta pārdošanas datu uzskaite
description: Šajā tēmā ir sniegta informācija par to, kā Project Operations tiek izsekota norise attiecībā pret darbaspēka ieņēmumiem projektā.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f9873dc3e709453a56cb53273b35cc1cd312127
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996980"
---
# <a name="project-sales-tracking"></a>Projekta pārdošanas datu uzskaite

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations izseko darbaspēka aprēķinus un ieņēmumus projekta plānā mazākajā nepieciešamajā līmenī. Darbaspēka ieņēmumu finanšu aprēķins ir balstīts uz plānoto ieguldījumu un vispārīgajiem vai nosauktajiem resursiem, kas projekta plānā tiek piešķirti katram lapas mezgla uzdevumam. Kad projekts sākas un cilvēki sāk ziņot par laiku dažādos projekta uzdevumos, tiek apkopoti faktiskie darbaspēka ieņēmumi, un tiek sākts prognožu aprēķins.

## <a name="labor-revenue-tracking-view"></a>Darbaspēka ieņēmumu uzskaites skats

Lai atvērtu skatu **Izmaksu uzskaite**, lapas **Projekti** cilnē **Uzskaite** atlasiet **Uzskaite** > **Izmaksas**. Vai arī atlasiet **Lietot** > **Rēķina likme**, lai atvērtu skatu **Ieņēmumu uzskaite**, kurā redzami darbaspēka ieņēmumi katrā projekta plāna uzdevumā. Šis skats salīdzina arī faktiskos uzdevuma darbaspēka ieņēmumus ar uzdevuma plānotajiem darbaspēka ieņēmumiem. Lai aprēķinātu darbaspēka ieņēmumu metriku, Project Operations izmanto šādas formulas:

- **Plānotie ieņēmumi**: visu piešķirto resursu prognozētās pārdošanas vērtības katrā lapas mezgla uzdevumā.
- **Faktiskie ieņēmumi**: visu rēķinos neietverto pārdošanas datu kopsumma uzdevumā reģistrētajam laikam.
- **Apmaksājamie ieņēmumi procentos**: faktiskie ieņēmumi÷ galīgie ieņēmumi
- **Atlikušie ieņēmumi**: galīgie ieņēmumi – faktiskie ieņēmumi
- **Galīgo ieņēmumu novērtējums**: atlikušie ieņēmumi + faktiskie ieņēmumi
- **Ieņēmumu novirze**: plānotie ieņēmumi – galīgo ieņēmumu novērtējums


> [!NOTE]
> Project Operations rāda tikai darbaspēka ieņēmumus lapā **Projekts**, cilnē **Uzskaite**. Lai gan materiālus un izdevumus var aprēķināt un uzskaitīt patēriņam, šie ieņēmumi nav iekļauti cilnē **Uzskaite**. Šī cilne ir paredzēta tikai darbaspēka ieņēmumu pārplānošanai, izmantojot ieguldījuma pārplānošanu.  
> Visas parādītās ieņēmumu summas tiek konvertētas projekta izmaksu valūtā. Projekta izmaksu valūta ir projekta līguma slēgšanas vienības valūta. Fiksētas cenas projektiem ieņēmumu dati skatā **Darbaspēka ieņēmumu uzskaite** nav atbilstoši, jo rēķinos neietvertie pārdošanas dati netiek reģistrēti laika apstiprināšanas brīdī.
> Novērtētās pārdošanas vērtības laikam, kas redzamas projekta cilnē **Novērtējums**, var neatbilst plānoto ieņēmumu vērtībai cilnē **Uzskaite**. Šai nesakritībai var būt divi tālāk minētie iemesli.
><ol>
   ><li> Cilnē <b>Novērtējums</b> ir redzams ieņēmumu novērtējums pārdošanas valūtā, savukārt cilnē <b>Uzskaite</b> redzami plānotie ieņēmumi, kas konvertēti izmaksu valūtā. </li>
   ><li> Kad novērtētās pārdošanas vērtības tiek konvertētas no līguma valūtas, kā redzams cilnē <b>Novērtējums</b>, uz projekta valūtu, konvertēšanas laikā var rasties neprecizitātes. </li>
><ol>
><li> Novērtētā pārdošanas summa līguma valūtā vispirms tiek konvertēta pamatvalūtā (konvertēšanas pirmais solis).</li>
><li> Novērtētā pārdošanas summa pamatvalūtā tiek konvertēta projekta izmaksu valūtā (konvertēšanas otrais solis). </li>
></ol>
></ol>
> Abos soļos tiek lietota valūtas precizitāte, kā rezultātā plānotie ieņēmumi projekta valūtā neatbilst plānotajiem pārdošanas apjomiem līguma valūtā.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Ieņēmumu pārplānošana lapas mezgla uzdevumos

Darbaspēka ieņēmumu lapas mezgla uzdevumam nevar tieši pārplānot cilnē **Uzskaite**, lapā **Projekts**. Varat izmantot skatu **Ieguldījuma uzskaite**, lai pārplānotu atlikušo uzdevuma ieguldījumu. Tādējādi tiek pārrēķināti uzdevuma atlikušie ieņēmumi. Tālāk sniegts apraksts par to, kā tas darbojas.

1. Projekta vadītājs var pārplānot ieguldījumu uzdevumos , atjauninot noklusējuma vērtību laukā **Atlikušais ieguldījums** ar atlikušo darba ieguldījumu. Pārplānošanas rezultātā tiek pārrēķināts uzdevuma galīgais ieguldījuma novērtējums, norises procentuālā daļa un paredzamā ieguldījuma novirze. Tiek pārrēķināts arī galīgo izmaksu novērtējums un progresa procentuālā daļa kopsavilkuma uzdevumiem, un tiek izveidots jauns prognozētā ieguldījuma novirzes novērtējums.
2. Pamatojoties uz uzdevuma atlikušā ieguldījuma jauno vērtību, sistēma aprēķina atlikušos ieņēmumus skatā **Ieņēmumu uzskaite**. Lai aprēķinātu atlikušos ieņēmumus, pamatojoties uz atlikušo ieguldījumu, sistēma vispirms uzdevumam kā plānotos ieņēmumus vai plānoto ieguldījumu aprēķina vienas stundas ieguldījuma vidējos ieņēmumus. Plānotie ieņēmumi ir visu uzdevuma resursu piešķīrumu ieņēmumu summa. Vidējie ieņēmumi stundā tiek izmantoti, lai aprēķinātu atlikušos ieņēmumus jaunajam novērtētajam atlikušajam ieguldījumam uzdevumā.
3. Lapas mezgla uzdevuma novērtētie ieņēmumi un ieņēmumu patēriņa procentuālā daļa tiek pārrēķinātas.
4. Tiek pārrēķināti galīgie ieņēmumi kopsavilkuma uzdevumiem līdz par saknes mezglam.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Ieņēmumu pārplānošana kopsavilkuma uzdevumos

Varat pārplānot darbaspēka ieņēmumus kopsavilkuma uzdevumos vai konteinera uzdevumos. Tomēr jūs nevarat pārplānot darbaspēka ieņēmumus tieši kopsavilkuma projektā cilnē **Uzskaite**, lapā **Projekts**. Līdzīgi kā lapas mezgla uzdevumiem, kopsavilkuma un konteinera uzdevumus var pārplānot skatā **Ieguldījuma uzskaite**. Šajā skatā varat pārplānot atlikušo ieguldījumu kopsavilkuma uzdevumā, tādējādi veicot atlikušo ieņēmumu pārrēķināšanu kopsavilkuma uzdevumā. Tālāk sniegts apraksts par to, kā tas darbojas.

1. Projekta vadītājs var pārplānot ieguldījumu uzdevumos, atjauninot noklusējuma vērtību laukā **Atlikušais ieguldījums** ar jaunu **atlikušā ieguldījuma** novērtējumu uzdevumā. Pārplānošanas rezultātā tiek pārrēķināts uzdevuma galīgo izmaksu novērtējums, norises procentuālā daļa un paredzamā ieguldījuma novirze. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.
2. Pamatojoties uz jauno vērtību laukā **Atlikušais ieguldījums**, sistēma aprēķina atlikušos ieņēmumus skatā **Ieņēmumu uzskaite**. Lai aprēķinātu atlikušos ieņēmumus, pamatojoties uz atlikušo ieguldījumu, sistēma vispirms uzdevumam kā plānotos ieņēmumus vai plānoto ieguldījumu aprēķina vienas stundas ieguldījuma vidējos ieņēmumus. Plānotie ieņēmumi ir visu uzdevuma resursu piešķīrumu ieņēmumu summa. Šie vidējie ieņēmumi stundā tiek izmantoti, lai aprēķinātu ieņēmumus jaunajam novērtētajam atlikušajam ieguldījumam uzdevumā.
3. Kopsavilkuma uzdevuma novērtētie ieņēmumi un ieņēmumu patēriņa procentuālā daļa tiek pārrēķinātas.
4. Jaunā novērtēto galīgo ieņēmumu vērtība tiek sadalīta uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējie plānotie ieņēmumi tika sadalīti uz uzdevumu.
5. Tiek aprēķināti jaunie novērtētie ieņēmumi uz katru no atsevišķajiem uzdevumiem līdz pat lapas mezgla uzdevumiem. Pamatojoties uz šo vērtību, ietekmētajiem pakārtotajiem uzdevumiem līdz lapas mezgliem tiks pārrēķināti alikušie ieņēmumi un patērētie ieņēmumi, ņemot vērā galīgo ieņēmumu vērtību. Šādi uzdevumam tiek iegūta jauna ieņēmumu novirzes prognoze. 
6. Tiek pārrēķināti galīgie ieņēmumi kopsavilkuma uzdevumiem līdz par saknes mezglam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

