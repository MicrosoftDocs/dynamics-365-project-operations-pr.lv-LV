---
title: Darba grupas dalībnieku pievienošana no darba grupas dalībnieku režģa
description: Šajā rakstā ir sniegta informācija par to, kā varat pārvaldīt grupas dalībnieku resursus.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928579"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Darba grupas dalībnieku pievienošana no darba grupas dalībnieku režģa

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations ietver Resursu pārvaldnieka informācijas paneli, kas nodrošina vizuālu pārskatu par resursu pieprasījumu un lietojumu visā organizācijā. Diagrammas šajā informācijas panelī var izmantot, lai vizualizētu tālāk norādīto informāciju.

- **Resursu pieprasījums**: diagrammā **Aktīvais resursu pieprasījums** ir parādīti iesniegtie resursi. Šie resursi ir apkopoti vai nu pēc lomas, vai pēc projekta.
- **Neiesniegts resursu pieprasījums**: diagrammā **Nepiešķirts resursu pieprasījums** ir parādītas visas resursu vajadzības, kas nav iesniegtas. Šī diagramma palīdz Resursu pārvaldniekiem apskatīt pieprasījumu, kas nav apstiprināts un ko varētu iesniegt, izmantojot resursa pieprasījumu.
- **Apmaksājamā izmantošana iepriekšējai nedēļai**: diagrammā **Izmantošana pēc lomas** ir parādīts organizācijas faktiskās apmaksājamajās izmantošanas procentuālais daudzums pēc lomas salīdzinājumā ar mērķa izmantošanu pēc lomas.

    > [!NOTE]
    > Lai diagrammu **Izmantošana pēc lomas** padarītu pieejamu, izveidojiet darbu, kurā tiek izpildīta darbplūsma **UpdateRoleUtilization**. Šis periodiskais darbs tiek palaists ik pēc septiņām dienām, lai aprēķinātu apmaksājamo izmantošanu iepriekšējām septiņām dienām. Rezultāti tiek apkopoti pēc lomas.

## <a name="manage-project-team-members"></a>Projekta darba grupas dalībnieku pārvaldīšana

Projektu vadītāji var izmantot šo Resursu pārvaldnieka informācijas paneli, lai projektos pārvaldītu resursus. Viņi var, piemēram, pievienot darba grupas dalībnieku tieši projektam un rezervēt darba grupas dalībnieku, lai izpildītu resursu vajadzības, kuras tvēra kāds vispārējais resurss.

### <a name="add-a-team-member-directly-to-a-project"></a>Darba grupas dalībnieka pievienošana tieši projektam

Lai kādu darba grupas dalībnieku pievienotu tieši projektam, veidlapā **Projekti**, cilnē **Darba grupa** atlasiet **Jauns**. Tiek parādīts dialoglodziņš **Ātrā izveide:Projekta darba grupas dalībnieks**. Šajā dialoglodziņā varat veikt tālāk norādītos uzdevumus.

- **Rezervēt nosauktu resursu**: laukā **Rezervējamais resurss** atlasiet resursa nosaukumu. Pēc tam atlasiet lomu, iestatiet periodu un atlasiet piešķiršanas metodi. Jūsu atlasītais nosauktais resurss tiek pievienots projektam, izmantojot atlasīto sadalījuma metodi un resursu kalendāru.
- **Pievienot vispārēju resursu**: lauku **Rezervējamais resurss** atstājiet tukšu un pēc tam atlasiet lomu, iestatiet periodu un atlasiet vēlamo piešķiršanas metodi. Darba grupai kā vietturis tiek pievienots vispārējs resurss. Vietturis uztur pieprasījuma modeli, kas tiek izmantots nosaukto resursu rezervēšanai darba grupā. Šī vajadzība tiek izpildīta atbilstoši projekta kalendāram.
- **Pievienot darba grupai nosauktu resursu, nepatērējot resursa noslodzi**: laukā **Rezervējamais resurss** atlasiet kādu resursu. Atlasiet periodu un pēc tam kā sadalījuma metodi atlasiet **Nav**. Resurss tiek pievienots darba grupai, bet ar rezervēšanu šī resursa noslodze netiek patērēta.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Darba grupas dalībnieka rezervēšana, lai izpildītu resursu vajadzības attiecībā uz vispārēju resursu

