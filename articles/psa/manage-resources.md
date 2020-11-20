---
title: Resursu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par to, kā varat pārvaldīt resursus.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132342"
---
# <a name="manage-resources"></a>Resursu pārvaldīšana

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation ietver resursu pārvaldnieka informācijas paneli, kas nodrošina vizuālu pārskatu par resursu pieprasījumu un lietojumu visā organizācijā. Diagrammas šajā informācijas panelī var izmantot, lai vizualizētu tālāk norādīto informāciju.

- **Resursu pieprasījums** — diagrammā **Aktīvais resursu pieprasījums** ir parādīti iesniegtie resursi. Šie resursi ir apkopoti vai nu pēc lomas, vai pēc projekta.
- **Neiesniegts resursu pieprasījums** — diagrammā **Nepiešķirts resursu pieprasījums** ir parādītas visas resursu vajadzības, kas nav iesniegtas. Tas palīdz resursu pārvaldniekiem apskatīt pieprasījumu, kas nav apstiprināts un ko varētu iesniegt, izmantojot resursa pieprasījumu.
- **Apmaksājamā izmantošana iepriekšējai nedēļai** —– diagrammā **Izmantošana pēc lomas** ir parādīts organizācijas faktiskās apmaksājamajās izmantošanas procentuālais daudzums pēc lomas salīdzinājumā ar tās mērķa izmantošanu pēc lomas.

    > [!NOTE]
    > Lai diagrammu **Izmantošana pēc lomas** padarītu pieejamu, izveidojiet darbu, kurā tiek izpildīta darbplūsma UpdateRoleUtilization. Šis periodiskais darbs tiek palaists ik pēc septiņām dienām, lai aprēķinātu apmaksājamo izmantošanu iepriekšējām septiņām dienām. Rezultāti tiek apkopoti pēc lomas.

## <a name="manage-project-team-members"></a>Projekta darba grupas dalībnieku pārvaldīšana

Projektu vadītāji var izmantot šo resursu pārvaldnieka informācijas paneli, lai projektos pārvaldītu resursus. Viņi var, piemēram, pievienot darba grupas dalībnieku tieši projektam un rezervēt darba grupas dalībnieku, lai izpildītu resursu vajadzības, kuras tvēra kāds vispārējais resurss.

### <a name="add-a-team-member-directly-to-a-project"></a>Darba grupas dalībnieka pievienošana tieši projektam

Lai kādu darba grupas dalībnieku pievienotu tieši projektam, lapā **Projekti**, cilnē **Darba grupa** atlasiet **Jauns**. Tiek parādīts dialoglodziņš **Ātrā izveide:Projekta darba grupas dalībnieks**. Šajā dialoglodziņā varat veikt tālāk norādītos uzdevumus.

- **Rezervēt nosauktu resursu** — laukā **Rezervējamais resurss** atlasiet resursa nosaukumu. Pēc tam atlasiet lomu, iestatiet periodu un atlasiet piešķiršanas metodi. Jūsu atlasītais nosauktais resurss tiek pievienots projektam, izmantojot atlasīto sadalījuma metodi un resursu kalendāru.
- **Pievienot vispārēju resursu** — lauku **Rezervējamais resurss** atstājiet tukšu un pēc tam atlasiet lomu, iestatiet periodu un atlasiet vēlamo piešķiršanas metodi. Darba grupai tiek pievienots vispārējs resurss kā vietturis, lai uzturētu pieprasījuma modeli, kas tiek izmantots nosaukto resursu rezervēšanai darba grupā. Šī vajadzība tiek izpildīta atbilstoši projekta kalendāram.
- **Pievienot darba grupai nosauktu resursu, nepatērējot resursa noslodzi** — laukā **Rezervējamais resurss** atlasiet kādu resursu. Pēc tam atlasiet periodu un kā sadalījuma metodi atlasiet **Nav**. Resurss tiek pievienots darba grupai, bet ar rezervēšanu šī resursa noslodze netiek patērēta.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Darba grupas dalībnieka rezervēšana, lai izpildītu resursu vajadzības attiecībā uz vispārēju resursu

