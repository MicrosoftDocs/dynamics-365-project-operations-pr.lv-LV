---
title: Jaunināšana no Project Service Automation uz Project Operations
description: Šajā rakstā ir sniegts pārskats par jaunināšanas procesu no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations.
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
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446045"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Jaunināšana no Project Service Automation uz Project Operations

Mēs ar prieku paziņojam par pirmo no trim posmiem jaunināšanai no Microsoft Dynamics 365 Project Service Automation līdz Dynamics 365 Project Operations. Šajā rakstā ir sniegts pārskats klientiem, kuri uzsāk šo aizraujošo ceļojumu. Turpmākajos rakstos tiks iekļauti izstrādātāju apsvērumi un detalizēta informācija par līdzekļu uzlabojumiem. Tie ne tikai sniegs norādījumus, kas palīdzēs jums sagatavoties jaunināšanai uz Project Operations, bet arī paskaidros, ko varat sagaidīt pēc jaunināšanas.

Jaunināšanas piegādes programma tiks sadalīta trīs fāzēs.

| Jaunināšanas piegāde | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. posms (2023. gada aprīļa vilnis)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu darba sadalījuma struktūras (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS pašlaik atbalstīto projektu operāciju robežās | | :heavy_check_mark: | :heavy_check_mark: |
| WBS, kas pārsniedz pašlaik atbalstītos Project Operations ierobežojumus, tostarp atbalstu Projekta darbvirsmas klientam | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Jaunināšanas procesa līdzekļi 

Jaunināšanas procesa ietvaros vietnes kartei esam pievienojuši jaunināšanas žurnālus, lai administratori varētu vieglāk diagnosticēt kļūmes. Papildus jaunajai saskarnei tiks pievienoti jauni validācijas noteikumi, lai nodrošinātu datu integritāti pēc jaunināšanas. Jaunināšanas procesam tiks pievienotas šādas validācijas.

| Apstiprinājumu | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. fāze  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS tiks validēts, ņemot vērā bieži sastopamus datu integritātes pārkāpumus (piemēram, resursu piešķires, kas ir saistītas ar vienu un to pašu vecākvotnes uzdevumu, bet kurām ir dažādi vecākprojekti). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēts, ņemot vērā zināmos [Web projekta ierobežojumus](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēts, ņemot vērā zināmos Project darbvirsmas klienta ierobežojumus. | |  | :heavy_check_mark: |
| Rezervējamie resursi un projektu kalendāri tiks novērtēti, ņemot vērā bieži sastopamos nesaderīgos kalendāra kārtulu izņēmumus. | | :heavy_check_mark: | :heavy_check_mark: |

2. posmā klienti, kuri veiks jaunināšanu uz Project Operations, savus esošos projektus atjauninās uz tikai lasāmu pieredzi projektu plānošanā. Šajā tikai lasāmajā pieredzē pilns WBS būs redzams izsekošanas režģī. Lai rediģētu WBS, projektu vadītāji galvenajā **projektu** lapā var atlasīt **Konvertēt**. Pēc tam projekts tiks atjaunināts, lai tas atbalstītu jauno projektu plānošanas pieredzi no project for the web. Šis posms ir piemērots klientiem, kuriem ir projekti, kas atbilst zināmajiem [project for the web](/project-for-the-web/project-for-the-web-limits-and-boundaries) ierobežojumiem.

3. posmā tiks pievienots atbalsts Project darbvirsmas klientam, lai sniegtu labumu klientiem, kuri vēlas turpināt rediģēt savus projektus no šīs lietojumprogrammas. Tomēr, ja esošie projekti tiek pārvērsti par jauno Web pieredzes projektu, piekļuve pievienojumprogrammai katram konvertētajam projektam tiks atspējota.

## <a name="prerequisites"></a>Priekšnoteikumi

Lai varētu piedalīties 1. posma jauninājumā, klientam ir jāatbilst šādiem kritērijiem:

- Mērķa vidē nedrīkst būt nekādu ierakstu msdyn_projecttask **vienībā**.
- Derīgas Project Operations licences ir jāpiešķir visiem klienta aktīvajiem lietotājiem. 
- Klientam ir jāvalidē jaunināšanas process vismaz vienā ar ražošanu nesaistītā vidē, kurā ir reprezentatīva datu kopa, kas ir saskaņota ar ražošanas datiem.
- Mērķa vide ir jāatjaunina uz Project Service Automation update Release 41 (3.10.62.162) vai jaunāku versiju.

Priekšnoteikumi 2. un 3. posmam tiks atjaunināti, tuvojoties vispārējiem pieejamības datumiem.

## <a name="licensing"></a>Licencēšana

Ja jums ir aktīvas licences Project Service Automation, varat instalēt un izmantot Project Operations, kas ietver visas Project Service Automation un citas iespējas. Tādējādi varat pārbaudīt Project Operations iespējas, kamēr turpināt izmantot Project Service Automation ražošanā. Pēc Project Service Automation licenču derīguma termiņa beigām jums būs jāpāriet uz Project Operations. Plānojot šo pāreju, ir jāņem vērā tas, ka Project Operations licencē nav iekļauta Project Service Automation licence.

## <a name="testing-and-refactoring-customizations"></a>Pielāgojumu testēšana un refaktorēšana

Vispirms importējiet visus pielāgojumus tīrā project operations (Lite) vidē, lai apstiprinātu, ka importēšana ir veiksmīga un ka biznesa operācijas darbojas, kā paredzēts.

Šeit ir dažas lietas, no kurām jāuzmanās:

- Importēšana var neizdoties, jo trūkst atkarību. Citiem vārdiem sakot, pielāgojumu atsauces lauki vai citi komponenti, kas ir noņemti programmā Project Operations. Šajā gadījumā noņemiet šīs atkarības no attīstības vides.
- Ja jūsu nepārvaldītajos un pārvaldītajos risinājumos ir iekļauti komponenti, kas nav pielāgoti, noņemiet šos komponentus no risinājuma. Piemēram, pielāgojot projekta **entītiju**, risinājumam pievienojiet tikai entītijas galveni. Nepievienojiet visus laukus. Ja iepriekš esat pievienojis visus apakškomponentus, iespējams, jums būs manuāli jāizveido jauns risinājums un jāpievieno tam atbilstoši komponenti.
- Veidlapas un skati var netikt rādīti, kā paredzēts. Dažos gadījumos, ja esat pielāgojis kādu no iebūvētajām veidlapām vai skatiem, pielāgojumi var neļaut stāties spēkā jauniem atjauninājumiem project operācijās. Lai noteiktu šīs problēmas, ieteicams līdzās pārskatīt tīru Project Operations instalāciju un instalēt Project Operations, kas ietver jūsu pielāgojumus. Salīdziniet visbiežāk izmantotās veidlapas savā uzņēmumā, lai pārliecinātos, ka veidlapas versijai joprojām ir jēga un veidlapas tīrajā versijā kaut kā netrūkst. Veiciet tāda paša veida līdzās esošu pārskatīšanu visiem pielāgotajiem skatiem.
- Biznesa loģika izpildlaikā var neizdoties. Tā kā importēšanas laikā atsauces uz laukiem spraudņos nav validētas, biznesa loģika var neizdoties, jo ir atsauces uz laukiem, kas vairs nepastāv, un var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram: "Projekta" entītija nesatur atribūtu ar Name = 'msdyn_plannedhours' un NameMapping = 'Logical'." Šādā gadījumā modificējiet pielāgojumus, lai tie izmantotu jaunos laukus. Ja spraudņa loģikā izmantojat automātiski ģenerētas starpniekservera klases un stipra tipa atsauces, apsveriet iespēju atjaunot šos starpniekserverus no tīras instalācijas. Tādā veidā jūs varat viegli identificēt visas vietas, kur jūsu spraudņi ir atkarīgi no novecojušiem laukiem.

Kad esat atjauninājis pielāgojumus, lai tīri importētu projekta operācijas, pārejiet pie nākamajām darbībām.

## <a name="end-to-end-testing-in-development-environments"></a>Testēšana no gala līdz galam izstrādes vidēs

### <a name="initiate-upgrade"></a>Jaunināšanas sākšana 

1. Power Platform Administrēšanas centrā atrodiet un atlasiet savu vidi. Pēc tam lietojumprogrammās atrodiet un atlasiet **Dynamics 365 Project Operations**.
2. Atlasiet **Instalēt**, lai sāktu jaunināšanu. Administrēšanas Power Platform centrs šo instalāciju prezentēs kā jaunu instalāciju. Tomēr tiks noteikta vecākas Project Service Automation versijas klātbūtne, un esošā instalācija tiks jaunināta.

    Kad jaunināšana ir pabeigta, videi ir jāparāda, ka project operations ir instalētas un ka project service automation nav instalēta.

    > [!NOTE]
    > Atkarībā no datu apjoma vidē jaunināšana var ilgt vairākas stundas. Galvenajai komandai, kas pārvalda jaunināšanu, ir attiecīgi jāplāno un jāveic jaunināšana ārpus darba laika. Dažos gadījumos, ja datu apjoms ir liels, jaunināšana jāveic nedēļas nogalē. Lēmums par plānošanu būtu jābalsta uz testēšanas rezultātiem zemākā vidē.

3. Pēc vajadzības jauniniet pielāgotus risinājumus. Šajā brīdī veiciet visas pielāgošanas [izmaiņas šī raksta sadaļā Testēšana un refaktorings pielāgojumi](#testing-and-refactoring-customizations).
4. Dodieties uz **Iestatījumu** \> **risinājumi** un atlasiet, lai atinstalētu **risinājumu Project Operations Novecojušie komponenti.**

    Šis risinājums ir pagaidu risinājums, kas satur esošo datu modeli un komponentus, kas atrodas jaunināšanas laikā. Noņemot šo risinājumu, jūs noņemat visus laukus un komponentus, kas vairs netiek izmantoti. Tādā veidā jūs palīdzat vienkāršot saskarni un atvieglot integrāciju un paplašināšanu.
    
### <a name="validate-common-scenarios"></a>Bieži lietotu scenāriju validēšana

Apstiprinot konkrētus pielāgojumus, ieteicams pārskatīt arī biznesa procesus, kas tiek atbalstīti visās lietojumprogrammās. Šie biznesa procesi ietver, bet neaprobežojas ar tādu pārdošanas entītiju izveidi kā kotācijas un līgumi, kā arī tādu projektu izveidi, kas ietver WBS, un faktisko vērtību apstiprināšanu.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Galvenās izmaiņas starp Project Service Automatizāciju un Project Operations

Šajā sadaļā ir sniegts kopsavilkums par galvenajām izmaiņām, ko varat sagaidīt starp Project Service Automation un Project Operations.

### <a name="project-planning"></a>Projektu plānošana

Projekta plānošanas iespējas project operations vairs nav atkarīgas no kombinācijas klienta puses loģikas un servera puses loģikas. Tā vietā Project Operations izmanto Project for the Web, jo tas ir plānošanas programma. Šīs plānošanas iespēju izmaiņas iespējo vairākus jaunus līdzekļus, piemēram, board un Gantt skatus, resursu vadītu plānošanu, [uzdevumu kontrolsaraksta vienumus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) un projektu plānošanas režīmus. Jaunās plānošanas iespējas atbalsta arī bagātīgs jaunu [lietojumprogrammu programmēšanas saskarņu (API)](../project-management/schedule-api-preview.md) komplekts. Šīs API ir paredzētas, lai palīdzētu nodrošināt, ka neviena programmatiska darbība entītijas izveidei, atjaunināšanai vai dzēšanai WBS nebojā grafika aprēķinātos laukus.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Turpinot ieguldījumus Project Operations, norēķinos un cenu noteikšanā ir pieejamas vairākas jaunas iespējas. Lūk, daži piemēri:

- [Materiālu lietojuma reģistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Apakšuzņēmuma līgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma nepārsniegšanas statuss un validācijas](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uz uzdevumiem balstīti norēķini

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kuri izvietošanas tipi pašlaik tiek atbalstīti jaunināšanai?

| Avots                                                 | Mērķis                                                    | Statuss                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekta operācijas Lite izvietošana                        | Atbalstīts               |
| Dynamics 365 Finance projektu vadība un grāmatvedība | Projekta operācijas Lite izvietošana                        | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un grāmatvedība              | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Project Service Automation 3.x                         | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Projekts tīmeklim (īpaša vide)            | Projekta operācijas Lite izvietošana                        | Pašlaik netiek atbalstīts |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kā instalēt Project Operations, pirms jaunināšanas rīks ir pieejams?

Pirms jaunināšanas rīku pieejamības Project Operations instalēšanai ir divas iespējas:

- Nodrošināt jaunu vidi.
- Izvietojiet Project Operations atsevišķi jebkurā pārdošanas organizācijā, kurā nav Project Service Automation.

> [!NOTE]
> Ja Project Service Automation ir instalēta organizācijā, bet tā netika izmantota, to var atinstalēt. Kad esat pilnībā noņēmis Project Service Automation, project operations var instalēt tajā pašā organizācijā.
