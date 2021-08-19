---
title: Darba sadalījuma struktūras pārskats
description: Darba sadalījuma struktūra (WBS) ir projekta darba apraksts. Tā ir uzdevumu hierarhija, kas atspoguļo projekta darba grupas izpratni par darba sastāvu un katra komponenta vai uzdevuma lielumu, izmaksām un ilgumu.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998830"
---
# <a name="work-breakdown-structures-overview"></a>Darba sadalījuma struktūras pārskats

[!include [banner](../includes/banner.md)]

Darba sadalījuma struktūra (WBS) ir projekta darba apraksts. Tā ir uzdevumu hierarhija, kas atspoguļo projekta darba grupas izpratni par darba sastāvu un katra komponenta vai uzdevuma lielumu, izmaksām un ilgumu. WBS ir trīs galvenie mērķi:

-   Aprakstīt darba dalījumu vai sastāvu uzdevumos.
-   Plānot projekta darbu.
-   Novērtēt katra uzdevuma izmaksas.

WBS detalizētības pakāpe ir atkarīga no novērtējuma prasītā precizitātes līmeņa un no šiem novērtējumiem nepieciešamā izsekošanas līmeņa. Projektiem, kuriem ir ļoti zema tolerance attiecībā uz grafika vai izmaksu novirzi, parasti nepieciešams detalizētāks WBS un rūpīga darba progresa un izmaksu izsekošana attiecībā uz WBS. Šāda veida projekti ir izplatīti būvniecības un mašīnbūves nozarēs. 

Turpretim projekti tādās nozarēs kā plašsaziņas līdzekļi un reklāma, programmatūra un IT infrastruktūra parasti ir sava veida projekti, un darba ražīgums ir atkarīgs no tā cilvēka pieredzes un kompetences, kurš veic šo uzdevumu. Tāpēc šīs nozares izmanto WBS, lai tuvinātu projekta apjomu, nevis lai detalizēti sekotu šā projekta virzībai. 

WBS izveide ir intensīvs process, ko parasti veic ilgā laika posmā un kam nepieciešama sadarbība un informācija no dažādām personām. Šajā tēmā ir aprakstīts, kā var izmantot WBS uzlabojumus, lai apmierinātu jūsu prasības attiecībā uz novērtējumiem un izsekošanu.

## <a name="prerequisites-for-creating-a-wbs"></a>Priekšnosacījumi WBS izveidei
Lai izveidotu WBS, ir jāspēj izveidot darba grafiku un novērtēt darba izmaksas.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Priekšnosacījumi darba grafika izveidei

Lai izmantotu visas WBS līdzekļu plānošanas iespējas, veiciet tālāk norādītos iestatījumus:

1.  Iestatiet noklusējuma kalendāru un projekta kalendāru:
    1.  Noklikšķiniet uz **Projekta pārvaldība un grāmatvedība** &gt; **Iestatīšana** &gt; **Projekta pārvaldības un grāmatvedības parametru** &gt; **Plānošana**. Laukā **Noklusējuma darba kalendārs** norādiet noklusējuma kalendāru. Tas būs jebkura jauna izveidotā projekta noklusējuma darba kalendārs.
    2.  Varat mainīt noteikta projekta noklusējuma kalendāru. Noklikšķiniet uz projekta informācijas lapas un pēc tam uz **Projekta darba grupa un plānošana** FastTab, atjauniniet lauku **Plānošanas kalendārs**, atlasot citu kalendāru.

2.  Iestatiet standarta darba dienas un darba stundas. Kalendārs, ko iestatījāt kā sava projekta darba kalendāru, tiks izmantots risinājumā WBS, lai noteiktu šādu informāciju:

-   Darba dienas un brīvdienas
-   Darba stundu skaits dienā

Lai kalendāram iestatītu darba dienas un darba stundas vai izveidotu jaunu kalendāru, noklikšķiniet uz **Organizācijas administrēšana** &gt; **Kopējs** &gt; **Kalendāri**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Darba izmaksu novērtēšanas priekšnosacījumi

Lai izmantotu pilnas izmaksu novērtējuma iespējas WBS, ir jāiestata darbinieku izmaksas un pārdošanas cenas, darba kategoriju izmaksas un maksas, kā arī preces.

-   Lai iestatītu darba izmaksu un pārdošanas cenu izmaksu un maksu kategorijām, noklikšķiniet uz **Projekta pārvaldība un grāmatvedība** &gt; **Iestatīšana** &gt; **Cenas**.
-   Lai iestatītu preču izmaksas un pārdošanas cenu, izmantojiet lapu **Tirdzniecības līgumi** katram vienumam **Izlaistie produkti** saraksta lapā Produktu informācijas pārvaldība.

