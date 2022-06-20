---
title: Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām
description: Šajā rakstā sniegta informācija un paraugi projektu grafika API izmantošanai.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ada06186121d41edddaa06f747b3e1687c303928
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929223"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_



## <a name="scheduling-entities"></a>Plānošanas entītijas

Projekta plānošanas API nodrošina iespēju veikt izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**. Šīs entītijas tiek pārvaldītas, izmantojot projekta tīmekļa plānošanas programmu. Iepriekšējos Dynamics 365 Project Operations laidienos tika ierobežotas izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.

Tālāk sniegtajā tabulā ir sniegts projekta plānošanas entītiju pilns saraksts.

| Entītijas nosaukums  | Entītijas loģiskais nosaukums |
| --- | --- |
| Project | msdyn_project |
| Projekta uzdevums  | msdyn_projecttask  |
| Projekta uzdevuma atkarība  | msdyn_projecttaskdependency  |
| Resursu piešķiršana | msdyn_resourceassignment |
| Projekta bloks  | msdyn_projectbucket |
| Projekta grupas dalībnieks | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet ir darba vienības shēma, ko var izmantot, kad transakcijā ir jāapstrādā vairāki plānošanas ietekmēšanas pieprasījumi.

## <a name="project-schedule-apis"></a>Projekta plānošanas API

Tālāk ir parādīts pašreizējo projekta plānošanas API saraksts.

- **msdyn_CreateProjectV1**: šo API var izmantot, lai izveidotu projektu. Projekts un noklusējuma projekta grupa tiek izveidoti nekavējoties.
- **msdyn_CreateTeamMemberV1**: šo API var izmantot, lai izveidotu projekta darba grupas dalībnieku. Darba grupas dalībnieka ieraksts tiek izveidots nekavējoties.
- **msdyn_CreateOperationSetV1**: šo API var izmantot, lai ieplānotu vairākus pieprasījumus, kas jāveic transakcijā.
- **msdyn_PSSCreateV1**: šo API var izmantot, lai izveidotu entītiju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta izveides operāciju.
- **msdyn_PSSUpdateV1**: šo API var izmantot, lai atjauninātu entītiju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta atjaunināšanas operāciju.
- **msdyn_PSSDeleteV1**: šo API var izmantot, lai dzēstu entītiju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta dzēšanas operāciju.
- **msdyn_ExecuteOperationSetV1**: šis API tiek izmantots, lai izpildītu visas operācijas attiecīgajā operāciju kopā.

## <a name="using-project-schedule-apis-with-operationset"></a>Projekta plānošanas API izmantošana ar OperationSet

Tā kā ieraksti, kuriem ir gan **CreateProjectV1**, gan **CreateTeamMemberV1**, tiek izveidoti nekavējoties, šos API nevar izmantot tieši kopā **OperationSet**. Tomēr API var lietot, lai izveidotu nepieciešamos ierakstus, izveidotu **OperationSet** un pēc tam izmantotu šos iepriekš izveidotos ierakstus kopā **OperationSet**.

## <a name="supported-operations"></a>Atbalstītās operācijas

| Plānošanas entītija | Izveide | Atjauninājums | Delete | Svarīgi ieteikumi |
| --- | --- | --- | --- | --- |
Projekta uzdevums | Jā | Jā | Jā | Laukus **Progress**, **EffortCompleted** un **EffortRemaining** var rediģēt programmā Project for the Web, bet tos nevar rediģēt programmā Project Operations.  |
| Projekta uzdevuma atkarība | Jā |  | Jā | Projekta uzdevumu atkarības ieraksti netiek atjaunināti. Tā vietā var izdzēst vecu ierakstu un izveidot jaunu ierakstu. |
| Resursu piešķiršana | Jā | Jā | | Netiek atbalstītas operācijas ar šādiem laukiem: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** un **PlannedWork**. Resursu piešķiršanas ieraksti netiek atjaunināti. Tā vietā veco ierakstu var izdzēst un izveidot jaunu ierakstu. |
| Projekta bloks | Jā | Jā | Jā | Noklusējuma spainis tiek izveidots, izmantojot **API CreateProjectV1**. Atbalsts projektu kausu izveidei un dzēšanai tika pievienots atjauninājuma laidienā Nr. 16. |
| Projekta darba grupas dalībnieks | Jā | Jā | Jā | Izveides operācijai izmantojiet **CreateTeamMemberV1** API. |
| Project | Jā | Jā |  | Netiek atbalstītas operācijas ar šādiem laukiem: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** un **Duration**. |

Šos API var izsaukt ar entītijas objektiem, kuros ir pielāgoti lauki.

