---
title: Jaunināšana no projektu pakalpojumu automatizācijas uz projekta operācijām
description: Šajā tēmā sniegts pārskats par jaunināšanas procesu no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626740"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Jaunināšana no projektu pakalpojumu automatizācijas uz projekta operācijām

Mēs esam priecīgi paziņot par pirmo no trim posmiem, lai uzlabotu no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations. Šī tēma sniedz pārskatu klientiem, kuri uzsāk šo aizraujošo ceļojumu. Turpmākās tēmas ietvers izstrādātāju apsvērumus un detalizētu informāciju par līdzekļu uzlabojumiem. Tie ne tikai sniegs norādījumus, kas palīdzēs sagatavoties jaunināšanai uz projekta operācijām, bet arī paskaidros, ko varat sagaidīt pēc jaunināšanas.

Jaunināšanas piegādes programma tiks sadalīta trīs posmos.

| Jaunināšanas piegāde | 1. posms (2022. gada janvāris) | 2. posms (2022. gada aprīļa vilnis) | 3. posms  |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu darba sadalījuma struktūras (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS pašlaik atbalstīto projektu operāciju robežās | | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem projekta operāciju ierobežojumiem, tostarp projekta darbvirsmas klienta atbalsta | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Jaunināšanas procesa līdzekļi 

Jaunināšanas procesa ietvaros vietnes kartei esam pievienojuši jaunināšanas žurnālus, lai administratori varētu vieglāk diagnosticēt kļūmes. Papildus jaunajam interfeisam tiks pievienoti jauni validācijas noteikumi, lai nodrošinātu datu integritāti pēc jaunināšanas. Jaunināšanas procesam tiks pievienotas šādas pārbaudes.

| Apstiprinājumu | 1. posms (2022. gada janvāris) | 2. posms (2022. gada aprīļa vilnis) | 3. posms  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS tiks validēta pret bieži sastopamiem datu integritātes pārkāpumiem (piemēram, resursu piešķires, kas ir saistītas ar vienu un to pašu primāro uzdevumu, bet kurām ir dažādi pamatprojekti). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēta, ņemot vērā zināmos [Project ierobežojumus tīmeklim](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēta, ņemot vērā zināmos Project darbvirsmas klienta ierobežojumus. | |  | :heavy_check_mark: |
| Rezervējamie resursi un projektu kalendāri tiks novērtēti pēc bieži sastopamiem nesaderīgiem kalendāra kārtulu izņēmumiem. | | :heavy_check_mark: | :heavy_check_mark: |

2. posmā klientiem, kuri veic jaunināšanu uz projekta operācijām, esošie projekti tiks jaunināti uz tikai lasāmu pieredzi projektu plānošanā. Šajā tikai lasāmajā pieredzē izsekošanas režģī būs redzama pilna WBS. Lai rediģētu WBS, projektu vadītāji var atlasīt **Konvertēt** galvenajā **lapā Projekti**. Pēc tam fona process atjauninās projektu tā, lai tas atbalstītu jauno projekta plānošanas pieredzi programmā Project for the Web. Šis posms ir piemērots klientiem, kuriem ir projekti, kas atbilst zināmajiem [Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) ierobežojumiem.

3. posmā tiks pievienots atbalsts project darbvirsmas klientam, lai gūtu labumu klientiem, kuri vēlas turpināt rediģēt savus projektus no šīs lietojumprogrammas. Tomēr, ja esošie projekti tiek pārvērsti par jauno Web pieredzes projektu, piekļuve pievienojumprogrammai tiks atspējota katram konvertētajam projektam.

## <a name="prerequisites"></a>Priekšnoteikumi

Lai varētu pretendēt uz 1. posma jauninājumu, klientam jāatbilst šādiem kritērijiem:

- Mērķa vidē nedrīkst būt ierakstu msdyn_projecttask **entītijā**.
- Derīgas projekta operāciju licences jāpiešķir visiem klienta aktīvajiem lietotājiem. 
- Klientam ir jāpārbauda jaunināšanas process vismaz vienā vidē, kas nav saistīta ar ražošanu un kurai ir reprezentatīva datu kopa, kas ir saskaņota ar ražošanas datiem.
- Mērķa vide ir jāatjaunina uz Project Service Automation Update Release 41 (3.10.62.162) vai jaunākām versijām.

Priekšnoteikumi 2. un 3. posmam tiks atjaunināti, tuvojoties vispārējiem pieejamības datumiem.

## <a name="licensing"></a>Licencēšana

Ja jums ir aktīvas licences projektu pakalpojumu automatizācijai, varat instalēt un izmantot projektu operācijas, kas ietver visas projektu pakalpojumu automatizācijas iespējas un daudz ko citu. Tādā veidā varat pārbaudīt projekta operāciju iespējas, kamēr ražošanā turpināt izmantot projektu pakalpojumu automatizāciju. Pēc project service automation licenču derīguma termiņa beigām jums būs jāpāriet uz projekta operācijām. Plānojot šo pāreju, ir jāņem vērā tas, ka projekta operāciju licencē nav iekļauta projektu pakalpojumu automatizācijas licence.

## <a name="testing-and-refactoring-customizations"></a>Pielāgojumu testēšana un pārveidošana

Vispirms importējiet visus pielāgojumus tīrā project operations (lite) vidē, lai apstiprinātu, ka importēšana ir veiksmīga un ka biznesa operācijas darbojas, kā paredzēts.

Šeit ir dažas lietas, no kurām jāuzmanās:

- Importēšana var neizdoties trūkstošo atkarību dēļ. Citiem vārdiem sakot, pielāgojumu atsauces lauki vai citi komponenti, kas ir noņemti projekta operācijās. Šādā gadījumā noņemiet šīs atkarības no attīstības vides.
- Ja nepārvaldītajos un pārvaldītajos risinājumos ir iekļauti komponenti, kas nav pielāgoti, noņemiet šos komponentus no risinājuma. Piemēram, pielāgojot entītiju **Projekts**, risinājumam pievienojiet tikai entītijas galveni. Nepievienojiet visus laukus. Ja iepriekš esat pievienojis visus apakškomponentus, iespējams, jums būs manuāli jāizveido jauns risinājums un jāpievieno tam atbilstoši komponenti.
- Veidlapas un skati var netikt parādīti, kā paredzēts. Dažos gadījumos, ja esat pielāgojis kādu no gatavajām formām vai skatiem, pielāgojumi var neļaut stāties spēkā jauniem atjauninājumiem projektu operācijās. Lai identificētu šīs problēmas, ieteicams veikt detalizētu pārskatu par tīru projekta operāciju instalāciju un projekta operāciju instalēšanu, kas ietver pielāgojumus. Salīdziniet visbiežāk izmantotās veidlapas savā uzņēmumā, lai apstiprinātu, ka veidlapas versijai joprojām ir jēga un ka veidlapas tīrajā versijā kaut kas nav pazudis. Veiciet tāda paša veida līdzāsparādīšanu visiem jūsu pielāgotajiem skatiem.
- Biznesa loģika izpildlaikā var neizdoties. Tā kā importēšanas laikā atsauces uz spraudņu laukiem nav validētas, biznesa loģika var neizdoties, jo ir atsauces uz laukiem, kas vairs nepastāv, un, iespējams, saņemsit kļūdas ziņojumu, kas atgādina šādu piemēru: entītijā "Projekts" nav atribūta ar nosaukumu = "msdyn_plannedhours" un NameMapping = 'Loģisks''. Šādā gadījumā modificējiet pielāgojumus, lai tie izmantotu jaunos laukus. Ja spraudņa loģikā izmantojat automātiski ģenerētas starpniekservera klases un spēcīgas tipa atsauces, apsveriet iespēju atjaunot šīs pilnvaras no tīras instalācijas. Tādā veidā jūs varat viegli identificēt visas vietas, kur jūsu spraudņi ir atkarīgi no novecojušiem laukiem.

Pēc pielāgojumu atjaunināšanas, lai tīri importētu projekta operācijas, pārejiet pie nākamajām darbībām.

## <a name="end-to-end-testing-in-development-environments"></a>Pilnīga testēšana izstrādes vidē

### <a name="initiate-upgrade"></a>Sākt jaunināšanu 

1. Administrēšanas Power Platform centrā atrodiet un atlasiet savu vidi. Pēc tam lietojumprogrammās atrodiet un atlasiet **Dynamics 365 Project Operations**.
2. Atlasiet **Instalēt**, lai sāktu jaunināšanu. Administrēšanas Power Platform centrs šo instalāciju prezentēs kā jaunu instalāciju. Tomēr tiks konstatēta vecākas Project Service Automation versijas klātbūtne, un esošā instalācija tiks jaunināta.

    Pēc jaunināšanas pabeigšanas vidē jāparāda, ka projekta operācijas ir instalētas un projektu pakalpojumu automatizācija nav instalēta.

    > [!NOTE]
    > Atkarībā no datu apjoma vidē jaunināšana var ilgt vairākas stundas. Galvenajai komandai, kas pārvalda jaunināšanu, ir attiecīgi jāplāno un jāpalaiž jaunināšana ārpus darba laika. Dažos gadījumos, ja datu apjoms ir liels, jaunināšana jāveic nedēļas nogalē. Lēmums par grafiku sastādīšanu jāpieņem, pamatojoties uz testēšanas rezultātiem zemākā vidē.

3. Pēc vajadzības jauniniet pielāgotus risinājumus. Šajā brīdī šīs tēmas [sadaļā Testēšana un pielāgošana pielāgojumi](#testing-and-refactoring-customizations) izvietojiet visas pielāgojumos veiktās izmaiņas.
4. Dodieties uz **Iestatījumu** \> **risinājumi** un atlasiet, lai atinstalētu **projektu operāciju novecojušo komponentu** risinājumu.

    Šis risinājums ir pagaidu risinājums, kurā ir esošais datu modelis un komponenti, kas atrodas jaunināšanas laikā. Noņemot šo risinājumu, tiek noņemti visi lauki un komponenti, kas vairs netiek izmantoti. Tādā veidā jūs palīdzat vienkāršot saskarni un atvieglot integrāciju un paplašinājumu.
    
### <a name="validate-common-scenarios"></a>Pārbaudīt bieži sastopamos scenārijus

Validējot konkrētos pielāgojumus, ieteicams pārskatīt arī biznesa procesus, kas tiek atbalstīti visās lietojumprogrammās. Šie biznesa procesi ietver, bet neaprobežojas ar tādu pārdošanas entītiju izveidi kā kotācijas un līgumi, kā arī tādu projektu izveidi, kas ietver PBS un faktisko apstiprinājumu.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Būtiskas izmaiņas starp projektu pakalpojumu automatizāciju un projekta darbībām

Šajā sadaļā sniegts kopsavilkums par galvenajām izmaiņām, ko var sagaidīt starp projektu pakalpojumu automatizāciju un projekta operācijām.

### <a name="project-planning"></a>Projektu plānošana

Projekta plānošanas iespējas projekta operācijās vairs nav atkarīgas no klienta puses loģikas un servera puses loģikas kombinācijas. Tā vietā projekta operācijas izmanto projektu tīmeklim, jo tas ir plānošanas programma. Šīs plānošanas iespēju izmaiņas iespējo vairākus jaunus līdzekļus, piemēram, Board un Gantt skatus, resursu virzītu plānošanu, [uzdevumu kontrolsaraksta vienumus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) un projektu plānošanas režīmus. Jaunās plānošanas iespējas atbalsta arī bagātīgs jaunu [lietojumprogrammu interfeisu (API](../project-management/schedule-api-preview.md)) kopums. Šie API ir paredzēti, lai palīdzētu nodrošināt, ka neviena programmatiska operācija WBS entītijas izveidei, atjaunināšanai vai dzēšanai nesabojā aprēķinātos laukus grafikā.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Turpinot ieguldījumus projektu operācijās, ir pieejamas vairākas jaunas iespējas norēķinos un cenu noteikšanā. Lūk, daži piemēri:

- [Materiālu lietojuma reģistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Apakšuzņēmuma līgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma vērtība, kas nepārsniedz statusu un pārbaudes](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uz uzdevumiem balstīti norēķini

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kuri izvietošanas tipi pašlaik tiek atbalstīti jaunināšanai?

| Avots                                                 | Mērķis                                                    | Statuss                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekta operāciju Lite izvietošana                        | Atbalstīts               |
| Dynamics 365 Finance projektu vadība un grāmatvedība | Projekta operāciju Lite izvietošana                        | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un grāmatvedība              | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un grāmatvedība              | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem | Pašlaik netiek atbalstīts |
| Projektu pakalpojumu automatizācija 3.x                         | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Projekts tīmeklim (īpaša vide)            | Projekta operāciju Lite izvietošana                        | Pašlaik netiek atbalstīts |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kā es varu instalēt project operations, pirms ir pieejama jaunināšanas rīks?

Pirms jaunināšanas rīka pieejamības ir pieejamas divas iespējas projekta operāciju instalēšanai:

- Nodrošiniet jaunu vidi.
- Izvietot projekta operācijas atsevišķi jebkurā pārdošanas organizācijā, kurā nav projektu pakalpojumu automatizācijas.

> [!NOTE]
> Ja project service automation ir instalēta organizācijā, bet tā netika izmantota, to var atinstalēt. Pēc pilnīgas projektu pakalpojumu automatizācijas noņemšanas projekta operācijas var instalēt tajā pašā organizācijā.