## <a name="creating-a-wbs"></a>WBS izveide
WBS izveide ietver trīs darbības:

1.  **Darba sadalīšana** — izveidojiet darba sadalījumu starp pārvaldāmiem gabaliņiem vai uzdevumiem.
2.  **Darba grafiks** — novērtējiet laiku, kas nepieciešams uzdevuma izpildei, iestatiet uzdevumu savstarpējās atkarības un atlasiet uzdevumu sākuma un beigu datumus.
3.  **Izmaksu novērtējums** — novērtējiet izmaksas katram uzdevumam.

Turpmākajās sadaļās ir aprakstīts, kā WBS iespējas var palīdzēt katrai no šīm darbībām.

### <a name="work-decomposition"></a>Darba sadalīšana

Darba sadalīšanas vai darba dekompozīcijas izveide parasti ir WBS izveides procesa pirmais solis. WBS funkcionalitāte atbalsta šādas pamata konstrukcijas darba sadalījumam vai sadalīšanai. 

**Projekta saknes uzdevums** Projekta saknes uzdevums ir projekta augšējā līmeņa kopsavilkuma uzdevums. Visi pārējie projekta uzdevumi tiek veidoti zem tā. Saknes uzdevuma nosaukums vienmēr ir iestatīts uz projekta nosaukumu. Saknes mezgla intensitāte, datumi un ilgums apkopo uzdevumu vērtības zem saknes uzdevuma. Saknes mezgla rekvizītus nevar modificēt vai dzēst.

**Kopsavilkumu vai konteineru uzdevumi** Kopsavilkuma uzdevums ir uzdevums, kam zem tā ir pakārtoti uzdevumi vai to sastāvdaļa. Kopsavilkuma uzdevumam nav jebkāda darba ieguldījuma vai izmaksu. Tā vietā darba intensitāte un kopsavilkuma uzdevuma izmaksas ir tās veidojošo uzdevumu darba intensitātes un izmaksu summa. Par kopsavilkuma uzdevuma sākuma datumu izmanto sākotnējo papilduzdevumu sākuma datumu, un par beigu datumu izmanto pēdējo papilduzdevumu beigu datumu. Kopsavilkuma uzdevuma nosaukumu var modificēt, bet nevar modificēt plānošanas rekvizītus intensitātes, datumu un ilguma dēļ. Ja izdzēšat kādu kopsavilkuma uzdevumu, tiek izdzēsti arī visi tā papilduzdevumi. 

**Lapas mezgla uzdevumi** Lapas mezgla uzdevums ir visgranulārākā projekta darba pakotne. Lapu mezglam ir novērtētā intensitāte, plānotais resursu skaits, plānotais sākuma un beigu datums un ilgums. 

Varat pabeigt šādas hierarhijas darbības, lai iespējotu darba hierarhijas izveidi vai projekta sadalīšanu. 

**Jauns uzdevums** Jebkurš jauns izveidotais uzdevums tiek automātiski pievienots zem saknes mezgla, un šim uzdevumam automātiski tiek piešķirts WBS numurs. WBS numurs norāda uzdevuma līmeni hierarhijā. Uzdevumiem, kas atrodas pirmajā līmenī zem projekta saknes uzdevuma, tiek izmantota numerācijas shēma 1, 2, 3 un tā tālāk. Uzdevumiem, kuri atrodas zem pirmā līmeņa, tiek izmantota numerācijas shēma 1.1, 1.2, 1.3 un tā tālāk. Katram līmenim, kas tiek pievienots zem iepriekšējā līmeņa, tiek pievienotas jaunas punktētas skaitļu sērijas. 

Pašlaik WBS numerāciju nevar pielāgot. 

**Uzdevuma atkāpe** Veidojot atkāpi uzdevumam, tas kļūst par pirms tā esošā uzdevuma pakārtoto elementu. Jaunā pakārtotā uzdevuma WBS numurs tiek automātiski pārrēķināts, pamatojoties uz tā jaunā vecāka WBS numuru. Pamatuzdevums tagad ir kopsavilkuma vai konteinera uzdevums, un tāpēc tas kļūst par tā sastāvā esošo uzdevumu apkopojumu. 

> [!NOTE] 
> Kad saskaņā ar uzdevumu, kas bija lapas mezgls pirms atkāpes darbības, tiek izveidota atkāpe, jaunizveidotais kopsavilkuma uzdevums zaudē savus datumus, intensitāti un resursu skaitu. Tagad tas izmanto savu jauno pamatuzdevumu vērtību kopsavilkumu. 