Programmā PSA vispārēju resursu varat rezervēt kādai projekta darba grupai un varat norādīt lomu, nepieciešamo noslodzi un veidu, kā šī noslodze ir jāizplata. Resursa vajadzībā varat norādīt atribūtus, kas ir saistīti ar šo vispārējo resursu. Šie atribūti tostarp ir nepieciešamās prasmes, vēlamā organizācijas struktūrvienība un vēlamie resursi.

Lai vispārējā resursā kādam izstrādātājam norādītu nepieciešamās prasmes, izpildiet tālāk aprakstīto procedūru.

1. Lapā **Projekti**, cilnē **Darba grupa** atlasiet vienumu **Jauns**, lai rezervētu kādu vispārējo resursu.

    ![Darba grupai rezervēts vispārējais resurss](media/Resource-Management-image9.png)

2. Skatā **Visi darba grupas dalībnieki**, kolonnā **Resursu vajadzība** atlasiet saiti, lai vispārīgajam resursam pievienotu nepieciešamās prasmes.

    ![Vajadzības saite](media/Resource-Management-image10.png)

3. Tiek parādīta lapa **Resursu vajadzība**, un tās režģī **Prasmes** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot jaunu vajadzības īpašību**, lai savam izstrādātājam pievienotu nepieciešamās prasmes.

    ![Komanda Pievienot jaunu vajadzības īpašību](media/Resource-Management-image11.png)

4. Tiek parādīts dialoglodziņš **Ātrā izveide: Vajadzības īpašība**, un tā laukā **Īpašība** atlasiet nepieciešamo prasmi. Pēc tam laukā **Novērtējuma vērtība** atlasiet kvalifikācijas līmeni šai prasmei. Visbeidzot laukā **Resursu vajadzība** iestatiet šo vajadzību, lai tā kā avotu izmantotu resursus no organizācijas struktūrvienībām vai pat nosauktiem resursiem. Kad esat pabeidzis, noklikšķiniet uz **saglabāt**.

    ![Dialoglodziņš Ātrā izveide: Vajadzības īpašība](media/Resource-Management-image12.png)

5. Lapā **Resursu vajadzība** atlasiet **Rezervēt**, lai izpildītu resursu vajadzību.

    ![Poga Rezervēt lapā Resursu vajadzība](media/Resource-Management-image13.png)

    Varat arī atlasīt vispārējo resursu režģī **Visi darba grupas dalībnieki** un pēc tam atlasīt vienumu **Rezervēt**.

    ![Poga Rezervēt virs režģa Visi darba grupas dalībnieki](media/Resource-Management-image14.png)

    > [!NOTE]
    > Šajā piemērā ir 40 pieprasītās stundas, bet nav faktiski rezervētu stundu, jo vispārējiem resursiem nav rezervāciju. Turklāt nav piešķirtu stundu, jo vispārējais resurss tika pievienots tieši darba grupai. Tas netika pievienots, izmantojot uzdevumu piešķiršanu.

    Lapā **Plānošanas palīgs** pieejamos resursus varat filtrēt pēc vajadzībām, kas ir norādītas resursu vajadzībā. Resursi tiek kārtoti atbilstoši plānošanas panelī norādītajiem kārtošanas parametriem.

    ![Lapa Plānošanas palīgs](media/Resource-Management-image15.png)

    Tālāk ir norādīti daži no bieži izmantotajiem filtriem.

    - **Īpašības kopā ar novērtējumu** — papildus kvalifikācijas novērtējumiem filtrēt arī pēc prasmēm, sertifikācijām un citām resursu īpašībām.
    - **Lomas** — filtrēt pēc noklusējuma lomām, kas ir piešķirtas rezervējamiem resursiem.
    - **Organizācijas struktūrvienības** — filtrēt rezervējamos resursus pēc organizācijas struktūrvienībām, kurām tie ir piešķirti.

