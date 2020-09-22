---
title: Projekta resursi
description: Šajā tēmā ir sniegta informācija par projekta resursiem.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753422"
---
# <a name="project-resourcing"></a>Projekta resursi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par projekta resursiem.

Viens no projekta vadītāju un resursu vadītāju uzdevumiem projekta plānošanas posmā ir resursu piešķiršana, kuras laikā viņiem ir jānosaka un jārezervē pareizais resurss, ar ko strādāt projektā. Programmā Dynamics 365 Finance iespēju noteikšanai projektiem varat definēt lomas, kas tiek uzskatītas par pagaidu resursiem, ko var rezervēt noteiktai piesaistei vai tās daļai. Šāda veida resursu plānošana ļauj projekta vadītājiem un resursu vadītājiem izpildīt šādus uzdevumus:

- Definēt lomu, kurai ir nepieciešamās kompetences, lai varētu viegli saskaņot resursus.
- Izmantot lomas, lai definētu sākotnēju iesaistes grafiku, kura pamatā ir rezervēti resursi.
- Aprēķināt izmaksas un noteikt sākotnējo budžetu, pamatojoties uz projektam piešķirtajām lomām un resursiem.
- Izmantot lomas, lai noteiktu to resursu rezervāciju skaitu, kuras ir nepieciešamas katrai iesaistei.
- Noteikt to resursu skaitu, kuri ir nepieciešami visam projekta dzīves ciklam
- Izveidojiet darba sadalījuma struktūras (WBS) melnrakstu, izmantojot sākotnējo resursu piešķiri.

