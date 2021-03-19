---
title: Projekta plānošana, izmantojot darba sadalījuma struktūru
description: Projekta plānošana, izmantojot darba sadalījuma struktūru programmā Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282702"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Projekta plānošana, izmantojot darba sadalījuma struktūru (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekta grafikā var uzzināt, kāds darbs ir jāveic un kuri resursi šo dabu veiks, kā arī laikposmu, kurā darbs ir jāveic. Projekta grafiks atspoguļo pilnībā visu darbu, kas saistīts ar savlaicīgu projekta nodošanu. Viena no pirmajām darbībām projekta sākuma fāzē projekta grafika izstrāde. Lai izveidotu projekta grafiku, ir jāizveido darba sadalījuma struktūra.  
  
 Izveidojot projekta struktūru ar darba sadalījuma struktūru, varat veikt šādas darbības:  
  
- sadalīt darbu pārvaldāmos uzdevumos;  
  
- aprēķināt uzdevuma izpildei nepieciešamo laiku;  
  
- iestatīt uzdevuma atkarības un ilgumu;  
  
- noteikt lomas, kas nepieciešamas, lai izpildītu katru uzdevumu.  
  
  Projekta grafikam darba sadalījuma struktūrā ir vienkāršs izskats un izkārtojums, kā arī tajā ir pieejama interaktīva Ganta diagramma.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Projekta darba sadalījuma struktūras izveide  
 Izveidojiet darba sadalījuma struktūru, lai norādītu projekta uzdevumu izpildes secību. Darba sadalījuma struktūra ietver uzdevumus un prasības attiecībā uz to izpildi, kā arī ieņēmumu un izdevumu informāciju. Darba sadalījuma struktūrai var pievienot:  
  
-   projekta uzdevumu izpildes secību hierarhijā;  
  
-   citus uzdevumus, ja tādi ir, kas jāizpilda, lai varētu sākt uzdevuma izpildi;  
  
-   uzdevuma sākuma datumu, beigu datumu un ilgumu;  
  
-   uzdevuma izpildei nepieciešamo stundu skaitu;  
  
-   visas nepieciešamās darba prasmes un izglītību;  
  
-   darbiniekus, kam uzdevums tika piešķirts;  
  
-   prognozējamos ieņēmumus un izdevumus.  
  
## <a name="task-types"></a>Uzdevumu tipi  
Veidojot darba sadalījuma struktūru, izmantosit tālāk aprakstīto veidu uzdevumus.  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projekta saknes mezgls** | Projekta augšējā līmeņa kopsavilkuma uzdevums. Visi citi projekta uzdevumi tiek izveidoti saskaņā ar to. Saknes uzdevuma nosaukums ir projekta nosaukums. Saknes mezgla ieguldījums, datumi un ilgums ir balstīti uz tās hierarhijas vērtībām, kas atrodas zem tā. Saknes mezgla rekvizītus nevar rediģēt un saknes mezglu nevar dzēst. | 
| **Kopsavilkuma vai konteinera uzdevumi** | Kopsavilkuma uzdevums ir uzdevums, kam ir pakārtoti apakšuzdevumi. Kopsavilkuma uzdevumam nav jebkāda darba ieguldījuma vai izmaksu. Tā darba ieguldījums un izmaksas ir tā apakšuzdevumu apkopojums. Kopsavilkuma uzdevuma nosaukumu var mainīt, tomēr nevar mainīt ieguldījumu, datumus vai ilgumu, jo šīs vērtības tiek aprēķinātas automātiski. Dzēšot kopsavilkuma uzdevumu, tiek dzēsts uzdevums un visi tā apakšuzdevumi.|  
| **Lapas mezgla uzdevumi** | Lapas mezgla uzdevums ir projekta darbs ar visdetalizētāko informāciju. Tajā ir ietverta aptuvenais ieguldījums, plānotais resursu skaits, plānotais sākuma un beigu datums un ilgums.|

  
## <a name="task-hierarchy"></a>Uzdevumu hierarhija  
 Veidojot uzdevumu hierarhiju, ir pieejamas tālāk minētās opcijas.  
  