6. Ja neesat apmierināts ar sākotnējās vajadzības meklēšanas rezultātiem, varat mainīt šos filtrēšanas kritērijus. Izvērsiet rūti **Filtra skats** kreisajā pusē un pēc tam atlasiet **Meklēt**, lai atrastu papildu resursus.

    ![Rūts Filtra skats](media/Resource-Management-image16.png)

7. Lai mainītu rezultātu kārtošanas veidu, atlasiet vienumu **Kārtot**.

    ![Komanda Kārtot](media/Resource-Management-image17.png)

8. Atlasiet resursus atbilstoši pieprasījumam, kas ir norādīts vajadzībā, kā redzams režģa augšpusē. Šūnu atlasi režģī varat notīrīt un atstāt šo resursa noslodzi atvērtu. Kā rezervētu vienlaikus var atlasīt tikai vienu resursu.

9. Atlasiet **Rezervēt**, lai rezervētu atlasīto resursu, un atstājiet plānošanas paneli atvērtu, lai varētu atlasīt papildu resursus. Var arī atlasīt **Rezervēt un iziet**, lai rezervētu atlasīto resursu un aizvērtu plānošanas paneli.

    ![Rezervējamais resurss](media/Resource-Management-image19.png)

    Jūs saņemat paziņojumu par rezervētajām stundām. Pieprasījuma indikatori rāda, cik ļoti rezervācijas vajadzība ir izpildīta un cik vēl ir atlicis. Varat arī redzēt, cik daudz no atlasītā resursa noslodzes ir patērēts. Atlasiet **Izvērst**, lai skatītu plašāku informāciju par resursu rezervēšanu.

9. Atgriezieties skatā **Visi darba grupas dalībnieki**. Pievērsiet uzmanību, ka režģī šis vispārējais resurss ir aizstāts ar nosaukto resursu, un 40 stundas šim resursam ir norādītas kā rezervētas.

    ![Atjauninātais skats Visi darba grupas dalībnieki](media/Resource-Management-image20.png)

    > [!NOTE]
    > Netiek rādīta neviena piešķirtā stunda, jo tās tika rezervētas tieši darba grupai. Tās netika rezervētas, izmantojot uzdevumu piešķiršanu.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Vispārēju resursu piešķiršana uzdevumiem un resursu vajadzību ģenerēšana

Programmā PSA varat izveidot uzdevumus un pēc tam šiem uzdevumiem piešķirt vispārējos resursus. Šādi resursu pieprasījumu var parādīt kā vietturus, kamēr veidojat grafika un finanšu skaitļu tāmi. Pēc tam varat ģenerēt resursu vajadzības attiecībā uz vispārīgajiem resursiem un izpildīt tās.

1. Lapā **Projekti**, cilnē **Grafiks** atlasiet vienumu **Pievienot**, lai izveidotu uzdevumu.

    ![Izveidots jauns uzdevums](media/Resource-Management-image21.png)

2. Laukā **Resursi** atlasiet simbolu **Resursu atlasītājs**. Tiek parādīts resursu atlasītājs, un tajā tiek rādīti šim projektam esošie darba grupas dalībnieki.

    ![Resursu atlasītājs](media/Resource-Management-image22.png)

3. Ievadiet jaunā vispārējā resursa nosaukumu un pēc tam atlasiet vienumu **Izveidot**.

    ![Ievadīts jaunā vispārējā resursa nosaukums](media/Resource-Management-image23.png)

