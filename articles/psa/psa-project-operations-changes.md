---
title: Līdzekļu izmaiņas no Project Service Automation uz Project Operations
description: Šajā rakstā sniegts pārskats par Project Service Automation izmaiņām programmā Dynamics 365 Project Operations.
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

Atjauninājums no Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations Lite tiks nodrošināts trīs posmos. Šajā rakstā ir sniegta informācija par galvenajām izmaiņām, kuras varētu tikt ieviestas pēc jaunināšanas izpildes.

| Jauninājuma nodrošināšana | 1. posms: <br>(2022. gada janvāris) | 2. posms: <br>(2022. gada novembris) | 3. posms:  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektiem nav atkarības no darba sadalījuma struktūras (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS ir iekļauts pašlaik atbalstītos Project Operations ierobežojumos. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem Project Operations ierobežojumiem, tostarp Project Desktop Client atbalsta. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projekta pārvaldība

Svarīgākās lietotāju pieredzes izmaiņas būs projekta plānošanas jomā. Project Operations izmanto jaunu modernu pieredzi darba sadalījuma struktūras (WBS) pārvaldīšanā, izmantojot [Project for the Web ](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) nodrošinātās plānošanas iespējas.

## <a name="differences-in-the-scheduling-experience"></a>Plānošanas funkcionalitāšu atšķirības

Tabulā tālāk apkopotas Project Service Automation un Project Operations plānošanas atšķirības.

|  Ieplānošana     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projekta veidnes — iespēja definēt un lietot projekta veidnes projekta izveides laikā  |  &nbsp;    | :heavy_check_mark: |
| Projekta darba sadalījuma struktūras (WBS) integrācija ar Desktop Client   |    &nbsp;  | :heavy_check_mark: |
| Ierobežojumi — sākt ne agrāk kā, pabeigt ne vēlāk kā  | :heavy_check_mark: |   &nbsp;  |
| Atskaites punkti — uzdevumi, kuru ilgums ir nulle   | :heavy_check_mark:  |  &nbsp;  |
| Resursu vadītos uzdevumos tiks ņemta vērā piešķirto resursu pieejamība   | :heavy_check_mark: |  &nbsp;    |
| Pakāpeniska rediģēšana — plānu rediģēšana un darbs no dienas uz dienu   |   &nbsp;  | :heavy_check_mark: |
| Automātiska/manuāla plānošana — izmantojiet projekta plānošanas programmu, lai automātiski vai manuāli plānotu uzdevumus |  &nbsp; | :heavy_check_mark:  |
| Rediģējiet apjomīgus projektus tieši lietotāja saskarnē: nav ierobežots rediģējamo plānu lielums  | 500 uzdevumu ierobežojums  | :heavy_check_mark:       |
| Pabeigtā daļa - atzīmējiet uzdevuma progresu   | :heavy_check_mark:  |  &nbsp;  |
| [Projekta grafika režīmi](../project-management/scheduling-modes.md) — definējiet projektu kā fiksētas vienības, fiksētu piepūli vai fiksētu ilgumu | :heavy_check_mark: | &nbsp; |
| Laika skalas — izveidojiet un pielāgojiet laika skalas skatu, lai vizualizētu grafika informāciju un sazinātos ar iesaistītajām pusēm. | :heavy_check_mark:  | &nbsp; |
| No piepūles vadīti uzdevumi — plānošanas programmas atbalsts uzdevuma kā no piepūles atkarīgai plānošanai  | :heavy_check_mark:  | &nbsp; |
| Dialoglodziņš **Informācija par uzdevumu** — Saglabājiet uzdevuma informāciju, izmantojot dialoglodziņu | :heavy_check_mark:  |  &nbsp;  |
| Velciet un nometiet — vairākatlasot uzdevumus un modificējiet to pozīciju WBS | :heavy_check_mark: | &nbsp;  |
| Elastīgi, mainīgi skati — definējiet daudz lielākus uzdevumu atribūtu skatus   | :heavy_check_mark:  | &nbsp; |
| WBS kārtošana un filtrēšana  | :heavy_check_mark:  | &nbsp; |
| Paneļu skats projekta piegādei bez kaskādes  | :heavy_check_mark:   | &nbsp; |
| Laika grafika skats — interaktīvā Ganta diagramma, ko izmanto WBS vizualizācijai un rediģēšanai   | :heavy_check_mark:  | &nbsp; |
| Īsinājumtaustiņi — izmantojiet īsinājumtaustiņus, kas tiek lietoti biežāk lietotajām operācijām, piemēram, atkāpēm vai ievietošanai  | :heavy_check_mark:  |  &nbsp; |
| Vairāku līmeņu atsaukšana — veiciet iespēju analīzi, lai pilnībā izprastu izmaiņu ietekmi, atgriežot un atkārtoti izmantojot visu operāciju kopu | :heavy_check_mark: | &nbsp; |
| Izgriezt/kopēt/ielīmēt — sadarbība plānošanas izstrādes laikā, kopējot un ielīmējot grafika informāciju no vienas lietojumprogrammas citā.  | :heavy_check_mark: | &nbsp; |
| Uzdevumu kontrolsaraksti — pievienojiet uzdevumam līdz 20 kontrolsarakstiem   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektu plānošana

Project Operations lapā **Projekts** ir ievērojams skaits atšķirību, salīdzinot ar Project Service Automation lapu **Projekts**.

1. posma atjauninājuma ietvaros no lapas **Projekti** ir noņemtas tālāk uzskaitītās darbības:

  - **Atvērt programmā MS Project**
  - **Izveidot veidni**
  - **Atcelt saistību ar MS Project**

Project Operations lapai **Project** ir tālāk uzskaitītās jaunās cilnes.

- **Materiālu aprēķini**
- **Uzdevuma norēķinu iestatīšana**

Ir noņemta cilne **Statuss**, un lauks **Statuss** turpmāk atrodas cilnē **Kopsavilkums** ar projekta plānošanas režīmu.

   ![Projekta lapas atjauninājumi.](media/projectform.png)

Cilne **Grafiks** ir pārdēvēta par cilni **Uzdevums**, un tai ir jauna projektu plānošanas funkcionalitāte, izmantojot Project for the Web.

   ![Jauna projekta uzdevumu cilne.](media/tasktab.png)

## <a name="scheduling-modes"></a>Plānošanas režīmi

Project Operations ir ieviesuši jaunu līdzekli — [Plānošanas režīmi](../project-management/scheduling-modes.md). Visi esošie Project Service Automation projekti programmā Project Operations tiks pēc noklusējuma iestatīti uz **fiksētu ilgumu**. Taču jauno projektu noklusējuma vērtību var pārvaldīt, dodoties uz **Iestatījumi** > **Parametri** > **Parametrs** > **Grafika režīms**.

   ![Projekta parametru iestatījumi Plānošanas režīmam.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekta plānošanas robežas

Project Operations visām projekta plānošanas darbībām izmanto Project for the Web. Project for the Web pārvalda darba sadalījuma struktūru, izmantojot robežas, kas norādītas tabulā tālāk.

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

## <a name="project-planning-extensibility-and-development"></a>Projektu plānošanas paplašināmība un attīstīšana

Pēc jaunināšanas uz Project Operations, ir jāizmanto Project Scheduling API, lai veiktu izveides, jaunināšanas un dzēšanas darbības tālāk uzskaitītajiem elementiem:

|   Entītijas nosaukums           |   Entītijas loģiskais nosaukums       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekta uzdevums            | msdyn_projecttask           |
| Projekta uzdevuma atkarība | msdyn_projecttaskdependency |
| Resursu piešķiršana     | msdyn_resourceassignment    |
| Projekta bloks          | msdyn_projectbucket         |
| Projekta grupas dalībnieks     | msdyn_projectteam           |

Ja pašlaik ir pielāgojumi, kas ietver šos elementus, skat. lapu [Project Schedule API izmantošana, lai veiktu darbības ar plānošanas elementiem](../project-management/schedule-api-preview.md), kurā sniegti norādījumi par ieviešanu.

## <a name="data-model-changes"></a>Datu modeļu izmaiņas

Jaunināšanas 1. posma ietvaros tiek veiktas izmaiņas datu modelī. Šīs izmaiņas primāri ir esošo entītiju lauka izmaiņas. 1. posmā elementi **msydn_project** un **msdyn_projectteam** ir pārstrukturēti pielāgojumi. 

> [!IMPORTANT]
> Šī sadaļa tiks jaunināta ar papildu elementiem, kad tiks pabeigti tālāki jaunināšanas posmi.

Tālāk uzskaitītie lauki ir aizstāti ar jauniem laukiem.

|   Tabula          |   Iepriekšējais loǵiskais nosaukums   |   Jaunais loǵiskais nosaukums    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Ir pievienoti tālāk uzskaitītie lauki.

|   Tabula          |   Loģiskais nosaukums                               |   Apraksts |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Rāda apkopoto faktisko izmaksu pārdošanu projektā. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Rāda apkopotās faktiskās materiālu izmaksas projektā. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Rāda apkopoto faktisko materiālu pārdošanu projektā. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Ar šo projektu saistītā līguma rinda. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Iekšējs sistēmas lauks, ko izmanto ar Correlation Identifier saistīto **Kopijas projektu**. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Iekšējs sistēmas lauks, ko izmanto ar Session Identifier saistīto **Kopijas projektu**. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Pēdējās sinhronizācijas xRM Global Revision marḱieris no Project Scheduling Service. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Project dokuments, kas ietilpst projektā. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Plānoto projekta materiālu izmaksu apkopojums. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Plānoto projekta materiālu pārdošanas apkopojums. Lietošanai vienīgi programmā Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programma, ar kuru ir saistīts šis projekts. |
| msdyn_project     | msdyn_quotelineproject                       | Ar šo projektu saistītā piedāvājuma rinda. |
| msdyn_project     | msdyn_replaylogheader                        | Atkārtojuma žurnālu galvene. |
| msdyn_project     | msdyn_schedulemode                           | Noklusējuma plānošanas režīms, kas tiek izmantots visiem projekta uzdevumiem.  |
| msdyn_project     | msdyn_taskearlieststart                      | Jebkura projekta uzdevuma agrākais sākuma datums.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rāda projekta darba grupas dalībnieku, no kura ir kopēts šis projekta darba grupas dalībnieks. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Norāda, vai jāizveido resursa prasība jaunajam vispārējam darba grupas dalībniekam.  |
| msdyn_projectteam | msdyn_deletestatus                           | Darba grupas dalībnieka dzēšanas statuss, lai izsekotu, vai uz PSS ir nosūtīts dzēšanas pieprasījums un vai Project Scheduling Service nosūta atbildi sekmīgi un paredzētajā laika periodā. |
| msdyn_projectteam | msdyn_effortcompleted                        | Izseko darba grupas dalībnieka veiktajiem pūliņiem, pildot savu uzdevumu. |
| msdyn_projectteam | msdyn_effortremaining                        | Izsekot pūliņiem, kas darba grupas dalībniekam vēl jāpieliek, pildot savus uzdevumus. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Gaidīšanas laiks no brīža, kad darba grupas dalībnieks nosūta Project Scheduling Service dzēšanas pieprasījumu, līdz darba grupas dalībnieks tiek faktiski dzēsts no Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laikspiedols, lai reǵistrētu laiku, kurā darba grupas dalībnieka dzēšanas pieprasījums ir nosūtīts programmai Project Scheduling Service. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rāda projekta darba grupas dalībnieku, no kura ir kopēts šis projekta darba grupas dalībnieks.  |

## <a name="project-templates"></a>Projektu veidnes

Project Operations nenodrošina projektu veidņu atbalstu. Tomēr, izmantojot [Projekta kopijas API](../project-management/dev-copy-project.md), varat replicēt lielu daļu pamata funkcionalitātes.

## <a name="desktop-add-in-support"></a>Datora pievienojumprogrammas atbalsts

Atbalsts Microsoft Project Desktop pievienojumprogrammai nebūs pieejams jaunināšanas pirmajās 2 versijās. 3. posmā klienti, kuriem ir projekti, kas pārsniedz pašlaik atbalstītos Project for the Web ierobežojumus, varēs izmantot datora pievienojumprogrammu.

## <a name="editing-resource-assignment-contours"></a>Resursu piešķiršanas kontūru rediģēšana

Iespēja rediģēt resursu piešķiršanas palīgus būs pieejama, kad būs pieejams jaunināšanas 2. posms.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Programmai Project Operations ir pievienoti tālāk uzskaitītie jaunie līdzekļi. Šie līdzekļi ir papildināmi pēc dabas, un tie neietekmē Project Service Automation datu modeli.

- [Materiālu lietojuma reǵistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Pakārtotā pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līgums, kas nepārsniedz statusu un pārbaudes](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Uzdevumā balstīta norēķinu iestatīšana](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Novecojušie komponenti

Tabulās tālāk aprakstīti visi novecojušie lauki, kas pēc jaunināšanas pārcelti uz novecojušo komponentu risinājumu. Papildinformāciju un saiti uz risinājumu skatiet sadaļā [Dynamics 365 Project Service Automation 3x uz Project Operations 4x novecojušajiem komponentiem ](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

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
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
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
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
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
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
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

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_opportunitylinetransactionclassificatio

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
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
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
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
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
| msdyn_projecttransactioncategory.msdyn_project                                                |
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
| msdyn_resourceassignment.msdyn_hours                                                          |
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