**Uzdevuma pārkaru atkāpes izveide** Kad izveidojat uzdevuma pārkaru atkāpes, tas vairs nav tā vecākuzdevums. Šī uzdevuma WBS numurs tiek automātiski pārrēķināts, lai atspoguļotu uzdevuma jauno līmeni hierarhijā. Uzdevuma iepriekšējā vecākuzdevuma intensitāte, izmaksas un datumi tiek pārrēķināti, lai izslēgtu šo uzdevumu. 

**Pārvietot uz augšu un pārvietot uz leju** Noklikšķinot uz **Pārvietot uz augšu** un **Pārvietot uz leju**, varat mainīt uzdevuma atrašanās vietu atbilstoši tā primārajai hierarhijai. Pozīcija neietekmē uzdevuma intensitāti, izmaksas, datumus un ilgumu. Tomēr uzdevuma WBS numurs tiek automātiski pārrēķināts, lai atspoguļotu uzdevuma jauno pozīciju.

### <a name="schedule-estimation"></a>Grafika novērtējums

Grafika novērtējums parasti ir otrais solis WBS izveidē. Pēc uzdevumu izveides kā labākā prakse ir jāveic grafika novērtēšana. Sadaļā Finanses lapai **Darba sadalījuma struktūra** ir divas sadaļas. Augšējā rūts ir paredzēta plānotajam novērtējumam, un apakšējā rūtī ir iekļauta cilne **Prognozējamās izmaksas un ieņēmumi**, ko var izmantot izmaksu novērtēšanai. 
**Uzdevumu atkarības** WBS varat izveidot pirmstecīgas relācijas starp uzdevumiem. Piešķirot uzdevumam pirmstecīgos uzdevumus, šo uzdevumu var sākt tikai pēc tam, kad visi pirmstecīgie uzdevumi ir izpildīti. Plānotā uzdevuma sākuma datums automātiski tiek iestatīts uz visu tā priekšteču pēdējo datumu. 

**Uzdevumu plānošana** Lapas mezglu uzdevumu plānošanai nosaka šādus faktorus:

-   Pirmstecīgie uzdevumi
-   Ieguldījums
-   Resursu skaits
-   Sākuma un beigu datumi

Lapas mezgla uzdevuma, kuram nav priekšteču, sākuma datums tiek automātiski iestatīts uz projekta plānošanas sākuma datumu. Lapas mezgla uzdevuma ilgums vienmēr tiek aprēķināts kā darba dienu skaits no tā sākuma līdz beigu datumam. 

*<strong><em>Plānošanas kārtulas</em></strong>* Kad ir ieslēgta automātiskās plānošanas palīdzība, lapas mezgla uzdevumiem tiek lietotas šādas kārtulas uzdevumu plānošanai:

-   Uzdevuma sākuma un beigu datumam ir jābūt darbdienās atbilstoši projekta plānošanas kalendāram.
-   Uzdevuma, kam ir pirmstecīgi uzdevumi, sākuma datums automātiski tiek iestatīts kā to pirmstecīgo uzdevumu vēlākais datums.
-   Uzdevuma intensitāti automātiski aprēķina šādi:

Personu skaits × Ilgums × Stundu skaits standarta projekta kalendāra darba dienā. 

Dažos gadījumos ieteicams atkāpties no šīm kārtulām. Varat izslēgt automātisko plānošanu, lai neļautu Finance automātisku lapas mezgla uzdevumu rekvizītu iestatīšanu vai labošanu. Ievadot informāciju par uzdevumu, kas izraisa jebkuru plānošanas noteikumu pārkāpumu, uzdevumam tiek parādīta plānošanas kļūdas ikona. Ja nevēlaties rādīt plānošanas kļūdas, noklikšķiniet uz **Tiek rādītas plānošanas kļūdas**, lai izslēgtu šo līdzekli. 

> [!NOTE] 
> Kopsavilkuma vai konteinera uzdevuma vērtības turpina aprēķināt kā saistīto uzdevumu vērtību summu neatkarīgi no tā, vai automātiskā plānošanas palīdzība ir ieslēgta vai izslēgta. 

**Plānošanas kļūdu labošana** Ja ir ieslēgta automātiskās plānošanas palīdzība, plānošanas kļūdas nav iespējamas. Tomēr, ja izslēdzat automātiskās plānošanas palīdzību un pēc tam vēlāk to atkal ieslēdzat, plānošanas kļūdu ikonas var tikt parādītas WBS. 

