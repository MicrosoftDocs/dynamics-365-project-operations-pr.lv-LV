---
title: Project Service Automation jaunināšana uz Project Operations
description: Šajā rakstā ir sniegts pārskats par procesu Microsoft Dynamics 365 Project Service Automation jaunināšanai uz Dynamics 365 Project Operations.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736676"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation jaunināšana uz Project Operations

Ar prieku izziņojam otro no trim jaunināšanas fāzēm no Microsoft Dynamics 365 Project Service Automation uz Microsoft Dynamics 365 Project Operations. Šajā rakstā ir sniegts pārskats klientiem, uz kuriem attiecas šīs aizraujošās pārmaiņas. 

Jauninājuma piegādes programma tiks sadalīta trīs posmos.

| Jauninājuma nodrošināšana | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. posms (2023. gada aprīļa laidiens)  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektiem nav atkarības no darba sadalījuma struktūras (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS ietilpst pašlaik atbalstītos Project Operations ierobežojumos | | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem Project Operations ierobežojumiem, tostarp Project Desktop Client atbalsta | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Jaunināšanas procesa līdzekļi 

Jaunināšanas procesa ietvaros mēs vietnes kartei esam pievienojuši jaunināšanas žurnālus, lai administratori varētu vieglāk diagnosticēt kļūmes. Papildus jaunajam interfeisam tiks pievienotas jaunas pārbaudes kārtulas, lai nodrošinātu datu integritāti pēc jaunināšanas. Jaunināšanas procesam tiks pievienotas tālāk norādītās pārbaudes.

| Pārbaudes | 1. posms (2022. gada janvāris) | 2. posms (2022. gada novembris) | 3. posms  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS tiks pārbaudīta attiecībā pret bieži sastopamām datu integritātes kļūdām (piemēram, resursu piešķīrumi, kas ir saistīti ar vienu un to pašu primāro uzdevumu, bet kam ir dažādi primārie projekti). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks pārbaudīta attiecībā pret [zināmajiem Project for the Web ierobežojumiem](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS tiks pārbaudīta attiecībā pret zināmajiem Project Desktop Client ierobežojumiem. | |  | :heavy_check_mark: |
| Rezervējamie resursi un projektu kalendāri tiek novērtēti, ņemot vērā bieži sastopamus nesaderīgu kalendāra kārtulu izņēmumus. | | :heavy_check_mark: | :heavy_check_mark: |

2. posmā klientiem, kas veic jaunināšanu uz Project Operations, esošie projekti tiks jaunināti uz tikai lasāmu pieredzi projektu plānošanai. Šajā tikai lasāmajā pieredzē izsekošanas režģī būs redzama visa WBS. Lai rediģētu WBS, projekta vadītāji projekta galvenajā lapā var atlasīt [**Pārvērst**](/PSA-Upgrade-Project-Conversion.md). Fona process pēc tam atjaunina projektu, lai tas atbalstītu jauno projektu plānošanas pieredzi no Project for the Web. Šis posms ir piemērots klientiem, kuriem ir projekti, kas iekļaujas [zināmajos Project for the Web ierobežojumos](/project-for-the-web/project-for-the-web-limits-and-boundaries).

3. posmā tiks pievienots Project Desktop Client atbalsts, nodrošinot ieguvumus klientiem, kuri vēlas turpināt savu projektu rediģēšanu šajā programmā. Tomēr, ja esošie projekti ir pārvērsti jaunajā Project for the Web funkcionalitātē, piekļuve pievienojumprogrammai katrā pārvērstajā projektā būs atspējota.

## <a name="prerequisites"></a>Priekšnoteikumi

Lai varētu veikt 1. posma jaunināšanu, nepieciešama atbilstība tālāk norādītajiem kritērijiem.

- Mērķa vidē nedrīkst būt neviena ieraksta entītijā **msdyn_projecttask**.
- Visiem aktīvajiem lietotājiem ir jābūt piešķirtām derīgām Project Operations licencēm. 
- Jaunināšanas process ir jāpārbauda vismaz vienā ar ražošanā nesaistītā vidē, kurā ir reprezentatīva datu kopa, kas ir saskaņota ar jūsu ražošanas vidi.
- Mērķa vide ir jāatjaunina uz Project Service Automation atjauninājumu laidienu 37 (V3.10.58.120) vai jaunāku versiju.

Lai varētu veikt 2. posma jaunināšanu, nepieciešama atbilstība tālāk norādītajiem kritērijiem.

- Visiem aktīvajiem lietotājiem ir jābūt piešķirtām derīgām Project Operations licencēm. 
- Jaunināšanas process ir jāpārbauda vismaz vienā ar ražošanā nesaistītā vidē, kurā ir reprezentatīva datu kopa, kas ir saskaņota ar jūsu ražošanas vidi.
- Mērķa vide ir jāatjaunina uz Project Service Automation atjauninājumu laidienu 37 (V3.10.58.120) vai jaunāku versiju.
- Vides, kurās ir uzdevumi (msdyn_projecttask), tiek atbalstītas tikai tad, ja kopējais uzdevumu skaits projektā ir 500 vai mazāk.

3. posma priekšnosacījumi tiks atjaunināti, tuvojoties vispārējās pieejamības datumam.

## <a name="licensing"></a>Licencēšana

Ja jums ir aktīvas Project Service Automation licences, varat instalēt un lietot Project Operations, kas ietver visas Project Service Automation iespējas un vairāk. Šādi varat pārbaudīt Project Operations iespējas, kamēr turpināsit izmantot Project Service Automation ražošanā. Pēc Project Service Automation licenču derīguma beigām būs nepieciešams pāriet uz Project Operations. Plānojot šo pāreju, ir jāņem vērā, ka Project Operations licencē nav iekļauta Project Service Automation licence. Klienti, kuriem ir scenāriji, kuros viņi ir izvietojuši Project Service Automation un kuriem ir nepieciešams turpināt lietot PSA licences vai palielināt to skaitu, kamēr notiek pārejas plānošana uz Project Operations, var pieprasīt pagaidu PSA licences, balstoties uz Project Operations iegādātajām licencēm. Vienai Project Operations licencei tiks izsniegta viena Project Service Automation licence. Pagaidu PSA licences var pieprasīt, izmantojot šo saiti: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Pielāgojumu testēšana un pārstrukturēšana

Vispirms importējiet visus pielāgojumus tīrā Project Operations (Lite) vidē, lai apstiprinātu, ka importēšana ir sekmīga un ka uzņēmējdarbības operācijas darbojas, kā paredzēts.

Tālāk ir uzskaitītas dažas lietas, kas jāņem vērā.

- Importēšana var neizdoties, jo trūkst atkarību. Citiem vārdiem, pielāgojumu atsauču lauki vai citi komponenti, kas ir noņemti programmā Project Operations. Šādā gadījumā noņemiet šīs atkarības no izstrādes vides.
- Ja nepārvaldītajos un pārvaldītajos risinājumos ir iekļauti komponenti, kas nav pielāgoti, noņemiet šos komponentus no risinājuma. Piemēram, pielāgojot entītiju **Projekts**, risinājumam pievienojiet tikai entītijas galveni. Nepievienojiet visus laukus. Ja esat iepriekš pievienojis visus apakškomponentus, iespējams, jums būs manuāli jāizveido jauns risinājums un jāpievieno tam attiecīgie komponenti.
- Veidlapas un skati var izskatīties citādāk, nekā paredzēts. Dažos gadījumos, ja ir pielāgota kāda no oriģinālajām veidlapām vai skatiem, pielāgojumi var traucēt Project Operations jaunajiem atjauninājumiem stāties spēkā. Lai identificētu šīs problēmas, ieteicams veikt tīrās Project Operations instalācijas pārskatīšanu, salīdzinot ar Project Operations instalāciju, kas ietver jūsu pielāgojumus. Salīdziniet uzņēmumā visbiežāk lietotās veidlapas, lai pārbaudītu, vai jūsu veidlapu versija joprojām ir pareiza un vai veidlapas tīrajā versijā nekā netrūkst. Veiciet tāda paša veida pārskatīšanu visiem pielāgotajiem skatiem.
- Uzņēmējdarbības loģika izpildlaikā var neizdoties. Tā kā atsauces uz laukiem spraudņos netiek pārbaudītas importēšanas laikā, uzņēmējdarbības loģika var neizdoties, jo pastāv atsauces uz laukiem, kas vairs nepastāv, un var tikt parādīts šim līdzīgs kļūdas ziņojums: “Entītija 'Project' nesatur atribūtu ar Name = 'msdyn_plannedhours' un NameMapping = 'Logical'”. Šādā gadījumā modificējiet pielāgojumus, lai tie izmantotu jaunos laukus. Ja jūsu spraudņa loģikā izmantojat automātiski ģenerētas starpniekklases un stiprā tipa atsauces, apsveriet iespēju reģenerēt šos starpniekus no tīras instalācijas. Tādējādi varat viegli identificēt visas vietas, kur spraudņi ir atkarīgi no novecojušiem laukiem.

Lai Pēc pielāgojumu atjaunināšanas, lai veiktu tīru Project Operations importēšanu, pārejiet pie nākamajām darbībām.

## <a name="end-to-end-testing-in-development-environments"></a>Testēšana izstrādes vidēs no sākuma līdz beigām

### <a name="initiate-upgrade"></a>Jaunināšanas inicializēšana 

1. Power Platform administrēšanas centrā atrodiet un atlasiet savu vidi. Pēc tam programmu sadaļā atrodiet un atlasiet **Dynamics 365 Project Operations**.
2. Lai sāktu jaunināšanu, atlasiet **Instalēt**. Power Platform administrēšanas centrs šo instalēšanu piedāvās kā jaunu instalēšanu. Tomēr tiek noteikta agrākas Project Service Automation versijas klātbūtne un esošā instalācija tiks jaunināta.

    Pēc jaunināšanas pabeigšanas vidē ir jābūt redzamam, ka ir instalēta programma Project Operations un nav instalēts Project Service Automation.

    Atkarībā no datu daudzuma vidē jaunināšana var aizņemt vairākas stundas. Pamata darba grupai, kas pārvalda jaunināšanu, ir atbilstoši jāplāno un jāveic jaunināšana ārpus darba laika. Dažos gadījumos, ja datu apjoms ir liels, jaunināšana jāveic nedēļas nogalē. Lēmums par plānošanu ir jāpieņem, balstoties uz testēšanas rezultātiem zemākās vidēs.

3. Jauniniet pielāgotos risinājumus pēc nepieciešamības. Šajā brīdī izvietojiet visas izmaiņas, ko vaicāt pielāgojumiem šī raksta sadaļā [Pielāgojumu testēšana un pārstrukturēšana](#testing-and-refactoring-customizations).
4. Pārejiet uz **make.powerapps.com**, atlasiet vidi nolaižamajā sarakstā portāla augšējā labajā stūrī, atlasiet **Risinājumi** kreisajā izvēlnē, atlasiet risinājumu **Project Operations novecojušie komponenti** un **Atinstalēt**.

    Šis risinājums ir pagaidu risinājums, kas patur esošo datu modeli un komponentus, kas ir klātesoši jaunināšanas laikā. Noņemot šo risinājumu, tiek noņemti visi lauki un komponenti, kas vairs netiek izmantoti. Šādi varat vienkāršot interfeisu un atvieglot integrāciju un paplašināšanu.
    
### <a name="upgrade-to-project-operations-lite"></a>Jaunināšana uz Project Operations Lite

Tālāk sniegtajā darbībā ir aprakstīts jaunināšanas process un ar to saistītā kļūdu reģistrēšana.

1. **PSA versijas pārbaude:** lai instalētu Project Operations, nepieciešama V3.10.58.120 vai jaunāka versija.
1. **Pirmspārbaude:** kad administrators sāk jaunināšanu, sistēma palaiž iepriekšēju pārbaudes darbību katrai entītijai, kas ir risinājuma Project Operations pamatā. Ar šo darbību tiek pārbaudīts, vai visas entītiju atsauces ir derīgas un vai dati, kas ir saistīti ar WBS, atrodas publicētajos Project for the Web ierobežojumos.
1. **Metadatu jaunināšana:** pēc sekmīgas pirmspārbaudes sistēma sāk shēmas izmaiņas un izveido novecojušo komponentu risinājumu. Pēc visu nepieciešamo pielāgojumu pārstrukturēšanas šo novecojušo risinājumu var noņemt. Šī darbība ir visgarākā jaunināšanas procesa daļa, un tās pabeigšana var ilgt līdz četrām stundām.
1. **Datu jaunināšana:** kad metadatu jaunināšanas posmā ir pabeigtas visas nepieciešamās shēmas izmaiņas, dati tiek migrēti uz jauno shēmu, un tiek veiktas visas nepieciešamās noklusējuma un pārrēķināšanas darbības.
1. **Projekta plānošanas programmas atjauninājums:** pēc sekmīgas datu jaunināšanas cilnes **Plānošana** apzīmējums galvenajā lapā tiek nomainīts uz **Uzdevumi**. Atlasot šo cilni pēc jaunināšanas, lietotājs tiek novirzīts uz izsekošanas režģi, lai skatītu tikai lasāmu WBS versiju. Lai rediģētu WBS, lietotājam ir jāinicializē plānošanas [pārvēršanas process](/PSA-Upgrade-Project-Conversion.md). Visi projekti bez iepriekš pastāvošām WBS var izmantot jauno plānošanas pieredzi tieši, bez pārvēršanas.
 
### <a name="validate-common-scenarios"></a>Bieži lietoto scenāriju pārbaudīšana

Kad validējat noteiktus pielāgojumus, ieteicams pārskatīt arī uzņēmējdarbības procesus, kas tiek atbalstīti dažādās programmās. Šie uzņēmējdarbības procesi ietver (bet ne tikai) pārdošanas entītiju, piemēram, piedāvājumu un līgumu, izveidi, kā arī tādu projektu izveidi, kas satur WBS, un faktisko datu apstiprināšanu.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Galvenās izmaiņas starp Project Service Automation un Project Operations

Šajā sadaļā sniegts kopsavilkums par galvenajām izmaiņām, kuras varat gaidīt starp Project Service Automation un Project Operations.

### <a name="project-planning"></a>Projektu plānošana

Project Operations projektu plānošanas iespējas vairs nepaļaujas uz kombinētu klienta puses loģiku un servera puses loģiku. Tā vietā Project Operations izmanto Project for the Web kā plānošanas programmu. Šīs plānošanas iespēju izmaiņas ļauj izmantot vairākus jaunus līdzekļus, piemēram, paneļa un Ganta skatus, uz resursiem balstītu plānošanu, [uzdevumu kontrolsaraksta vienumus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) un projektu plānošanas režīmus. Jaunās plānošanas iespējas atbalsta arī bagātīgs jaunu [programmu programmēšanas saskarņu (API)](../project-management/schedule-api-preview.md) klāsts. Šie API ir paredzēti, lai palīdzētu nodrošināt, ka neviena programmēta darbība WBS entītiju izveidošanai, atjaunināšanai vai dzēšanai grafikā neradītu kļūdas aprēķinātajos laukos.

### <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Nepārtrauktu ieguldījumu ietvaros programmā Project Operations ir pieejamas vairākas jaunas iespējas sadaļā Cenu noteikšana un norēķini. Lūk, daži piemēri:

- [Materiālu lietojuma reǵistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Pakārtotā pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līgums, kas nepārsniedz statusu un pārbaudes](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uzdevumā balstīti norēķini

### <a name="resource-management"></a>Resursu pārvaldība

Project Operations nodrošina neobligātu atbalstu Universal Resource Scheduling (URS) panelim un plānošanas palīgam. Šī jaunā pieredze 2023. gada aprīļa laidienā kļūs obligāta.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kādi izvietošanas tipi pašlaik jauninājumam tiek atbalstīti?

| Avots                                                 | Mērķis                                                    | Statuss                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite izvietošana                        | Atbalstīts               |
| Dynamics 365 Finance projektu pārvaldība un uzskaite | Project Operations Lite izvietošana                        | Pašlaik netiek atbalstīts |
| Finance projektu pārvaldība un uzskaite              | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Project Service Automation 3.x                         | Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem     | Pašlaik netiek atbalstīts |
| Project for the Web (īpašā vide)            | Project Operations Lite izvietošana                        | Pašlaik netiek atbalstīts |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kā instalēt Project Operations, pirms ir pieejams jaunināšanas rīku komplekts?

Kamēr jaunināšanas rīku komplekts nav pieejams, ir divas opcijas, kā instalēt Project Operations.

- Jaunas vides nodrošināšana.
- Project Operations izvietošana atsevišķi jebkurā pārdošanas organizācijā, kurā nav Project Service Automation.

Ja Project Service Automation organizācijā ir instalēts, bet netiek izmantots, to var atinstalēt. Kad Project Service Automation ir pilnībā noņemts, Project Operations var instalēt tajā pašā organizācijā.
