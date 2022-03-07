---
title: Kas jauns vai mainīts Project Service Automation 3. versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns un mainīts Project Service Automation 3. versijā.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2388aedec25915b3d364001fed11ca537b0f5507
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281127"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Kas jauns vai mainīts Project Service Automation 3. versijā

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir sniegta informācija par izmaiņām Project Service Automation (PSA) lietotāja interfeisā (UI), funkcionalitātē un terminoloģijā starp 1. vai 2. versiju un 3. versiju.

## <a name="project-scheduling"></a>Projekta plānošana
Projekta plāns, kas iepriekšējās versijās tika dēvēts par darba sadalījuma struktūru (WBS), ir pārdēvēts par plānu un ir pieejams, noklikšķinot uz cilnes **Plāns**. 

![Projekta plāns](media/psa-schedule-01.png)

Grafikā tagad ir jauna virsma mijiedarbībai, kas ir gan mūsdienīga, gan pieejama. Tomēr pamata Project Service Automation plānošanas programma nav mainījusies. Vadības pogas grafika režģa lentē ļauj mijiedarboties ar grafiku līdzīgi kā iepriekšējā Project Service Automation versijā. Plānā ir šādas papildu izmaiņas.

- **Ganta diagramma** — vairs nav pieejama Ganta diagramma. Jauna Ganta vizualizācija atgriezīsies turpmākā atjauninājumā.
- **Kolonnu virsraksti** — kolonnu virsrakstus varat paslēpt režģī, noklikšķinot uz lejupvērstā indikatora blakus kolonnas virsrakstam. 
- **Kolonnas** — paslēptas kolonnas varat parādīt, noklikšķinot uz **Pievienot kolonnu**. 
- **Transakcijas kategorija** — plāna režģim pievienota uzmeklēšana **Transakcijas kategorija**, un tā tiek rādīta pēc noklusējuma. 
 
## <a name="project-templates"></a>Projekta veidnes
Projekta veidņu funkcionalitātē ir veiktas tālāk minētās izmaiņas.

### <a name="create-a-project-template"></a>Projekta veidnes izveide 
3. versijā varat izveidot projekta veidni līdzīgi kā iepriekšējā Project Service Automation versijā. Veidne var saturēt tikai plānu, un plānā var būt iekļautas piešķires, taču tās nav nepieciešamas. Ja plānam ir piešķires, tās var būt tikai vispārējam resursam. Varat ģenerēt resursu prasības vispārējiem resursiem, taču tos nevar rezervēt ar reāliem resursiem veidnē. Darba grupai veidnē nevar rezervēt reālu resursu. 

### <a name="create-a-template-from-an-existing-template"></a>Jaunas veidnes izveidošana no esošas veidnes
Kad Project Service Automation 3.versijā izveidojat jaunu projekta veidni no esošas veidnes, notiek tālāk minētās darbības. 

- Avota projekta plāns tiek iekopēts veidnē. 
- Vispārējie resursi tiek kopēti darba grupā, un jebkuras vispārējo resursu piešķires tiek pārkopētas. Prasības vispārējiem resursiem netiek pārkopētas. 

### <a name="create-a-template-from-an-existing-project"></a>Jaunas veidnes izveidošana no esoša projekta
Ja izveidojat jaunu projekta veidni no esoša projekta, notiek tālāk minētās darbības. 

- Avota projekta plāns tiek iekopēts veidnē. 
- Vispārējie resursi tiek kopēti darba grupā, un jebkuras vispārējo resursu piešķires tiek saglabātas. Prasības vispārējiem resursiem netiek pārkopētas.    
- Nosauktie resursi — gan piešķirtie, gan nepiešķirtie — tiek noņemti no darba grupas un aizstāti ar vispārējiem resursiem.
- Informācija par klientu tiek noņemta, ja tā ir pieejama. 
- Atsauces uz piedāvājumiem un līgumiem tiek noņemtas, ja tās ir pieejamas. 

### <a name="create-a-project-from-a-template"></a>Projekta izveidošana no veidnes
Project Service Automation 3.versijā, kad izveidojat jaunu projekta veidni no esošas veidnes, notiek tālāk minētās darbības.

