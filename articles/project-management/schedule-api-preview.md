---
title: Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām
description: Šajā rakstā ir sniegta informācija un paraugi projekta plānošanas API izmantošanai.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541134"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


**Plānošanas entītijas**

Projekta plānošanas API nodrošina iespēju veikt izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**. Šīs entītijas tiek pārvaldītas, izmantojot projekta tīmekļa plānošanas programmu. Iepriekšējos Dynamics 365 Project Operations laidienos tika ierobežotas izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.

Tālāk sniegtajā tabulā ir sniegts projekta plānošanas entītiju pilns saraksts.

| **Entītijas nosaukums**         | **Entītijas loģiskais nosaukums**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekta uzdevums            | msdyn_projecttask           |
| Projekta uzdevuma atkarība | msdyn_projecttaskdependency |
| Resursu piešķiršana     | msdyn_resourceassignment    |
| Projekta bloks          | msdyn_projectbucket         |
| Projekta grupas dalībnieks     | msdyn_projectteam           |
| Projekta kontrolsaraksti      | msdyn_projectchecklist      |
| Projekta etiķete           | msdyn_projectlabel          |
| Marķējamais projekta uzdevums   | msdyn_projecttasktolabel    |
| Projekta sprints          | msdyn_projectsprint         |

**OperationSet**

OperationSet ir darba vienības shēma, ko var izmantot, kad transakcijā ir jāapstrādā vairāki plānošanas ietekmēšanas pieprasījumi.

**Projekta plānošanas API**

Tālāk ir parādīts pašreizējo projekta plānošanas API saraksts.

| **API**                                 | Apraksts                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Šis API tiek izmantots, lai izveidotu projektu. Nekavējoties tiek izveidots projekts un noklusējuma projekta bloks.                         |
| **msdyn_CreateTeamMemberV1**            | Šis API tiek izmantots, lai izveidotu projekta darba grupas dalībnieku. Darba grupas dalībnieka ieraksts tiek izveidots nekavējoties.                                  |
| **msdyn_CreateOperationSetV1**          | Šo API var izmantot, lai ieplānotu vairākus pieprasījumus, kas jāveic transakcijā.                                        |
| **msdyn_PssCreateV1**                   | Šis API tiek izmantots, lai izveidotu entitīju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta izveides operāciju. |
| **msdyn_PssUpdateV1**                   | Šis API tiek izmantots, lai atjauninātu entitīju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta atjaunināšanas operāciju.  |
| **msdyn_PssDeleteV1**                   | Šis API tiek izmantots, lai dzēstu entitīju. Entītija var būt jebkura no projekta plānošanas entītijām, kas atbalsta dzēšanas operāciju. |
| **msdyn_ExecuteOperationSetV1**         | Šis API tiek izmantots, lai izpildītu visas operācijas attiecīgajā operāciju kopā.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Šis API tiek izmantots, lai atjauninātu resursu piešķiršanas plānoto darba noslodzi.                                                        |



**Projekta plānošanas API izmantošana ar OperationSet**

Tā kā ieraksti, kuriem ir gan **CreateProjectV1**, gan **CreateTeamMemberV1**, tiek izveidoti nekavējoties, šos API nevar izmantot tieši kopā **OperationSet**. Tomēr API var lietot, lai izveidotu nepieciešamos ierakstus, izveidotu **OperationSet** un pēc tam izmantotu šos iepriekš izveidotos ierakstus kopā **OperationSet**.

**Atbalstītās operācijas**