Pakalpojumā Project Operations varat rezervētu kādu vispārējo resursu projekta darba grupā. Varat arī norādīt lomu, nepieciešamo noslodzi un veidu, kā šī noslodze ir jāizplata. Kā resursa vajadzību varat norādīt atribūtus, kas ir saistīti ar šo vispārējo resursu. Šie atribūti tostarp ir nepieciešamās prasmes, vēlamā organizācijas struktūrvienība un vēlamie resursi.

Lai vispārējā resursā kādam izstrādātājam norādītu nepieciešamās prasmes, izpildiet tālāk aprakstītās darbības.

1. Veidlapā **Projekti**, cilnē **Darba grupa** atlasiet vienumu **Jauns**, lai rezervētu kādu vispārējo resursu.
2. Skatā **Visi darba grupas dalībnieki**, kolonnā **Resursu vajadzība** atlasiet saiti, lai vispārīgajam resursam pievienotu nepieciešamās prasmes.
3. Veidlapā **Resursu vajadzība**, režģī **Prasmes** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot jaunu vajadzības īpašību**, lai savam izstrādātājam pievienotu nepieciešamās prasmes.
4. Dialoga veidlapā **Ātrā izveide: Vajadzības īpašība**, un tā laukā **Īpašība** atlasiet nepieciešamo prasmi.
5. Laukā **Novērtējuma vērtība** atlasiet kvalifikācijas līmeni šai prasmei. 
6. Laukā **Resursu vajadzība** iestatiet šo vajadzību, lai tā kā avotu izmantotu resursus no organizācijas struktūrvienībām vai pat nosauktiem resursiem. Kad esat pabeidzis, noklikšķiniet uz **Saglabāt**.
7. Veidlapā **Resursu vajadzība** atlasiet **Rezervēt**, lai izpildītu resursu vajadzību. Varat arī atlasīt vispārējo resursu režģī **Visi darba grupas dalībnieki** un pēc tam atlasīt vienumu **Rezervēt**.

    > [!NOTE]
    > Šajā piemērā ir 40 pieprasītās stundas, bet nav faktiski rezervētu stundu, jo vispārējiem resursiem nav rezervāciju. Turklāt nav piešķirtu stundu, jo vispārējais resurss tika pievienots tieši darba grupai, nevis pievienots, izmantojot uzdevuma piešķiri.

    Veidlapā **Plānošanas palīgs** pieejamos resursus varat filtrēt pēc vajadzībām, kas ir norādītas resursu vajadzībā. Resursi tiek kārtoti atbilstoši plānošanas panelī norādītajiem kārtošanas parametriem.

   Daži no biežāk izmantotajiem filtriem ir šādi:

    - **Īpašības kopā ar novērtējumu**: papildus kvalifikācijas novērtējumiem filtrēt arī pēc prasmēm, sertifikācijām un citām resursu īpašībām.
    - **Lomas**: filtrēt pēc noklusējuma lomām, kas ir piešķirtas rezervējamiem resursiem.
    - **Organizācijas struktūrvienības**: filtrēt rezervējamos resursus pēc organizācijas struktūrvienībām, kurām tie ir piešķirti.

8. Ja neesat apmierināts ar sākotnējās vajadzības meklēšanas rezultātiem, varat mainīt šos filtrēšanas kritērijus. Izvērsiet rūti **Filtra skats** kreisajā pusē un pēc tam atlasiet **Meklēt**, lai atrastu papildu resursus. Lai mainītu rezultātu kārtošanas veidu, atlasiet vienumu **Kārtot**.
9. Atlasiet resursus atbilstoši pieprasījumam, kas ir norādīts vajadzībā, kā redzams režģa augšpusē. Šūnu atlasi režģī varat notīrīt un atstāt šo resursa noslodzi atvērtu. Kā rezervētu vienlaikus var atlasīt tikai vienu resursu.
10. Atlasiet **Rezervēt**, lai rezervētu atlasīto resursu, un atstājiet plānošanas paneli atvērtu, lai varētu atlasīt papildu resursus. Var arī atlasīt **Rezervēt un iziet**, lai rezervētu atlasīto resursu un aizvērtu plānošanas paneli.
11. Atgriezieties skatā **Visi darba grupas dalībnieki**. Pievērsiet uzmanību, ka režģī šis vispārējais resurss ir aizstāts ar nosaukto resursu, un 40 stundas šim resursam ir norādītas kā rezervētas.

    > [!NOTE]
    > Netiek rādīta neviena piešķirtā stunda, jo tās tika rezervētas tieši darba grupai. Tās netika rezervētas, izmantojot uzdevumu piešķiršanu.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Vispārēju resursu piešķiršana uzdevumiem un resursu vajadzību ģenerēšana