4. Tiek parādīts dialoglodziņš **Ātrā izveide: Projekta darba grupas dalībnieks**, un tā laukā **Loma** atlasiet lomu šim vispārējam resursam. Laukā **Resursu vienība** atlasiet organizācijas struktūrvienību šim vispārējam resursam. Pēc tam atlasiet **Saglabāt**.

    ![Dialoglodziņš Ātrā izveide: Projekta darba grupas dalībnieks](media/Resource-Management-image24.png)

    Tagad vispārējais darba grupas dalībnieks ir piešķirts šim uzdevumam.

    ![Vispārējais darba grupas dalībnieks ir piešķirts uzdevumam](media/Resource-Management-image25.png)

    Cilnē **Darba grupa** ir redzams jaunais vispārējais darba grupas dalībnieks. Ievērojiet, ka tam ir tikai piešķirtas stundas. Šīs stundas ir summa no visiem tiem uzdevumiem, kas ir piešķirti vispārējam darba grupas dalībniekam. Vispārējam darba grupas dalībniekam vēl nav nepieciešamo stundu vai resursu vajadzības.

    ![Vispārējais darba grupas dalībnieks cilnē Darba grupa](media/Resource-Management-image26.png)

5. Tagad šo vispārējo darba grupas dalībnieku varat piešķirt citiem uzdevumiem, izmantojot resursu atlasītāju.

    ![Vispārējais darba grupas dalībnieks resursu atlasītājā](media/Resource-Management-image27.png)

    Kad esat beidzis vispārējā resursa piešķiršanu uzdevumiem, varat ģenerēt resursu vajadzību šim vispārējam resursam.

5. Cilnē **Darba grupa** atlasiet vispārējo resursu un pēc tam atlasiet **Ģenerēt vajadzību**.

    ![Komanda Ģenerēt vajadzību](media/Resource-Management-image28.png)

    Kad vajadzība ir ģenerēta, vispārējam darba grupas dalībniekam būs nepieciešamās stundas un saite šai resursu vajadzībai.

    ![Resursu vajadzības saite](media/Resource-Management-image29.png)

    Kad ir rezervēts kāds nosaukts resurss, vispārējais resurss no darba grupas tiek noņemts un aizstāts ar nosaukto resursu.

    ![Vispārējais resurss ir aizstāts ar nosaukto resursu](media/Resource-Management-image30.png)

    Cilnē **Grafiks** vispārējo resursu piešķires tiek noņemtas un aizstātas ar nosaukto resursu.

    ![Cilnē Grafiks vispārējā resursa piešķires ir aizstātas ar nosaukto resursu](media/Resource-Management-image31.png)

    > [!NOTE]
    > Tas notiek tikai tad, ja vispārējā resursa vajadzībai nosauktais resurss ir rezervēts pilnībā. Ja nosaukts resurss vispārējā resursa vajadzību aizstāj tikai daļēji vai ja vispārējā resursa vajadzību aizstāj vairāki nosauktie resursi, vispārējais resurss paliek piešķirts uzdevumam.

    Nākamajā ilustrācijā ir parādīts, ka 80 stundu uzdevums ir plānots piecu dienu ilgumā (16 stundas dienā piecu dienu ilgumā) un piešķirts vispārējam resursam ar nosaukumu **Funkcionāls**.

    ![Astoņdesmit stundu, piecu dienu uzdevums, kas ir piešķirts vispārējam resursam Funkcionāls](media/Resource-Management-image32.png)

    Kad ģenerējat šo vajadzību, tā ir 80 stundām piecu dienu ilgumā.

    ![Vajadzība ir ģenerēta 80 stundām piecu dienu ilgumā](media/Resource-Management-image33.png)

    Tā kā pieejamie resursi darbojas tikai astoņas stundas dienā, šīs vajadzības izpildīšanai ir nepieciešami divi resursi.

    ![Otrais resurss](media/Resource-Management-image35.png)

    Tagad cilnē **Darba grupa** varat redzēt, ka vispārējam resursam nav nepieciešamo stundu, bet piešķirtās stundas joprojām tiek rādītas kopā ar abiem nosauktajiem resursiem, kas veido šo izpildi.

    ![Divi nosauktie resursi cilnē Darba grupa](media/Resource-Management-image36.png)

    Cilnē **Grafiks** vispārējais resurss paliek piešķirts šim uzdevumam.

    ![Vispārējie resursi cilnē Grafiks](media/Resource-Management-image37.png)

