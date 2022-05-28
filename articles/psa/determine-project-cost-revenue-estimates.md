---
title: Projekta izmaksu un ieņēmumu tāmju noteikšana
description: Projekta izmaksu un ieņēmumu tāmju noteikšana programmā Project Service
author: ruhercul
ms.prod: ''
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5d1bdde3c376a74952d54a1e7fade1f48e675d2f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580235"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Projekta izmaksu un ieņēmumu tāmju noteikšana 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekta tāmes sniedz finanšu skatu par prognozēto un plānoto darbu projekta darba sadalījuma struktūrā. Tāmju skats jūs informē par plānotā darba ietekmi uz izmaksām un ieņēmumiem. Tāmju skats sniedz rīku, ar ko redzēt informāciju par dažādām iepriekš definētām dimensijām, lai jūs optimāli informētu par projekta finansiālo ietekmi.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Projekta izmaksu un pārdošanas vērtība  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cenrāži definē izmaksu un rēķinu koeficientus attiecībā uz projektu izmantotajām lomām. Pamatojoties uz lomām, kas ir saistīts ar uzdevumiem projekta darba sadalījuma struktūrā, varat noteikt ieguldītā darba ietekmi uz izmaksām un ieņēmumiem.  
  
## <a name="cost-price-defaulting"></a>Izmaksu cenas noklusējuma izmantošana  
Katrs projekts pieder kādai organizācijai (norādīta projekta laukā **Atbildīgā vienība**). Ar atbildīgo uzņēmuma struktūrvienību saistītais cenrādis nosaka vienības izmaksu cenu. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] nosaka izmaksu cenas attiecībā uz lomām, izmaksu cenrādī meklējot lomas, vienības un organizācijas vienības kombināciju, lai tāmju rindās spēkā stāšanās datumam iegūtu pareizo izmaksu cenu.  
  
Ja lomas, vienības un uzņēmuma struktūrvienības kombinācija nesniedz izmaksu cenu no atbildīgās vienības cenrāža, tad vienība netiek ņemta vērā par labu lomas un uzņēmuma struktūrvienības kombinācijai. Ja izmaksu cena pastāv, šī cena tiek konvertēta uz vienību, kuru izvēlējāties tāmes rindā.  
  
Ja lomas un uzņēmuma struktūrvienības kombinācija nesniedz izmaksu cenu, tad uzņēmuma struktūrvienība netiek ņemta vērā par labu lomas un vienības kombinācijai, un cena tiek iestatīta uz noklusējuma vērtību pēc jebkādas konvertēšanas lietošanas, ja nepieciešams.  
  
 Ja šai lomai nav cenas, tad izmaksu cena tāmes rindā pēc noklusējuma tiek iestatīta uz 0,00.  
  
 Visas izmaksu summas projekta izmaksu tāmju rindās ir norādītas atbildīgās uzņēmuma struktūrvienības valūtā.  
  
## <a name="sales-price-defaulting"></a>Pārdošanas cenas noklusējuma izmantošana  
Pārdošanas cenrādis ir balstīts uz pārdošanas vienību, kādai projekts ir piesaistīts. Ar piedāvājumu vai līgumu saistītais pārdošanas cenrādis nosaka vienības pārdošanas cenu. Ja piedāvājumam vai līgumam ir pielāgots cenrādis, tas projekta tāmēm veido noklusējuma pārdošanas cenrādi. Ja nav saistības ar pārdošanas entītijām, tad noklusējuma pārdošanas cenrādis šim projektam ir parametru iestatījumos konfigurētais noklusējuma pārdošanas cenrādis. Katrai tāmes rindai ir piesaistīta resursu uzņēmuma struktūrvienība, lai norādītu uzņēmuma struktūrvienību, no kuras tiks rezervēti resursi uzdevuma pabeigšanai. Pārdošanas cena saistītajām lomām tiek noteikta, pārdošanas cenrādī meklējot lomas, vienības un resursa uzņēmuma struktūrvienības kombināciju, lai tāmju rindās spēkā stāšanās datumam iegūtu pareizo pārdošanas cenu.  
  
Ja lomas, vienības un resursa uzņēmuma struktūrvienības kombinācija nesniedz pārdošanas cenu no pārdošanas cenrāža, tad sistēma ignorē vienību un meklē lomas un resursa uzņēmuma struktūrvienības kombināciju. Ja pārdošanas cena netiek atrasta, šī vērtība tiek konvertēta uz vienību, kuru izvēlējāties pārdošanas tāmes rindā.  
  
Ja sistēma neatrod cenu šai lomai, tad pārdošanas cenai tāmes rindā pēc noklusējuma ir jākļūst par 0,00.  
  