| **Plānošanas entītija**   | **Izveide** | **Atjaunināšana** | **Dzēšana** | **Svarīgi ieteikumi**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projekta uzdevums            | Jā        | Jā        | Jā        | Laukus **Progress**, **EffortCompleted** un **EffortRemaining** var rediģēt Project for the Web, bet tos nevar rediģēt Project Operations.                                                                                                                                                                                             |
| Projekta uzdevuma atkarība | Jā        | Nē.         | Jā        | Projekta uzdevumu atkarības ieraksti netiek atjaunināti. Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu.                                                                                                                                                                                                                                 |
| Resursu piešķiršana     | Jā        | Jā\*      | Jā        | Netiek atbalstītas operācijas ar šādiem laukiem: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** un **PlannedWork**. Resursu piešķiršanas ieraksti netiek atjaunināti. Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu. Resursu piešķiršanas noslodžu atjaunināšanai ir nodrošināts atsevišķs API. |
| Projekta bloks          | Jā        | Jā        | Jā        | Noklusējuma bloks tiek izveidots, izmantojot **CreateProjectV1** API. 16. atjauninājumu laidienā tika pievienots atbalsts projekta intervālu izveidošanai un dzēšanai.                                                                                                                                                                                                   |
| Projekta darba grupas dalībnieks     | Jā        | Jā        | Jā        | Izveides operācijai izmantojiet **CreateTeamMemberV1** API.                                                                                                                                                                                                                                                                                           |
| Project                 | Jā        | Jā        |            | Netiek atbalstītas operācijas ar šādiem laukiem: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** un **Duration**.                                                                                       |
| Projekta kontrolsaraksti      | Jā        | Jā        | Jā        |                                                                                                                                                                                                                                                                                                                                                         |
| Projekta etiķete           | Nē.         | Jā        | Nē.         | Etiķešu nosaukumus var mainīt. Šis līdzeklis ir pieejams vienīgi Project for the Web                                                                                                                                                                                                                                                                      |
| Marķējamais projekta uzdevums   | Jā        | Nē.         | Jā        | Šis līdzeklis ir pieejams vienīgi Project for the Web                                                                                                                                                                                                                                                                                                  |
| Projekta sprints          | Jā        | Jā        | Jā        | Laukam **Sākums** jābūt ar datumu, kas agrāks par lauku **Beigas**. Viena un tā paša projekta sprinti nevar savstarpēji pārklāties. Šis līdzeklis ir pieejams vienīgi Project for the Web                                                                                                                                                                    |




Rekvizīts ID nav obligāts. Ja tas ir nodrošināts, sistēma mēģina to izmantot un rodas izņēmums, ja to nevar izmantot. Ja tas nav nodrošināts, sistēma to ģenerēs.

**Zināmās problēmas un ierobežojumi**

Tālāk ir saraksts ar ierobežojumiem un zināmajām problēmām.

-   Projekta plānošanas API var izmantot tikai **lietotāji ar Microsoft Project licenci**. Tos nevar izmantot tālāk minētie lietotāji.
    -   Programmas lietotāji
    -   Sistēmas lietotāji
    -   Integrācijas lietotāji
    -   Citi lietotāji, kuriem nav nepieciešamās licences
-   Katrai **OperationSet** var būt ne vairāk par 100 operācijām.
-   Katram lietotājam var būt ne vairāk par 10 atvērtām **OperationSets**.
-   Project Operations pašlaik atbalsta ne vairāk kā 500 uzdevumu vienā projektā.
-   Katra resursa piešķiršanas papildu operācija tiek skaitīta kā atsevišķa operācija.
-   Katrā atjaunināto kontūru sarakstā var būt maksimāli 100 laika sektoru.
-   **OperationSet** kļūmes statusa un kļūmju žurnāli pašlaik nav pieejami.
-   Katram projektam ir ne vairāk kā 400 sprintu.
-   [Projektu un uzdevumu ierobežojumi un robežas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Pašlaik etiķetes ir pieejamas vienīgi Project for the Web.

**Kļūdu apstrāde**

-   Lai pārskatītu operāciju kopās ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **Operāciju kopas**.
-   Lai pārskatītu projekta plānošanas pakalpojuma ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānošanas integrācija** \> **PSS kļūdu žurnāli**.

**Resursu piešķiršanas kontūru rediģēšana**

Atšķirībā no visiem citiem projekta plānošanas API, kas atjaunina entītiju, resursu piešķiršanas kontūru API ir atbildīgs tikai par viena lauka atjauninājumiem ( msdyn_plannedwork), kas atrodas vienā entītijā, msydn_resourceassignment.

Dotais plānošanas režīms:

-   **fiksētas vienības**
-   Projekta kalendārs ir 9-5p ir 9-5pst, Pirm., Otrd., Cet., Piektd. (NAV DARBA TREŠDIENĀS)
-   Un resursu kalendārs ir 9-1p PST Pirm. līdz piektd.

Šis piešķīrums ir vienai nedēļai, četrām stundām dienā. Tas ir tāpēc, ka resursu kalendārs ir no 9-1 PST vai četrām stundām dienā.

| &nbsp;     | Uzdevums | Sākuma datums | Beigu datums  | Daudzums | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 darbinieks |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Piemēram, ja vēlaties, lai darbinieks katru dienu strādātu tikai trīs stundas šajā nedēļā un citiem uzdevumiem atļautu vienu stundu.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours parauga slodze:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Šis ir piešķīrums pēc tam, kad ir palaists Kontūras plānošanas atjauninājuma API.

| &nbsp;     | Uzdevums | Sākuma datums | Beigu datums  | Daudzums | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 darbinieks | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Scenārija paraugs**

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

** Papildu paraugi

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