Programmā Project Operations varat izveidot uzdevumus un pēc tam šiem uzdevumiem piešķirt vispārējos resursus. Pēc tam resursu pieprasījumu var parādīt kā vietturus, kamēr veidojat grafika un finanšu skaitļu tāmi. Pēc tam varat ģenerēt resursu vajadzības attiecībā uz vispārīgajiem resursiem un izpildīt tās.

1. Veidlapā **Projekti**, cilnē **Grafiks** atlasiet vienumu **Pievienot**, lai izveidotu uzdevumu.
2. Laukā **Resursi** atlasiet simbolu **Resursu atlasītājs**. Tiek parādīts resursu atlasītājs, un tajā tiek rādīti šim projektam esošie darba grupas dalībnieki.
3. Ievadiet jaunā vispārējā resursa nosaukumu un pēc tam atlasiet vienumu **Izveidot**.
4. Tiek parādīts dialoglodziņš **Ātrā izveide: Projekta darba grupas dalībnieks**, un tā laukā **Loma** atlasiet lomu šim vispārējam resursam. 
5. Laukā **Resursu vienība** atlasiet organizācijas struktūrvienību šim vispārējam resursam. Pēc tam atlasiet **Saglabāt**. Tagad vispārējais darba grupas dalībnieks ir piešķirts šim uzdevumam.

   Cilnē **Darba grupa** ir redzams jaunais vispārējais darba grupas dalībnieks. Ievērojiet, ka tam ir tikai piešķirtas stundas. Šīs stundas ir summa no visiem tiem uzdevumiem, kas ir piešķirti vispārējam darba grupas dalībniekam. Vispārējam darba grupas dalībniekam nav nepieciešamo stundu vai resursu vajadzības.

6. Tagad šo vispārējo darba grupas dalībnieku varat piešķirt citiem uzdevumiem, izmantojot resursu atlasītāju.

   Kad esat beidzis vispārējā resursa piešķiršanu uzdevumiem, varat ģenerēt resursu vajadzību šim vispārējam resursam.

7. Cilnē **Darba grupa** atlasiet vispārējo resursu un pēc tam atlasiet **Ģenerēt vajadzību**. Kad vajadzība ir ģenerēta, vispārējam darba grupas dalībniekam būs nepieciešamās stundas un saite šai resursu vajadzībai.

  Kad ir rezervēts kāds nosaukts resurss, vispārējais resurss no darba grupas tiek noņemts un aizstāts ar nosaukto resursu. Cilnē **Grafiks** vispārējo resursu piešķires tiek noņemtas un aizstātas ar nosaukto resursu.

  > [!NOTE]
  > Tas notiek tikai tad, ja vispārējā resursa vajadzībai nosauktais resurss ir rezervēts pilnībā. Ja nosaukts resurss vispārējā resursa vajadzību aizstāj tikai daļēji vai ja vispārējā resursa vajadzību aizstāj vairāki nosauktie resursi, vispārējais resurss paliek piešķirts uzdevumam.

Project Operations nepiešķir abus resursus šim uzdevumam, jo šāda uzvedība radītu mazāk prognozējamu grafiku. Šajā vienkāršajā piemērā stundas var viegli sadalīt vienādi starp diviem resursiem. Taču sarežģītākos scenārijos, kas ietver vairākus uzdevumus un vairākus resursus, programmai PSA būtu jāizdara pieņēmumi par veidu, kā piešķirt rezervācijas, kas ir saņemtas par vairākiem resursiem vairākos uzdevumos.