Tāmju skatam ir režģa skats, kurā tiek rādīts plakans tīkls ar tāmju rindām, kurās ir iekļauta vienība un kopējās izmaksas, un pārdošanas cena.  
  
## <a name="time-phased-view-of-project-estimates"></a>Projekta tāmju skats ar laika fāzēm  
Projekta tāmju skatā ar laika fāzēm tāmju dati no režģa skata tiek pārveidoti pēc noklusējuma atkarībā no lomas, un tiek rādīti kā tāmju datu izklājums izvēlētās laika skalas laika līnijā.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Piepūles tāmes sadalījums, pamatojoties uz uzdevumu režīmu  
Skatā ar laika fāzēm kopējā uzdevumam prognozētā piepūle tiek sadalīta, noteiktu piepūles stundu skaitu piešķirot katram izvēlētās laika skalas vienības laika periodam. Pakalpojumos Project Service uzdevumu režīms nosaka, kā piepūle tiek sadalīta visā uzdevuma ilgumā. Abi sadalījuma veidi ir vienmērīgs sadalījums un uz darba stundām balstīts sadalījums. 
  
## <a name="work-hours-based-allocation"></a>Uz darba stundām pamatotais sadalījums  
Automātiskas plānošanas uzdevumu režīms uzdevumam nosaka, ka uzdevumam prognozēto resursu skaitam tie ir prognozēti izmantošanai uz pilnu dienas darba stundu skaitu. Tas attiecas uz gadījumiem, kad piepūle tiek sadalīta, sadalot to visā uzdevumu ilgumā arī skatā ar laika fāzēm. Piemēram, vienā laika skalā "Diena" uzdevumam, ko ir prognozēts izpildīt ar vienu resursu, vienā dienā piešķirta piepūle nepārsniegs projekta kalendārā dienai definēto darba stundu skaitu. Tādēļ piepūles sadalījums vienmēr nodrošina, ka resursi tiek plānoti izmantošanai uz pilnu dienu.  
  
## <a name="even-distribution"></a>Vienmērīgs sadalījums  
Manuālas plānošanas uzdevumu režīms neņem vērā darba stundas, projekta kalendāru vai uzdevumam definēto resursu skaitu. Uzdevuma grafiks ir balstīts uz lietotāja ievadi. Šādiem uzdevumiem piepūles sadalījumam uz vienības laika periodu izvēlētajā laika skalā nav nekādu ierobežojošo faktoru. Uzdevuma kopējā piepūle tiek vienmērīgi sadalīta un piešķirta katram vienības laika periodam izvēlētajā laika skalā.  
  
Šādi uzdevumam definētais uzdevumu režīms nosaka piepūles sadalījumu vai piepūles piešķiršanu uz vienības laika periodu tāmēs ar laika fāzēm.  
  
## <a name="grouping-and-time-phasing-options"></a>Grupēšanas opcijas un opcijas sadalīšanai laika fāzēs  
Šis skats jums palīdz izprast piepūles, izmaksu un pārdošanas tāmju sadalījumu uz dienu, nedēļu, mēnesi vai gadu. Opcija Grupēt pēc jums ļauj tāmes datus attēlot pēc divām citām dimensijām: kategorijas un resursa. Gan režģa skatā, gan skatā ar laika fāzēm varat izvēlēties parādāmos laukus. Katram laika blokam apakšā tiek rādītas kopsummas, norādot kopējo prognozēto piepūli, izmaksas un dienā, nedēļā, mēnesī vai gadā pārdoto.  
  
Izmaksu un pārdošanas cenas noklusējuma datums ir spēkā stāšanās datums. Ja mainās lomām noteiktie koeficienti, tie būs pārredzamāki skatā ar laika fāzēm, kad tāmes dati tiek skatīti pēc entītijas“Resurss” un skatā ar nedēļas laika fāzi.  
  
## <a name="expense-estimates"></a>Izdevumu tāmes  
Jebkādus projekta ietvaros radītos izdevumus, kas nav tieši saistīti ar iztērējamo darbu, var reģistrēt projekta tāmēs režģa skatā. To varat panākt, režģa skatā izmantojot opciju **Pievienot izdevumu tāmi**. Izdevumu tāmes var ierakstīt konkrētam uzdevumam vai visam projektam. Šajās rindās varat izvēlēties izdevumu kategorijas un izvēlēties varbūtēju datumu, kurā paredzami izdevumi. Ja saistītajam izmaksu un pārdošanas cenrādim ir noklusējuma cenas vai izdevumu kategorijām ir definēts uzcenojuma procentuālais daudzums, tad pēc saistīšanas šī vērtība pēc noklusējuma tiks iestatīta uz šo tāmes rindu.  
  
### <a name="see-also"></a>Skatiet arī  
 [Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