- Plāns, darba grupa un piešķires tiek kopētas uz jauno projektu.   
- Sākuma datums ir vai nu kopijas datums, vai lietotāja atlasīts datums.   
- Visiem vispārējās darba grupas dalībniekiem, kuriem ir resursu prasības veidnē, prasības netiek automātiski kopētas vai ģenerētas. Tās ir jāģenerē. 

## <a name="copy-a-project"></a>Projekta kopēšana
Project Service Automation 3. versijā, kad kopējat projektu, notiek tālāk minētās darbības. 

- Tiek kopēts plānotais sākuma datums, bet to var mainīt.  
- Tiek kopēts projekta plāns un uzdevumi. 
- Tiek kopēti vispārējie resursi un to piešķires. Netiek kopētas resursa prasības vispārējiem resursiem. Tās ir jāģenerē atkārtoti. 
- Netiek kopēti reālie resursi un to piešķires. Tā vietā tie tiek aizstāti ar vispārējiem resursiem. 
- Faktiskās vērtības netiek kopētas uz jauno projektu. 

## <a name="move-a-scheduled-project"></a>Plānotā projekta pārvietošana
Ja pārvietojot uz priekšu esoša projekta plānu, notiek tālāk minētās darbības. 

- Uzdevuma datumi tiek automātiski pārvietoti, lai tie atbilstu pārvietošanas periodam. 
- Piešķirtie vispārējie resursi joprojām paliek piešķirti.   
- Ja tie tika ģenerēti pirms projekta pārvietošanas, prasības vispārējiem resursiem paliek tādas pašas un netiek automātiski ģenerētas atkārtoti. Tās ir jāģenerē vēlreiz, lai atspoguļotu jaunās piešķires, kas saistītas ar uzdevuma pārvietošanu. 
- Reālo resursu piešķires mainās, lai atbilstu uzdevuma datuma pārvietošanai. Reālo resursu rezervācijas nemainās. Nepieciešams modificēt rezervācijas, izmantojot saskaņošanas skatu. 
- Darba grupas resursi ar rezervācijām, bet ne piešķirēm, nemainās. 
- Faktiskās vērtības netiek pārvietotas. 

## <a name="estimates"></a>Prognozes
Prognozes ir sadalītas divās cilnēs: **Resursu piešķires** un **Prognozes**. Cilne **Resursu piešķires** satur darba prognozes un parāda uzdevumu resursu piešķires uzdevumiem laika periodu skatā. Prognozes var rediģēt, pamatojoties uz to, ko ģenerējusi plānošanas programma.

![Resursu piešķires cilnes parāda darba prognozes un resursu piešķires uzdevumiem](media/resource-assignments-tab-02.png)

Cilne **Prognozes** parāda resursu piešķires izmaksas un pārdošanas summas. Summām ir tikai lasāms statuss. Izmaksas un pārdošanas cenas tagad tiek vadītas no darba grupas dalībnieka piešķirēm plānā. Tas nozīmē, ja jums ir uzdevums bez piešķires, uzdevums tiks parādīts pie nepiešķirta intervāla. Tas nozīmē arī to, ka bez **lomas**, kas ir noklusējuma izcenojuma dimensija, nebūs prognozēto izmaksu vai pārdošanas, ja ar šo projektu ir saistīts klients vai līgums / piedāvājums. 

![Prognožu cilnes parādītas izmaksas un pārdošanas summas](media/estimates-tab-03.png)
  
Kategorija tiek atbalstīta arī uzdevumiem plānošanas skatā. Grupējot pēc kategorijas prognožu laika periodu skatā, tiek nodrošināta labāka pieredze, īpaši, ja projektā ir arī izdevumu prognozes. Izdevumu prognozes tiek ievadītas, izmantojot režģi atsevišķā cilnē. 

Izdevumu prognozes var ievadīt režģī cilnē **Izdevumu prognozes**. 

