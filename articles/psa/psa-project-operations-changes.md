---
title: Līdzekļu izmaiņas no Project Service Automation uz Project Operations
description: Šajā rakstā sniegts pārskats par līdzekļu izmaiņām no project service automation uz Dynamics 365 Project Operations.
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
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925359"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Līdzekļu izmaiņas no Project Service Automation uz Project Operations

Jauninājums no Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations Lite tiks piegādāts trīs posmos. Šajā rakstā ir sniegta informācija par galvenajām izmaiņām, kuras var sagaidīt, kad jaunināšana būs pabeigta.

| Jaunināšanas piegāde | 1. posms <br>(2022. gada janvāris) | 2. posms <br>(Aprīļa vilnis 2022) | 3. posms  |
|------------------|------------------------|---------------------------|---------------------------|
| Nav atkarības no projektu darba sadalījuma struktūras (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS ir iekļauta pašlaik atbalstītajos projektu operāciju ierobežojumos. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS ārpus pašlaik atbalstītajiem projekta operāciju ierobežojumiem, ieskaitot atbalstu projekta darbvirsmas klientam. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projekta pārvaldība

Būtiskākās izmaiņas lietotāju pieredzē būs projektu plānošanas jomā. Projekta operācijas pieņem jaunu modernu pieredzi darba sadalījuma struktūras (WBS) pārvaldībā, izmantojot plānošanas iespējas, ko [nodrošina project tīmeklim](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Plānošanas pieredzes atšķirības

Šajā tabulā ir apkopotas plānošanas atšķirības starp projektu pakalpojumu automatizāciju un projekta operācijām.

|  Ieplānošana     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektu veidnes — iespēja definēt un lietot projektu veidnes, veidojot projektu  |  &nbsp;    | :heavy_check_mark: |
| Projekta darba sadalījuma struktūras (WBS) integrācija ar darbvirsmas klientu   |    &nbsp;  | :heavy_check_mark: |
| Ierobežojumi - sākt ne agrāk kā, pabeigt ne vēlāk kā  | :heavy_check_mark: |   &nbsp;  |
| Atskaites punkti - uzdevumi ar nulles ilgumu   | :heavy_check_mark:  |  &nbsp;  |
| Uz resursiem balstīti uzdevumi ņems vērā piešķirto resursu pieejamību   | :heavy_check_mark: |  &nbsp;    |
| Rediģēšana laikā - plānu rediģēšana un darbs katru dienu   |   &nbsp;  | :heavy_check_mark: |
| Automātiska/manuāla plānošana — izmantojiet projektu plānošanas programmu, lai automātiski vai manuāli plānotu uzdevumus |  &nbsp; | :heavy_check_mark:  |
| Rediģēt lielus projektus tieši lietotāja interfeisā: Rediģējamo plānu lielumam nav ierobežojumu  | 500 uzdevumu ierobežojums  | :heavy_check_mark:       |
| Pabeigts procentos — atzīmējiet uzdevuma norisi   | :heavy_check_mark:  |  &nbsp;  |
| [Projekta grafika režīmi](../project-management/scheduling-modes.md) — definējiet projektu kā fiksētas vienības, fiksētas piepūles vai fiksēta ilguma | :heavy_check_mark: | &nbsp; |
| Laika skala — izveidojiet un pielāgojiet laika skalas skatu, lai vizualizētu detalizētu informāciju par grafiku un sazinātos ar ieinteresētajām personām. | :heavy_check_mark:  | &nbsp; |
| Uz piepūli balstīti uzdevumi - programmas atbalsta plānošana uzdevuma plānošanai kā piepūles virzītam uzdevumam  | :heavy_check_mark:  | &nbsp; |
| **Dialoglodziņš Uzdevuma informācija** — uzdevuma detalizētās informācijas saglabāšana, izmantojot dialoglodziņu | :heavy_check_mark:  |  &nbsp;  |
| Vilkšana un nomešana - vairākatlasiet uzdevumus un modificējiet to pozīciju WBS | :heavy_check_mark: | &nbsp;  |
| Elastīgi pastāvīgi skati — definējiet detalizētākus uzdevumu atribūtu skatus   | :heavy_check_mark:  | &nbsp; |
| WBS kārtošana un filtrēšana  | :heavy_check_mark:  | &nbsp; |
| Dēļu skats projektu piegādei, kas nav ūdenskrituma projekts  | :heavy_check_mark:   | &nbsp; |
| Laika skalas skats - interaktīvā Ganta diagramma, ko izmanto WBS vizualizēšanai un rediģēšanai   | :heavy_check_mark:  | &nbsp; |
| Īsinājumtaustiņi — īsinājumtaustiņu izmantošana bieži lietotām darbībām, piemēram, atkāpei vai ievietošanai  | :heavy_check_mark:  |  &nbsp; |
| Daudzlīmeņu atsaukšana - veiciet iespēju analīzi, lai pilnībā izprastu izmaiņu ietekmi, atceļot un atkārtoti piemērojot visu darbību kopumu | :heavy_check_mark: | &nbsp; |
| Izgriezt/kopēt/ielīmēt - sadarbojieties grafika izstrādē, kopējot un ielīmējot detalizētu informāciju par grafiku starp lietojumprogrammām  | :heavy_check_mark: | &nbsp; |
| Uzdevumu kontrolsaraksti — uzdevumam pievienojiet līdz 20 kontrolsaraksta elementiem   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektu plānošana

Projekta **operāciju lapā Projekts** ir ievērojamas atšķirības salīdzinājumā **ar projektu pakalpojumu automatizācijas lapu Projekts**.

1. posma jauninājuma **ietvaros no lapas Projekti** ir izņemtas šādas darbības:

  - **Atvērt programmā MS Project**
  - **Izveidot veidni**
  - **Atcelt saistību ar MS Project**

**Projekta operāciju lapā Projekts** ir iekļautas šādas jaunas cilnes.

- **Materiālu aprēķini**
- **Uzdevuma norēķinu iestatīšana**

Cilne **Statuss** ir noņemta, **un lauks Statuss** tagad **atrodas cilnē Kopsavilkums** ar projekta plānošanas režīmu.

   ![Lapas Projekts atjauninājumi.](media/projectform.png)

Cilne **Grafiks** ir pārdēvēta par cilni Uzdevums **,** un tajā ir redzama jaunā projekta plānošanas pieredze ar programmu Project for the Web.

   ![Cilne Jauni projekta uzdevumi.](media/tasktab.png)

## <a name="scheduling-modes"></a>Plānošanas režīmi

Projekta operācijas ir ieviesušas jaunu funkciju Plānošanas [režīmi](../project-management/scheduling-modes.md). Visi esošie projektu pakalpojumu automatizācijas projekti projekta operācijās pēc noklusējuma **būs fiksēts ilgums**. Tomēr jaunu projektu noklusējumu var pārvaldīt, dodoties uz **Iestatījumu** > **parametru** > **parametru** > **grafika režīmu**.

   ![Projekta parametru iestatījumi grafika režīmam.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekta plānošanas ierobežojumi

Projekta operācijas paļaujas uz Web projektu visām projekta plānošanas operācijām. Web projekts pārvalda darba sadalījuma struktūru, izmantojot šajā tabulā norādītos ierobežojumus.

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

## <a name="project-planning-extensibility-and-development"></a>Projektu plānošanas paplašināmība un izstrāde

Pēc jaunināšanas uz projekta operācijām ir jāizmanto projektu plānošanas API, lai izpildītu izveides, atjaunināšanas un dzēšanas operācijas šādās entītijās:

|   Entītijas nosaukums           |   Entītijas loģiskais nosaukums       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekta uzdevums            | msdyn_projecttask           |
| Projekta uzdevuma atkarība | msdyn_projecttaskdependency |
| Resursu piešķiršana     | msdyn_resourceassignment    |
| Projekta bloks          | msdyn_projectbucket         |
| Projekta grupas dalībnieks     | msdyn_projectteam           |

Ja pašlaik ir pielāgojumi, kuros iesaistītas šīs entītijas, skatiet rakstu [Projekta grafika API izmantošana, lai veiktu ieviešanas vadlīnijas ar plānošanas entītijām](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Datu modeļa izmaiņas

Jaunināšanas 1. fāzes ietvaros ir izmaiņas datu modelī. Šīs izmaiņas galvenokārt ir lauka izmaiņas esošajās entītijās. 1. fāzē entītijas, **msydn_project** un **msdyn_projectteam** ir pielāgojumu pārfaktorēšana. 

> [!IMPORTANT]
> Šī sadaļa tiks atjaunināta ar papildu entītijām, kad tiks pabeigti turpmākie jaunināšanas posmi.

Šie lauki ir aizstāti ar jauniem laukiem.

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
| msdyn_project     | msdyn_actualfeesales                         | Rāda projekta faktisko papildmaksu pārdošanas apjomu apkopojumu. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_actualmaterialcost                     | Rāda projekta faktisko materiālu izmaksu kopsummu. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_actualmaterialsales                    | Rāda projekta faktisko materiālu pārdošanas apjomu apkopojumu. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Ar šo projektu saistītā līguma rinda. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Šis ir iekšējais sistēmas lauks, kas tiek izmantots projekta **kopēšanai**, kas saistīta ar korelācijas identifikatoru. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Šis ir iekšējais sistēmas lauks, ko izmanto, lai kopētu **projektu**, kas saistīts ar sesijas identifikatoru. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Pēdējās sinhronizācijas xRM globālās pārskatīšanas pilnvaras no projekta plānošanas pakalpojuma. |
| msdyn_project     | msdyn_msprojectdocument                      | Projektam piederošais Microsoft Project dokuments. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projekta plānoto materiālu izmaksu kopums. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Projektā plānoto materiālu pārdošanas apjomu kopums. Izmantošanai tikai projektu pakalpojumu automatizācijā. |
| msdyn_project     | msdyn_program                                | Programma, ar kuru ir saistīts šis projekts. |
| msdyn_project     | msdyn_quotelineproject                       | Ar šo projektu saistītā piedāvājuma rinda. |
| msdyn_project     | msdyn_replaylogheader                        | Atkārtojuma žurnālu galvene. |
| msdyn_project     | msdyn_schedulemode                           | Noklusējuma plānošanas režīms, kas tiek izmantots visiem projekta uzdevumiem.  |
| msdyn_project     | msdyn_taskearlieststart                      | Jebkura projekta uzdevuma agrākais sākuma datums.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projekta komandas dalībnieks, no kura tika kopēts šis projekta grupas dalībnieks. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Norāda, vai izveidot resursu vajadzību jaunizveidotam vispārējam grupas dalībniekam.  |
| msdyn_projectteam | msdyn_deletestatus                           | Grupas dalībnieka dzēšanas statuss, lai izsekotu, vai pakalpojumam Projektu plānošana ir nosūtīts dzēšanas pieprasījums un vai tas veiksmīgi nosūta atbildi atpakaļ paredzētajā laika logā. |
| msdyn_projectteam | msdyn_effortcompleted                        | Izseko komandas dalībnieka paveikto darbu viņu uzdevumos. |
| msdyn_projectteam | msdyn_effortremaining                        | Izseko pūles, kas komandas dalībniekam vēl jāpabeidz viņu uzdevumos. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Gaidīšanas periods no brīža, kad grupas dalībnieks nosūta dzēšanas pieprasījumu pakalpojumam Projektu plānošana, līdz grupas dalībnieks tiek faktiski izdzēsts programmā Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laikspiedols, kas jāreģistrē, kad grupas dalībnieks dzēš pieprasījumu, tiek nosūtīts uz projektu plānošanas pakalpojumu. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rāda projekta darba grupas dalībnieku, no kura ir kopēts šis projekta darba grupas dalībnieks.  |

## <a name="project-templates"></a>Projektu veidnes

Projekta operācijas nenodrošina atbalstu projektu veidnēm. Tomēr jūs varat atkārtot lielu daļu pamatfunkcijas, izmantojot projekta kopēšanas [API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Darbvirsmas pievienojumprogrammas atbalsts

Microsoft Project Desktop pievienojumprogrammas atbalsts nebūs pieejams jaunināšanas pirmajos 2 posmos. 3. posmā klienti, kuru projekti ir lielāki par pašlaik atbalstītajiem Project ierobežojumiem tīmeklim, varēs izmantot darbvirsmas pievienojumprogrammu.

## <a name="editing-resource-assignment-contours"></a>Resursu piešķires kontūru rediģēšana

Iespēja rediģēt resursu piešķiršanas kontūras būs pieejama, kad būs pieejama jaunināšanas 2. fāze.

## <a name="billing-and-pricing"></a>Cenu noteikšana un norēķini

Projekta operācijās ir pievienoti šādi jauni līdzekļi. Šīs funkcijas ir papildinošas un neietekmē projektu pakalpojumu automatizācijas datu modeli.

- [Materiālu lietojuma reģistrēšana projektos un projekta uzdevumos](../material/material-usage-log.md)
- [Apakšuzņēmuma līgumu pārvaldība](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi un līgumi, kuru pamatā ir saistības](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Līguma vērtība, kas nepārsniedz statusu un pārbaudes](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Uz uzdevumiem balstīti norēķini](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Novecojuši komponenti

Šajās tabulās ir dokumentēti visi novecojušie lauki, kas tiek pārvietoti uz novecojušo komponentu risinājumu pēc jaunināšanas. Plašāku informāciju un saiti uz risinājumu skatiet rakstā [Dynamics 365 Project Service Automation 3x uz Project Operations 4x novecojuši komponenti.](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution)

### <a name="invoicedetail"></a>Rēķinu detail

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
| msdyn_opportunitylinetransaction.msdyn_exchangerated                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_cenrādis                                              |
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
| msdyn_projecttaskstatususer.msdyn_expectedhoursto completelete                                     |
| msdyn_projecttaskstatususer.msdyn_is completed                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Kolonnas                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantspieejams                                                   |
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

