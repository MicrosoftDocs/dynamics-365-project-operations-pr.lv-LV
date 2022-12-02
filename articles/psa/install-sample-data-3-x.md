---
title: Parauga datu instalācija
description: Šajā rakstā ir sniegta informācija par datu parauga instalēšanu pakalpojumā Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 8fb3854c139125abbf499622d048e2ff0791516a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926785"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Lietojumprogrammas Project Service datu parauga instalēšana

[!include [banner](../includes/psa-now-project-operations.md)]

Lai palīdzētu jums izveidot savu izmēģinājumversijas vidi, Microsoft nodrošina lejupielādējamas datu paketes, kas demonstrē jūsu lietotņu iespējas. Ir pieejami divi datu paraugu pakotņu veidi:
- atsauc./iestat. dati
- demonstr. dati (atsauces/iestat. un darbību dati, piem., darba uzd. un projekti)

**Atsauc.** datu paraugu pakotnes var lejupiel., izmantojot 3 daž. pakotnes, tāpēc varat instalēt tikai progr. Project Service vai tikai Field Service paredzētos datus vai vienlaikus instalēt abām progr. paredzētos datus.

Tālāk ir norād. iestat./ats. datu par. pak.

- [**V902PSMasterData** — tikai Project Service versijai 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** — tikai Field Service versijai 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** — Field Service 8.x un Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Jaunākā **demonstr.** datu pak. ir:

 - [**FPSDemoData** - Field Service 8.x un Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Instal. norād. nedaudz atšķiras lietot., lai izveidotu un konfigurētu sadaļu, bet pārējie norād. ir tādi paši kā iepriekš. [**emuāra ierakstā**](https://aka.ms/fpsdemodatablog). Šajā pakotnē ir samazin. demonstr. datu kopa, un tās instalēš. aizņem aptuveni 3 stundas.

Šīs datu paraugu pakotnes ir pieejamas tikai angļu valodā.

> [!IMPORTANT]
> **Datu paraugu nevar nekādā veidā atinstalēt.** Šīs pakotnes drīkst instalēt tikai demonstrācijas, novērtēšanas, apmācības vai izmēģinājuma sistēmās. Ņemiet vērā arī to, ka pēc vienas atsevišķās pakotnes instalēšanas nevar instalēt otru atsevišķo pakotni. (Citiem vārdiem sakot, nevarat instalēt pakotni **FSMasterData** un pēc tam pakotni **PSMasterData** vai pretēji.) Ja jums šķiet, ka kaut kad vēlāk jums būs vajadzīgi abu lietojumprogrammu datu paraugi, instalējiet pakotni **v902FPSMasterData**.

Instalējot jebkuru no datu paraugu pakotnēm, instalēšanas procesa laikā tiek veiktas tālāk norādītās darbības.

- Tiek izveidoti vai iestatīti Project Service, Field Service vai abu lietojumprogrammu (ja tas ir attiecināms) lietošanas noklusējuma parametri.

- Tiek importēti lietojumprogrammu datu paraugi, piemēram, rezervējamie resursi, lietojumprogrammai raksturīgās lomas, pārdošanas un izmaksu cenu saraksti, organizācijas struktūrvienības, pārdošanas procesa ieraksti un citas entītijas, kas sniedz iespēju demonstrēt galvenās iespējas.  

Kopā ar **demonstr. datu** pakotni saņemat minētos un papildu darbību datus, piemēram, darba uzdevumus un projektus.

Vai vēlaties uzzināt, kādas iespējas varat demonstrēt, izmantojot datu paraugu? Sk. sadaļā [Tehn. piez.](#technical-notes) aprakstīto Fabrikam Robotics fiktīvo scen.

Ja jums ir jautājumi par šo datu paraugu pakotņu instalēšanu, [rakstiet mums uz e-pasta adresi fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Prasības

Instalēšanas protokols pieņem, ka jūsu mērķa instance (organizācija) atbilst tālāk norādītajām prasībām.

- Pamatval. ir angļu val., un pamatvalūta ir ASV dolāri (USD, $).

- Organiz. vēl nav Project Service vai Field Service datu vai ir tikai pam. noklus. dati, kas tiek nodroš. visām jaunām organ.

- Jau ir instalēta pareizā biznesa lietojumprogrammas versija, kā tas ir norādīts tālāk.
       
    - **FPSDemoData vai v902FPSMasterData:** organizācijai ir instal. Field Service vers. 8.x un Project Service vers. 3.x.

    - **Pakotnei v902PSMasterData:** organizācijai ir instalēta Project Service versija 3.x.

    - **Pakotnei v902FSMasterData:** organizācijai ir instalēta Field Service versija 8.x.

> [!NOTE]
> Ja datu paraugs ir jāinstalē esošā Project Service un Field Service izmēģinājumversijas vai demonstrācijas vidē, kurā jau ir dati (nav ieteicams), ir jāaiztur instalēšanas programmas veiktās drošības priekšpārbaudes. Papildinformāciju skatiet tālāk esošajā sadaļā “Tehniskās piezīmes”.

## <a name="prepare-for-installation"></a>Sistēmas sagatavošana instalēšanai

Instalēšanas programma ir jāpalaiž datorā, kurā tiek darbināta nesen izlaista Windows versija (vēlams Windows 10).

Ņemiet vērā, ka instalēšana ilgst līdz **1 stundai** **iestat./atsauc. datiem** un šajā laikā datoram ir jābūt pievienotam tīklam. (Parasti instalēšanai nepieciešamas aptuveni 30 minūtes **FPSMasterData** pakotnei, kas ietver datu paraugu abām programmām.) Pakotnei **FPSDemoData** instalēšana ilgs aptuveni **3 stundas**.

Datorā ir jābūt izslēgtai ekrānsaudzētāja funkcijai. Pretējā gadījumā ekrānsaudzētāja aktivizēšanas brīdī var tikt zaudēti instalēšanas sesijas akreditācijas dati (ja vien sesija nav aktīva visa procesa laikā).

> [!div class="mx-imgBorder"]
> ![Ekrānuzņēmums: ekrānsaudzētāja iestatījumi, kurā ir izslēgts ekrānsaudzētājs.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Lejupielāde un pakotnes atvēršana

Project Service un Field Service datu parauga instalēšanas programma tiek izplatīta pašizvilces izpildāmā faila formātā. Failu nosaukumi var atšķirties atkarībā no datu parauga pakotnes, taču citādi visu pakotņu instalēšanas darbības ir vienādas.

Pēc pakotnes lejupiel. palaidiet .exe failu un tad piekrītiet noteik. un nosac., lai atvērtu tilpsasp. faila pak. Pēc tam šī faila saturs ir jāizvelk kādā no datorā esošajām mapēm.

Atkarībā no operētājsistēmas un drošības iestatījumiem pēc tilpsaspiestā faila pakotnes atvēršanas, iespējams, ir jāveic tālāk norādītās darbības.

1. Atrodiet failu **FPSDemoData.dll** mapē **v902FPSMasterData** / **PackageDeployer_FPSDemoData** un veiciet dubultkl.

2. Izvēlieties vienumu **Atbloķēt**.

3. Atlasiet vienumu **Lietot**.

4. Atlasiet **Labi**.


## <a name="create-or-configure-users"></a>Lietotāju izveide vai konfigurēšana

**FPSDemoData** pakotnei vajag 6 lietot., savukārt **FPSMasterData** pakotnei vajag 1 lietot. Izvēlieties pareizo parauga datu pakotni.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Izveid. vai konfig. lietot. — iestat./atsauc. datu pak.

Pakotne **FPSMasterData** ir paredzēta instalēšanai sistēmā ar vienu lietotāju Spencer Low un tālāk norādītajiem iestatījumiem. Lai pareizi instalētu pakotni, jums jārada (vai īslaicīgi jāpārdēvē) lietotāji savā vidē, lai tie atbilstu ienākošā parauga datu konfigurācijai.

Lai izveidotu vai konfigurētu lietotājus, pārejiet uz sadaļu **Iestatījumi** > **Drošība** > **Lietotāji** un veiciet tālāk norādītās darbības.

1. Lietotājam ar parametru UserFullname=“Spencer Low” un lietotājvārdu spencerl (**ar mazajiem burtiem**) iestatiet lomas Projekta vadītājs un Prakses pārvaldnieks.

2. Atlasiet lietotāju **Spencer Low** un pēc tam atlasiet vienumu **Pārvaldīt lomas**. Atrodiet un atlasiet lomu **Sistēmas administrators** un pēc tam atlasiet vienumu **Labi**, lai piešķirtu lietotājam Spencer Low visas administratora tiesības. Šī darbība ir nepieciešama, lai nodrošinātu, ka izveidotajiem ierakstu paraugiem ir pareizs lietotāja īpašumtiesību iestatījums un tādējādi tiek pareizi aizpildīti skati.

3. Lejupielādētajā pakotnē jums ir jāatjaunina datu kartēšanas fails, izmantojot noklusējuma lietotāju konteksta e-pasta adreses. Lai to izdarītu, atveriet mapi **PkgFolder**, atrodiet failu **ImportUserMapFile.xml** un pēc tam atveriet to Notepad (vai Visual Studio, vai citā XML redaktorā). Kā lauka **DefaultUserToMapTo=** vērtību iestatiet lietotāja Spencer Low e-pasta adresi.

4. Ja neizmantojat lietotāju Spencer Low ar lietotājvārdu **spencerl**, ir jāatjaunina vēl viens fails. Atveriet failu **DemoDataPreImportConfig.xml** un pēc tam atrodiet tagu **userstocreateandconfigure**. Atjauniniet tagu **\<login\>**, izmantojot Spencer Low lietotāja lietotājvārdu. Papildinform. skatiet: [Tehniskās piezīmes](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Lietot. izveide/konfig. — demonstr. datu pak.

Demonstr. datu pak. vajag 6 lietotājus. Lai pakotni instalētu pareizi, veiciet šādas darbības:

 1. Izveidojiet vai īslaicīgi pārdēv. esošos lietot. atbilstoši ienākošo parauga datu konfig., atverot **Iestat.** > **Droš.** > **Lietotāji**.
 
    Šīs lomas vajag tikai uz pers. balstītām demonstr.  
    - User Fullname=“DavidSo” kā Field Service tehn. spec.   
    - User Fullname=“Jamie Reding” kā Customer Service un Field Service dispečers   
    - User Fullname=“Molly Clark” kā uzņēm. pārv.   
    - User Fullname=“Spencer Low” kā darbību un projektu pārv.  
    - User Fullname=“Veronica Quek” kā gr. dalībn.   
    - User Fullname=“William Contoso”
  
2. Demonstr. datu import. ietvaros piešķiriet minētajiem 6 lietot. admin. lomu, lai ierakstu paraugi tiktu pareizi importēti. 

3. Atv. **PkgFolder**, tad atrodiet un atv. **ImportUserMapFile.xml**. Atjauniniet laukus **New=** ar attiecīgo lietotāju e-pasta adresēm jūsu sistēmā.

   > [!div class="mx-imgBorder"]
   > ![UserMapFile ekrānuzņēmums.](media/sample-data-7.png)

4. Ja lietotājam ar pilno vārdu “Spencer Low” ir cits lietotāja ID, nevis **“spencerl”**, tad ir jāatjaunina papildu fails. Atv. **DemoDataPreImportConfig.xml** un atrod. tagu **userstocreateandconfigure**. Atjauniniet tagu **\<login\>** ar loginId (reģistrjutīgs). 

5. Pirmā lietot. kalendāru (tagā **userstocreateandconfigure**) izmanto, lai aizpildītu darba st. visiem rezervējamiem resurs., importējot demonstr. datus. Atv. **Iestatījumi** > **Drošība** > **Lietotāji**, atrodiet lietot. “Spencer Low” un atv. opciju “Darba stundas”. Rediģējiet esošās darba st., atlasot opciju **Viss periodiskais iknedēļas grafiks no sākuma līdz beigām**. **Darba st. jābūt iestat. 8.00–17.00 (9 st.), no pirmd. līdz piektd., un laika joslai jābūt iest. Klusā ok. laiks (ASV un Kanāda)**. Tas jādara, lai pareizi parādītu projektu un plānošanas paneli.

**Ieteikums.** Apsveriet iespēju tagad izveidot savas organizācijas dublējumu, ko izmantot gadījumā, ja datu parauga instalēšana neizdodas un ir jāatjauno sākotnējais stāvoklis. Papildinformāciju skatiet rakstā [Instanču dublēšana un atjaunošana](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Palaist Package Deployer

1. Atr. un pal. failu **PackageDeployer.exe** mapē **v902FPSMasterData** VAI **PackageDeployer_FPSDemoData**.

2. Piekrītiet noteikumiem un nosacījumiem.

3. Nākamajā logā

   a. Atlasiet izvietošanas tipu **Office 365**.

   b. Izmantojiet tā sistēmas administratora lietotājvārdu un paroli, ko konfigurējāt, izpildot sadaļā “Lietotāju izveide vai konfigurēšana” sniegtos norādījumus (lietotājs Spencer Low ar lietotājvārdu spencerl).

   c. Pārliecinieties, vai ir atzīmēta izvēles rūtiņa **Rādīt pieejamo organizāciju sarakstu**.

      > [!div class="mx-imgBorder"]
      > ![Package Deployer ekrānuzņēmuma logs, kurā ir atlasīts “Rādīt pieejamo organizāciju sarakstu”](media/sample-data-2.png)

4. Atlasiet organizāciju, kurā vēlaties instalēt datu paraugu.

5. Atlasiet vienumu **Tālāk**, līdz tiek parādīts dialoglodziņš **Demonstrācijas datu iestatīšana**.

   > [!div class="mx-imgBorder"]
   > ![Ekrānuzņēmums: demonstrācijas datu instalēšanas programmas statusa logs.](media/sample-data-3.png)

6. Pirms turpināšanas ņemiet vērā, ka datu parauga instalēšana var ilgt līdz vienai stundai (parasti ~10 minūtes). Jums ir jānodrošina, lai dators būtu ieslēgts un savienots ar tīklu visa instalēšanas procesa laikā un netiktu deaktivizēta jūsu sesija.   

7. Kad viss ir sagatavots, noklikšķiniet uz **Tālāk**, lai sāktu datu parauga instalēšanas procesu. Pēc datu parauga ielādes noklikšķiniet uz **Pabeigt**.

## <a name="verify-the-sample-data-installation"></a>Datu parauga instalēšanas pārbaude

Lai veiktu atbilstības pārbaudi, pārliecinieties, vai ierakstu skaits un entītiju tipi atbilst Fabrikam Robotics fiktīvā scenārija datiem.

Kad datu paraugs ir pilnībā ielādēts, pierakstieties kā lietotājs Spencer Low un pārliecinieties par tālāk norādīto.

- Ja ir instalēta lietojumprogramma Project Service, pārejiet uz sadaļu **Project Service** > **Iestatījumi** > **Cenrāži**. Pārliecinieties, vai pastāv rēķinu likmes un izmaksu likmes katrai datu kopā ietvertajai valstij/reģionam atbilstošajā valūtā.

- Ja ir instalēta programma Project Service, dodieties uz **Universal Resource Scheduling** > **Iestatījumi** > **Organizatoriskās vienības**. Pārliecinieties, vai ar katru organizācijas struktūrvienību (izņemot pilsētu ierakstus) ir saistīts izmaksu cenrādis atbilstošajā valūtā. Ja kāda trūkst, atrodiet un piesaistiet pareizo izmaksu cenrādi.

- Ja ir instalēta lietojumprogramma Field Service, pārejiet uz sadaļu **Project Service** > **Iestatījumi** > **Cenrāži**. Pārliecinieties, vai pastāv rēķinu likmes un izmaksu likmes. Pārejiet uz sadaļu **Field Service** > **Iestatījumi** > **Cenrāži** un pārbaudiet, vai pastāv rēķinu likmes un izmaksu likmes katrai datu kopā ietvertajai valstij/reģionam atbilstošajā valūtā.

  > [!div class="mx-imgBorder"]
  > ![Ekrānuzņēmums: aktīvie cenrāži.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Ekrānuzņēmums: aktīvās organizācijas struktūrvienības.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tehniskās piezīmes

Tālāk ir sniegta tehniskā papildinformācija par šo datu instalēšanu.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Datu paraugu instalēšana vidē ar esošiem datiem (nav ieteicams)

Ja datu paraugs ir jāinstalē esošā Field Service vai Project Service izmēģinājumversijas vai demonstrācijas vidē, kurā jau ir dati, ir jāaiztur instalēšanas programmas veiktās drošības priekšpārbaudes.

Lai to izdarītu, pārejiet uz mapi **PkgFolder**, atrodiet failu **DemoDataPreImportConfig.xml** un atveriet to programmā Piezīmjbloks (vai citā XML redaktorā).

Atrodiet tālāk norādīto vērtību un mainiet iestatījumu no true uz false.

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Šīs izmaiņas izraisa to, ka instalēšanas programma izlaiž dažas svarīgas drošības pārbaudes, tostarp tālāk norādītās.

- Pārbaude, vai ir ne vairāk kā viens aktīvs tipa **Organizācijas struktūrvienība** ieraksts, un tā pārdēvēšana par **Fabrikam US**.

- Pārbaude, vai ir ne vairāk kā viens aktīvs tipa **Darba veidne** ieraksts.

- Pārbaude, vai ir ne vairāk kā viens aktīvs tipa **Projekta parametrs** ieraksts, un šī ieraksta pārdēvēšana par **Parametri**.

### <a name="configuration-components"></a>Konfigurācijas komponenti

Šajā pirmsimportēšanas konfigurācijas failā ir ietverti vairāki citi konfigurācijas komponenti. Tostarp tālāk norādītie, kas ir paredzēti lietotājiem ar tehniskajām zināšanām.

- **\<RequiredSolutions\>**: tiek norādīti iepriekš instalējamie risinājumi un to versiju numuri.

- **\<InstallSampleData\>** kontrolē, vai tiek instalēti papildu parauga datu paraugi.

    - False — šie iebūvētie dati (kas ir noņemami) netiek instalēti.

    - True — vienlaikus ar FS un PSA datu paraugiem tiek instalēti iebūvētie dati.

- **\<PreImportDataCollection\>**: tiek norādīti atsevišķa faila datu kartējumi un saistītie ieraksti, kas ir jāimportē pirms galvenā datu parauga instalēšanas procesa.

- **\<EntitiesToEnableScheduling\>** nosaka, kuras entītijas ir jāiespējo rezervēšanai Microsoft Dynamics Scheduling (sauktai arī par Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>**: tiek norādīti rezervējamie resursi, kas tiks izveidoti (ja tie vēl nepastāv) pirms datu parauga importēšanas izpildes. Ņemiet vērā, ka katra avota sist. datu parauga rezervējamā resursa ieraksta param. FullName un login atbilst mērķa sist. rezervējamā resursa ieraksta param. Tāpēc šajā priekškonfigurācijas failā nevar mainīt vārdus, ja vien iepriekš neimportējat datu paraugu mērķa sistēmā, izmantojot šos vārdus, pēc tam nepārdēvējat rezervējamos resursus un iespējoto lietotāju ierakstus, izmantojot vēlamo vārdu kopu, un pēc tam vēlreiz neeksportējat datus importēšanai galamērķa sistēmā (atbilstošā veidā atjauninot **ImportUserMapFile.xml** vecos un jaunos ierakstus).

- **\<PluginsToDisable\>**: tiek norādīti atsevišķi rindas elementu spraudņi, kas ir jāatspējo datu parauga importēšanas laikā un pēc tam atkal jāiespējo.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics fiktīvais scenārijs

Instalējot Field Service un Project Service atsauces datu paraugu pakotnes, tiek instalēts **Fabrikam ražošanas galveno datu (v3.0.0.0) risinājums**, kā arī aptuveni 4000 ierakstu un aptuveni 40 dažādas entītijas. Atsevišķajā Field Service vai Project Service datu parauga pakotnē ir ietverta attiecīgajai lietojumprogrammai paredzēta pakotnes **v902FPSMasterData** datu parauga apakškopa. **Demonstrācijas datu** pakotne instalē **Fabrikam ražošanas demonstrācija datu (v3.0.0.7) risin.** ar aptuveni 22 000 ierakstu visām 148 entītijām.

Fiktīvais uzņēmums Fabrikam Robotics ražo elektroierīču montāžas līnijas robotus un ir slavens ar produktu kvalitāti, inovācijām un lielisku klientu apkalpošanu, tostarp uzstādīšanas plānošanas, ieviešanas un turpmākās apkopes pakalpojumiem. Uzņēmuma Fabrikam centrālais birojs atrodas ASV (Fabrikam US), un tam ir projektu tipa pakalpojumu sniegšanas centri Francijā, Indijā, Apvienotajā Karalistē un Šveicē.

Vietas pakalpojumu sniegšanas centri atrodas ASV, pārsvarā lielākajā Sietlas apgabalā. Uzņēmuma mērķis ir izmantot lietiskā interneta (IoT) savienojamību, lai pārraudzītu klientu līdzekļu veiktspēju un sniegtu aizvien proaktīvākus pakalpojumus ekspluatācijas vietā.

Tālāk ir sniegts datu paraugu augsta līmeņa pārskats.

- Kopīgie datu paraugu elementi (ietverti abām lietojumprogrammām)

    - 1 lietotājs

    - 71 uzņēmums

    - 137 kontaktpersonas

    - Dažādi transakciju tipi un kategorijas

    - 50 produkti ar 1 produktu cenrādi

    - 14 cenrāži/izmaksu saraksti

    - 31 īpašība (resursu prasme) 2 vērtēšanas modeļos ar 3 līmeņiem (vērtēšanas vērtībām)

- Project Service

    - 8 organizācijas struktūrvienības

    - 6 lomai raksturīgi izmantošanas līmeņi

    - Vairāk nekā 2,8 000 lomas cenas specifikāciju

- Field Service

    - 4 teritorijas

    - 5 darba pasūtījumu tipi

    - 22 klienta līdzekļi

    - 9 incidentu tipi ar vairākām saistītajām resursu īpašībām (9), pakalpojumiem (13) un pakalpojumu uzdevumiem (13).
   
**Demonstrācijas datu** pakotne instalē aptuveni 179 darba pasūtījumus, 12 projektus un saistītos darbību datus. 

### <a name="change-the-work-hours-for-sample-resources"></a>Resursu paraugu darba stundu maiņa

Pēc nokl. visiem rezervēj. resurs. ir iest. 24 darba st. kalend.

Ja ir jāmaina rezervējamo resursu paraugu darba stundas, dodieties uz **Universal Resource Scheduling** > **Plānošana** > **Resursi**.

Atlasiet lietotāju (piemēram, Spencer Low) un mainiet šī lietotāja darba stundas, izmantojot iestatījumu, ko vēlaties lietot vairākiem lietotājiem. Dodieties uz **Universal Resource Scheduling** > **Iestatījumi** > **Darba stundu veidnes** un rediģējiet ierakstu **Noklusējuma darba veidne**. Laukā **Veidnes resurss** atlasiet lietotāju, kura darba stundu iestatījumu vēlaties lietot citiem resursiem. Dodieties uz **Universal Resource Scheduling** > **Plānošana** > **Resursi** > **Aktīvie rezervējamie resursi**. Atlasiet resursus, kurus vēlaties mainīt, un pēc tam atlasiet vienumu **Iestatīt kalendāru**. Nolaižamajā sarakstā **Darba veidne** atlasiet veidni **Noklusējuma darba stundas** vai citu veidni, kurā ir ietvers vajadzīgais veidnes resurss. Tagad plānošanas panelī resursiem tiek rādītas atjauninātās darba stundu vērtības.

> [!div class="mx-imgBorder"]
> ![Ekrānuzņēmums: aktīvie rezervējamie resursi.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]