PSA nepiešķir abus resursus šim uzdevumam, jo šāda uzvedība radītu mazāk prognozējamu grafiku. Šajā vienkāršajā piemērā stundas var viegli sadalīt vienādi starp diviem resursiem. Taču sarežģītākos scenārijos, kas ietver vairākus uzdevumus un vairākus resursus, programmai PSA būtu jāizdara pieņēmumi par veidu, kā piešķirt rezervācijas, kas ir saņemtas par vairākiem resursiem vairākos uzdevumos.

Tādēļ šajos scenārijos projektu vadītājs ir atbildīgs par vairāku rezervāciju parsēšanu un to piešķiršanu pēc nepieciešamības. Lai sadalītu rezervācijas, projektu vadītājs no vispārējiem resursiem piešķir uzdevumus nosauktajiem resursiem un pēc tam izmanto skatu **Saskaņošana**, lai pārliecinātos, ka sadalīšana ar šādām rezervācijām darbojas.

### <a name="edit-a-resource-requirement"></a>Resursu vajadzības rediģēšana

Kad resursu vajadzība ir izveidota, projektu vadītājs vai resursu pārvaldnieks varētu vēlēties rediģēt detalizēto informāciju, lai precizētu meklēšanas kritērijus, kad tiek izmantots plānošanas panelis. Lai rediģētu resursu vajadzību, izpildiet tālāk aprakstītās darbības.

1. Lapā **Projekti**, cilnē **Darba grupa** atlasiet saiti uz jebkuru no vispārējo resursu vajadzībām.
2. Tiek parādīta lapa **Resursu vajadzība**, un tajā varat atjaunināt vairākus atribūtus. Lūk, daži piemēri:

    - Nosaukums
    - Sākuma datums
    - Beigu datums
    - Ilgums
    - Resursa tips

Lapā **Resursu vajadzība** projektu vadītājs vai resursu pārvaldnieks var arī definēt tālāk norādīto informāciju.

- Prasmes
- Lomas
- Resursu preferences
- Vēlamā organizācijas struktūrvienība

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resursu rezervāciju atjaunināšana pēc to rezervēšanas projektam

Kad vispārēju vai nosauktu resursu esat pievienojis projekta darba grupai, varat mainīt šī resursa rezervācijas.

1. Lapā **Projekti**, cilnē **Darba grupa** atlasiet kādu darba grupas dalībnieku un pēc tam atlasiet vienumu **Uzturēt rezervācijas**.

    ![Plānošanas panelis ir atvērts atlasītajam darba grupas dalībniekam](media/Resource-Management-image40.png)

    Tiek parādīts plānošanas panelis, un tajā ir redzamas projekta darba grupas dalībnieku rezervācijas. Izvērsiet darba grupas dalībnieka ierakstu, lai skatītu informāciju par stundām, kuras ir rezervētas šim projektam un citiem projektiem, kas patērē šī darba grupas dalībnieka noslodzi.

2. Atlasiet un velciet rezervāciju, lai to paplašinātu vai saīsinātu. Tiek parādīts dialoglodziņš **Izveidot resursu rezervāciju**, un tajā varat pielāgot šo rezervāciju.

    ![Dialoglodziņš Izveidot resursu rezervāciju](media/Resource-Management-image41.png)

3. Ar peles labo pogu noklikšķiniet uz rezervācijas. Pēc tam varat izmantot īsinājumizvēlni, lai veiktu tālāk norādītās darbības.

    - Mainīt rezervācijas statusu.
    - Rediģēt rezervāciju.
    - Aizstāt resursu projekta grupā.

