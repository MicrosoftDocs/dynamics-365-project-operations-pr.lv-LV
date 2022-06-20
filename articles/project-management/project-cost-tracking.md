---
title: Projekta izmaksu uzskaite
description: Šajā rakstā ir sniegta informācija par to, kā projekta operācijas seko progresam attiecībā pret darbaspēka izmaksām un tēriņiem projektam.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923749"
---
# <a name="labor-cost-tracking-on-projects"></a>Projektu darbaspēka izmaksu uzskaite

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations izseko darba aprēķinus un izmaksas projekta plānā mazākajā nepieciešamajā līmenī. Darbaspēka izmaksu finanšu aprēķins ir balstīts uz plānoto ieguldījumu un vispārīgajiem vai nosauktajiem resursiem, kas projekta plānā tiek piešķirti katram lapas mezgla uzdevumam. Kad projekts sākas un cilvēki sāk ziņot par laiku dažādos projekta uzdevumos, tiek apkopotas faktiskās darbaspēka izmaksas, kas sāk prognozēto aprēķinu.

## <a name="labor-cost-tracking-view"></a>Darbaspēka izmaksu uzskaites skats

Lapas **Projekti** cilnē **Uzskaite** varat atlasīt **Uzskaite** > **Izmaksas**, lai atvērtu skatu **Izmaksu uzskaite** un aplūkotu katra uzdevuma darbaspeka izmaksas projekta plānā. Šis skats salīdzina arī faktiskās darbaspēka izmaksas, kas iztērētas uzdevumam, ar uzdevuma plānotajām darbaspēka izmaksām. Lai aprēķinātu darba izmaksu metriku, Project Operations izmanto šādas formulas:

- **Plānotās izmaksas**: visu piešķirto resursu prognozētās izmaksas katrā lapas mezgla uzdevumā.
- **Faktiskās izmaksas**: visu uzdevumam reģistrēto izmaksu faktisko izmaksu summa.
- **Izmaksu patēriņa procents**: faktiskās izmaksas÷ galīgo izmaksu novērtējums
- **Atlikušās izmaksas**: galīgo izmaksu novērtējums – faktiskās izmaksas.
- **Galīgās izmaksas**: atlikušās izmaksas + faktiskās izmaksas.
- **Izmaksu novirze**: plānotās izmaksas – galīgo izmaksu novērtējums.

Katrs uzdevums parāda izmaksu novirzes projekciju. Ja galīgo izmaksu novērtējums pārsniedz plānotās izmaksas, tiek plānots, ka uzdevums pārsniegs budžetu. Ja galīgo izmaksu novērtējums ir mazāks par plānotajām izmaksām, tiek plānots, ka uzdevums nepārsniegs budžetu.