- **Uzdevuma pievienošana**.   Varat pievienot uzdevumu izvēlētajā pozīcijā uzdevumu hierarhijā. Ja pozīciju neatlasāt, jaunais uzdevums tiek pievienots beigās.  
  
- **Uzdevuma atkāpes izveide**.   Veidojiet uzdevumam atkāpi, lai tas būtu tā uzdevuma apakšuzdevums, kas atrodas tieši virs šī uzdevuma.  
  
- **Uzdevuma pārkaru atkāpes izveide**   Veidojiet uzdevumam pārkaru atkāpi, lai tas vairs nebūtu sākotnējā galvenā uzdevuma apakšuzdevums.  
  
- **Pārvietot augšup un pārvietot lejup**.   Pārvietojiet uzdevumus augšup un lejup galveno uzdevumu hierarhijā. Pārvietojot uzdevumu augšup vai lejup, netiek ietekmēts tā ieguldījums, izmaksas, datumi vai ilgums.  
  
## <a name="task-attributes"></a>Uzdevuma atribūti  
 Uzdevuma nosaukums raksturo darbu, kas jāizpilda. Uzdevuma grafika un darbspēka vajadzību aprakstīšanai izmanto dažādus uzdevuma atribūtus.  
  
### <a name="schedule-attributes"></a>Grafika atribūti

 - Piešķiriet vērtības atribūtam **Ieguldījuma stundas**, **Resursu skaits**, **Sākuma datums**, **Beigu datums** un **Ilgums**, lai noteiktu uzdevuma grafiku. 
 - Atribūts **Ieguldījums** ir aptuvenais laiks stundās, kas nepieciešams uzdevuma izpildei.
 - Atribūts **Resursu skaits** ir aprēķins, ko projekta vadītājs iestata uzdevumam, lai izstrādātu vislabāko iespējamo grafiku. 
 - Atribūts **Ilgums** (dienās) norāda darba dienu skaitu, kas nepieciešams uzdevuma izpildei.  
  
### <a name="staffing-attributes"></a>Darbspēka atribūti

 - Atribūts **Loma**, **Resursu organizācijas struktūrvienība**, **Resursu skaits** un **Resursi** apraksta darbspēka vajadzības šim uzdevumam. 
 - Atribūts **Loma** apraksta, kāda tipa resurss ir vajadzīgs uzdevuma izpildei. 
 - Atribūts **Resursu organizācijas struktūrvienība** norāda organizācijas struktūrvienību, no kuras jānodrošina resursi šī uzdevuma izpildei; tas ietekmē arī uzdevuma izmaksu un pārdošanas budžeta aprēķinus, jo tiek ņemts vērā, nosakot struktūrvienības pārdošanas cenu šim resursam. 
 - Atribūts **Resursi** satur vispārējus resurss vai nosauktos resursus, ja tādi tiek atrasti.  
  
## <a name="task-dependencies"></a>Uzdevuma atkarības  
 Vienam vai vairākiem darba sadalījuma struktūras uzdevumiem varat izveidot pirmstecīgas relācijas. Pirmstecīga uzdevuma laukam var iestatīt vienu vai vairākas vērtības, lai norādītu uzdevumus, no kuriem tas būs atkarīgs. Piešķirot uzdevumam pirmstecīgu vērtību, uzdevumu var sākt tikai tad, kad ir pabeigti visi pirmstecīgie uzdevumi. Iestatot uzdevumam šādu atkarību, tiks pārrēķināts plānotaisuzdevuma sākuma datums, ņemot vērā visu pirmstecīgo uzdevumu pēdējo beigu datumu. Pirmstecīgie uzdevumi ietekmē ne tikai grafika uzdevuma režīmu, kas definēts uzdevumā.  
  
## <a name="task-mode"></a>Uzdevuma režīms  
 Uzdevuma režīms ir viens no svarīgajiem faktoriem, kas nosaka lapu mezgla uzdevumu plānošanu. Katram uzdevumam ir divi uzdevuma režīmi: automātisks plānošanas režīms un manuāls plānošanas režīms.  
  