### <a name="change-the-booking-status"></a>Rezervācijas statusa mainīšana

Varat mainīt jebkuru noklusējuma vai pielāgoto rezervācijas statusu.

![Komanda Mainīt statusu](media/Resource-Management-image42.png)

Programmā PSA ir tālāk norādītie statusi.

- **Atcelts** — šis statuss atceļ resursa rezervāciju un atbrīvo resursa noslodzi.
- **Stingrā rezervēšana** — šis statuss patērē resursa noslodzi. Ja vienumu **Uzturēt rezervācijas** atverat no režģa **Visi darba grupas dalībnieki** lapā **Projekti**, rezervācijai parasti ir šis statuss.
- **Vieglā rezervēšana** — šis statuss resursu pievieno darba grupai, bet nepatērē resursa noslodzi. Tas norāda, ka resurss ir rezervēts iespējamam darbam, bet tam joprojām ir noslodze, ja gadījumā tas ir nepieciešams citiem uzdevumiem. Vispārīgās resursu pieejamības ziņā vieglajai rezervēšanai ir citāds statuss nekā stingrajai rezervēšanai.
- **Piedāvāts** — šis statuss apzīmē resursu pārvaldnieka vai projektu vadītāja piedāvājumu kādam resursam. Piedāvājumi nepatērē resursa noslodzi, un resurss netiek pievienots projekta grupai. Lai resursam veiktu stingro rezervēšanu darba grupai, projektu vadītājam ir jāpieņem piedāvājums.

### <a name="submit-resource-requests"></a>Resursu pieprasījumu iesniegšana

Resursu pieprasījumi tiek izmantoti, lai ievērotu pieprasījumu (resursu vajadzību), kas ir jāizpilda kādam resursu pārvaldniekam. Vispārējam resursam, kas jau ir darba grupā, resursu pieprasījumu varat iesniegt tieši. Resursu pieprasījumu var izpildīt divos tālāk aprakstītajos veidos.

- Resursu pārvaldnieks pieprasījumu izpilda tieši. Šādā gadījumā vispārējais resurss tiek aizstāts ar stingro rezervēšanu, kurai ir nosaukts resurss.
- Resursu pārvaldnieks piedāvā kādu resursu projektu vadītājam, un projektu vadītājs apstiprina vai noraida šo piedāvāto resursu.

#### <a name="direct-fulfillment-of-resource-requests"></a>Resursu pieprasījumu tiešā izpildīšana

Kad resursu vajadzība ir ģenerēta, projektu vadītājs var iesniegt resursu pieprasījumu vispārējam resursam, atlasot šo resursu un pēc tam atlasot vienumu **Iesniegt pieprasījumu**.

![Poga Iesniegt pieprasījumu](media/Resource-Management-image45.png)

Resursu pārvaldniekam, kurš izpilda pieprasījumu, var sniegt komentārus par šo resursu. Kad pieprasījums ir iesniegts, lauks **Statuss** attiecīgajam darba grupas dalībniekam mainās uz **Iesniegts**.

![Neobligātu komentāru ievadīšana](media/Resource-Management-image46.png)

Kad resursu pārvaldnieks izpilda pieprasījumu, režģī **Visi darba grupas dalībnieki** vispārējais darba grupas dalībnieks tiek aizstāts ar nosaukto resursu.