Rekvizīts ID nav obligāts. Ja tas ir nodrošināts, sistēma mēģina to izmantot un rodas izņēmums, ja to nevar izmantot. Ja tas nav nodrošināts, sistēma to ģenerēs.

## <a name="restricted-fields"></a>Ierobežotie lauki

Šajās tabulās ir definēti lauki, kas ir ierobežoti no **izveides** un **rediģēšanas**.

### <a name="project-task"></a>Projekta uzdevums

| Loģiskais nosaukums                           | Var izveidot     | Var rediģēt         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | Nē.             | Nē.               |
| msdyn_actualcost_base                  | Nē.             | Nē.               |
| msdyn_actualend                        | Nē.             | Nē.               |
| msdyn_actualsales                      | Nē.             | Nē.               |
| msdyn_actualsales_base                 | Nē.             | Nē.               |
| msdyn_actualstart                      | Nē.             | Nē.               |
| msdyn_costatcompleteestimate           | Nē.             | Nē.               |
| msdyn_costatcompleteestimate_base      | Nē.             | Nē.               |
| msdyn_costconsumptionpercentage        | Nē.             | Nē.               |
| msdyn_effortcompleted                  | Nē (jā projektam)             | Nē (jā projektam)               |
| msdyn_effortremaining                  | Nē (jā projektam)              | Nē (jā projektam)                |
| msdyn_effortestimateatcomplete         | Nē.             | Nē.               |
| msdyn_iscritical                       | Nē.             | Nē.               |
| msdyn_iscriticalname                   | Nē.             | Nē.               |
| msdyn_ismanual                         | Nē.             | Nē.               |
| msdyn_ismanualname                     | Nē.             | Nē.               |
| msdyn_ismilestone                      | Nē.             | Nē.               |
| msdyn_ismilestonename                  | Nē.             | Nē.               |
| msdyn_LinkStatus                       | Nē.             | Nē.               |
| msdyn_linkstatusname                   | Nē.             | Nē.               |
| msdyn_msprojectclientid                | Nē.             | Nē.               |
| msdyn_plannedcost                      | Nē.             | Nē.               |
| msdyn_plannedcost_base                 | Nē.             | Nē.               |
| msdyn_plannedsales                     | Nē.             | Nē.               |
| msdyn_plannedsales_base                | Nē.             | Nē.               |
| msdyn_pluginprocessingdata             | Nē.             | Nē.               |
| msdyn_progress                         | Nē (jā projektam)             | Nē (jā projektam) |
| msdyn_remainingcost                    | Nē.             | Nē.               |
| msdyn_remainingcost_base               | Nē.             | Nē.               |
| msdyn_remainingsales                   | Nē.             | Nē.               |
| msdyn_remainingsales_base              | Nē.             | Nē.               |
| msdyn_requestedhours                   | Nē.             | Nē.               |
| msdyn_resourcecategory                 | Nē.             | Nē.               |
| msdyn_resourcecategoryname             | Nē.             | Nē.               |
| msdyn_resourceorganizationalunitid     | Nē.             | Nē.               |
| msdyn_resourceorganizationalunitidname | Nē.             | Nē.               |
| msdyn_salesconsumptionpercentage       | Nē.             | Nē.               |
| msdyn_salesestimateatcomplete          | Nē.             | Nē.               |
| msdyn_salesestimateatcomplete_base     | Nē.             | Nē.               |
| msdyn_salesvariance                    | Nē.             | Nē.               |
| msdyn_salesvariance_base               | Nē.             | Nē.               |
| msdyn_scheduleddurationminutes         | Nē.             | Nē.               |
| msdyn_scheduledend                     | Nē.             | Nē.               |
| msdyn_scheduledstart                   | Nē.             | Nē.               |
| msdyn_schedulevariance                 | Nē.             | Nē.               |
| msdyn_skipupdateestimateline           | Nē.             | Nē.               |
| msdyn_skipupdateestimatelinename       | Nē.             | Nē.               |
| msdyn_summary                          | Nē.             | Nē.               |
| msdyn_varianceofcost                   | Nē.             | Nē.               |
| msdyn_varianceofcost_base              | Nē.             | Nē.               |

### <a name="project-task-dependency"></a>Projekta uzdevuma atkarība

| Loģiskais nosaukums                  | Var izveidot     | Var rediģēt     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | Nē.             | Nē.           |
| msdyn_linktypename            | Nē.             | Nē.           |
| msdyn_predecessortask         | Jā            | Nē.           |
| msdyn_predecessortaskname     | Jā            | Nē.           |
| msdyn_project                 | Jā            | Nē.           |
| msdyn_projectname             | Jā            | Nē.           |
| msdyn_projecttaskdependencyid | Jā            | Nē.           |
| msdyn_successortask           | Jā            | Nē.           |
| msdyn_successortaskname       | Jā            | Nē.           |

