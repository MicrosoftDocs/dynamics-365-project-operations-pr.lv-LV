---
title: Līdzekļu izmaiņas no Project Service Automation uz Project Operations
description: Šajā rakstā ir sniegts pārskats par līdzekļu izmaiņām no Project Service Automation uz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459936"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Līdzekļu izmaiņas no Project Service Automation uz Project Operations

Jauninājums no Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations Lite tiks piegādāts trīs posmos. Šajā rakstā ir sniegta informācija par galvenajām izmaiņām, kuras varat sagaidīt, kad jaunināšana būs pabeigta.

| Jaunināšanas piegāde | 1. fāze <br>(Janvāris 2022) | 2. fāze <br>(2022. gada novembris) | 3. fāze  |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu darba sadalījuma struktūras (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS ir iekļauts pašlaik atbalstītajos projektu operāciju ierobežojumos. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem Project Operations ierobežojumiem, ieskaitot atbalstu Projekta darbvirsmas klientam. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projekta pārvaldība

Visnozīmīgākās izmaiņas lietotāja pieredzē būs projektu plānošanas jomā. Project Operations ievieš jaunu, modernu pieredzi darba sadalījuma struktūras (WBS) pārvaldībai, izmantojot plānošanas iespējas, ko [project nodrošina tīmeklim](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Plānošanas pieredzes atšķirības

Nākamajā tabulā ir apkopotas plānošanas atšķirības starp Project Service Automation un Project Operations.

|  Ieplānošana     |   Project Operations   |   Psa   |
|-----------------|------------------------|---------|
| Projekta veidnes — iespēja definēt un lietot projekta veidnes, kad tiek izveidots projekts  |  &nbsp;    | :heavy_check_mark: |
| Projekta darba sadalījuma struktūras (WBS) integrācija ar darbvirsmas klientu   |    &nbsp;  | :heavy_check_mark: |
| Ierobežojumi - Sāciet ne agrāk kā, pabeidziet ne vēlāk kā  | :heavy_check_mark: |   &nbsp;  |
| Atskaites punkti - uzdevumi ar nulles ilgumu   | :heavy_check_mark:  |  &nbsp;  |
| Uz resursiem orientētos uzdevumos tiks ņemta vērā piešķirto resursu pieejamība   | :heavy_check_mark: |  &nbsp;    |
| Rediģēšana pakāpeniski ar laika posmu — plānu rediģēšana un darbs katru dienu   |   &nbsp;  | :heavy_check_mark: |
| Automātiska/manuāla plānošana — izmantojiet programmu Projektu plānošana, lai automātiski vai manuāli plānotu uzdevumus |  &nbsp; | :heavy_check_mark:  |
| Rediģējiet lielus projektus tieši lietotāja saskarnē: rediģējamo plānu lielumam nav ierobežojumu  | 500 uzdevumu ierobežojums  | :heavy_check_mark:       |
| Procenti pabeigti — atzīmējiet uzdevuma progresu   | :heavy_check_mark:  |  &nbsp;  |
| [Projekta plānošanas režīmi](../project-management/scheduling-modes.md) — definējiet projektu kā fiksētas vienības, fiksētu piepūli vai fiksētu ilgumu | :heavy_check_mark: | &nbsp; |
| Laika grafiks — izveidojiet un pielāgojiet laika grafika skatu, lai vizualizētu detalizētu informāciju par grafiku un sazinātos ar ieinteresētajām personām. | :heavy_check_mark:  | &nbsp; |
| Uz piepūli balstīti uzdevumi — programmas atbalsta plānošana uzdevuma plānošanai kā piepūlei  | :heavy_check_mark:  | &nbsp; |
| **dialoglodziņš Informācija par** uzdevumu — uzdevuma informācijas saglabāšana, izmantojot dialoglodziņu | :heavy_check_mark:  |  &nbsp;  |
| Vilkšana un nomešana - vairākatlases uzdevumi un to pozīcijas modificēšana WBS | :heavy_check_mark: | &nbsp;  |
| Elastīgi noturīgi skati — uzdevumu atribūtu detalizētāku skatu definēšana   | :heavy_check_mark:  | &nbsp; |
| WBS kārtošana un filtrēšana  | :heavy_check_mark:  | &nbsp; |
| Plātņu skats, lai projektu, kas nav ūdenskritums, tiktu īstenots  | :heavy_check_mark:   | &nbsp; |
| Laika skalas skats - interaktīva Ganta diagramma, ko izmanto, lai vizualizētu un rediģētu WBS   | :heavy_check_mark:  | &nbsp; |
| Īsinājumtaustiņi — izmantojiet īsinājumtaustiņus bieži veicamām darbībām, piemēram, atkāpei vai ievietošanai  | :heavy_check_mark:  |  &nbsp; |
| Vairāku līmeņu atsaukšana — veiciet iespēju analīzi, lai pilnībā izprastu izmaiņu ietekmi, apvēršot un atkārtoti piemērojot visu darbību kopu | :heavy_check_mark: | &nbsp; |
| Izgriešana/ kopēšana/ielīmēšana — sadarbojieties grafika izstrādē, kopējot un ielīmējot grafika informāciju starp lietojumprogrammām  | :heavy_check_mark: | &nbsp; |
| Uzdevumu kontrolsaraksti — pievienojiet uzdevumam līdz 20 kontrolsaraksta elementiem   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektu plānošana

**Project** lapā Project operations ir ievērojams skaits atšķirību salīdzinājumā ar **project** lapu programmā Project Service Automation.

1. posma jaunināšanas ietvaros no **lapas Projekti** ir noņemtas šādas darbības:

  - **Atvērt programmā MS Project**
  - **Izveidot veidni**
  - **Atcelt saistību ar MS Project**

**Project** lapā project operations ir iekļautas tālāk norādītās jaunās cilnes.

- **Materiālu aprēķini**
- **Uzdevuma norēķinu iestatīšana**

Cilne **Statuss** ir noņemta, un lauks **Statuss** tagad **atrodas cilnē Kopsavilkums** ar projekta plānošanas režīmu.

   ![Projekta lapas atjauninājumi.](media/projectform.png)

Cilne Grafiks **ir** pārdēvēta **par cilni Uzdevums**, un tajā ir iekļautas jaunās projektu plānošanas iespējas programmā Project for the Web.

   ![Cilne Jauni projekta uzdevumi.](media/tasktab.png)

## <a name="scheduling-modes"></a>Plānošanas režīmi

Project Operations ir ieviesis jaunu līdzekli — [plānošanas režīmus](../project-management/scheduling-modes.md). Visiem esošajiem Project Service Automation projektiem pēc noklusējuma **būs fiksēts ilgums** project operations. Tomēr jaunu projektu noklusējumu var pārvaldīt, dodoties uz **iestatījumu** > **parametru** > **parametru** > **plānošanas režīmu**.

   ![Projekta parametru iestatījumi plānošanas režīmam.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekta plānošanas ierobežojumi

Project Operations paļaujas uz Project for the Web visās projektu plānošanas operācijās. Project for the Web pārvalda darba sadalījuma struktūru, izmantojot ierobežojumus nākamajā tabulā.

| **Lauks**                                          | **Ierobežojums**             |
|----------------------------------------------------|-----------------------|
| Projekta maksimālais uzdevumu skaits                  | 500                   |
| Projekta maksimālais ilgums               | 3650 dienas (10 gadi)  |
| Projekta maksimālais resursu skaits              | 300                   |
| Projekta maksimālais saišu skaits (tikai pēctecis) | 600                   |
| Projekta maksimālais pielāgoto lauku skaits          | 10                    |
| Maksimālais hierarhijas līmenis                            | 10 līmeņi             |
| Maksimālais saišu skaits (pēctecis + priekštecis)            | 20                    |
| Maksimālais atbildes uzdevuma ilgums                      | 1250 dienas             |
| Maksimālais kopsavilkuma uzdevuma ilgums                 | 3650 dienas (10 gadi)  |
| Maksimālais uzdevumam piešķirto resursu skaits               | 20 resursi          |
| Atbalstītais uzdevuma datumu diapazons                    | 1/1/2000 - 12/31/2149 |
| Kontrolsaraksta elementi                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projekta plānošana paplašināmība un attīstība

Pēc jaunināšanas uz Project Operations ir jāizmanto projektu plānošanas API, lai izpildītu izveides, atjaunināšanas un dzēšanas operācijas ar tālāk norādītajām entītijām.

|   Entītijas nosaukums           |   Entītijas loģiskais nosaukums       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekta uzdevums            | msdyn_projecttask           |
| Projekta uzdevuma atkarība | msdyn_projecttaskdependency |
| Resursu piešķiršana     | msdyn_resourceassignment    |
| Projekta bloks          | msdyn_projectbucket         |
| Projekta grupas dalībnieks     | msdyn_projectteam           |

Ja jums pašlaik ir pielāgojumi, kas saistīti ar šīm entītijām, skatiet rakstu [Projektu grafika API izmantošana, lai veiktu darbības ar plānošanas entītijām](../project-management/schedule-api-preview.md) ieviešanas norādījumiem.

## <a name="data-model-changes"></a>Datu modeļa izmaiņas

1. jaunināšanas fāzes ietvaros datu modelī ir izmaiņas. Šīs izmaiņas galvenokārt ir lauka izmaiņas esošajās entītijās. 1. posmā entītijas, **msydn_project** un **msdyn_projectteam** ir pielāgojumu pārfrāzēšana. 

> [!IMPORTANT]
> Šī sadaļa tiks atjaunināta ar papildu entītijām, kad būs pabeigti turpmākie jaunināšanas posmi.

Tālāk norādītie lauki ir aizstāti ar jauniem laukiem.

|   Tabula          |   Vecais loģiskais nosaukums   |   Jauns loģiskais nosaukums    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Ir pievienoti šādi lauki.

|   Tabula          |   Loģiskais nosaukums                               |   Apraksts |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Parāda projekta faktisko pārdošanas apjomu kopsummu. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Parāda projekta faktisko materiālo izmaksu kopsummu. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Parāda projekta faktisko materiālu pārdošanas apjomu. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Ar šo projektu saistītā līguma līnija. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Šis ir iekšējs sistēmas lauks, kas tiek izmantots kopēšanas **projektam**, kas saistīts ar korelācijas identifikatoru. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Šis ir iekšējs sistēmas lauks, ko izmanto kopēšanas **projektam**, kas saistīts ar sesijas identifikatoru. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Pēdējā sinhronizācija xRM globālās pārskatīšanas marķieris no projekta plānošanas pakalpojuma. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Project dokuments, kas pieder projektam. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projekta plānoto materiālu izmaksu kopsumma. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Projekta plānoto materiālu pārdošanas kopsumma. Lietošanai tikai programmā Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programma, ar kuru ir saistīts šis projekts. |
| msdyn_project     | msdyn_quotelineproject                       | Ar šo projektu saistītā citāta rindiņa. |
| msdyn_project     | msdyn_replaylogheader                        | Atkārtotas atskaņošanas žurnālu galvene. |
| msdyn_project     | msdyn_schedulemode                           | Noklusējuma plānošanas režīms, kas tiek izmantots visiem projekta uzdevumiem.  |
| msdyn_project     | msdyn_taskearlieststart                      | Jebkura projekta uzdevuma agrākais sākuma datums.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projekta komandas loceklis, no kura tika kopēts šis projekta komandas loceklis. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Norāda, vai izveidot resursu nepieciešamību jaunizveidotam vispārīgam darba grupas dalībniekam.  |
| msdyn_projectteam | msdyn_deletestatus                           | Grupas dalībnieka dzēšanas statuss, lai izsekotu, vai projekta plānošanas pakalpojumam ir nosūtīts dzēšanas pieprasījums un vai tas veiksmīgi nosūta atbildi atpakaļ paredzētajā laika logā. |
| msdyn_projectteam | msdyn_effortcompleted                        | Izseko komandas locekļa paveikto darbu uzdevumos. |
| msdyn_projectteam | msdyn_effortremaining                        | Izseko pūlēm, kas komandas dalībniekam vēl ir jāpabeidz savos uzdevumos. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Gaidīšanas periods no brīža, kad darba grupas dalībnieks nosūta dzēšanas pieprasījumu projekta plānošanas pakalpojumam, līdz darba grupas dalībniekam tiek faktiski izdzēsts Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laikspiedols, kas jāieraksta, kad grupas dalībnieka dzēšanas pieprasījums tiek nosūtīts projekta plānošanas pakalpojumam. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rāda projekta darba grupas dalībnieku, no kura ir kopēts šis projekta darba grupas dalībnieks.  |

## <a name="project-templates"></a>Projektu veidnes

Project Operations nenodrošina atbalstu projektu veidnēm. Tomēr lielu daļu pamatfunkciju var atkārtot, izmantojot [project copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Datora pievienojumprogrammu atbalsts

Microsoft Project Desktop pievienojumprogrammas atbalsts nebūs pieejams pirmajos 2 jaunināšanas posmos. 3. posmā klienti, kuru projekti ir lielāki par pašlaik atbalstītajiem Project for the Web ierobežojumiem, varēs izmantot datora pievienojumprogrammu.

## <a name="editing-resource-assignment-contours"></a>Resursu piešķiršanas kontūru rediģēšana

Iespēja rediģēt resursu piešķiršanas kontūras būs pieejama, kad būs pieejama jaunināšanas 2. fāze.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Project Operations ir pievienoti tālāk norādītie jaunie līdzekļi. Šiem līdzekļiem ir papildinošs raksturs, un tie neietekmē Project Service Automation datu modeli.

- [Materiālu lietojuma reģistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Apakšuzņēmuma līgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma nepārsniegšanas statuss un validācijas](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Uz uzdevumiem balstīti norēķini](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Novecojuši komponenti

Tālāk sniegtajās tabulās ir dokumentēti visi novecojušie lauki, kas pēc jaunināšanas tiek pārvietoti uz novecojušo komponentu risinājumu. Papildinformāciju un saiti uz risinājumu skatiet rakstā [Dynamics 365 Project Service Automation 3x līdz Project Operations 4x novecojuši komponenti](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>rēķinsdetail

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_raksturojums                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_nosaukums                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_vērtība                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_apraksts                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransakcijuklasifikācija          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_summa                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_bāzes summa                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_apraksts                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_procentos                                                |
| msdyn_opportunitylinetransaction.msdyn_cena                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_cenrādis                                              |
| msdyn_opportunitylinetransaction.msdyn_produkts                                                |
| msdyn_opportunitylinetransaction.msdyn_projekts                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_vienība                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_apraksts                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_apraksts                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_auto plānošana                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_resursu skaits                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_apraksts                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantkonts                                                        |
| msdyn_projectteam.msdyn_pretendenti pieejami                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_apraksts                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_numurs                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_projekts                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_stundas                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