>[!NOTE]
> Project Operations rāda tikai darbaspēka izmaksas lapā **Projekts**, cilnē **Uzskaite**. Lai gan materiālus un izdevumus var aprēķināt un uzskaitīt patēriņam, šīs izmaksas nav iekļautas cilnē **Uzskaite**. Šī cilne ir paredzēta tikai darbaspēka izmaksu pārplānošanai, izmantojot ieguldījuma pārplānošanu.
Visas parādītās izmaksu summas tiek konvertētas projekta izmaksu valūtā no projekta izmaksu valūtas, kas tiek izmantota izmaksu likmes noteikšanai. Projekta izmaksu valūta ir projekta līguma slēgšanas vienības valūta. Aprēķināto izmaksu vērtības, kas tiek rādītas cilnē **Aprēķini**, lapā **Projekts**, var nesakrist ar cilnē **Uzskaite** redzamajām plānotajām izmaksām. Šīs neatbilstības iemesls ir atšķirība starp to, kā aprēķinātās izmaksas tiek saskaitītas režģī **Aprēķini**, un to, kā plānotās izmaksas tiek aprēķinātas režģī **Uzskaite**. 
>
> - Cilnē **Aprēķini** tiek aprēķinātas prognozētās izmaksas, cenrāža izmaksu likmei izmantojot tādu pašu valūtu. Pēc tam prognozētās izmaksas cenrāža valūtā tiek konvertētas projekta izmaksu valūtā prognozētajām izmaksām. Projekta valūtā prognozētās izmaksas tiek noapaļotas līdz 2 decimālzīmēm. Šīs pārvēršanas laikā netiek izmantota valūtas precizitāte. 
> - Cilnē **Uzskaite** plānotās izmaksas tiek aprēķinātas, izmantojot citādu aprēķinu secību, kas ietver valūtas precizitātes piemērošanu divos līmeņos. 
   ><ol>
   ><li>Prognozēto izmaksu summa cenrāža valūtā tiek konvertēta pamatvalūtā (konvertēšanas pirmais solis).</li>
   ><li>Prognozēto izmaksu summa pamatvalūtā tiek konvertēta projekta izmaksu valūtā (konvertēšanas otrais solis). </li>
   ></ol>
   >Abos soļos tiek lietota valūtas precizitāte, lai iegūtu plānotās izmaksas (cilnē **Uzskaite**), kas nedaudz atšķiras no prognozētajām izmaksām (cilnes **Aprēķini** skatā **Skats ar laika fāzēm**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Izmaksu pārplānošana lapas mezgla uzdevumos

Darbaspēka izmaksas lapas mezgla uzdevumam nevar tieši pārplānot cilnē **Uzskaite**, lapā **Projekts**. Varat izmantot skatu **Ieguldījuma uzskaite**, lai pārplānotu atlikušo uzdevuma ieguldījumu. Tādējādi tiek pārrēķinātas uzdevuma atlikušās izmaksas. Tālāk sniegts apraksts par to, kā tas darbojas.

1. Projekta vadītājs var pārplānot ieguldījumu uzdevumos , atjauninot noklusējuma vērtību laukā **Atlikušais ieguldījums** ar atlikušo darba ieguldījumu. Pārplānošanas rezultātā tiek pārrēķināts uzdevuma galīgais ieguldījuma novērtējums, norises procentuālā daļa un paredzamā ieguldījuma novirze. Tiek pārrēķināts arī galīgo izmaksu novērtējums un progresa procentuālā daļa kopsavilkuma uzdevumiem, un tiek izveidots jauns prognozētā ieguldījuma novirzes novērtējums.
2. Pamatojoties uz uzdevuma atlikušā ieguldījuma jauno vērtību, sistēma atlikušās izmaksas aprēķina skatā **Izmaksu uzskaite**. Lai aprēķinātu atlikušās izmaksas, pamatojoties uz atlikušo ieguldījumu, sistēma vispirms uzdevumam kā plānotās izmaksas vai plānoto ieguldījumu aprēķina vienas stundas ieguldījumu. Plānotās izmaksas ir visu uzdevuma resursu piešķiru izmaksu summa. Vidējās izmaksas stundā tiek izmantotas, lai aprēķinātu jaunās prognozētās uzdevuma atlikušās izmaksas.
3. Lapas mezgla uzdevuma izmaksas pēc pabeigšanas un izmaksu patēriņa procentuālā daļa tiek pārrēķinātas.
4. Tiek pārrēķinātas galīgās izmaksas kopsavilkuma uzdevumiem līdz par saknes mezglam.

## <a name="reprojecting-costs-on-summary-tasks"></a>Izmaksu pārplānošana kopsavilkuma uzdevumos

Varat pārplānot darbaspēka izmaksas kopsavilkuma uzdevumos vai konteinera uzdevumos. Tomēr jūs nevarat pārplānot darbaspēka izmaksas tieši kopsavilkuma projektā cilnē **Uzskaite**, lapā **Projekts**. Līdzīgi kā lapas mezgla uzdevumiem, kopsavilkuma un konteinera uzdevumus var pārplānot skatā **Ieguldījuma uzskaite**. Šajā skatā varat pārplānot atlikušo ieguldījumu kopsavilkuma uzdevumā, tādējādi veicot atlikušo izmaksu pārrēķināšanu kopsavilkuma uzdevumā. Tālāk sniegts apraksts par to, kā tas darbojas.

1. Projekta vadītājs var pārplānot ieguldījumu kopsavilkuma uzdevumos, atjauninot atlikušā ieguldījuma noklusējuma vērtību ar jaunu prognozēto vērtību. Šādas atjaunināšanas rezultātā tiek pārrēķināts kopsavilkuma uzdevuma galīgais ieguldījuma novērtējums, norises procentuālā daļa un paredzamā ieguldījuma novirze. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.
2. Pamatojoties uz kopsavilkuma uzdevuma atlikušā ieguldījuma jauno vērtību, sistēma atlikušās izmaksas aprēķina skatā **Izmaksu uzskaite**. Lai aprēķinātu atlikušās izmaksas, pamatojoties uz atlikušo ieguldījumu, sistēma vispirms kopsavilkuma uzdevumam kā plānotās izmaksas vai plānoto ieguldījumu aprēķina vienas stundas ieguldījumu. Vidējās izmaksas stundā tiek izmantotas, lai aprēķinātu jaunās prognozētās kopsavilkuma uzdevuma atlikušās izmaksas.
3. Kopsavilkuma uzdevuma izmaksas pēc pabeigšanas un izmaksu patēriņa procentuālā daļa tiek pārrēķinātas.
4. Jaunais galīgo izmaksu novērtējums tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējās plānotās izmaksas tika sadalītas uz uzdevumu.
5. Tiek aprēķināta jaunā galīgo izmaksu vērtība uz katru no atsevišķajiem uzdevumiem līdz pat lapas mezgla uzdevumiem. Pamatojoties uz šo vērtību, ietekmētajiem pakārtotajiem uzdevumiem līdz lapas mezgliem tiks pārrēķinātas alikušās izmaksas un patērētās izmaksas, ņemot vērā galīgo izmaksu vērtību. Šīs vērtības rezultātā tiek iegūta jauna uzdevuma izmaksu novirzes prognoze. 


Lauku **Izmaksu veikstspēja** var iestatīt no uzskaites datiem. Ja izmaksu novirze saknes mezglam skatā **Izmaksu uzskaite** ir negatīva, varat iestatīt šo lauku uz **Nepārsniedz budžetu**. Ja saknes mezgla izmaksu novirze ir pozitīva, vērtību var iestatīt kā **Pārsniegts budžets**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