**Plānošanas kļūdu labošana pēc uzdevuma** Veicot dubultklikšķi uz plānošanas kļūdas ikonas noteiktam uzdevumam, dialoglodziņā tiek parādītas visas šī uzdevuma plānošanas kļūdas. Varat izlemt, kādas plānošanas kļūdas uzdevumam ir jālabo. 

**Visu plānošanas kļūdu labošana** Ja vēlaties, lai Finance labotu visas plānošanas kļūdas WBS, darbību rūtī noklikšķiniet uz **Labot visas plānošanas neatbilstības**. 

> [!NOTE] 
> Šis līdzeklis var izraisīt nozīmīgas WBS modifikācijas. Kļūdas tiek labotas šādā secībā:

1.  Visu uzdevumu aprēķinātā intensitāte tiek modificēta, lai tā būtu vienāda ar projekta kalendārā noteikto noslodzi.
2.  Katra uzdevuma sākuma datums tiek mainīts, lai uzdevums sāktos pēc tam, kad visi priekštecīgie uzdevumi ir pabeigti.
3.  Katra uzdevuma sākuma datums tiek modificēts, lai noņemtu nepilnības priekštecīgo uzdevumu sākuma datumos.

### <a name="cost-estimation"></a>Izmaksu aprēķins

Kā minēts iepriekš šajā dokumentā, ir jāievada izmaksu novērtējums katram lapas mezgla uzdevumam, izmantojot cilni **Prognozējamās izmaksas un ieņēmumi**, kas atrodas lapas **Darba sadalīšanas struktūra** apakšējā rūtī. 

> [!NOTE] 
> Kopsavilkuma vai konteinera uzdevuma izmaksu novērtējumu nevar modificēt. Kopsavilkuma uzdevuma izmaksu novērtējums ir vienāds ar tās lapu mezgla uzdevumu izmaksu aplēses summu. Katram uzdevumam paredzētās kopējās izmaksas aprēķina kā šādu transakciju tipu prognozējamo izmaksu summu:

-   Darbs
-   Elements vai materiāls
-   Izdevumi

Transakcijas tips **Maksa** tiek izmantots, lai novērtētu uz izmaksām balstītus ieņēmumus. Šis transakcijas tips nav izmaksu komponents, un tāpēc netiek ņemts vērā, kad tiek aprēķinātas izmaksas. 

Transakcijas tips **Uzņēmuma** tiek izmantots, lai fiksētas vērtības projekta tipā reģistrētu līgumā noteikto pārdošanas vērtību. Šis transakcijas tips netiek ņemts vērā, novērtējot izmaksas. 

Novērtējot izmaksas attiecībā uz darbu, materiāliem un izdevumiem katram uzdevumam, ir jāpiešķir projekta kategorija prognozējamām izmaksām. 

**Darba izmaksu novērtēšana** Katram lapas mezgla uzdevumam piešķirat darba intensitāti stundās un noklusējuma kategoriju. Tāpēc, iestatot uzdevuma grafiku, darba izmaksu novērtējums šim uzdevumam tiek automātiski pievienots darba noklusējuma kategorijā. Šis izmaksu novērtējums ir redzams šī uzdevuma režģī **Rindas papildinformācija**, cilnē **Novērtētās izmaksas un ieņēmumi**. Ja ir nepieciešami papildu darba izmaksu novērtējumi, tos var pievienot šajā cilnē. Ja darba izmaksu novērtējumā tiek palielinātas vai samazinātas stundas, uzdevuma grafiks tiek automātiski pārrēķināts. 

**Izmaksu un materiālu izmaksu novērtējums** Cilnē **Novērtētās izmaksas un ieņēmumi** var novērtēt uzdevuma izmaksas un materiālu izmaksas, ja novērtējumi ir nepieciešami. 

Izmaksu un pārdošanas cena katrai darba vai izdevumu novērtējuma rindai ir balstīta uz iestatījumiem, kas katrai kategorijai ir definēti cenu noteikšanas tabulās šeit: **Projekta pārvaldība un grāmatvedība** &gt; **Iestatīšana** &gt; **Cenas noteikšana**. Vienumiem izmaksu un pārdošanas cena pēc noklusējuma tiek pievienota no vienuma vai tirdzniecības līgumiem saraksta lapā **Izlaistie produkti** sadaļā Produktu informācijas pārvaldība.

## <a name="tracking-progress-on-the-wbs"></a>Sekošana norisei risinājumā WBS
Dažas nozares seko projekta norisei attiecībā uz WBS ļoti detalizētā līmenī, savukārt citas seko norisei augstākā WBS līmenī. Šajā sadaļā ir aprakstīts, kā var izmantot WBS izsekošanu jūsu projekta vajadzībām. 