![Izdevumu prognožu cilnes parādīts izdevumu prognožu režģis](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Resursu pārvaldība
Project Service Automation 3. versijā, izmantojot jauno vienotā klienta lietotāja interfeisu un izmaiņas attiecībās starp rezervācijām un piešķirēm, personāla komplektēšana projektam ar vispārējiem vai reāliem resursiem ir būtiski mainījusies, salīdzinot ar 2. un 1. versiju. Tomēr rezervējamo resursu koncepcijas gan **reāliem**, gan **vispārējiem** resursiem paliek tādas pašas, tāpat kā darba grupas dalībnieki, prasības, piešķires un rezervācijas.   

![Resursu atlasītāja izmantošana](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Reāla rezervējama resursa piešķiršana 
Project Service Automation 3. versijā rezervācijas un uzdevumu piešķires nav tik cieši saistītas kā iepriekšējās Project Service Automation versijās. Darba grupas režģi var izmantot, lai rezervētu **reālu** darba grupas dalībnieku, līdzīgi kā iekšējā tirgū.

Izmantojot resursu atlasītāju plānā, varat atlasīt darba grupas dalībnieku, kas izveidots darba grupas skatā, un pēc tam piešķirt to uzdevumiem. Varat arī turpināt piešķirt tiem uzdevumus pat pēc to rezervācijas. Izmantojiet cilni **Saskaņošana**, lai saskaņotu darba grupas dalībniekus ar atšķirībām rezervācijās un piešķirēs.

Resursu atlasītājs parādīs darba grupas dalībniekus šim projektam. Varat arī izmantot resursu atlasītāju, lai meklētu un skatītu citus rezervējamos resursus, kas nav projekta darba grupas daļa. Tos varat piešķirt uzdevumam, un tie kļūs par projekta darba grupas daļu. Tos nepieciešams rezervēt, izmantojot cilni **Plānošanas panelis** vai **Saskaņošana**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Vispārēja rezervējama resursa piešķiršana uzdevumam un projekta darba grupai, pēc tam izpildot ar īstu resursu, izmantojot plānošanas paneli 
Project Service Automation 3. versijā ģenerēšanas darba grupas funkcionalitāte netiek izmantota vispārējiem resursiem. Tā vietā varat izveidot un tieši piešķirt vispārējo resursu no plāna, ierakstot plāna resursa šūnā attiecīgā vispārējā resursa pozīcijas nosaukumu. Vai arī varat atlasīt resursu ikonu šūnā un pēc tam, izmantojot resursu atlasītāju, ierakstīt tā vispārējā resursa nosaukumu, ko vēlaties izveidot. Tiks atvērts ātrās izveides panelis, kas ļauj iestatīt vispārējā resursa darba grupas dalībnieka lomu un organizācijas vienību. Kad resurss ir izveidots, tas tiek piešķirts uzdevumam, un šo vispārējo resursu varat arī turpināt piešķirt citiem uzdevumiem plānā.    
 
Kad resurss ir piešķirts visiem atbilstošajiem uzdevumiem, varat ģenerēt resursa vajadzību un pēc tam to izpildīt, veicot tiešu rezervāciju, izmantojot **Plānošanas paneli**, vai iesniedzot resursa pieprasījumu. Varat arī pievienot vispārējos resursus tieši darba grupas dalībnieka režģim. 

Vispārējie resursi tiek pievienoti projekta darba grupai bez resursu vajadzībām un ar projekta sākuma / beigu datumiem, līdz tiek ģenerēta resursa vajadzība. Lai ģenerētu vajadzību, atlasiet vispārējo resursu un noklikšķiniet uz **Ģenerēt**. Tagad tiek rādīta vajadzības saite, un nepieciešamās stundas tiks aizpildītas ar piešķirtajām stundām. Varat noklikšķināt uz saites, lai atvērtu un atjauninātu šo vajadzību.
  
Kad rezervācija ir pabeigta un to pilnībā izpilda nosaukts resurss, vispārējais resurss tiek aizstāts ar nosaukto resursu, un piešķire plānā tiek atjaunināta ar nosaukto resursu. 

Vajadzībām piedāvātie resursi tagad tiek glabāti cilnē, nevis atsevišķā sadaļā.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Vairāki nosauktie resursi, kas izpilda vispārējo resursu
Ja vajadzība ir izpildīta ar vairākiem resursiem, vispārējais resurss paliek darba grupā un piešķirts uzdevumam. Nosauktie darba grupas dalībnieki, kas ir rezervēti, netiek piešķirti kā daļa no pozīcijas. Projekta vadītājs pēc nepieciešamības var piešķirt darbu reālajiem resursiem.  Skats **Saskaņošana** nodrošina rezervāciju sadalījumu starp vairākiem resursiem uz vairākām uzdevumu piešķirēm. Tas netiek darīts automātiski, jo sarežģītākās situācijās, piemēram, ja ir vairāku uzdevumu komplekts, kas veido vajadzību, jāpieņem nolūks, kā projektu vadītājs vēlas veikt piešķiršanu. Tā kā sistēma nevar saprast nolūku, pieņēmumi visticamāk būs citādi, nekā paredzēts, un radīsies nepareizs vai neparedzams rezultāts. Prognozējamais rezultāts ir tāds, ka vispārējais resurss paliek piešķirts, kamēr projektu vadītājs apzināti piešķir resursus, izmantojot skatu **Saskaņošana**.

### <a name="reconciliation"></a>Saskaņošana
Cilnē **Saskaņošana** tiek parādītas rezervācijas un visas piešķires katram projekta darba grupas dalībniekam. Skatā šūnās redzamas stundas, kas var attēlot laika punktus no mēnešiem līdz dienām. Šis skats ļauj projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un to piešķires attiecībā uz savu projekta darba grupu. Tas ir noderīgi, jo rezervācijas un uzdevumu piešķires nav cieši savienotas, kas pieļauj elastīgāku projekta plānošanu. 

![Saskaņošanas cilnē parādītās rezervācijas un piešķires projekta darba grupas dalībniekiem](media/resource-reconciliation-tab-06.png)

Katrā resursā skats izmanto atšķirību starp darba grupas dalībnieka rezervācijām un viņa uzdevumu piešķiru apkopojumu, un parāda tālāk minētās divas atšķirības, kas var rasties ar rezervācijām un piešķirēm projektā. 

- **Rezervācijas deficīts** — rezervācijas deficīti rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var to izlabot, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību. 
- **Rezervāciju pārsniegšana** — pārmērīga rezervācija rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem.  Tas var būt pieņemams gadījums, piemēram, ja resurss ir rezervēts pirms uzdevuma piešķires. Tomēr citos gadījumos resurss var nebūt plānots piešķiršanai, un projektu vadītājam jāapsver iespēja atcelt resursa rezervācijas, lai noslodzi varētu izmantot citam projektam. 

Ja resursam ir uzdevuma piešķires bez rezervācijām (rezervācijas deficīts), varat atlasīt apkopojošo rezervācijas deficītu un noklikšķināt uz **Pagarināt rezervāciju**. Šeit varat skatīt rezervāciju, kas ir nepieciešama resursa deficīta novēršanai un tā pieejamībai. 
 
## <a name="time-and-expense"></a>Laiks un izdevumi
Šajā sadaļā ir sniegta informācija par laika, izdevumu un apstiprinājuma izmaiņām Project Service Automation 3. versijā. Kā daļa no Dynamics 365 Project Service Automation risinājuma, līdzeklis **Laika ieraksts** ir atsvaidzināts, lai gūtu labumu no vienotā interfeisa struktūras. Tas iespējo konsekventa, vienota lietotāja interfeisa nodrošināšanu, kas seko atsaucīgam dizainam optimālai skatīšanai jebkāda izmēra ekrānā vai ierīcē. 

### <a name="landing-page"></a>Reklāmas mērķlapa
Nepaplašināmā pielāgotā laika ieraksta pieredze 3. versijā ir novecojusi. Tās vietā tagad ir paplašināma un pieejama vietējā režģa pieredze. Varat piekļūt laika ieraksta funkcionalitātei, izmantojot vietnes karti kreisajā pusē. Ar šo izmaiņu vairs nebūs iespējams katrā reizē ievadīt laiku nedēļai. Tā vietā ir jāizveido laika ieraksts katrai dienai režģī. Pēc dažu laika ierakstu izveidošanas lietotāji var izveidot lielapjoma laika ierakstus, izmantojot funkciju **Kopēt**, kas paskaidrota šīs tēmas turpinājumā. 

![Laika ieraksta reklāmas mērķlapa](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Jaunu laika ierakstu izveide 
Lentē noklikšķiniet **Jauns**, lai atvērtu ātrās izveides lapu laika ieraksta, kur ievadīt ilgumu minūtēs, stundās vai dienās. Lai to izdarītu, vienkārši sāciet rakstīt s, m vai d kopā ar daudzumu.  

![Laika ieraksta ātrā izveide](media/quick-create-time-entry-08.png)

Uzmeklēšanas laukus atbalsta sistēmas skati. Piemēram, pēc projekta informācijas ievadīšanas lauks **Projekta uzdevums** pēc noklusējuma ir iestatīts uz skatu **Mani atvērtie projekta uzdevumi**. Lai izveidotu laika ierakstus uzdevumiem, kas nav piešķirti lietotājam, uzmeklēšanā noklikšķiniet **Mainīt skatu** un pēc tam atlasiet **Visi aktīvie projekta uzdevumi**. Pēc tam, kad laika ieraksts ir izveidots un parādīts režģī, varat rediģēt jebkuras rindas vērtības režģī.  

### <a name="bulk-createcopy"></a>Lielapjoma izveide / kopēšana 
Pēc tam, kad izveidoti daži laika ieraksti, varat izmantot kopēšanas funkcionalitāti, lai izveidotu papildu lielapjoma laika ierakstus. Noklikšķiniet **Kopēt**, lai atvērtu dialogu **Kopēt**. **No perioda: sākuma datums** iestatiet datu diapazonu, no kura jākopē laika periodi. **Uz periodu: sākuma datums** norādiet datumu, kuram jāizveido laika ieraksti. Noklikšķiniet **Kopēt**, lai kopētu laika ierakstus uz atbilstošo nedēļas dienu, kas norādīta **Uz periodu**. Piemēram, pirmdienas laika ieraksts no iepriekšējās nedēļas tiks kopēts uz pirmdienu nedēļā, kas norādīta **Uz periodu**. 

![Lielapjoma laika ierakstu kopēšana](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Datu importēšana 
Piešķires un maiņa seko tam pašam lietotāja interfeisa modelim, kas lietotājam ļauj norādīt datumu diapazonu, kad ir jāimportē rezervācijas. Pēc tam ir tieši jāizvēlas rezervācijas, kas ir jākopē laika ierakstos **Melnraksts**. 3. versijā vairs nevar redzēt laika ierakstu **Ieteikts** modeli režģī un kalendārā.  

### <a name="change-in-calendar-control"></a>Kalendāra vadīklas maiņa
3. versijā esam pavirzījušies prom no pielāgotās kalendāra vadīklas un tagad izmantojam vienoto sakaru kalendāru, lai parādītu laika ierakstus nedēļai. Izmantojot šo kalendāru, varat apskatīt dienu, nedēļu un mēnesi. 

> [!NOTE]
> Kalendāra ierobežojums ir tāds, ka šī vadīkla neatbalsta darbības atsevišķos kalendāra vienumos. Piemēram, nebūs iespējams atlasīt vienu vai vairākus kalendāra vienumus un tos iesniegt vai dzēst. Noklikšķinot uz kalendāra vienuma, tiks atvērta lapa **Laika ieraksta entītija** papildu darbību veikšanai. 

### <a name="extensibility"></a>Paplašināmība
**Datu tveršana pielāgotos laukos tikai laika un izdevumu ierakstu entītijās** — laika ieraksts izmanto rediģējamu režģi, kas ir tikai lasāms, un kalendāra vadīklas no platformas. Visas šīs vadīklas ir vietējās, un tāpēc tās atbalstīs pielāgošanu. Project Service Automation 3. versijā varat pievienot papildu pielāgotus laukus, iestatīt uzmeklēšanas laukus un dublēt tos ar pielāgotiem skatiem. Varat arī iestatīt pielāgotu biznesa loģiku, pamatojoties uz atlasītajām vērtībām pielāgotos laukos.  

**Datu apkopošana par pielāgotiem laukiem laika un izdevumu ierakstā un šo izmaiņu ieviešana, izmantojot entītijas, kas atbalsta iesniegšanas un apstiprināšanas plūsmu** — tipiska laika ierakstu apstrāde parādīta tālāk redzamajā shēmā.

![Laika ievades plūsmas apstrāde](media/process-time-entries-10.png)

Ja biznesa prasības nosaka, ka laika un izdevumu entītijām ir jātver pielāgotas izcenojuma dimensijas un jāievieš vērtības, kuras iestata laika un ierakstu resurss pielāgotā izcenojuma dimensijā, izmantojot visas iepriekšējā grafikā iekļautās entītijas, skatiet [Pielāgotu lauku iestatīšana kā izcenojuma dimensijas](set-up-pricing-dimensions.md)

Lai atbalstītu biznesa prasības gadījumos, kad laika un izdevumu entītijām ir jātver pielāgotas dimensijas, kuras nav izcenojumi, un jāievieš vērtības, varat izmantot izcenojuma dimensiju iestatīšanu un izteikt pielāgotās dimensijas kā izcenojuma dimensijas bez izmaksu vai rēķinu likmes. Cits scenārijs būtu pievienot pielāgotu lauku katrai entītijai, izmantojot tādu pašu lauka nosaukumu visās entītijās. Pielāgotus spraudņus var izveidot, lai tos saistītu ar ierakstus entītijās, kas piedalās iesniegšanā / apstiprināšanas plūsmā, izmantojot transakcijas izcelsmi un transakcijas savienojuma entītijas.  

### <a name="delegate-time-and-expense-entry"></a>Laika un izmaksu ieraksta deleģēšana
Common Data Service platforma neatbalsta viena lietotāja uzdošanos par citu, kas nozīmē, ka ir Project Service Automation 3. versijā netiek atbalstīts deleģētais laiks un izdevumu ieraksts. Taču partneri un klienti gūst labumu no risinājuma, kas iespējo atbalstu deleģētā laika ieraksta pieredzi 3. versijā. Tas ir tikai konkrēts, nevis pilnīgs risinājums, tāpēc ir svarīgi izprast ierobežojumus un izmantot šo pieeju tikai tad, ja ierobežojumi ir pieņemami. 

> [!IMPORTANT]
> Šī informācija ir jāuzskata par ieteiktiem norādījumiem attiecībā uz partnera / klienta veiktu pielāgotu ieviešanu. Produkta darba grupa nesniegs oficiālu atbalstu šai funkcionalitātei, izmantojot jebkuru no mūsu atbalsta kanāliem.

### <a name="customization-details"></a>Pielāgošanas papildinformācija 
Pielāgošana ļauj pievienot **Rezervējamais resurss**, lai izveidotu un rediģētu pieredzes, kas lietotājam ļaus darboties kā pārstāvim, mainot lauku **Resursa rezervācija** citam lietotājam, kuram jāieraksta laika un izdevumu ieraksts. Tālāk minētajās darbībās tiek aptverta laika ieraksta deleģēšana. Tāda pati informācija attiecas uz izdevumu ieraksta deleģēšanu. 
 
1.  Pārliecinieties, vai deleģētajam lietotājam ir globālā drošības piekļuve projektiem un projektu uzdevumiem. 
1.  Tā kā **Rezervējamais resurss**, kas ir lauks entītijā **Laika ieraksts**, netiek parādīts lapā **Ātrā izveide**, tas ir jāpievieno.

    Vai

    Izveidojiet pielāgotu skatu, kas ietver kolonnu **Rezervējamais resurss**, lai skatītu tikai resursam izveidotos laika ierakstus. Publicējiet pielāgojumus programmas moduļa noformētājā, lai šis skats parādītos zem **Skatīt atlasītāju** lapā **Laika ieraksti**. Pastāv divi spraudņi, kas regulē vadītāja iestatīšanu ar projektu nesaistītos laika ierakstos.

    - Pirmsvalidācijas laika ieraksta izveide
    - Pirmsvalidācijas laika ieraksta atjaunināšana
 
1. Izveidojiet jaunu spraudni, lai pārrakstītu lauku **Vadītājs** tā lietotāja vadītājam, kurš ir piešķirts laukā **Rezervējamais resurss**. Lietojiet to pašu **Izpildes posmu** kā ārpusjoslas (OOB) spraudnim (pirmsvalidācijas) un izmantojiet **Izpildes pasūtījumu**, kas ir lielāks nekā OOB spraudņi (lielāks nekā 1). Tas nodrošinās, ka pielāgotais spraudnis tiek izpildīts pēc OOB spraudņiem.  
 
### <a name="end-user-experience"></a>Gala lietotāja pieredze
1.  Kad ātrās izveides lapā izveidojat laika ierakstu, ievadiet projekta un projekta uzdevuma papildinformāciju un pēc tam izvēlieties lietotāju laukā **Rezervējamais resurss**, kuram jāieraksta laika ieraksti. 
2.  Pēc noklusējuma šis lauks tiek noklusēts lietotājam, kurš ir pieteicies, tomēr, ņemot vērā, ka lietotājs pārlabojis šo lauku, laika ieraksts tagad tiek izveidots izvēlētajam **Rezervējamam resursam**.
3.  Iesniedzot laika ierakstus, kas izveidoti šiem ierakstiem, ieraksti tiks sarindoti projekta apstiprinātājam, kā paredzēts. 
4.  Atsaucot citam lietotājam izveidotos laika ierakstus, šie laika ieraksti atgriezīsies stāvoklī **Melnraksts** kopā ar lauku **Rezervējamais resurss**, kas iestatīts citam lietotājam. 
5.  Pēc izvēles varat pārslēgties uz pielāgoto skatu, lai filtrētu citam lietotājam izveidotos laika ierakstus. 
 
### <a name="limitations"></a>Ierobežojumi
Funkcionalitāte **Kopēt** un **Importēt** darbojas tikai saistībā ar to lietotāju, kurš ir pieteicies. Tas nozīmē, ka nav iespējams kopēt vai importēt laika ierakstus, kas izveidoti lietotājam, kurš ir pieteicies kā rezervējamais resurss.

Laika ieraksti, kas nav paredzēti projektam, tiks novirzīti apstiprināšanai rezervējamo resursu vadītājam tikai tad, ja ir izpildīts iepriekš minētās sadaļas **Pielāgošanas papildinformācija** 4. solis. Pretējā gadījumā ar projektu nesaistītie laika ieraksti citam lietotājam tiks nepareizi novirzīti tā lietotāja, kurš ir pieteicies, vadītājam. 

### <a name="other-changes"></a>Citas izmaiņas 
**Rezervēšanas un uzdevumu** funkcionalitāte ir noņemta. 

## <a name="multidimensional-pricing"></a>Vairākdimensiju izcenojums
Lai palielinātu elastību un atbilstu dažādām biznesa prasībām, Project Service Automation 3. versija atbalsta diskrētu izcenojuma dimensiju kopu piemērošanu izmaksām un rēķinu likmēm. Dimensiju vērtības var iestatīt kā noklusējumu un pēc tam ieviest izmaksu un izcenojumu procesā no resursu profilēšanas līdz laika ierakstam, lai atspoguļotu faktisko. Klientam specifiskā konfigurācija un modifikācija vai paplašinājums gūst labumu no standarta pielāgošanas infrastruktūras.

Project Service Automation tiek nosūtīts ar izcenojuma dimensiju, lomu un resursa vienību noklusējuma kopu un ļauj iestatīt cenas un izmaksas katrai lomas un organizācijas vienības kombinācijai.

Project Service Automation klientiem, kas vēlas turpināt izmantot šos iebūvētos laukus kā izcenojuma dimensijas 3. versijā, nebūs vērojamu izmaiņu. Varat turpināt lietot programmu Project Service Automation kā parasti. Tomēr, ja nepieciešams noteikt savu resursu cenu vai izmaksas, izmantojot citus papildu atribūtus, 3. versija ļauj pievienot Project Service Automation savas pielāgotās izcenojuma dimensijas. Pielāgotā izcenojuma dimensijas paplašinājums ir sarežģīta konfigurācijas pieredze. 

## <a name="quotes-and-contracts"></a>Piedāvājumi un līgumi
Project Service Automation 3. versijā ir mainījušies iestatījumu un pārvaldības aspekti piedāvājumiem un līgumiem. Nākamajās sadaļās ir sniegta papildinformācija.

### <a name="set-up-chargeability-options"></a>Maksas iekasēšanas opciju iestatīšana
1. un 2. versijā maksas iekasēšanas iestatīšana noteiktu piedāvājumu un līgumu lomām un kategorijām tika veikta, izmantojot skatu **Maksas iekasēšana**, kas atradās piedāvājuma vai līguma rindas navigācijas augšpusē. Turpat bija iespējams iestatīt šo lomu cenas un izdevumu kategorijas.

Sākot ar 3. versiju, maksas iekasēšanas opciju pēc lomas un izdevumu kategorijas iestatīšana tiks veikta piedāvājuma vai līguma rindas līmenī. Izcenojuma iestatīšana ir atdalīta no maksas iekasēšanas iestatīšanas. Varat atrast **Lomas ar maksas iekasēšanu** un **Kategorijas ar maksas iekasēšanu** kā cilnes lapās **Piedāvājuma rinda** un **Līguma rindu**, neizmantojot navigācijas augšpusi.

![Rēķinā iekļaujamās lomas](media/chargeable-12.png)
 
Lomu ar maksas iekasēšanu un kategoriju ar maksas iekasēšanu iestatīšana arī gūst labumu no iekļautās rediģējamās režģa vadīklas. Katrai lomai un kategorijai atbalstītās norēķinu tipa opcijas piedāvājuma un līguma slēgšanas fāzes laikā paliek nemainīgas no iepriekšējām versijām kā **Ar maksas iekasēšanu** un **Bez maksas iekasēšanas**. **Papildu** tips netiek atbalstīts piedāvājuma vai līguma slēgšanas fāzē. **Papildu** tiek atbalstīts tikai laika vai izdevumu apstiprināšanas laikā.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Pielāgota izcenojuma izveide un rediģēšana Project Service Automation piedāvājumam un projekta līgumam
1. un 2. versijā pielāgota cenrāža izmantošana noteiktiem piedāvājumiem un līgumiem tika veikta, izmantojot **Rediģēt cenas** skatā **Maksas iekasēšana**. Skats **Maksas iekasēšana** atradās piedāvājuma rindas vai līguma rindas navigācijas augšpusē. Turpat bija iespējams iestatīt maksas iekasēšanas opcijas lomām un izdevumu kategorijām.

Sākot ar 3. versiju, pielāgota projekta cenrāža izveide un izmantošana Project Service Automation piedāvājumam un Project Service Automation projekta līgumam ir atdalīta no maksas iekasēšanas iestatīšanas. Project Service Automation piedāvājumam un Project Service Automation projekta līgumiem ir jaunas cilnes, kas tiek sauktas **Projekta cenrāži**. Šajā cilnē ir redzams saistītais skats visiem projekta cenrāžiem, kas pievienoti Project Service Automation piedāvājumam vai projekta līgumam. Lai izveidotu pielāgotu cenrādi no esoša cenrāža, kas jau ir saistīts ar projekta piedāvājumu vai līgumu, noklikšķiniet **Izveidot pielāgotu izcenojumu**. Tas izveidos kopiju no visiem saistītajiem cenrāžiem un pievienos tos piedāvājumam vai līgumam. Tagad varat atvērt cenrādi un rediģēt lomu vai izdevumu kategorijas cenu, lai šīs izcenojuma izmaiņas attiektos tikai uz šo piedāvājumu vai līgumu. 
  
Šis attēls uzņemts pirms ir izveidoti pielāgoti cenrāži.

![Pirms pielāgotiem cenrāžiem](media/before-custom-price-lists-13.png)

Šis attēls parāda izskatu pēc pielāgotu cenrāžu izveides.

![Pēc pielāgotiem cenrāžiem](media/after-custom-price-lists-14.png)

> [!NOTE]
> Var rasties īsa aizkave starp noklikšķināšanu uz **Izveidot pielāgotu izcenojumu** un brīdi, kad tiek izveidots pielāgots cenrādis. Iesakām atsvaidzināt režģi, nevis klikšķināt vairākas reizes. Pielāgots cenrādis ir izveidots, ja ar saistītā cenrāža nosaukumam ir pievienots piedāvājuma nosaukums vai projekta līguma nosaukums.


[!INCLUDE[footer-include](../includes/footer-banner.md)]