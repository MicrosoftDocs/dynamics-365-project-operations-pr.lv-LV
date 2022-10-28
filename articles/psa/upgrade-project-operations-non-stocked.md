---
title: Project Service Automation jaunināšana uz Project Operations
description: Šajā rakstā ir sniegts pārskats par jaunināšanas procesu no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 06a4de89be8176049d3a14a8c0d6427e228744ba
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709454"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation jaunināšana uz Project Operations

Mēs ar prieku paziņojam par otro no trim posmiem jaunināšanai no Microsoft Dynamics 365 Project Service Automation Microsoft uz Microsoft Dynamics 365 Project Operations. Šajā rakstā ir sniegts pārskats klientiem, kuri uzsāk šo aizraujošo ceļojumu. 

Jaunināšanas piegādes programma tiks sadalīta trīs fāzēs.

| Jauninājumu piegāde | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. fāze (2023. gada aprīļa vilnis)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu sadalījuma struktūras (PBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS pašlaik atbalstīto projekta operāciju robežās | | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem Project Operations ierobežojumiem, tostarp Project datora klienta atbalsts | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Jaunināšanas procesa līdzekļi 

Jaunināšanas procesa ietvaros vietnes kartei esam pievienojuši jaunināšanas žurnālus, lai administratori varētu vieglāk diagnosticēt kļūmes. Papildus jaunajai saskarnei tiks pievienoti jauni validācijas noteikumi, lai nodrošinātu datu integritāti pēc jaunināšanas. Tālāk norādītās validācijas tiks pievienotas jaunināšanas procesam.

| Apstiprinājumu | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. fāze  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS tiks validēts, lai novērstu bieži sastopamus datu integritātes pārkāpumus (piemēram, resursu piešķires, kas ir saistītas ar vienu un to pašu vecākuzdevumu, bet kurām ir dažādi vecākprojekti). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēts, ņemot vērā zināmos [Project tīmeklim ierobežojumus](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēts, ņemot vērā Project datora klienta zināmos ierobežojumus. | |  | :heavy_check_mark: |
| Rezervējamie resursi un projektu kalendāri tiks novērtēti, ņemot vērā bieži sastopamos nesaderīgos kalendāra kārtulu izņēmumus. | | :heavy_check_mark: | :heavy_check_mark: |

2. posmā klienti, kuri veic jaunināšanu uz programmu Project Operations, savus esošos projektus jauninās uz tikai lasīšanas iespējām projektu plānošanā. Šajā tikai lasīšanas pieredzē izsekošanas režģī būs redzams pilns WBS. Lai rediģētu WBS, projektu vadītāji projekta galvenajā lapā var atlasīt [**Konvertēt**](/PSA-Upgrade-Project-Conversion.md). Pēc tam fona process atjaunina projektu, lai tas atbalstītu jauno projekta plānošanas pieredzi programmā Project tīmeklī. Šī fāze ir piemērota klientiem, kuriem ir projekti, kas atbilst programmas Project tīmeklim [zināmajās](/project-for-the-web/project-for-the-web-limits-and-boundaries) robežās.

3. posmā tiks pievienots atbalsts Project datora klientam to klientu labā, kuri vēlas turpināt rediģēt savus projektus no šīs lietojumprogrammas. Tomēr, ja esošie projekti tiek pārveidoti par jauno Project for the Web pieredzi, piekļuve pievienojumprogrammai tiks atspējota katram pārvērstajam projektam.

## <a name="prerequisites"></a>Priekšnoteikumi

Lai varētu izmantot 1. posma jaunināšanu, jums ir jāatbilst tālāk norādītajiem kritērijiem.

- Mērķa vidē nedrīkst būt msdyn_projecttask **entītijas ierakstu**.
- Derīgas Project Operations licences ir jāpiešķir visiem aktīvajiem lietotājiem. 
- Jaunināšanas process ir jāvalidē vismaz vienā vidē, kas nav ražošanas vide un kurā ir reprezentatīva datu kopa, kas ir saskaņota ar jūsu ražošanas vidi.
- Mērķa vide ir jāatjaunina uz Project Service Automation Update Release 37 (V3.10.58.120) vai jaunāku versiju.

Lai varētu veikt 2. posma jaunināšanu, jums ir jāatbilst tālāk norādītajiem kritērijiem.

- Derīgas Project Operations licences ir jāpiešķir visiem aktīvajiem lietotājiem. 
- Jaunināšanas process ir jāvalidē vismaz vienā vidē, kas nav ražošanas vide un kurā ir reprezentatīva datu kopa, kas ir saskaņota ar jūsu ražošanas vidi.
- Mērķa vide ir jāatjaunina uz Project Service Automation Update Release 37 (V3.10.58.120) vai jaunāku versiju.
- Vides, kurās ir uzdevumi (msdyn_projecttask), tiek atbalstītas tikai tad, ja kopējais uzdevumu skaits vienā projektā ir 500 vai mazāks.

Priekšnosacījumi 3. posmam tiks atjaunināti, tuvojoties vispārējās pieejamības datumam.

## <a name="licensing"></a>Licencēšana

Ja jums ir aktīvas Project Service Automation licences, varat instalēt un izmantot Project Operations, kas ietver visas Project Service Automation un citas iespējas. Šādā veidā varat pārbaudīt Project Operations iespējas, turpinot izmantot Project Service Automation ražošanā. Pēc Project Service Automation licenču derīguma termiņa beigām jums būs jāpāriet uz Project Operations. Plānojot šo pāreju, jums ir jāņem vērā fakts, ka Project Operations licencē nav iekļauta Project Service Automation licence. Klienti, kuriem ir scenāriji, kuros viņi ir izvietojuši Project Service Automation un kuriem ir jāturpina izmantot vai palielināt savas PSA licences, kamēr viņi plāno pāriet uz Project Operations, var pieprasīt pagaidu PSA licences, pamatojoties uz Project Operations iegādātajām licencēm. Vienai Project Service Automation licencei tiks izsniegta viena Project Service Automation licence. Pagaidu PSA licences var pieprasīt, izmantojot šo saiti: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Pielāgojumu testēšana un refaktorizēšana

Sākumā importējiet visus pielāgojumus tīrā Project Operations (Lite) vidē, lai apstiprinātu, ka importēšana ir veiksmīga un ka biznesa operācijas darbojas, kā paredzēts.

Lūk, dažas lietas, no kurām jāuzmanās:

- Importēšana var neizdoties, jo trūkst atkarību. Citiem vārdiem sakot, pielāgojumi atsaucas uz laukiem vai citiem komponentiem, kas ir noņemti programmā Project Operations. Šajā gadījumā noņemiet šīs atkarības no attīstības vides.
- Ja nepārvaldītie un pārvaldītie risinājumi ietver komponentus, kas nav pielāgoti, noņemiet tos no risinājuma. Piemēram, pielāgojot **projekta** entītiju, risinājumam pievienojiet tikai entītijas galveni. Nepievienojiet visus laukus. Ja iepriekš esat pievienojis visus apakškomponentus, iespējams, būs manuāli jāizveido jauns risinājums un tam jāpievieno atbilstoši komponenti.
- Veidlapas un skati var netikt rādīti, kā paredzēts. Dažos gadījumos, ja esat pielāgojis kādu no iebūvētajām veidlapām vai skatiem, pielāgojumi var neļaut stāties spēkā jauniem atjauninājumiem programmā Project Operations. Lai noteiktu šīs problēmas, ieteicams līdzāspusē pārskatīt projekta operāciju tīro instalāciju un projekta operāciju instalāciju, kas ietver jūsu pielāgojumus. Salīdziniet visbiežāk izmantotās veidlapas savā uzņēmumā, lai pārliecinātos, ka jūsu veidlapas versijai joprojām ir jēga un ka veidlapas tīrajā versijā kaut kā netrūkst. Veiciet tāda paša veida vienlaicīgu pārskatīšanu visiem pielāgotajiem skatiem.
- Biznesa loģika izpildlaikā var neizdoties. Tā kā importēšanas laikā atsauces uz laukiem spraudņos netiek validētas, biznesa loģika var neizdoties, jo ir atsauces uz laukiem, kas vairs nepastāv, un var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram: entītija "Projekts" nesatur atribūtu ar Name = "msdyn_plannedhours" un NameMapping = "Logical"." Šādā gadījumā modificējiet pielāgojumus, lai tie izmantotu jaunos laukus. Ja spraudņa loģikā izmantojat automātiski ģenerētas starpniekservera klases un spēcīga tipa atsauces, apsveriet iespēju atjaunot šos starpniekserverus no tīras instalācijas. Tādā veidā jūs varat viegli identificēt visas vietas, kur spraudņi ir atkarīgi no novecojušiem laukiem.

Pēc pielāgojumu atjaunināšanas, lai tīri importētu Project Operations, pārejiet pie nākamajām darbībām.

## <a name="end-to-end-testing-in-development-environments"></a>Pilnīga testēšana izstrādes vidē

### <a name="initiate-upgrade"></a>Jaunināšanas sākšana 

1. Administrēšanas Power Platform centrā atrodiet un atlasiet savu vidi. Pēc tam lietojumprogrammās atrodiet un atlasiet **Dynamics 365 Project Operations**.
2. Atlasiet **Instalēt**, lai sāktu jaunināšanu. Administrēšanas Power Platform centrs prezentēs šo instalāciju kā jaunu instalāciju. Tomēr tiks noteikta vecākas Project Service Automation versijas klātbūtne, un esošā instalācija tiks jaunināta.

    Kad jaunināšana ir pabeigta, vidē ir jāparāda, ka programma Project Operations ir instalēta un ka programma Project Service Automation nav instalēta.

    Atkarībā no datu apjoma vidē jaunināšana var ilgt vairākas stundas. Galvenajai komandai, kas pārvalda jaunināšanu, ir atbilstoši jāplāno un jāpalaiž jaunināšana ārpus darba laika. Dažos gadījumos, ja datu apjoms ir liels, jaunināšana jāveic nedēļas nogalē. Lēmums par plānošanu jāpieņem, pamatojoties uz testēšanas rezultātiem zemākās vidēs.

3. Ja nepieciešams, jauniniet pielāgotus risinājumus. Šajā brīdī izvietojiet visas pielāgojumos veiktās [izmaiņas šī raksta sadaļā Pielāgojumu](#testing-and-refactoring-customizations) testēšana un pārveidošana.
4. Dodieties uz **Iestatījumu** \> **risinājumi** un atlasiet, lai atinstalētu **risinājumu Project Operations Deprecated Components.**

    Šis risinājums ir pagaidu risinājums, kas satur esošo datu modeli un komponentus, kas atrodas jaunināšanas laikā. Noņemot šo risinājumu, tiek noņemti visi lauki un komponenti, kas vairs netiek izmantoti. Tādā veidā jūs palīdzat vienkāršot saskarni un atvieglot integrāciju un paplašināšanu.
    
### <a name="upgrade-to-project-operations-lite"></a>Jaunināšana uz Project Operations Lite

Tālāk norādītajās darbībās ir aprakstīts jaunināšanas process un ar to saistītā kļūdu reģistrēšana.

1. **PSA versijas pārbaude:** lai instalētu Project Operations, ir nepieciešama V3.10.58.120 vai jaunāka versija.
1. **Pirmsvalidācija:** kad administrators uzsāk jaunināšanu, sistēma palaiž pirmsvalidācijas operāciju katrai entītijai, kas ir projekta operāciju risinājuma pamatā. Šajā darbībā tiek pārbaudīts, vai visas entītiju atsauces ir derīgas, un tiek nodrošināts, ka ar WBS saistītie dati ir Project for the Web publicēšanas robežās.
1. **Metadatu jaunināšana:** pēc veiksmīgas pirmsvalidācijas sistēma uzsāk izmaiņas shēmā un izveido novecojušu komponentu risinājumu. Šo novecojušo risinājumu varat noņemt pēc tam, kad esat pabeidzis visus nepieciešamos pielāgojumus. Šī darbība ir garākā jaunināšanas procesa daļa, un tās pabeigšana var ilgt līdz četrām stundām.
1. **Datu jaunināšana:** kad metadatu jaunināšanas darbībā ir pabeigtas visas nepieciešamās shēmas izmaiņas, dati tiek migrēti uz jauno shēmu un tiek veikta visa nepieciešamā noklusēšana un pārrēķināšana.
1. **Projekta grafika programmas atjaunināšana:** pēc veiksmīgas datu jaunināšanas **galvenās lapas cilne Grafiks** tiek pārmarķēta kā **Uzdevumi**. Kad lietotājs pēc jaunināšanas atlasa šo cilni, viņš tiek novirzīts, lai naviģētu uz izsekošanas režģi, lai skatītu tikai lasāmu WBS versiju. Lai rediģētu WBS, viņiem ir jāuzsāk grafika [konvertēšanas process](/PSA-Upgrade-Project-Conversion.md). Visi projekti bez iepriekš esošas WBS var izmantot jauno plānošanas pieredzi tieši, bez konvertēšanas.
 
### <a name="validate-common-scenarios"></a>Bieži sastopamu scenāriju validēšana

Kad validējat savus konkrētos pielāgojumus, ieteicams pārskatīt arī biznesa procesus, kas tiek atbalstīti lietojumprogrammās. Šie biznesa procesi ietver, bet neaprobežojas ar pārdošanas entītiju, piemēram, piedāvājumu un līgumu, izveidi un tādu projektu izveidi, kas ietver PBS, un faktisko datu apstiprināšanu.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Būtiskas izmaiņas starp Project Service Automation un Project Operations

Šajā sadaļā ir sniegts kopsavilkums par galvenajām izmaiņām, ko varat sagaidīt starp Project Service Automation un Project Operations.

### <a name="project-planning"></a>Projektu plānošana

Project Operations projekta plānošanas iespējas vairs nav atkarīgas no klienta puses loģikas un servera puses loģikas kombinācijas. Tā vietā Project Operations izmanto Project tīmeklim kā plānošanas programmu. Šīs izmaiņas plānošanas iespējās iespējo vairākus jaunus līdzekļus, piemēram, paneļa un Ganta skatus, uz resursiem balstītu plānošanu, [uzdevumu kontrolsaraksta vienumus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) un projektu plānošanas režīmus. Jaunās plānošanas iespējas atbalsta arī bagātīgs jaunu [lietojumprogrammu saskarņu (API)](../project-management/schedule-api-preview.md) komplekts. Šie API ir paredzēti, lai palīdzētu nodrošināt, ka neviena programmatiska operācija entītijas izveidei, atjaunināšanai vai dzēšanai WBS nebojā aprēķinātos laukus grafikā.

### <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Turpinot investēt projekta operācijās, ir pieejamas vairākas jaunas iespējas norēķinu un cenu noteikšanas jomā. Lūk, daži piemēri:

- [Materiālu lietojuma reģistrēšana projektos un projektu uzdevumos](../material/material-usage-log.md)
- [Apakšlīgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma nepārkāpšanas statuss un validācijas](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uz uzdevumiem balstīti norēķini

### <a name="resource-management"></a>Resursu pārvaldība

Project Operations nodrošina papildu atbalstu (URS) panelim Universal Resource Scheduling un plānošanas palīgam. Šī jaunā pieredze kļūs obligāta 2023. gada aprīļa vilnī.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kuri izvietošanas veidi pašlaik tiek atbalstīti jaunināšanai?

| Avots                                                 | Mērķis                                                    | Statuss                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite izvietošana                        | Atbalstīts               |
| Dynamics 365 Finance Projektu vadība un uzskaite | Project Operations Lite izvietošana                        | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un uzskaite              | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Project Service Automation 3.x                         | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Projekts tīmeklim (atvēlēta vide)            | Project Operations Lite izvietošana                        | Pašlaik netiek atbalstīts |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kā instalēt programmu Project Operations, pirms ir pieejami jaunināšanas rīki?

Ir divas opcijas, kā instalēt Project Operations, pirms jaunināšanas rīks ir pieejams:

- Nodrošināt jaunu vidi.
- Izvietojiet Project Operations atsevišķi jebkurā pārdošanas organizācijā, kurā nav Project Service Automation.

Ja Project Service Automation ir instalēta organizācijā, bet tā netika izmantota, to var atinstalēt. Pēc Project Service Automation pilnīgas noņemšanas Project Operations var instalēt tajā pašā organizācijā.