Finance ir trīs skati projekta WBS: plānošanas skats, intensitātes izsekošanas skats un izmaksu izsekošanas skats.

### <a name="planning-view"></a>Plānošanas skats

Plānošanas skatā tiek parādīts plānotais vai bāzlīnijas grafiks un informācija par izmaksām. Kaut arī nav līdzekļu, kas attiecas uz projekta WBS versiju un bāzlīniju izsekošanu, šajā skatā ietvertās vērtības ir paredzētas, lai attēlotu bāzlīnijas versiju. Šīs tēmas Grafika novērtējuma un Izmaksu novērtējuma sadaļas apraksta šo skatu un to, kā tas tiek izmantots WBS izveidei.

### <a name="effort-tracking-view"></a>Piepūles izsekošanas skats

Skats Intensitātes izsekošana parāda darba izpildes sekošanu WBS. Tas salīdzina resursa uzkrāto faktisko intensitāti ar plānotās intensitātes stundām. Šīs formulas nodrošina vērtības Intensitātes izsekošanas skatā:

-   Progresa procentuālais = Faktiskā intensitāte līdz šim ÷ Uzdevumam plānotā intensitāte
-   Atlikusī intensitāte (zināma arī kā Novērtējumi līdz \[ETC\] pabeigšanai) = Plānotā intensitāte – Faktiskā intensitāte līdz šim
-   Novērtējums pabeigšanas laikā (EAC) = Atlikusī intensitāte + Faktiskā intensitāte līdz šim
-   Projektētā piepūles novirze = Plānotā piepūle - EAC

Intensitātes izsekošanas skats parāda uzdevuma intensitātes novirzes projekciju, pamatojoties uz to, vai EAC ir lielāks vai mazāks par plānoto intensitāti:

-   Ja EAC ir lielāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs vairāk laika, nekā sākotnēji plānots, un tas atpaliek no grafika.
-   Ja EAC ir mazāks par plānoto intensitāti, tiek prognozēts, ka uzdevums prasīs mazāk laika, nekā sākotnēji plānots, un tas ir pirms grafika.

**Projekta pārvaldnieka intensitātes atkārtota projicēšana** Dažkārt projekta pārvaldniekam vai citai personai, kas seko projekta norisei, ir jāpārskata uzdevuma sākotnējie novērtējumi. Dažādu iemeslu dēļ uzdevums var norisēt ātrāk vai lēnāk, nekā sākotnēji bija paredzēts. Piemēram, tvērums ir samazināts vai arī darbiniekiem ir mazāk pieredzes, nekā sākotnēji plānots. Prognozes ir projekta pārvaldnieka izpratne par novērtējumiem, pamatojoties uz projekta pašreizējo statusu. Parasti bāzlīnijas skaitļus nevajadzētu mainīt, jo projekta bāzlīnija attēlo projekta grafika un izmaksu tāmes dokumentu, kam piekritušas visas projekta ieinteresētās puses. 

Ir divi veidi, kā projektu pārvaldnieki var mainīt uzdevumu intensitāti:

-   Modificēt atlikušo intensitāti, kas tiek automātiski iestatīta atjaunināt uzdevuma faktisko atlikušo intensitāti.
-   Modificēt norises procentuālo vērtību, kas automātiski iestatīta, lai atjauninātu uzdevuma patieso norisi.

Abas šīs pieejas izraisa uzdevuma ETC, EAC progresa procentu, kā arī uzdevuma prognozētās intensitātes novirzes pārrēķināšanu. Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un to prognozētā intensitātes novirze tiek atjaunināta. 

**Pārveidota intensitāte kopsavilkuma uzdevumiem** Varat mainīt kopsavilkuma vai konteinera uzdevumu intensitāti. Neatkarīgi no tā, vai modificējat šīs vērtības, izmantojot atlikušo intensitāti vai izpildes procentuālo daudzumu kopsavilkuma uzdevumos, aprēķini tiek veikti automātiski šādā secībā:

1.  Uzdevumam tiek aprēķināts EAC, ETC un progresa procentuālais daudzums.
2.  Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādā pašā proporcijā kā sākotnējā EAC summa.
3.  Katram lapas mezgla uzdevumam tiek aprēķināts jauns EAC.
4.  Atlikusī intensitāte un norises procenti tiek pārrēķināti visiem ietekmētajiem pakārtotajiem uzdevumiem, pamatojoties uz jauno EAC vērtību. Tiek pārrēķināta arī uzdevumu intensitātes novirze.
5.  Kopsavilkuma uzdevumu EAC tiek pārrēķināts arī no lapu mezgliem.