![Vispārējais darba grupas dalībnieks tiek aizstāts ar nosaukto resursu režģī Visi darba grupas dalībnieki](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Resursu piedāvājumu lietošana resursu pieprasījumiem

Tā vietā, lai resursu tieši rezervētu resursu pieprasījumā, resursu pārvaldnieks resursu var piedāvāt projektu vadītājam. Resursu pārvaldnieks var izmantot šo opciju, ja precīza atbilstība vajadzībām nav pieejama. Kad resursu pārvaldnieks piedāvā kādu resursu, projektu vadītājs redz, ka lauks **Statuss** attiecīgajam vispārējam darba grupas dalībniekam tiek mainīts uz **Jāpārskata**.

![Vispārējā darba grupas dalībnieka statuss ir mainīts uz Jāpārskata](media/Resource-Management-image48.png)

Lai piedāvāto resursu skatītu kopā ar piedāvājuma rezervācijas efekta vizualizāciju, veiciet dubultklikšķi uz darba grupas dalībnieka, kura statuss ir **Jāpārskata**. Pēc tam atlasiet cilni **Piedāvātie resursi**.

![Cilne Piedāvātie resursi](media/Resource-Management-image49.png)

Atlasiet **Pieņemt visus piedāvājumus**, lai pieņemtu visus piedāvātos resursus, vai atlasiet **Noraidīt visus piedāvājumus**, lai tos noraidītu. Ja pieņemat piedāvātos resursus, tie ir stingri rezervēti projektā kā darba grupas dalībnieki un aizstāj vispārējos resursus.

> [!NOTE]
> Ir jāpieņem vai jānoraida visi piedāvātie resursi. Tos nevar pieņemt vai noraidīt daļēji.

### <a name="substitute-a-resource-on-the-project-team"></a>Resursa aizstāšana projekta grupā

Reizēm projektu vadītājam projektā ir jāaizstāj kāds no rezervētajiem darba grupas dalībniekiem.

1. Lapā **Projekti**, cilnē **Darba grupa** atlasiet kādu resursu, kam ir nepieciešams aizstājējs, un pēc tam atlasiet vienumu **Uzturēt rezervācijas**.
2. Izvērsiet resursu, lai apskatītu projektus, kuriem tas ir piešķirts.

    ![Resurss ir izvērsts, lai parādītu piešķirtos projektus](media/Resource-Management-image50.png)

3. Ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet vienumu **Aizstāt resursu**.
4. Ja zināt, ar kuru resursu aizstāt pašreizējo resursu, atlasiet vai ierakstiet nosaukumu un pēc tam atlasiet vienumu **Pārpiešķirt**.

    ![Aizstājošā resursa norādīšana](media/Resource-Management-image51.png)

    Vai arī izpildiet tālāk norādītās darbības, lai meklētu kādu resursu.

    1. Atlasiet **Atrast aizstājēju**.

        ![Aizstājošā resursa meklēšana](media/Resource-Management-image52.png)

        Plānošanas palīgs parāda sarakstu ar pieejamajiem aizstājējiem. Plānošanas palīgā pieejamos resursus varat papildus filtrēt, lai atrastu piemērotu aizstājēju.

        ![Pieejamo aizstājēju saraksts](media/Resource-Management-image53.png)

    2. Lai aizstātu resursu, atlasiet nepieciešamo resursu un pēc tam atlasiet **Aizstāt**.

        ![Aizstājošais resurss ir atlasīts](media/Resource-Management-image54.png)

    Rezervācijas un piešķires tiek aizstātas ar jauno resursu.

    ![Rezervācijas un piešķires ir aizstātas ar jauno resursu](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Darba grupas dalībnieku rezervāciju un piešķiru saskaņošana

Darba grupas dalībniekiem rezervācijas un piešķires ir brīvi savienotas. Citiem vārdiem sakot — resursiem var būt piešķires, bet var nebūt rezervāciju, vai arī tiem var būt rezervācijas, bet var nebūt piešķiru. Ideālā gadījumā rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze uzdevumu piešķiru izpildīšanai. Taču rezervācijas var būt balstītas uz pieejamību, un projekta gaitā uzdevumu laiki var mainīties. Tādēļ rezervāciju un piešķiru brīvais savienojums nodrošina elastību.

Programmā PSA ir cilne **Saskaņošana**, kas ļauj projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un viņu piešķires projektu darba grupās.

![Cilne Saskaņošana](media/Resource-Management-image56.png)

Cilnē **Saskaņošana** rezervācijas un piešķires katram darba grupas dalībniekam ir parādītas līdz atsevišķa uzdevuma piešķires līmenim. Tur tiek rādītas stundas šūnās, kas apzīmē laika periodus no mēnešiem līdz dienām.

Šajā cilnē ir redzama arī projekta vispārējā neto kopsumma kopā ar kolonnu kopsummu.

Katram resursam šī cilne aprēķina atšķirību starp darba grupas dalībnieka rezervācijām un darba grupas dalībnieka uzdevumu piešķiru apkopojumu. Ideālā gadījumā šai atšķirībai vajadzētu būt 0 (nulle). Citiem vārdiem sakot — starp rezervācijām un piešķirēm nevajadzētu būt nekādai starpībai. Atšķirības tiek iekrāsotas un ieēnotas, lai pievērstu uzmanību diviem tālāk aprakstītajiem apstākļiem.

- **Rezervācijas deficīts** — rezervācijas deficīts rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var vēlēties izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību.
- **Rezervāciju pārsniegšana** — rezervāciju pārsniegšana rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem. Šis apstāklis var būt pieņemams gadījumos, kad resurss projektam tika rezervēts vēl pirms tam, kad radās uzdevuma piešķire. Taču citos gadījumos resursu nav plānots piešķirt uzdevumiem. Šādos gadījumos projektu vadītājam ir jāapsver resursa rezervācijas atcelšana, lai šo noslodzi varētu izmantot citam projektam.

Reizēm, kad laiku skatāt augstākā līmenī nekā dienas līmenis (piemēram, mēneša līmenī), varat pamanīt, ka neto starpība resursam ir nulle (citiem vārdiem sakot, rezervācijas = piešķires). Taču, ja laiku skatāt nedēļas līmenī, varat redzēt, ka pirmajā nedēļā piešķires ir nulle stundu un rezervācijas ir 40 stundas, bet otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir nulle stundu. Kopumā rezervācijas un piešķires ir saskaņotas, bet katrai nedēļai tās atšķiras.

Kad laiku skatāties augstākos līmeņos, šūnām cilnē **Saskaņošana** ir indikators, lai informētu jūs, ka pastāv atšķirības zemākos līmeņos. Veicot dubultklikšķi uz šūnas, varat tuvināt, lai apskatītu atšķirību. Pēc tam varat noklikšķināt ar peles labo pogu, lai tālinātu. Atlasot kādu resursu un pēc tam režģa rīkjoslā izmantojot vadīklu **Nākamā atšķirība**, varat pāriet uz nākamo atšķirību starp šī resursa rezervācijām un piešķirēm. Pēc tam varat izmantot vadīklu **Iepriekšējā atšķirība**, lai dotos atpakaļ. Varat arī izslēgt atšķirību indikatoru un navigācijas uzvedību sadaļā **Iestatījumi**.

![Atšķirību indikators](media/Resource-Management-image57.png)

Ja jums ir uzdevumu piešķires kādam resursam, bet nav nevienas rezervācijas, lapā **Projekti**, cilnē **Saskaņošana** atlasiet rezervāciju deficītu un pēc tam atlasiet vienumu **Paplašināt rezervāciju**. Tiek parādīts dialoglodziņš **Paplašināt rezervāciju**, un tajā ir redzama rezervācija, kura ir nepieciešama, lai novērstu šo resursu deficītu. Tur ir redzamas arī resursu esošās rezervācijas visos projektos vai citos plānojamos elementos. Ja atlasāt **Labi**, lai izveidotu rezervāciju attiecīgajam resursam neatkarīgi no šī resursa pieejamības, varat izraisīt virsrezervāciju.

![Dialoglodziņš Paplašināt rezervāciju](media/Resource-Management-image58.png)

Pēc tam projektu vadītājs vai resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu visas situācijas, kur resursa rezervācija pārsniedz tā noslodzi.