-   **Automātiskā plānošana**.   Automātisks plānošanas režīms. Iestatot uzdevuma režīmu Automātiski plānots, uzdevuma plānošanas programma izmanto plānošanas kartulas šādos uzdevumu atribūtos, lai noteiktu uzdevumu grafiku:  
  
    -   Pirmstecīgie uzdevumi  
  
    -   Ieguldījums  
  
    -   Resursu skaits  
  
    -   Sākuma un beigu datumi  
  
-   **Plānošanas kārtulas**.   Tā lapas mezgla uzdevuma sākuma datums, kam projekta plānošanas sākuma datumā nav noklusējuma pirmstecīgu uzdevumu. Lapas mezgla uzdevuma ilgums vienmēr tiek aprēķināts kā darba dienu skaits no tā sākuma līdz beigu datumam. Ja uzdevums tiek plānots automātiski, plānošanas programma ievēro tālāk aprakstītās kārtulas.  
  
    -   Uzdevuma sākuma un beigu datumam vienmēr jābūt darbdienās atbilstoši projekta plānošanas kalendāram.  
  
    -   Uzdevuma, kam ir pirmstecīgi uzdevumi, sākuma datums pēc noklusējuma tiek iestatīts kā to pirmstecīgo uzdevumu vēlākais datums.  
  
    -   Ieguldījums = personu skaits * Ilgums * Stundas standarta projekta kalendāra darba dienā  
  
-   **Manuāla plānošana**.   Dažos gadījumos ieteicams atkāpties no šīm kārtulām. Šajos gadījumos uzdevuma režīmam var iestatīt manuālu plānošanu. Tas aptur plānošanas programmu no citu plānošanas atribūtu vērtību aprēķināšanas. Iestatot pirmstecīgus uzdevumus, vienmēr tiek ietekmēti atkarīgo uzdevumu sākuma datums.  
  
## <a name="create-a-work-breakdown-structure"></a>Darba sadalījuma struktūras izveide  
  
1.  Dodieties uz **Project Service > Projekti**.  
  
2.  Noklikšķiniet uz projekta, pie kura gribat strādāt.  
  
3.  Ekrāna augšdaļā esošajā joslā atlasiet lejupvērsto bultiņu pie projekta nosaukuma un pēc tam noklikšķiniet uz Darba sadalījuma struktūra.  
  
4.  Lai pievienotu uzdevumu, noklikšķiniet uz **Pievienot uzdevumu**. Aizpildiet uzdevuma laukus un pēc tam noklikšķiniet uz vienuma **Saglabāt**.  
  
5.  Turpiniet pievienot uzdevumus, līdz darba sadalījuma struktūra ir pabeigta. Veidojot darba sadalījuma struktūru, varat veikt tālāk minētās darbības, lai sakārtotu uzdevumus.  
  
    -   Atlasiet uzdevumu un noklikšķiniet uz **Izveidot atkāpi**, lai to pārvietotu zem cita uzdevuma, vai noklikšķiniet uz Izveidot pārkaru atkāpi, lai to izņemto no esošā līmeņa.  
  
    -   Atlasiet uzdevumu un noklikšķiniet uz **Pārvietot uz augšu** vai **Pārvietot uz leju**, lai to pārvietotu augšup vai lejup sarakstā.  
  
    -   Noklikšķiniet uz **Paslēpt Ganta diagrammu**, lai paslēptu Ganta diagrammu, un noklikšķiniet uz **Parādīt Ganta diagrammu**, lai to atkal parādītu.  
  
    -   Atlasiet dažādus laika posmus Ganta diagrammas sadaļā **Laika skala**.  
  
6.  Lai pievienotu lomas, ko projekta darba grupa dalībniekiem norādījāt darba sadalījuma struktūrā, noklikšķiniet uz **Ģenerēt projekta darba grupu**.  
  
7.  Kad esat pabeidzis izmaiņu veikšanu, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.  
  
### <a name="see-also"></a>Skatiet arī  
 [Projektu vadītāja rokasgrāmata](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]