### <a name="resource-assignment"></a>Resursu piešķiršana

| Loģiskais nosaukums                 | Var izveidot     | Var rediģēt     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Jā            | Nē.           |
| msdyn_bookableresourceidname | Jā            | Nē.           |
| msdyn_bookingstatusid        | Nē.             | Nē.           |
| msdyn_bookingstatusidname    | Nē.             | Nē.           |
| msdyn_committype             | Nē.             | Nē.           |
| msdyn_committypename         | Nē.             | Nē.           |
| msdyn_effort                 | Nē.             | Nē.           |
| msdyn_effortcompleted        | Nē.             | Nē.           |
| msdyn_effortremaining        | Nē.             | Nē.           |
| msdyn_finish                 | Nē.             | Nē.           |
| msdyn_plannedcost            | Nē.             | Nē.           |
| msdyn_plannedcost_base       | Nē.             | Nē.           |
| msdyn_plannedcostcontour     | Nē.             | Nē.           |
| msdyn_plannedsales           | Nē.             | Nē.           |
| msdyn_plannedsales_base      | Nē.             | Nē.           |
| msdyn_plannedsalescontour    | Nē.             | Nē.           |
| msdyn_plannedwork            | Nē.             | Nē.           |
| msdyn_projectid              | Jā            | Nē.           |
| msdyn_projectidname          | Nē.             | Nē.           |
| msdyn_projectteamid          | Nē.             | Nē.           |
| msdyn_projectteamidname      | Nē.             | Nē.           |
| msdyn_start                  | Nē.             | Nē.           |
| msdyn_taskid                 | Nē.             | Nē.           |
| msdyn_taskidname             | Nē.             | Nē.           |
| msdyn_userresourceid         | Nē.             | Nē.           |

### <a name="project-team-member"></a>Projekta darba grupas dalībnieks

| Loģiskais nosaukums                                     | Var izveidot     | Var rediģēt     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | Nē.             | Nē.           |
| msdyn_creategenericteammemberwithrequirementname | Nē.             | Nē.           |
| msdyn_deletestatus                               | Nē.             | Nē.           |
| msdyn_deletestatusname                           | Nē.             | Nē.           |
| msdyn_effort                                     | Nē.             | Nē.           |
| msdyn_effortcompleted                            | Nē.             | Nē.           |
| msdyn_effortremaining                            | Nē.             | Nē.           |
| msdyn_finish                                     | Nē.             | Nē.           |
| msdyn_hardbookedhours                            | Nē.             | Nē.           |
| msdyn_hours                                      | Nē.             | Nē.           |
| msdyn_markedfordeletiontimer                     | Nē.             | Nē.           |
| msdyn_markedfordeletiontimestamp                 | Nē.             | Nē.           |
| msdyn_msprojectclientid                          | Nē.             | Nē.           |
| msdyn_percentage                                 | Nē.             | Nē.           |
| msdyn_requiredhours                              | Nē.             | Nē.           |
| msdyn_softbookedhours                            | Nē.             | Nē.           |
| msdyn_start                                      | Nē.             | Nē.           |

### <a name="project"></a>Project