Tādēļ šajos scenārijos Projektu vadītājs ir atbildīgs par vairāku rezervāciju parsēšanu un to piešķiršanu pēc nepieciešamības. Lai sadalītu rezervācijas, Projektu vadītājs no vispārējiem resursiem piešķir uzdevumus nosauktajiem resursiem un pēc tam izmanto skatu **Saskaņošana**, lai pārliecinātos, ka sadalīšana ar šādām rezervācijām darbojas.

### <a name="edit-a-resource-requirement"></a>Resursu vajadzības rediģēšana

Kad resursu vajadzība ir izveidota, Projektu vadītājs vai Resursu pārvaldnieks varētu vēlēties rediģēt detalizēto informāciju, lai precizētu meklēšanas kritērijus, kad tiek izmantots plānošanas panelis. Lai rediģētu resursu vajadzību, izpildiet tālāk aprakstītās darbības.

1. Veidlapā **Projekti**, cilnē **Darba grupa** atlasiet saiti uz jebkuru prasību vispārējam resursam.
2. Parādās veidlapa **Resursu prasības** – tajā ievadiet nepieciešamo informāciju laukos

   Veidlapā **Resursu vajadzība** Projektu vadītājs vai Resursu pārvaldnieks var arī definēt prasmes, lomas, resursu preferences un vēlamo organizācijas vienību.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resursu rezervāciju atjaunināšana pēc to rezervēšanas projektam

Kad vispārēju vai nosauktu resursu esat pievienojis projekta darba grupai, varat mainīt šī resursa rezervācijas.

1. Veidlapā **Projekti**, cilnē **Darba grupa** atlasiet darba grupas dalībnieku un pēc tam atlasiet **Uzturēt rezervācijas**.
 
   Tiek parādīts plānošanas panelis, un tajā ir redzamas projekta darba grupas dalībnieku rezervācijas. Izvērsiet darba grupas dalībnieka ierakstu, lai skatītu informāciju par stundām, kuras ir rezervētas šim projektam un citiem projektiem, kas patērē šī darba grupas dalībnieka noslodzi.

2. Atlasiet un velciet rezervāciju, lai to paplašinātu vai saīsinātu. Tiek parādīts dialoglodziņš **Izveidot resursu rezervāciju**, un tajā varat pielāgot šo rezervāciju.
3. Ar peles labo pogu noklikšķiniet uz rezervācijas. Pēc tam varat izmantot īsinājumizvēlni, lai veiktu tālāk norādītās darbības.

    - Rezervācijas statusa mainīšana
    - Rezervācijas rediģēšana
    - Resursa aizstāšana projekta grupā

### <a name="change-the-booking-status"></a>Rezervācijas statusa mainīšana

Varat mainīt jebkuru noklusējuma vai pielāgoto rezervācijas statusu.

Programmā Project Operations ir tālāk norādītie statusi.

- **Atcelts**: atceļ resursa rezervāciju un atbrīvo resursa noslodzi.
- **Veikt stingro rezervāciju**: patērē resursu noslodzi. Ja vienumu **Uzturēt rezervācijas** atverat no režģa **Visi darba grupas dalībnieki** veidlapā **Projekti**, rezervācijai parasti ir šis statuss.
- **Veikt vieglo rezervāciju**: resursu pievieno darba grupai, bet nepatērē resursa noslodzi. Šis statuss norāda, ka resurss ir rezervēts iespējamam darbam, bet tam joprojām ir noslodze, ja gadījumā tas ir nepieciešams citiem uzdevumiem. Vispārīgās resursu pieejamības ziņā vieglajai rezervēšanai ir citāds statuss nekā stingrajai rezervēšanai.
- **Piedāvāts**: apzīmē Resursu pārvaldnieka vai Projektu vadītāja piedāvājumu kādam resursam. Piedāvājumi nepatērē resursa noslodzi, un resurss netiek pievienots projekta grupai. Lai resursam veiktu stingro rezervēšanu darba grupai, Projektu vadītājam ir jāpieņem piedāvājums.

### <a name="submit-resource-requests"></a>Resursu pieprasījumu iesniegšana

Resursu pieprasījumi tiek izmantoti, lai ievērotu pieprasījumu vai resursu vajadzību, kas ir jāizpilda kādam Resursu pārvaldniekam. Vispārējam resursam, kas jau ir darba grupā, resursu pieprasījumu varat iesniegt tieši. Resursu pieprasījumu var izpildīt divos tālāk aprakstītajos veidos.

