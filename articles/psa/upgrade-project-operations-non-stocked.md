---
title: Jaunināšana no projekta pakalpojumu automatizācijas uz projekta operācijām
description: Šajā tēmā ir sniegts pārskats par jaunināšanas procesu no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954296"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Jaunināšana no projekta pakalpojumu automatizācijas uz projekta operācijām

Mēs esam priecīgi paziņot par pirmo no trim posmiem jaunināšanai no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations. Šī tēma sniedz pārskatu klientiem, kuri uzsāk šo aizraujošo ceļojumu. Turpmākajās tēmās tiks iekļauti izstrādātāja apsvērumi un detalizēta informācija par līdzekļu uzlabojumiem. Tie ne tikai sniegs norādījumus, kas palīdzēs sagatavoties jaunināšanai uz projekta operācijām, bet arī izskaidros, ko varat sagaidīt pēc jaunināšanas.

Jaunināšanas piegādes programma tiks sadalīta trīs fāzēs.

| Jaunināt piegādi | 1. posms (2022. gada janvāris) | 2. posms (2022. gada aprīļa vilnis) | 3. posms (2022. gada aprīļa vilnis) |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu darba sadalījuma struktūras (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS pašlaik atbalstīto projekta operāciju robežās | | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem projekta operāciju ierobežojumiem, tostarp atbalsts projekta darbvirsmas klientam | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Jaunināšanas procesa līdzekļi 

Jaunināšanas procesa ietvaros vietnes kartei esam pievienojuši jaunināšanas žurnālus, lai administratori varētu vieglāk diagnosticēt kļūmes. Papildus jaunajai saskarnei tiks pievienoti jauni validācijas noteikumi, lai nodrošinātu datu integritāti pēc jaunināšanas. Jaunināšanas procesam tiks pievienotas šādas validācijas.

| Apstiprinājumu | 1. posms (2022. gada janvāris) | 2. posms (2022. gada aprīļa vilnis) | 3. posms (2022. gada aprīļa vilnis) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS tiks validēta pret bieži sastopamiem datu integritātes pārkāpumiem (piemēram, resursu piešķirēm, kas ir saistītas ar vienu un to pašu primāro uzdevumu, bet kurām ir atšķirīgi pamatprojekti). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēta, ņemot vērā [zināmās Projekta tīmekļa ierobežojumus](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks validēta, ņemot vērā projekta darbvirsmas klienta zināmās robežas. | | :heavy_check_mark: | :heavy_check_mark: |
| Rezervējamie resursi un projektu kalendāri tiks novērtēti, izmantojot bieži sastopamus nesaderīgus kalendāra kārtulu izņēmumus. | | :heavy_check_mark: | :heavy_check_mark: |

2. posmā klientiem, kuri veic jaunināšanu uz projekta operācijām, esošie projekti tiks jaunināti uz tikai lasīšanas pieredzi projektu plānošanā. Šajā tikai lasāmajā pieredzē izsekošanas režģī būs redzama pilna WBS. Lai rediģētu WBS, projektu vadītāji galvenajā lapā Projekti var **atlasīt** **Konvertēt**. Pēc tam fona process atjauninās projektu, lai tas atbalstītu jauno projekta plānošanas pieredzi no projekta tīmeklim. Šis posms ir piemērots klientiem, kuriem ir projekti, kas atbilst [zināmajām projekta web robežām](/project-for-the-web/project-for-the-web-limits-and-boundaries).

3. posmā tiks pievienots atbalsts projekta darbvirsmas klientam, lai ieguvēji būtu klienti, kuri vēlas turpināt rediģēt savus projektus no šīs lietojumprogrammas. Tomēr, ja esošie projekti web pieredzes dēļ tiek pārvērsti par jauno projektu, piekļuve pievienojumprogrammai tiks atspējota katram konvertētajam projektam.

## <a name="prerequisites"></a>Priekšnoteikumi

Lai varētu veikt 1. posma jaunināšanu, klientam jāatbilst šādiem kritērijiem:

- Mērķa vidē nedrīkst būt ierakstu **msdyn_projecttask** entītijā.
- Derīgas projekta operāciju licences ir jāpiešķir visiem klienta aktīvajiem lietotājiem. 
- Klientam ir jāvalidē jaunināšanas process vismaz vienā vidē, kas nav ražošanas vide un kam ir reprezentatīva datu kopa, kas ir saskaņota ar ražošanas datiem.
- Mērķa vide ir jāatjaunina uz Project Service Automation Update Release 38 vai jaunāku versiju.

2. un 3. posma priekšnosacījumi tiks atjaunināti, tuvojoties vispārējiem pieejamības datumiem.

## <a name="licensing"></a>Licencēšana

Ja jums ir aktīvas licences project pakalpojumu automatizācijai, varat instalēt un izmantot Project Operations, kas ietver visas Project Service Automation iespējas un daudz ko citu. Tādā veidā varat pārbaudīt projekta operāciju iespējas, kamēr ražošanā turpināt izmantot project pakalpojumu automatizāciju. Pēc projektu pakalpojumu automatizācijas licenču derīguma termiņa beigām jums būs jāpāriet uz projekta operācijām. Plānojot šo pāreju, ir jāuzskaita, ka projekta operāciju licencē nav iekļauta projekta pakalpojumu automatizācijas licence.

## <a name="testing-and-refactoring-customizations"></a>Pielāgojumu testēšana un pārfaktorēšana

Vispirms importējiet visus pielāgojumus tīrā projekta operāciju (lite) vidē, lai apstiprinātu, ka importēšana ir veiksmīga un ka biznesa operācijas darbojas, kā paredzēts.

Šeit ir dažas lietas, no kurām jāuzmanās:

- Importēšana var neizdoties, jo trūkst atkarību. Citiem vārdiem sakot, pielāgojumu atsauces lauki vai citi komponenti, kas ir noņemti projekta operācijās. Šajā gadījumā noņemiet šīs atkarības no attīstības vides.
- Ja nepārvaldīs un pārvaldītie risinājumi ietver komponentus, kas netiek pielāgoti, noņemiet šos komponentus no risinājuma. Piemēram, pielāgojot **projekta** entītiju, risinājumam pievienojiet tikai entītijas virsrakstu. Nepievienojiet visus laukus. Ja iepriekš esat pievienojis visas apakškomponentes, iespējams, būs manuāli jāizveido jauns risinājums un jāpievieno tam atbilstoši komponenti.
- Formas un skati var neticīties tik negaidīti. Dažos gadījumos, ja esat pielāgojis kādu no iebūvētajām veidlapām vai skatiem, pielāgojumi var neļaut jauniem atjauninājumiem projekta operācijās stāties spēkā. Lai identificētu šīs problēmas, ieteicams veikt projekta operāciju tīras instalācijas un projekta operāciju instalācijas, kas ietver jūsu pielāgojumus, pārskatīšanu līdzās. Salīdziniet visbiežāk izmantotās veidlapas savā uzņēmumā, lai apstiprinātu, ka jūsu veidlapas versija joprojām ir jēga un netrūkst kaut kā no veidlapas tīrās versijas. Veiciet tāda paša veida recenziju līdzās visiem jūsu pielāgotajiem skatiem.
- Biznesa loģika izpildlaikā var neizdoties. Tā kā atsauces uz spraudņu laukiem importēšanas laikā netiek validētas, biznesa loģika var neizdoties, jo ir atsauces uz laukiem, kas vairs nepastāv, un var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram: entītijā "Projekts" nav atribūta ar nosaukumu = "msdyn_plannedhours" un NameMapping = "Logical"." Šādā gadījumā modificējiet pielāgojumus, lai tie izmantotu jaunos laukus. Ja spraudņa loģikā izmantojat automātiski ģenerētas starpniekservera klases un spēcīgas tipa atsauces, apsveriet iespēju atkārtoti ģenerēt šos starpniekserverus no tīras instalācijas. Tādā veidā varat viegli identificēt visas vietas, kur spraudņi ir atkarīgi no novecojušiem laukiem.

Pēc pielāgojumu atjaunināšanas, lai tīri importētu projekta operācijas, pārejiet pie nākamajām darbībām.

## <a name="end-to-end-testing-in-lower-environments"></a>Testēšana no gala līdz galam zemākā vidē

### <a name="run-the-upgrade-in-production"></a>Palaist jaunināšanu ražošanā

1. Administrēšanas Power Platform centrā atrodiet un atlasiet savu vidi. Pēc tam lietojumprogrammās atrodiet un atlasiet **Dynamics 365 Project Operations**.
2. Atlasiet **Instalēt**, lai sāktu jaunināšanu. Power Platform Administrēšanas centrs prezentēs šo instalāciju kā jaunu instalāciju. Tomēr tiks konstatēta vecākas project service automation versijas klātbūtne, un esošā instalācija tiks jaunināta.

    Kad jaunināšana ir pabeigta, videi ir jāparāda, ka projekta operācijas ir instalētas un ka project pakalpojumu automatizācija nav instalēta.

    > [!NOTE]
    > Atkarībā no datu apjoma vidē jaunināšana var ilgt vairākas stundas. Pamatgrupai, kas pārvalda jaunināšanu, ir atbilstoši jāplāno un jāveic jaunināšana ārpus darba laika. Dažos gadījumos, ja datu apjoms ir liels, jaunināšana jāveic nedēļas nogalē. Lēmums par plānošanu jāpamato ar testēšanas rezultātiem zemākā vidē.

3. Pēc vajadzības jauniniet pielāgotus risinājumus. Šajā brīdī šīs tēmas sadaļā Pielāgojumu testēšana un [pārfaktori izvietojiet visas pielāgošanas](#testing-and-refactoring-customizations) izmaiņas.
4. Dodieties uz **Iestatījumu** \> **risinājumi un** atlasiet, lai atinstalētu **projektu operāciju novecojušo komponentu** risinājumu.

    Šis risinājums ir pagaidu risinājums, kas satur esošo datu modeli un komponentus, kas atrodas jaunināšanas laikā. Noņemot šo risinājumu, tiek noņemti visi lauki un komponenti, kas vairs netiek izmantoti. Tādā veidā jūs palīdzat vienkāršot saskarni un atvieglot integrāciju un paplašināšanu.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Būtiskas izmaiņas starp projekta pakalpojumu automatizāciju un projekta operācijām

Šajā sadaļā ir sniegts kopsavilkums par galvenajām izmaiņām, ko var sagaidīt starp project service automation un project operations.

### <a name="project-planning"></a>Projektu plānošana

Projekta plānošanas iespējas projekta operācijās vairs nav atkarīgas no klienta puses loģikas un servera puses loģikas kombinācijas. Tā vietā projekta operācijas izmanto projektu tīmeklim kā plānošanas programmu. Šīs plānošanas iespēju izmaiņas iespējo vairākus jaunus līdzekļus, piemēram, Board un Gantt skatus, resursu virzītu plānošanu, [uzdevumu kontrolsaraksta](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) vienumus un projekta plānošanas režīmus. Jaunās plānošanas iespējas atbalsta arī bagātīgs jaunu [lietojumprogrammu programmēšanas interfeisu (API) kopums](../project-management/schedule-api-preview.md). Šie API ir paredzēti, lai palīdzētu nodrošināt, ka neviena programmatiska operācija, lai izveidotu, atjauninātu vai dzēstu entītiju WBS, sabojā aprēķinātos laukus grafikā.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Turpinot ieguldījumus projekta operācijās, norēķinu un cenu noteikšanā ir pieejamas vairākas jaunas iespējas. Lūk, daži piemēri:

- [Materiālu izmantošanas reģistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Apakšuzņēmuma līgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma nepārsniegt statusu un pārbaudes](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uz uzdevumiem balstīti norēķini

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kuri izvietošanas tipi pašlaik tiek atbalstīti jaunināšanai?

| Avots                                                 | Mērķis                                                    | Statuss                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekta operāciju Lite izvietošana                        | Atbalstīts               |
| Dynamics 365 Finance Projektu vadība un grāmatvedība | Projekta operāciju Lite izvietošana                        | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un grāmatvedība              | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Finanšu projektu vadība un grāmatvedība              | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem | Pašlaik netiek atbalstīts |
| Projekta pakalpojumu automatizācija 3.x                         | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Projekts tīmeklim (īpaša vide)            | Projekta operāciju Lite izvietošana                        | Pašlaik netiek atbalstīts |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kā instalēt projekta operācijas, pirms jaunināšanas rīki ir pieejami?

Pirms jaunināšanas rīku pieejamības ir divas projekta operāciju instalēšanas opcijas:

- Nodrošināt jaunu vidi.
- Izvietot projekta operācijas atsevišķi jebkurā pārdošanas organizācijā, kurā nav project service automation.

> [!NOTE]
> Ja project service automation ir instalēts organizācijā, bet tas netika izmantots, to var atinstalēt. Pēc projekta servisa automatizācijas pilnīgas noņemšanas project operations var instalēt tajā pašā organizācijā.
