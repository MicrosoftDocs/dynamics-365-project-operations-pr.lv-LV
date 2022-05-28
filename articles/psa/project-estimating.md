---
title: Projekta izmaksas un ieņēmumi
description: Šajā tēmā ir sniegta informācija par projekta izmaksu un ieņēmumu prognozēšanu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ecac3a08b2405e697eb260bbab991458dbe69f4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581891"
---
# <a name="project-costs-and-revenue"></a>Projekta izmaksas un ieņēmumi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta tāmes sniedz finansiālu ieskatu par darbu, kāds ir prognozēts un plānots attiecīgajā projekta grafikā. Lapas **Projekti** cilnē **Tāmes** ir parādīta izmaksu un ieņēmumu ietekme uz jūsu plānoto darbu. Tā sniedz arī informāciju par daudzām iepriekš definētām dimensijām. 

> ![Cilne Tāmes.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Projekta izmaksu un pārdošanas vērtības

Cenrāži nosaka izmaksu un norēķinu likmes projektā esošajām lomām. Darba izmaksu un ieņēmumu ietekmi varat noteikt, pamatojoties uz lomām, kuras ir saistītas ar amata nosaukumu, un nosaukto resursu, kurš ir piešķirts kādam uzdevumam. Ja pastāv uzdevumi, kuriem nav nevienas (vispārējas vai nosauktas) piešķires, izmaksu un pārdošanas tāmes nevar iegūt. Izmaksu un pārdošanas vērtībām tiek ņemts vērā cenrāžos noteiktais datums.

### <a name="default-cost-price"></a>Noklusējuma izmaksu cena  

Katrs projekts pieder kādai organizācijai. Šī organizācija ir parādīta projekta laukā **Līgumslēdzēja struktūrvienība**. Lai noteiktu vienības izmaksu cenu, tiek izmantots cenrādis, kurš ir saistīts ar šo līgumslēdzēja struktūrvienību. Lai noteiktu pareizās izmaksu cenas lomām tam datumam, kurš ir norādīts tāmes rindās, izmaksu cenrādī meklējiet lomas, vienības un organizācijas struktūrvienības kombināciju. 

Lai uzdevumiem varētu aprēķināt izmaksu cenas, visiem uzdevumiem ir jābūt piešķirtiem kādam resursam. Visu nepiešķirto uzdevumu izmaksu cena ir 0,00.

Ja lomas, vienības un organizācijas struktūrvienības kombinācija neatgriež izmaksu cenu no līgumslēdzējas struktūrvienības cenrāža, sistēma ignorē šo vienību. Tā vietā tiek meklēta kombinācija no tikai lomas un organizācijas struktūrvienības. Ja izmaksu cena tiek atrasta, tiek izmantoti konvertēšanas koeficienti, lai to konvertētu par vienību, kuru atlasījāt tāmes rindā.

Ja lomas un organizācijas struktūrvienības kombinācija neatgriež izmaksu cenu, sistēma ignorē šo organizācijas struktūrvienību. Tā vietā tiek meklēta kombinācija no lomas un vienības, lai iestatītu noklusējuma cenu (pēc tam, kad ir izmantota jebkāda konvertēšana).

Ja sistēma neatrod cenu šai lomai, izmaksu cena tāmes rindā tiek iestatīta uz noklusējuma vērtību **0,00**. Visas izmaksu summas projekta izmaksu tāmju rindās tiek ierakstītas līgumslēdzējas struktūrvienības valūtā.

> [!NOTE]
> Programmatūra Microsoft Dynamics 365 izmaksu summas pēc noklusējuma glabā jūsu pamatvalūtā. Taču izmaksu summas, kas tiek rādītas cilnē **Tāmes**, ir līgumslēdzējas struktūrvienības valūtā.  

### <a name="default-sales-price"></a>Noklusējuma pārdošanas cena 

Pārdošanas cenrādi nosaka vai nu pārdošanas entītija, kurai šis projekts ir pievienots, vai projekta klients. Ja ar projektu ir saistīta kāda pārdošanas entītija, piemēram, iespēja, piedāvājums vai līgums, šīs pārdošanas entītijas pārdošanas cenu nosaka pēc cenrāža, kurš ir saistīts ar piedāvājumu vai līgumu. Ja piedāvājumam vai līgumam ir pielāgots cenrādis, projekta tāmēm šis cenrādis tiek izmantots kā noklusējuma pārdošanas cenrādis. Ja nav saistību ar pārdošanas entītijām, kā projekta noklusējuma pārdošanas cenrādis tiek izmantots noklusējuma pārdošanas cenrādis no parametriem, kas atbilst projektā definētajai klienta valūtai.

Katrai tāmes rindai ir ar to saistītā resursu vienība. Resursu vienība norāda organizācijas struktūrvienību, no kuras tiek rezervēti resursi šī uzdevuma izpildīšanai. Lai saistītajām lomām noteiktu pārdošanas cenu, pārdošanas cenrādī meklējiet kombināciju no lomas, vienības un resursu vienības. Ja uzdevumam nav piešķiru, pārdošanas cena šim uzdevumam ir 0,00.

Ja lomas, vienības un resursu vienības kombinācija neatgriež pārdošanas cenu no pārdošanas cenrāža, sistēma ignorē šo vienību. Tā vietā tiek meklēta kombinācija no tikai lomas un resursu vienības. Ja pārdošanas cena tiek atrasta, tiek izmantoti konvertēšanas koeficienti, lai to konvertētu par vienību, kuru atlasījāt pārdošanas tāmes rindā. 

Ja lomas un resursu vienības kombinācija neatgriež pārdošanas cenu no pārdošanas cenrāža, sistēma ignorē šo resursu vienību. Tā vietā tiek meklēta kombinācija no lomas un vienības, lai iestatītu noklusējuma cenu (pēc tam, kad ir izmantota jebkāda konvertēšana).

Ja sistēma neatrod cenu šai lomai, pārdošanas cena tāmes rindā tiek iestatīta uz noklusējuma vērtību **0,00**.

Cilnē **Tāmes** ir režģa skats, kurā ir parādītas tāmju rindas. Šajā režģī ir kolonnas vienībai, kopējai izmaksu cenai un kopējai pārdošanas cenai, kā parādīts nākamajā ilustrācijā. 

> ![Režģa skats cilnē Tāmes.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Projekta tāmju skats ar laika fāzēm

Projekta tāmju skats ar laika fāzēm rāda tāmju datus no režģa skata visā laika grafikā tajā laika skalā, ko atlasījāt. Pēc noklusējuma tāmju dati tiek rādīti dimensijā **Loma**.

> ![Skats ar laika fāzēm projekta tāmēm.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Prognozētās piepūles sadalījums, pamatojoties uz uzdevuma režīmu

Skatā ar laika fāzēm visu uzdevumam prognozēto piepūli varat sadalīt, piepūles stundas piešķirot katram vienības laika periodam atlasītajā laika skalā. Uzdevuma režīms nosaka, kā piepūle tiek sadalīta visā uzdevuma ilgumā. Abi pieejami sadalījumu veidi ir **Vienādi** un **Pamatojoties uz darba stundām**.

### <a name="work-hours-based-allocation"></a>Uz darba stundām pamatotais sadalījums
 
Automātiskās plānošanas uzdevumu režīmā dienas noklusējuma stundu skaits uzdevuma resursiem tiek iestatīts uz pilnu darba stundu koeficientu. Šāda uzvedība ir spēkā, kad piepūle tiek piešķirta, sadalot to visā uzdevuma ilgumā skatā ar laika fāzēm. Piemēram, ja prognozējat, ka uzdevumu pabeigs viens resurss laika skalā **Diena**, tad piepūle, kas tiek piešķirta katrai dienai, nepārsniegs projekta kalendārā definēto dienas darba stundu skaitu. Tādēļ piepūles sadalījums vienmēr nodrošina, lai resursus būtu paredzēts izmantot pilnu dienu.

### <a name="even-allocation"></a>Vienāds sadalījums

Manuālās plānošanas uzdevuma režīmā netiek lietots darba stundu skaits no projekta kalendāra. Tā vietā uzdevuma grafiks ir balstīts uz lietotāja ievadi. Šādiem uzdevumiem piepūles sadalījumam uz vienības laika periodu atlasītajā laika skalā nav nekādu ierobežojošo faktoru. Uzdevuma kopējā piepūle tiek vienādi sadalīta un piešķirta katram vienības laika periodam atlasītajā laika skalā. Tādēļ uzdevumam definētais uzdevuma režīms nosaka piepūles sadalījumu vai piepūles piešķiršanu uz vienības laika periodu tāmēs ar laika fāzēm.

## <a name="grouping-and-time-phasing-options"></a>Grupēšanas opcijas un opcijas sadalīšanai laika fāzēs

Šis skats ar laika fāzēm rāda piepūles, izmaksu un pārdošanas tāmju sadalījumu, pamatojoties uz dienu, nedēļu, mēnesi vai gadu. Pēc noklusējuma tāmju dati tiek rādīti dimensijā **Loma**. Taču varat izmantot opciju **Grupēt pēc**, lai rādīšanai izmantotu divas citas dimensijas: **Kategorija** un **Resurss**.

Gan režģa skatā, gan skatā ar laika fāzēm varat atlasīt, kurus laukus rādīt. Katra laika bloka kopsummas tiek rādītas projekta apakšā. Tajos tiek rādīta kopējā paredzamā piepūle, izmaksas un pārdošana rādītāji par dienu, nedēļu, mēnesi vai gadu. Noklusējuma izmaksu cenai un pārdošanas cenai ir spēkā stāšanās datums. Citiem vārdiem sakot — katram resursam tās mainās, pamatojoties uz jūsu atlasīto skatu ar laika fāzēm.

## <a name="expense-estimates"></a>Izdevumu tāmes

Poga **Pievienot jaunu izdevumu tāmi** režģa skatā ļauj jums ierakstīt jebkādus izdevumus, kas šim projektam ir radušies, bet kas nav tieši saistīti ar darbaspēku. Izdevumu tāmes varat ierakstīt konkrētam uzdevumam vai visam projektam. Atlasiet izdevumu kategorijas un varbūtējo datumu, kad prognozējat šo izdevumu rašanos. Ja saistītajam izmaksu cenrādim un pārdošanas cenrādim ir noklusējuma cenas (vai ja izdevumu kategorijām ir definēts uzcenojuma procentuālais daudzums), pēc piesaistīšanas šīs cenas tiek automātiski ievadītas tāmes rindā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