- Resursu pārvaldnieks pieprasījumu izpilda tieši. Šādā gadījumā vispārējais resurss tiek aizstāts ar stingro rezervēšanu, kurai ir nosaukts resurss.
- Resursu pārvaldnieks piedāvā kādu resursu Projektu vadītājam, un Projektu vadītājs apstiprina vai noraida šo piedāvāto resursu.

#### <a name="direct-fulfillment-of-resource-requests"></a>Resursu pieprasījumu tiešā izpildīšana

Kad resursu vajadzība ir ģenerēta, Projektu vadītājs var iesniegt resursu pieprasījumu vispārējam resursam, atlasot šo resursu un pēc tam atlasot vienumu **Iesniegt pieprasījumu**. Resursu pārvaldniekam, kurš izpilda pieprasījumu, var sniegt komentārus par šo resursu. Kad pieprasījums ir iesniegts, lauks **Statuss** attiecīgajam darba grupas dalībniekam mainās uz **Iesniegts**. Kad Resursu pārvaldnieks izpilda pieprasījumu, režģī **Visi darba grupas dalībnieki** vispārējais darba grupas dalībnieks tiek aizstāts ar nosaukto resursu.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Resursu piedāvājumu lietošana resursu pieprasījumiem

Tā vietā, lai resursu tieši rezervētu resursu pieprasījumā, Resursu pārvaldnieks resursu var piedāvāt Projektu vadītājam. Resursu pārvaldnieks var izmantot šo opciju, ja precīza atbilstība vajadzībām nav pieejama. Kad Resursu pārvaldnieks piedāvā kādu resursu, Projektu vadītājs redz, ka lauks **Statuss** attiecīgajam vispārējam darba grupas dalībniekam tiek mainīts uz **Jāpārskata**.

Varat skatīt piedāvāto resursu kopā ar piedāvājuma rezervācijas iedarbības vizualizāciju. 

1. Veiciet dubultklikšķi uz darba grupas dalībnieka vienuma, kam ir statuss **Jāpārskata**. 
2. Atlasiet cilni **Piedāvātie resursi**.
3. Atlasiet **Pieņemt visus piedāvājumus**, lai pieņemtu visus piedāvātos resursus, vai atlasiet **Noraidīt visus piedāvājumus**, lai tos noraidītu. Ja pieņemat piedāvātos resursus, tie ir stingri rezervēti projektā kā darba grupas dalībnieki un aizstāj vispārējos resursus.

> [!NOTE]
> Ir jāpieņem vai jānoraida visi piedāvātie resursi. Tos nevar pieņemt vai noraidīt daļēji.

### <a name="substitute-a-resource-on-the-project-team"></a>Resursa aizstāšana projekta grupā

Reizēm Projektu vadītājam projektā ir jāaizstāj kāds no rezervētajiem darba grupas dalībniekiem.

1. Veidlapā **Projekti**, cilnē **Darba grupa** atlasiet resursu, kam vajadzīgs aizstājējs, un pēc tam atlasiet **Uzturēt rezervācijas**.
2. Izvērsiet resursu, lai apskatītu projektus, kuriem tas ir piešķirts.
3. Ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet vienumu **Aizstāt resursu**.
4. Ja zināt, ar kuru resursu aizstāt pašreizējo resursu, atlasiet vai ierakstiet nosaukumu un pēc tam atlasiet vienumu **Pārpiešķirt**.

Vai arī: ja jums jāmeklē resurss, izpildiet tālāk aprakstītās darbības.

1. Atlasiet **Atrast aizstājēju**.

   Plānošanas palīgs parāda sarakstu ar pieejamajiem aizstājējiem. Plānošanas palīgā pieejamos resursus varat papildus filtrēt, lai atrastu piemērotu aizstājēju.

2. Lai aizstātu resursu, atlasiet nepieciešamo resursu un pēc tam atlasiet **Aizstāt**.   

   Rezervācijas un piešķires tiek aizstātas ar jauno resursu.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Darba grupas dalībnieku rezervāciju un piešķiru saskaņošana