Noklikšķiniet uz **Izvērst līdz līmenim** intensitātes izsekošanas skatā, lai iestatītu līmeni, kurā izsekot un uzturēt jūsu WBS. WBS tiek automātiski izvērsta līdz šim līmeni Intensitātes izsekošanas skatā, kad vien tas tiek atvērts.

### <a name="cost-tracking-view"></a>Izmaksu izsekošanas skats

Izmaksu izsekošanas skats rāda uzdevuma izmaksu patēriņa izsekošanu. Šajā skatā faktiskās izmaksas, kas tika iztērētas uzdevumam līdz šim, tiek salīdzinātas ar uzdevuma plānotajām izmaksām. Šīs formulas nodrošina vērtības izmaksu izsekošanas skatā:

-   Patērēto izmaksu procentuālais daudzums = Faktiskās izmaksas līdz šim ÷ Uzdevumam plānotās izmaksas
-   Izmaksas līdz pabeigšanai (CTC) = Plānotās izmaksas - Faktiskās izmaksas līdz šim
-   Novērtējums pie pabeigšanas (EAC) = CTC + Faktiskās izmaksas līdz šim
-   Projektētā izmaksu novirze = Plānotās izmaksas - EAC

Izmaksu izsekošanas skats parāda uzdevuma izmaksu starpības projekciju, pamatojoties uz to, vai EAC ir lielāka vai mazāka par plānotajām izmaksām:

-   Ja EAC ir lielākas par plānotajām izmaksām, tiek prognozēts, ka uzdevums izmantos vairāk naudas, nekā sākotnēji plānots, un tas pārsniegs budžetu.
-   Ja EAC ir mazākas par plānotajām izmaksām, tiek prognozēts, ka uzdevums izmantos mazāk naudas, nekā sākotnēji plānots, un tas iekļausies budžetā.

**Projektu vadītāja veiktā izmaksu pārprojektēšana** Projektu pārvaldniekiem jāizmanto CTC, lai pārskatītu uzdevuma sākotnējo izmaksu novērtējumu. Projekta pārvaldnieks var modificēt CTC vērtību izmaksām, kas nepieciešamas, lai izpildītu šo uzdevumu. Ja modificējat CTC vērtību, tiek pārrēķināta uzdevuma CTC, EAC un patērētās izmaksas procentuālā daļa, kā arī uzdevuma prognozētā izmaksu novirze. Tiek pārrēķināta arī EAC, ETC un procentuālā daļa no izmaksām, kas patērētas, veicot kopsavilkuma uzdevumus, un tiek atjaunināta to plānotā izmaksu starpība. 

> [!NOTE] 
> Pārskatot intensitāti WBS uzdevumam Intensitātes izsekošanas skatā, uzdevuma CTC, EAC, patērētā izmaksu procentuālā daļa, un plānotā izmaksu novirze tiek pārrēķināta izmaksu izsekošanas skatā. Tomēr izmaksu pārskatīšana neietekmē vērtības Intensitātes izsekošanas skatā, jo izmaksas pa darbību tipiem (darbs, materiāls vai izdevumi) vai projekta kategorijām netiek pārskatītas. 

**Izmaksu prognozes pārskatīšana par kopsavilkuma uzdevumiem** Varat pārskatīt izmaksas kopsavilkuma uzdevumiem, un aprēķini tiek veikti automātiski šādā secībā:

1.  Uzdevumam patērētās izmaksas EAC, CTC un procentuālā tiek pārrēķinātas.
2.  Jaunā EAC pakārtotajiem uzdevumiem tiek sadalīta tādā pašā proporcijā kā sākotnējā EAC uzdevumiem.
3.  Tiek aprēķināts jaunais katra uzdevuma EAC.
4.  CTS un patērētās izmaksas procentos tiek pārrēķinātas ietekmētajiem pakārtotajiem uzdevumiem, pamatojoties uz EAC vērtību. Tiek pārrēķināta arī uzdevumu izmaksu novirze.
5.  Visu kopsavilkuma uzdevumu EAC tiek pārrēķinātas, pamatojoties uz šīm izmaiņām.

Noklikšķiniet uz **Izvērst līdz līmenim** izmaksu izsekošanas skatā, lai iestatītu līmeni, kurā izsekot un uzturēt jūsu WBS. WBS tiek izvērsta līdz šim līmeni izmaksu izsekošanas skatā, kad vien tas tiek atvērts.