[![Projekta dzīves cikls](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Turpinoties projekta plānošanai, plānotos resursus var aizstāt ar personāla resursiem. Turklāt projekta vadītājs var atgriezties un atjaunināt resursu rezervācijas jebkurā projekta posmā.

## <a name="set-up-project-resources"></a>Projekta resursu iestatīšana
Ir jāiestata kalendārs un tas jāsaista ar darbinieku vai darba ņēmēju. Tiek izmantots kalendārs, lai ieplānotu projektu un projektam rezervēto resursu darba laiku. Kalendāra iestatīšanas laikā projekta vadītāji var resursu optimizācijas ietvaros veikt resursu pielāgošanu. Atkarībā no kalendāra grafika resursiem var piemērot ierobežojumus. Kalendāru varat iestatīt lapā **Kalendāri**.

Iestatot darba ņēmēju kā projekta resursu, varat izvēlēties no darba ņēmējiem, kuri strādā uzņēmumā, kuram iestatāt resursus. Vai arī varat atlasīt darba ņēmējus no citiem savas organizācijas uzņēmumiem. Šie darba ņēmēji ir pazīstami kā starpuzņēmumu resursi.

Tālāk aprakstītajās procedūrās ir paskaidrots, kā jūsu uzņēmumā iestatīt darba ņēmēju kā projekta resursu un kā iestatīt starpuzņēmumu projekta resursu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Darba ņēmēja kā projekta resursa iestatīšana

1. Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēju, kuru pievienojat kā projekta resursu, un atveriet darba ņēmēja ierakstu.
2. Darbību rūtī atlasiet **Projekts**&gt; **Iestatīšana** &gt; **Projekta iestatīšana**.
3. Atlasiet kalendāru un pēc tam aizveriet lapu.

Resursam noklusējuma projektus var arī norādīt kā iepriekšējas piešķiršanas tipu. Iepriekšējo piešķiri var izmantot, ja resursu pārvaldnieks vai projekta vadītājs iepriekš zina, ar kuriem resursiem projekts strādās. Iepriekšējo piešķiri var arī balstīt projekta sponsora vai klienta pieprasījumā. Lai iepriekš piešķirtu projektu, lapas **Piešķirt projektu** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet atbilstošo projektu.

### <a name="set-up-an-intercompany-resource"></a>Starpuzņēmumu resursa iestatīšana

Iestatot darba ņēmēju kā starpuzņēmumu resursu, iestatīšana ir jāizpilda gan gan patapinošajam uzņēmumam, gan uzņēmumam, kas aizņemas.

**Patapinošajā uzņēmumā**

1. Risinājumā Finance pārbaudiet, vai ir atlasīts patapinošais uzņēmums, un pēc tam izpildiet iepriekšējā sadaļā "Darba ņēmēja kā projekta resursa iestatīšana" aprakstītās darbības.
2. Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauna**.
3. Laukā **Juridiskās personas ID** atlasiet patapinošo uzņēmumu. Atbilstoši aizpildiet atlikušos laukus un pēc tam atlasiet **Saglabāt**.
4. Lapā **Pārnest cenu** atlasiet **Jauna**.
5. Laukā **Juridiskā persona, kas aizņemas** atlasiet atbilstošo uzņēmumu.
6. Lai patapinātu uzņēmumam, kas aizņemas, tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu. Lai uzņēmumam, kas aizņemas, varētu būt pieejami visi patapinošā uzņēmuma resursi, atstājiet lauku **Resurss** tukšu.
7. Lapas **Projekta pārvaldības un uzskaites parametri** cilnē **Starpuzņēmumu** iestatiet opciju **Iespējot starpuzņēmumu resursu plānošanu un darba laika uzskaites tabulas** uz **Jā**.

**Uzņēmumā, kas aizņemas**

- Lapas **Resursu saraksts** meklēšanas filtrā ievadiet patapinošajam uzņēmumam izveidotā resursa nosaukumu, lai apstiprinātu, ka nosaukums tiek iekļauts uzņēmuma, kas aizņemas, resursu sarakstā.

## <a name="manage-resource-competencies"></a>Resursu kompetenču pārvaldība
Resursu kompetences ir būtiska resursu pārvaldības daļa. Kompetences var izmantot kā bāzlīniju, lai noteiktu resursus, kuriem ir pareizais prasmju, izglītības, sertifikācijas un projekta pieredzes līdzsvars. Šī informācija ir jāiestata katram resursam un tā regulāri jāatjaunina. Tādējādi iespējas var maksimizēt, ja projekta resursu piešķires laikā tiek saskaņotas noteiktas resursu kompetences.

[![Prasmju, sertifikāciju, izglītības un projekta pieredzes piemēri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Tālāk aprakstītajās procedūrās ir paskaidrots, kā iestatīt dažas resursa kompetences.

Lai iestatītu kompetences darba ņēmējam, varat izmantot Cilvēkresursu saraksta lapu **Darba ņēmēji** vai Projekta pārvaldības un uzskaites lapu **Resursi**. Šīm procedūrām tiek izmantota Cilvēkresursu saraksta lapa **Darba ņēmēji**.

### <a name="set-up-competencies-certificates"></a>Kompetenču iestatīšana: Sertifikāti

1. Saraksta lapā **Darba ņēmēji** atlasiet tā darba ņēmēja rindu, kurai jāpievieno sertifikāta informācija.
2. Darbību rūts cilnes **Darba ņēmējs** grupā **Kompetences** atlasiet **Sertifikāti**.
3. Atlasiet **Jauna** un pēc tam laukā **Sertifikāta veids** atlasiet **PMP**.
4. Laukā **Sākuma datums** atlasiet **10/1/2015** un pēc tam atlasiet **Saglabāt**.

### <a name="set-up-competencies-skills"></a>Kompetenču iestatīšana: Prasmes

1. Saraksta lapā **Darba ņēmēji** pārliecinieties, ka joprojām ir atlasīts darba ņēmējs, kuru izmantojāt iepriekšējā procedūrā. Pēc tam darbību rūts cilnes **Darba ņēmējs** grupā **Kompetences** atlasiet **Prasmes**.
2. Atlasiet **Jauns**.
3. Laukā **Prasmes** atlasiet **Projektu pārvaldība**.
4. Laukā **Līmenis** atlasiet **5 Eksperts**.
5. Laukā **Līmeņa datums** atlasiet **1-/14/2014**.
6. Laukā **Pieredze gados** ievadiet **10**.
7. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-new-project"></a>Izveidot jaunu projektu
1. Lapā **Projektu pārvaldība** atlasiet **Jauns projekts** un ievadiet šādas vērtības:

    - **Projekta veids:** Laiks un materiāls
    - **Projekta nosaukums:** XYZ Jaunināšanas fāze 2
    - **Projekta grupa:** TM\_WIP
    - **Projekta līguma ID:** 00000002

2. Atlasiet **Izveidot projektu**.

### <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1. Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēja ierakstu, kuram iepriekš iestatījāt kompetences, un atveriet darba ņēmēja ierakstu.
2. Darbību rūts cilnes **Projekts** grupā **Kompetences** atlasiet **Piešķirt projektus**.
3. Lapas **Resursu validācijas projekta piešķire** cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet projektu **XYZ Jaunināšanas fāze 2**.
4. Rūtī **Atlikušie projekti** atlasiet projektu un pēc tam atlasiet bulttaustiņu, lai to pievienotu rūtij **Atlasītie projekti**.

Varat arī pēc nepieciešamības resursam piešķirt kategorijas. Kategorijas veids ir vai nu **Izmaksas** vai **Ieņēmumi**. Kategorijas veidu nosaka jūsu organizācija. Ja resursam netiek piešķirtas kategorijas, Finance uzmeklē noklusējuma kategoriju izmaksu un ieņēmumu stundu cenām.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu raksturlielumu iestatīšana

Projekta vadītājs var izmantot projekta resursu funkcionalitāti, lai izveidotu projektam nepieciešamās lomas. Lomas var izmantot, ja apstiprinātie resursi joprojām nav zināmi, kad resursi tiek rezervēti. Lomas var īslaicīgi rezervēt kā plānotos resursu, lai varat turpināt projekta plānošanas posmus.

[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** Contoso nolīga, lai pabeigtu laika un materiālu projektu, kam ir apstiprināta projekta privilēģija. Jaunākais projekta vadītājs joprojām izpilda projekta tvērumu. Resursu pārvaldnieks pašlaik identificē konkrētus resursus, kuri tiks rezervēti darbam projektā. Projekta būtiskā rakstura dēļ projekta sponsors pieprasīja Vecāko projekta pārvaldnieku kā vienu no lomām. Resursu pārvaldniekam ir jāiegūst jaunais resurss un jādefinē loma sistēmā gadījumā, ja jaunākajam projekta pārvaldniekam projekta plānošanas laikā ir nepieciešama resursa informācija.

Tālāk minētajās darbībās parādīts, kā resursu pārvaldnieks var iestatīt vecākā projekta vadītāja lomu un ar to saistīt resursa raksturlielumus. Pēc tam lomu var izmantot, lai meklētu pieejamos resursus, kuri atbilst nepieciešamajām resursu kompetencēm.

1. Lapā **Lomu iestatīšana** atlasiet **Jauna** un ievadiet šādas vērtības:

    - **Lomas ID:** Vecākais projekta vadītājs
    - **Apraksts:** Vecākais projekta vadītājs

2. Atlasiet **Izveidot**.
3. Atlasiet lomu **Vecākais projekta vadītājs** un pēc tam atlasiet **Konfigurēt raksturlielumus**.
4. Laukā **Raksturlielumu veids** atlasiet **Prasme**.
5. Laukā **Pieejamie raksturlielumi** ievadiet meklējamo prasmi.
6. Laukā **Raksturlieluma veids** atlasiet **Sertifikāts**.
7. Laukā **Pieejamie raksturlielumi** ievadiet meklējamo sertifikāta veidu.

### <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1. Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.
2. Cilnē **Projekta komanda un plānošana** atlasiet **Pievienot**.
3. Laukā **Loma** atlasiet **Darba grupas dalībnieks**.
4. Atlasiet **Rezervēt no kalendāra**.
5. Lapā **Resursu pieejamība** atlasiet **Skatīt iestatījumus**.
6. Lapā **Pielāgot skata iestatījumus** ievadiet šādas vērtības:

    - **Datu diapazona skata formāts:** Diena
    - **Rādīt pieejamības aprakstus:** Jā
    - **Rādīt atlikušo noslodzi:** Jā

7. Resursu sarakstā atlasiet resursu.
8. Atlasiet **Stingrā rezervācija** un **Pilnā noslodze**.


### <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu, projekta vai resursa pārvaldnieki var sīkāk skatīt resursus, kurus var rezervēt projektam. Noklusējuma lomu varat saistīt ar esošu resursu vai nesen iegūtu resursu. Piemēram, kad tika nolīgts Daniels, viņam bija pieredze un prasmes biznesa analītiķa lomas pildīšanai. Resursu pārvaldnieks šo lomu piešķīra kā Daniela noklusējuma lomu. Tāpēc resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam ar projektiem.

Resursa rezervācijas laikā projektu pārvaldnieki var filtrēt darbam ar projektiem pieejamos lomu resursus. Šo informāciju viņi var izmantot kā vienu kritēriju, resursu izpildes laikā veicot daudzkritēriju lēmumu analīzi. Viņi var arī pievienot filtram citus resursa raksturlielumus, lai meklētu resursus, kam ir īpašas prasmes, izglītība un pieredze attiecībā uz konkrēto projektu.

**Scenārijs:** Tika sākts apstiprināts projekts, un projekta plānošanas posmā vecākā projekta vadītāja loma tika rezervēta kā plānots resurss. Resursu pārvaldnieks tagad ir ieguvis resursu, lai izpildītu vecākā projekta vadītāja lomu.

1. Lapā **Resursu saraksts** atlasiet **Daniels Goldšmits**.
2. Lapā **Resursa loma** atlasiet **Jauna** un ievadiet šādas vērtības:

    - **Stājas spēka:** Ievadiet pašreizējo datumu.
    - **Derīguma beigu datums:** Ievadiet **Nekad**.
    - **Loma:** Ievadiet **Vecākais projekta vadītājs**.

3. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
4. Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.

## <a name="set-up-role-based-pricing"></a>Iestatīt lomā balstītas cenas
Lomām var iestatīt visas izmaksu, pārdošanas un pārsūtīšanas cenas.

1. Lapā **Pārdošanas cena (stunda)** atlasiet **Jauna** un ievadiet spēkā stāšanās datumu.
2. Kolonnā **Loma** atlasiet lomu.
3. Kolonnā **Cena** ievadiet atlasītās resursu lomas cenu.

## <a name="form-a-project-team"></a>Projekta komandas izveide
Lai izmantotu projektā iepriekš iestatītās lomas, projekta vadītājam šīs lomas ir jāsaista ar projektu. Projektam var piešķirt vairākas lomas. Lai izvairītos no pārpratumiem, šīs lomas rezervācijas laikā tiek automātiski apzīmētas. Piemēram, ja projekta vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs programmatūras inženieru lomas, kurām ir etiķetes **programmatūras inženieris 1**, **programmatūras inženieris 2** un **programmatūras inženieris 3**. Ja lomai tika iepriekš iestatīti lomu raksturlielumi, tās resursa meklēšanas laikā tiek piemērotas kā filtrs. Lai precizētu meklēšanu, var pievienot papildu raksturlielumus.

Lai nodrošinātu labāku skatu uz resursu pieejamību, var arī pielāgot skatīšanas iestatījumus. Ir pieejamas opcijas rādīt stundas, dienas, nedēļas, mēneša, ceturkšņa un gada pieejamību. Ir arī opcija rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībā, ja aprēķināt darbībām pieejamo laiku vai resursu pieejamību.

Projekta vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst prasībai, atlasīt rezervēt resursu lomas izpildei. Ņemiet vērā, ka šajā plānošanas posma brīdī resursi jārezervē. Izveidojot WBS, varat aizstāt lomas ar projekta personāla resursiem. Ja lomas WBS aizstāj ar personāla resursiem, resursa iestatījums automātiski atjaunina projekta darba grupu sarakstu un plānu.

[![Projekta darba grupu uzskaitījums, kas ietver gan lomas, gan faktiskos resursus](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekta vadītājam ir dažādas opcijas resursa rezervēšanai projektam, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes daļa** un **Konkretizēt laiku**. Šīs rezervācijas opcijas var atcelt jebkurā laikā, ja resursu piešķires mainās. Tiek atbalstītas divu veidu rezervācijas:

- **Stingrā rezervācija** — Resursa rezervācija tika apstiprināta darbam ar iesaisti uz konkrēto ilgumu.
- **Vieglā rezervācija** — Resursa rezervācijas tika provizoriski iestatītam darbam ar iesaisti uz konkrēto ilgumu.

Šajā procedūrā paskaidrots, kā izveidot projekta komandu.

### <a name="create-a-project-team"></a>Projekta komandas izveide

1. Saraksta lapā **Visi projekti** atlasiet projektu un pēc tam atlasiet **Rediģēt**.
2. Lauka **Plānot beigu datumu** cilnē **Projekta komanda un plānošana** ievadiet grafika sākuma datumu, pieskaitot vienu mēnesi. Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.
3. Atlasīt **Pievienot**.
4. Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Vecākais projektu vadītājs**.
5. Atlasiet **Nepieciešamās kompetences**.
6. Lapā **Izvēlieties raksturlielumus** pēc noklusējuma tiek atlasīti raksturlielumi, kurus iepriekš iestatījāt vecākā projektu vadītāja lomai. Atlasiet **Labi**.
7. Lauka **Resursu skaits** lapā **Pievienot projektam lomas** ievadiet **1**.
8. Laukā **Resurss** uzmeklēšana rāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Daniels Goldšmits** un pēc tam atlasiet **Izveidot**.
9. **Projekta** lapā atlasiet **Pievienot**.
10. Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Darba grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Atlasiet **Izveidot**.
12. Lapā **Projekti** atlasiet **Izpildīt resursu**.

## <a name="resource-capacity-synchronization"></a>Resursa noslodzes sinhronizēšana
Resursa sinhronizēšanas procesi palīdz nodrošināt, ka kalendāra un bāzes kalendāra informācija nonāk projekta resursa plānošanā. Ja kalendārs ir mainīts, procesi veic nepieciešamos projekta resursu plānošanas atjauninājumus. Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursa informācija tiek iepriekš sinhronizēta. Tāpēc resursa plānošanas informācijas atjauninājumi tiek veikti ātrāk. Mēs jums iesakām plānot procesus kā paketi, nevis pa vienam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs iekļaujošos datumus, kuros informācija pēdējo reizi tika sinhronizēta. Ja iekļaujošie datumi netiek lietoti, datumu sinhronizācijas laikā var rasties atstarpes.

![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizējiet resursa noslodzes apkopojumus

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursa kalendāra informāciju. Šī informācija ietver bāzes kalendāra informāciju par jebkādām izmaiņām, kas veiktas projekta resursa kalendāra noslodzes tabulā. Ja projektam tiek pievienoti jauni resursi, sinhronizācija palīdz nodrošināt, ka ir pieejama atjaunināta informācija par kalendāru. Šo sinhronizāciju var veikt jebkurā laikā.

Mēs iesakām lietot paketi. Opcijas ir pieejamas noslodzes rezervāciju sinhronizācijas laikā.

1. Atlasiet **Projekta pārvaldība un uzskaite** &gt; **Periodiski** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.
2. Iestatiet opcijas no šīs tabulas.

    | Opcija      | Apraksts |
    |-------------|-------------|
    | Perioda kods | Ja vēlaties, atlasiet virsgrāmatas datuma intervāla kodu, lai iestatītu sākuma un beigu datumus resursu noslodzes apkopojumu sinhronizācijas procesam. |
    | Sākuma datums  | Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa sākuma datumu. |
    | Beigu datums    | Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa beigu datumu. |

[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Lomu iestatīšana WBS veidnēs
Projekta vadītāji var iestatīt WBS veidnes, kuras viņi var lietot, veidojot WBS jauniem projektiem. Veidnes izveides laikā projektu vadītāji var pievienot lomas. Lai WBS veidnei piešķirtu lomu, izmantojiet šādu procedūru.

1. Atlasiet **Projektu vadība un uzskaite** &gt; **Iestatīšana** &gt; **Projekti** &gt; **Darba sadalījuma struktūras veidnes**.
2. Atlasiet atlasītās WBS veidnes **Informāciju**.
3. Sarakstā atlasiet uzdevumu un pēc tam laukā **Loma** atlasiet lomu, kuru piešķirt uzdevumam.

### <a name="work-with-a-wbs"></a>Darbs ar WBS

Varat izveidot jaunu WBS vai varat nokopēt WBS no esošas WBS veidnes. Projekta vadītājs var viegli pārvaldīt resursus, piešķirot lomas jauniem WBS uzdevumiem. Lomas var aizstāt vai nu pēc tam, kas resurss ir iegūts, vai pēc tam, kad darbam ar uzdevumu ir identificēts apstiprināts resurss. Šāda elastība ļauj projektu vadītājiem veikt šādus uzdevumus:

- Identificēt to resursu skaitu, kuri ir nepieciešami WBS darba pakotnēm.
- Aprēķināt projekta izmaksas.
- Noteikt provizorisko budžetu.
- Aprēķināt darbības ilgumu, pamatojoties uz lomām un resursiem.
- Izstrādāt projekta vadības plānus, pamatojoties uz pieejamo projekta informāciju.

WBS ir pievienotas papildu opcijas, lai labāk izmantotu resursu plānošanas funkcionalitāti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resursu piešķīrumi</td>
<td>Skatiet WBS uzdevumiem piešķirtos resursus, datumus, stundu skaitu un rezervācijas veidu.</td>
</tr>
<tr class="even">
<td>Darba grupas automātiska ģenerēšana</td>
<td>Automātiski pievienojiet plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Finance automātiski iesaka plānotos resursu, izmantojot daudzkritēriju lēmumu analīzi, kas ir balstīta lomās. Pēc tam, kad WBS uzdevumiem ir iestatītas lomas un darbs (stundās) un pēc struktūras izlaišanas atlasiet <strong>Automātiski ģenerēt darba grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS un cilnei <strong>Projekta un darba grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri</strong> varat atlasīt resursus stingrajai vai vieglajai rezervēšanai, pamatojoties uz norādīto ilgumu. Varat pielāgot skatīšanas iestatījumus, lai redzētu un iestatītu resursu darbību ilgumu. Varat atlasīt un piešķirt resursus darba pakotnes līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Piekrist</strong> – Apstipriniet uzdevumam piešķirta resursa izmaiņas.</li>
<li><strong>Atcelt</strong> – Atceliet uzdevumam piešķirta resursa izmaiņas.</li>
<li><strong>Piešķirt automātiski</strong> — Pieejamais personāla resurss, kuram ir atbilstoša loma, tiek automātiski atlasīts un piešķirts atlasītajam uzdevumam.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.
2. Atlasiet **Plāns** &gt; **Darbības** &gt; **Darba sadalījuma struktūra**.
3. Atlasiet **Jauns**, lai WBS pievienotu šādas pirmā līmeņa darbības:

    - Uzsākšana
    - Plānošana
    - Tiek izpildīts
    - Pārraudzība un vadība
    - Slēgt

4. Iestatiet datumus un darbu (stundās), kā parādīts šajā ilustrācijā.

    [![Datumu un darba iestatīšana](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Atlasiet **Uzsākšanas** uzdevuma rindu un pēc tam laukā **Loma** atlasiet **Vecākais projekta vadītājs**.
6. Atlasiet **Publicēt**.
7. Šīs pašas rindas laukā **Resurss** atlasiet **Daniels Goldšmits** un pēc tam atlasiet **Piekrist**.
8. Atlasiet **Plānošanas** uzdevuma rindu un pēc tam laukā **Loma** atlasiet **Biznesa analītiķis**.
9. Atlasiet **Publicēt** un pēc tam atlasiet **Automātiski ģenerēt komandu**.
10. Parādītajā ziņojuma lodziņā atlasiet **Jā**.
11. Laukā **Resurss** apstipriniet, ka vērtība ir **Biznesa analītiķis 1**.
12. Resursam **Biznesa analītiķis 1** atveriet uzmeklēšanu un atlasiet **Palaist resursu piešķires**. Pēc tam atlasiet uzdevuma darbinieku.
13. Atlasiet **Vieglā piešķire** &gt; **Pilnā noslodze**.

    > [!NOTE] 
    > Jūs nesaņemat brīdinājumu, ka norādītais resurss tagad ir 2, jo resursa numurs joprojām ir 1.

14. **Darba sadalījuma struktūras** lapā pārbaudiet resursa piešķiri WBS un pēc tam atlasiet **Saglabāt**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resursa izpilde plānotiem resursiem
Projekta vadītājs var plānot projektam nepieciešamās resursu lomas. Resursu pārvaldnieks redzēs šos plānotos resursus kā pieprasījumus lapā **Resursa izpilde** un varēt piešķirt faktiskos resursus.

1. Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.
2. Atlasiet **Projekts** un pēc tam atlasiet **Rediģēt**.
3. Cilnē **Projekta komanda un plānošana** atlasiet **Pievienot**.
4. Dialoglodziņā **Pievienot lomas** atlasiet lomu **Programmatūras izstrādātājs**.
5. Atlasiet **Izveidot** un pēc tam aizveriet projekta lapu.
6. Lapā **Resursa izpilde** atlasiet **Programmatūras izstrādātājs 1** projektam **XYZ jaunināšanas projekta fāze 2**.
7. Atlasiet darbinieku un pēc tam atlasiet **Piešķirt**.
8. Pārbaudiet, vai **Programmatūras izstrādātāja 1** rinda ir noņemta projektam **XYZ jaunināšanas projekta fāze 2**.
9. Cilnē **Projekta darba grupa un plānošana** projektam **XYZ jaunināšanas fāze 2** pārliecinieties, ka iepriekšējā darbībā atlasītais darbinieks ir pievienots kā **Programmatūras izstrādātājs**.

## <a name="requests-for-project-resources"></a>Projekta resursu pieprasījumi
Projekta resursa plānošanas funkcionalitāte tikai ļauj resursu pārvaldniekiem izplatīt personāla resursus iesaistēm vai projektiem. Lai iespējotu šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārbaudiet, vai tie ir izpildīti:

- Iestatiet numuru secības.
- Iestatiet projekta vadības un uzskaites darbplūsmas.
- Iespējojiet resursa pieprasījumu darbplūsmas.

Pēc tam, kad ir izpildīti iepriekšējie uzdevumi, jūs varat pēc nepieciešamības izpildīt šādus uzdevumus:

- Izveidot resursa pieprasījumu no vieglās rezervācijas resursa.
- Uzraudzīt resursu pieprasījumus.
- Izpildīt resursu pieprasījumus.
- Pieprasīt personāla resursu no WBS.
- Rezervēt resursus projektam bez personāla resursa pieprasīšanas.

## <a name="monitor-project-teams"></a>Projekta darba grupu uzraudzība
1. Lapā **Visi projekti** atlasiet projekta **XYZ jaunināšanas fāze 2** saiti **Projekta ID**.
2. Kopsavilkuma cilnē **Projekta komanda un plānošana** pārbaudiet, vai uzskaitītie projekta resursi ir pareizi.