| Loģiskais nosaukums                           | Var izveidot     | Var rediģēt     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | Nē.             | Nē.           |
| msdyn_actualexpensecost_base           | Nē.             | Nē.           |
| msdyn_actuallaborcost                  | Nē.             | Nē.           |
| msdyn_actuallaborcost_base             | Nē.             | Nē.           |
| msdyn_actualsales                      | Nē.             | Nē.           |
| msdyn_actualsales_base                 | Nē.             | Nē.           |
| msdyn_contractlineproject              | Jā            | Nē.           |
| msdyn_contractorganizationalunitid     | Jā            | Nē.           |
| msdyn_contractorganizationalunitidname | Jā            | Nē.           |
| msdyn_costconsumption                  | Nē.             | Nē.           |
| msdyn_costestimateatcomplete           | Nē.             | Nē.           |
| msdyn_costestimateatcomplete_base      | Nē.             | Nē.           |
| msdyn_costvariance                     | Nē.             | Nē.           |
| msdyn_costvariance_base                | Nē.             | Nē.           |
| msdyn_duration                         | Nē.             | Nē.           |
| msdyn_effort                           | Nē.             | Nē.           |
| msdyn_effortcompleted                  | Nē.             | Nē.           |
| msdyn_effortestimateatcompleteeac      | Nē.             | Nē.           |
| msdyn_effortremaining                  | Nē.             | Nē.           |
| msdyn_finish                           | Jā            | Jā          |
| msdyn_globalrevisiontoken              | Nē.             | Nē.           |
| msdyn_islinkedtomsprojectclient        | Nē.             | Nē.           |
| msdyn_islinkedtomsprojectclientname    | Nē.             | Nē.           |
| msdyn_linkeddocumenturl                | Nē.             | Nē.           |
| msdyn_msprojectdocument                | Nē.             | Nē.           |
| msdyn_msprojectdocumentname            | Nē.             | Nē.           |
| msdyn_plannedexpensecost               | Nē.             | Nē.           |
| msdyn_plannedexpensecost_base          | Nē.             | Nē.           |
| msdyn_plannedlaborcost                 | Nē.             | Nē.           |
| msdyn_plannedlaborcost_base            | Nē.             | Nē.           |
| msdyn_plannedsales                     | Nē.             | Nē.           |
| msdyn_plannedsales_base                | Nē.             | Nē.           |
| msdyn_progress                         | Nē.             | Nē.           |
| msdyn_remainingcost                    | Nē.             | Nē.           |
| msdyn_remainingcost_base               | Nē.             | Nē.           |
| msdyn_remainingsales                   | Nē.             | Nē.           |
| msdyn_remainingsales_base              | Nē.             | Nē.           |
| msdyn_replaylogheader                  | Nē.             | Nē.           |
| msdyn_salesconsumption                 | Nē.             | Nē.           |
| msdyn_salesestimateatcompleteeac       | Nē.             | Nē.           |
| msdyn_salesestimateatcompleteeac_base  | Nē.             | Nē.           |
| msdyn_salesvariance                    | Nē.             | Nē.           |
| msdyn_salesvariance_base               | Nē.             | Nē.           |
| msdyn_scheduleperformance              | Nē.             | Nē.           |
| msdyn_scheduleperformancename          | Nē.             | Nē.           |
| msdyn_schedulevariance                 | Nē.             | Nē.           |
| msdyn_taskearlieststart                | Nē.             | Nē.           |
| msdyn_teamsize                         | Nē.             | Nē.           |
| msdyn_teamsize_date                    | Nē.             | Nē.           |
| msdyn_teamsize_state                   | Nē.             | Nē.           |
| msdyn_totalactualcost                  | Nē.             | Nē.           |
| msdyn_totalactualcost_base             | Nē.             | Nē.           |
| msdyn_totalplannedcost                 | Nē.             | Nē.           |
| msdyn_totalplannedcost_base            | Nē.             | Nē.           |

### <a name="project-bucket"></a>Projekta bloks

| Loģiskais nosaukums          | Var izveidot      | Var rediģēt     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Jā             | Nē.           |
| msdyn_name            | Jā             | Jā          |
| msdyn_project         | Jā             | Nē.           |
| msdyn_projectbucketid | Jā             | Nē.           |

## <a name="limitations-and-known-issues"></a>Zināmās problēmas un ierobežojumi
Tālāk ir saraksts ar ierobežojumiem un zināmajām problēmām.

- Projektu grafika API var izmantot **tikai lietotāji ar Microsoft Project licenci**. Tos nevar izmantot tālāk minētie lietotāji.

    - Programmas lietotāji
    - Sistēmas lietotāji
    - Integrācijas lietotāji
    - Citi lietotāji, kuriem nav nepieciešamās licences

- Katrai **OperationSet** var būt ne vairāk par 100 operācijām.
- Katram lietotājam var būt ne vairāk par 10 atvērtām **OperationSets**.
- Project Operations pašlaik atbalsta ne vairāk kā 500 uzdevumu vienā projektā.
- **OperationSet** kļūmes statusa un kļūmju žurnāli pašlaik nav pieejami.
- [Projektu un uzdevumu ierobežojumi un robežas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Kļūdu apstrāde

- Lai pārskatītu operāciju kopās ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **Operāciju kopas**.
- Lai pārskatītu projekta plānošanas pakalpojuma ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānošanas integrācija** \> **PSS kļūdu žurnāli**.

## <a name="sample-scenario"></a>Scenārija paraugs

Šādā scenārijā jums būs jāizveido projekts, darba grupas dalībnieks, četri uzdevumi un divi resursu piešķīrumi. Pēc tam jūs atjaunināsiet vienu uzdevumu, atjaunināsiet projektu, izdzēsiet vienu uzdevumu, izdzēsiet vienu resursa piešķīrumu un izveidosiet uzdevuma atkarību.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Papildu paraugi

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
   
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