### <a name="earned-value-management"></a>Iegūtās vērtības pārvaldība

Var izmantot iegūto vērtību metodi (EVM), lai sekotu projekta norisei. Iegūtās vērtības datus var skatīt projekta pārvaldnieka lomu centrā. Iegūto vērtību diagrammas komponents parāda plānotās vērtības un faktiskās izmaksas laika fāzes vērtības. Iegūtā vērtība no pašreizējā datuma tiek parādīta kā punkts. Iegūtās vērtības laika posma dati pašlaik nav pieejami. 

Laika posms iegūto vērtību diagrammā tiek parādīts pēc nedēļas vai mēneša. Šajā sadaļā aprakstīti trīs EVM pīlāri: plānotā vērtība, iegūtā vērtība un faktiskās izmaksas. 

**Plānotā vērtība** EVM teorija nosaka, ka plānotā vērtība ir likme, pēc kuras projekta darba grupa plāno iegūt projekta vērtību. 

Finance izmanto 0:100 peļņas kārtulu, kad tā atzīmē plānoto vērtību. Saskaņā ar šo kārtulu uzdevuma vērtība uzdevumam tiek grāmatota tā beigu datumā. Vērtība netiek grāmatota, kamēr uzdevums nav izpildīts par 100 procentiem. 

Sadaļā Projektu pārvaldība un grāmatvedība ievadiet lapas mezglu beigu datumu un tam paredzētās izmaksas. Kad plānotās vērtības grafiks tiek parādīts pēc nedēļas, plānotā vērtība projekta darbības laikā tiek apkopota pēc nedēļas visiem lapu mezgla uzdevumiem. 

**Iegūtā vērtība** EVM teorija nosaka, ka iegūtā vērtība ir likme, pēc kuras projekta darba grupa patiesībā iegūst projekta vērtību. 

Finance izmanto 0:100 peļņas kārtulu, kad tā atzīmē iegūto vērtību. Saskaņā ar šo kārtulu uzdevuma vērtība uzdevumam tiek grāmatota tā beigu datumā. Vērtība netiek grāmatota, kamēr uzdevums nav izpildīts par 100 procentiem. 

Kad tiek aprēķināta iegūtā vērtība, tiek ņemta vērā katra uzdevuma norise procentos. Saskaņā ar 0:100 peļņas kārtulu, tiek ņemti vērā tikai uzdevumi, kas ir pabeigti noteiktā laika periodā, aprēķinot iegūto vērtību no šī perioda beigām. Projektā iegūtā vērtība tiek aprēķināta, izmantojot visus uzdevumus, kas ir pabeigti, kad grafiks ir izveidots. 

> [!NOTE] 
> Pašlaik WBS izsekošanas sistēmai nav datu struktūru, lai katrā no šiem uzdevumiem glabātu vēsturiskos norises procentus. Tāpēc iegūto vērtību var uzrādīt tikai no kuba apstrādes brīža. Regulāri apstrādājiet kubu, lai atjauninātu iegūto vērtību datus, kas tiek rādīti lomu centrā. 

**Faktiskās izmaksas** EVM teorija norāda, ka faktiskais izmaksu rādītājs ir likme, ar kādu nauda tiek tērēta projektā. 

Transakcijas, kas ir grāmatotas projektā, tiek izmantotas, lai iezīmētu faktisko izmaksu rindu. Izmaksas tiek apkopotas pēc datuma. Pēc tam šie dati tiek izmantoti, lai uzkrātu faktiskās izmaksas pēc nedēļas vai mēneša iegūto vērtību diagrammā.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Kā izmantot plānotās vērtības, iegūtās vērtības un faktisko izmaksu konceptus

**Plānošanas novirzes** Plānošanas laikā izveidojiet prognozi darbam ar laika grafiku. Tāpēc plānotā vērtība ir likme, pēc kuras projekta plānotāji domāja, ka projekta īstenošana tiks pabeigta. Pēc tam, kad projekts ir progresā, darbs ir pabeigts, un projekts iegūst vērtību. Salīdzinot plānoto vērtību ar iegūto vērtību, varat apskatīt, kā virzās darbs ar projektu. Šī salīdzinājuma rezultātu sauc par grafika novirzi. 

Ja plānotā vērtība periodam ir lielāka par iegūto vērtību, projekta darba apjoms ir mazāks par plānoto. Tāpēc projekts atpaliek no grafika. Tā kā plānotā vērtība un nopelnītā vērtība ir izteikta naudas izteiksmē, kavētajam laikam projektā tiek piešķirta arī naudas vērtība. 