Darba grupas dalībniekiem rezervācijas un piešķires ir brīvi savienotas. Citiem vārdiem sakot — resursiem var būt piešķires, bet var nebūt rezervāciju, vai arī tiem var būt rezervācijas, bet var nebūt piešķiru. Ideālā gadījumā rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze uzdevumu piešķiru izpildīšanai. Taču rezervācijas var būt balstītas uz pieejamību, un projekta gaitā uzdevumu laiki var mainīties. Tādēļ rezervāciju un piešķiru brīvais savienojums nodrošina elastību.

Programmā Project Operations ir cilne **Saskaņošana**, kas ļauj Projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un viņu piešķires projektu darba grupās.

Cilnē **Saskaņošana** rezervācijas un piešķires katram darba grupas dalībniekam ir parādītas līdz atsevišķa uzdevuma piešķires līmenim. Tur tiek rādītas stundas šūnās, kas apzīmē laika periodus no mēnešiem līdz dienām.

Šajā cilnē ir redzama arī projekta vispārējā neto kopsumma kopā ar kolonnu kopsummu.

Katram resursam šī cilne aprēķina atšķirību starp darba grupas dalībnieka rezervācijām un darba grupas dalībnieka uzdevumu piešķiru apkopojumu. Ideālā gadījumā šai atšķirībai vajadzētu būt 0 (nulle). Citiem vārdiem sakot — starp rezervācijām un piešķirēm nevajadzētu būt nekādai starpībai. Atšķirības tiek iekrāsotas un ieēnotas, lai pievērstu uzmanību diviem tālāk aprakstītajiem apstākļiem.

- **Rezervācijas deficīts**: rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, Projektu vadītājs var vēlēties izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību.
- **Rezervāciju pārsniegšana**: rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem. Šis apstāklis var būt pieņemams gadījumos, kad resurss projektam tika rezervēts vēl pirms tam, kad radās uzdevuma piešķire. Taču citos gadījumos resursu nav plānots piešķirt uzdevumiem. Šādos gadījumos Projektu vadītājam ir jāapsver resursa rezervācijas atcelšana, lai šo noslodzi varētu izmantot citam projektam.

Reizēm, kad laiku skatāt augstākā līmenī nekā dienas līmenis, piemēram, mēneša līmenī, varat pamanīt, ka neto starpība resursam ir nulle. Citiem vārdiem sakot, rezervējumi = norīkojumi. Taču, ja laiku skatāt nedēļas līmenī, varat redzēt, ka pirmajā nedēļā piešķires ir nulle stundu un rezervācijas ir 40 stundas, bet otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir nulle stundu. Kopumā rezervācijas un piešķires ir saskaņotas, bet katrai nedēļai tās atšķiras.

Kad laiku skatāties augstākos līmeņos, šūnām cilnē **Saskaņošana** ir indikators, lai informētu jūs, ka pastāv atšķirības zemākos līmeņos. Veiciet dubultklikšķi uz šūnas, lai tuvinātu un apskatītu atšķirību. Pēc tam varat noklikšķināt ar peles labo pogu, lai tālinātu. Atlasot kādu resursu un pēc tam režģa rīkjoslā atlasot **Nākamā atšķirība**, varat pāriet uz nākamo atšķirību starp šī resursa rezervācijām un piešķirēm. Lai atgrieztos, atlasiet **Iepriekšējā atšķirība**. Varat arī izslēgt atšķirību indikatoru un navigācijas uzvedību sadaļā **Iestatījumi**.

Ja jums ir uzdevumu piešķires kādam resursam, bet nav nevienas rezervācijas, veidlapā **Projekti**, cilnē **Saskaņošana** atlasiet rezervāciju deficītu un pēc tam atlasiet vienumu **Paplašināt rezervāciju**. Tiek parādīts dialoglodziņš **Paplašināt rezervāciju**, un tajā ir redzama rezervācija, kura ir nepieciešama, lai novērstu šo resursu deficītu. Dialoglodziņā redzamas arī resursu esošās rezervācijas visos projektos vai citos plānojamos elementos. Ja atlasāt **Labi**, lai izveidotu rezervāciju attiecīgajam resursam neatkarīgi no šī resursa pieejamības, varat izraisīt virsrezervāciju.

Pēc tam Projektu vadītājs vai Resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu visas situācijas, kur resursa rezervācija pārsniedz tā noslodzi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]