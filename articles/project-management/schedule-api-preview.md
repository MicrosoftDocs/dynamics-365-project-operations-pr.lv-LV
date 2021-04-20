---
title: Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām
description: Šajā tēmā ir sniegta informācija un piemēri plānošanas API izmantošanai.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868138"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

> [!IMPORTANT] 
> Daļa vai visa šajā tēmā norādītā funkcionalitāte ir pieejama lietotājiem kā daļa no priekšskatījuma laidiena. Saturs un funkcionalitāte var mainīties. 

## <a name="scheduling-entities"></a>Plānošanas entītijas

Plānošanas API nodrošina iespēju veikt izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**. Šīs entītijas tiek pārvaldītas, izmantojot projekta tīmekļa plānošanas programmu. Iepriekšējos Dynamics 365 Project Operations laidienos tika ierobežotas izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.

Tālāk sniegtajā tabulā ir sniegts pilnīgs **plānošanas entītiju** saraksts.

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

## <a name="schedule-apis"></a>Plānošanas API

Tālāk ir saraksts ar pašreizējiem plānošanas API.

- **msdyn_CreateProjectV1**: šo API var izmantot, lai izveidotu projektu. Nekavējoties tiek izveidots projekts un noklusējuma projekta bloks.
- **msdyn_CreateTeamMemberV1**: šo API var izmantot, lai izveidotu projekta darba grupas dalībnieku. Darba grupas dalībnieka ieraksts tiek izveidots nekavējoties.
- **msdyn_CreateOperationSetV1**: šo API var izmantot, lai ieplānotu vairākus pieprasījumus, kas jāveic transakcijā.
- **msdyn_PSSCreateV1**: šo API var izmantot, lai izveidotu entītiju. Entītija var būt jebkura no plānošanas entītijām, kas atbalsta izveides operāciju.
- **msdyn_PSSUpdateV1**: šo API var izmantot, lai atjauninātu entītiju. Entītija var būt jebkura no plānošanas entītijām, kas atbalsta atjaunināšanas operāciju.
- **msdyn_PSSDeleteV1**: šo API var izmantot, lai dzēstu entītiju. Entītija var būt jebkura no plānošanas entītijām, kas atbalsta dzēšanas operāciju.
- **msdyn_ExecuteOperationSetV1**: šis API tiek izmantots, lai izpildītu visas operācijas attiecīgajā operāciju kopā.

## <a name="using-schedule-apis-with-operationset"></a>Plānošanas API izmantošana ar OperationSet

Tā kā ieraksti, kuriem ir gan **CreateProjectV1**, gan **CreateTeamMemberV1**, tiek izveidoti nekavējoties, šos API nevar izmantot tieši kopā **OperationSet**. Tomēr API var lietot, lai izveidotu nepieciešamos ierakstus, izveidotu **OperationSet** un pēc tam izmantotu šos iepriekš izveidotos ierakstus kopā **OperationSet**.

## <a name="supported-operations"></a>Atbalstītās operācijas

| Plānošanas entītija | Izveide | Atjaunināšana | Delete | Svarīgi ieteikumi |
| --- | --- | --- | --- | --- |
Projekta uzdevums | Jā | Jā | Jā | Nevienu |
| Projekta uzdevuma atkarība | Jā | Jā | | Projekta uzdevumu atkarības ieraksti netiek atjaunināti. Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu. |
| Resursu piešķiršana | Jā | Jā | | Netiek atbalstītas operācijas ar šādiem laukiem: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** un **PlannedWork**. Resursu piešķiršanas ieraksti netiek atjaunināti. Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu. |
| Projekta bloks | Nav attiecināms | Nav attiecināms | Nav attiecināms | Noklusējuma bloks tiek izveidots, izmantojot **CreateProjectV1** API. |
| Projekta darba grupas dalībnieks | Jā | Jā | Jā | Izveides operācijai izmantojiet **CreateTeamMemberV1** API. |
| Project | Jā | Jā | Nav attiecināms | Netiek atbalstītas operācijas ar šādiem laukiem: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** un **Duration**. |

Šos API var izsaukt ar entītijas objektiem, kuros ir pielāgoti lauki.

Rekvizīts ID nav obligāts. Ja tas ir nodrošināts, sistēma mēģina to izmantot un rodas izņēmums, ja to nevar izmantot. Ja tas nav nodrošināts, sistēma to ģenerēs.

## <a name="limitations-and-known-issues"></a>Zināmās problēmas un ierobežojumi
Tālāk ir saraksts ar ierobežojumiem un zināmajām problēmām.

- Plānošanas API var izmantot tikai **lietotāji ar Microsoft Project License.** Tos nevar izmantot tālāk minētie lietotāji.
    - Programmas lietotāji
    - Sistēmas lietotāji
    - Integrācijas lietotāji
    - Citi lietotāji, kuriem nav nepieciešamās licences
- Katrai **OperationSet** var būt ne vairāk par 100 operācijām.
- Katram lietotājam var būt ne vairāk par 10 atvērtām **OperationSets**.
- Project Operations pašlaik atbalsta ne vairāk kā 500 uzdevumu vienā projektā.
- **OperationSet** kļūmes statusa un kļūmju žurnāli pašlaik nav pieejami.
- Plānošanas API ir publiskā priekšskatījumā. Korporācija Microsoft neatbalsta šo API izmantošana ražošanas vidē.

## <a name="sample-scenario"></a>Scenārija paraugs

Šādā scenārijā jums būs jāizveido projekts, darba grupas dalībnieks, četri uzdevumi un divi resursu piešķīrumi. Pēc tam jūs atjaunināsiet vienu uzdevumu, atjaunināsiet projektu, izdzēsiet vienu uzdevumu, izdzēsiet vienu resursa piešķīrumu un izveidosiet uzdevuma atkarību.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Papildu paraugi

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