Ja plānotā vērtība periodam ir mazāka par nopelnīto vērtību, projekta darba apjoms ir lielāks par plānoto. Tāpēc projekts ir pirms grafika. Šim interesenta laikam tiek piešķirta arī naudas vērtība.

**Izmaksu novirze** Tā kā iegūtā vērtība izmanto izmaksu cenu kā reizinātāju, iegūtā vērtība norāda projekta darba izmaksas. Projekta norises laikā transakciju žurnāls sniedz ierakstu par naudu, kas faktiski tiek tērēta šim projektam. Salīdzinot iegūto vērtību ar faktiskajām izmaksām, varat skatīt naudas summu, kas tiek tērēta, salīdzinot ar vērtību, kas ir iegūta. Šī salīdzinājuma rezultātu sauc par izmaksu novirzi. 

Ja faktiskās izmaksas, kas tiek tērētas par periodu, ir lielākas nekā iegūtā vērtība, ir iztērēts vairāk naudas nekā iegūts. Tāpēc projekts pārsniedz budžetu. 

Ja faktiskās izmaksas, kas tiek tērētas par periodu, ir mazākas par iegūto vērtību, tad vairāk naudas tika nopelnīts nekā iegūts. Tāpēc projekts nepārsniedz budžetu.

## <a name="wbs-templates"></a>WBS veidnes
WBS veidņu funkcionalitāti var izmantot, lai projektiem izveidotu standarta veidnes. Ja jūsu uzņēmuma piedāvātajos projektos ir daudz atkārtojamu darbu, apsveriet iespēju izveidot WBS veidni. 

WBS veidni var izveidot no esoša projekta WBS, lai šī projekta plānošanas laikā iegūtās zināšanas un paraugpraksi varētu atkārtoti izmantot līdzīgos projektos nākotnē. Tomēr dažkārt nav jēgas saglabāt visu WBS kā veidni. Tāpēc veidnes var izveidot arī no projekta WBS daļām.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekta WBS kā veidnes saglabāšana

Pēc veidnes izveides to var importēt jaunā projekta WBS zem saknes mezgla vai jebkurā projekta WBS uzdevumā.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS veidnes importēšana projekta WBS

Importējot uzdevumus, tie veidnē tiek organizēti, pamatojoties uz tā uzdevuma sākuma datumu, kurā tie ir importēti. Importēšanas laikā pirmstecīgas relācijas veidnes uzdevumos tiek izmantotas, lai aprēķinātu importēto uzdevumu sākuma datumus. Mērķa projekta standarta darba kalendārs tiek lietots, lai aprēķinātu importēto uzdevumu beigu datumus tā, lai tiktu saglabātas darba dienas un standarta darba stundas, kas ir definētas pašreizējā projekta darba kalendārā. 

Izmaksu summas un pārdošanas cenas novērtējuma rindās tiek lietotas, lai garantētu, ka projektam vai projekta līgumam raksturīgās cenas ir derīgas.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projekta WBS un WBS veidnes atšķirības

-   WBS veidnēs nav sākuma datumu un beigu datumu.

Darba un ārpus darba dienas nav iestatītas WBS veidnēm.

-   WBS veidnes vienmēr izmanto plānošanas kalendāru, kas ir iestatīts kā visu projektu noklusējuma kalendārs.

Noklusējuma plānošanas kalendārs tiek izmantots tikai, lai noteiktu stundas standarta darba dienā.

-   Pirmstecīgas relācijas netiek iekopētas WBS veidnē.

Tā kā WBS veidnēm nav datumu, sākuma datuma loģika, kuras pamatā ir priekšteča beigu datums, nav obligāti jāaizpilda.

-   Darba izmaksu novērtējuma rinda tiek izveidota automātiski, kad uzdevums ir izveidots WBS veidnē. Pārdošanas cena un izmaksu summa tiek kopēta no atlasītā darbinieka.

Izmaksu un vienumu izmaksas var izveidot manuāli, tāpat kā to var darīt projekta WBS.

-   Plānošanas kļūdas tiek parādītas, ja ir novirzes no šādas formulas:

Intensitāte = Resursu skaits × Ilgums × Stundu skaits standarta darba dienā 

Vienlaikus var labot visas plānošanas kļūdas, noklikšķinot uz **Labot visas plānošanas kļūdas**. 

Vai arī plānošanas kļūdas var labot atsevišķi, noklikšķinot uz katra uzdevuma brīdinājuma ikonas.





[!INCLUDE[footer-include](../includes/footer-banner.md)]