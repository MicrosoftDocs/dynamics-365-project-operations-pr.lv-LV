---
title: Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana
description: Šajā tēmā ir sniegta informācija par to, kā izveidot projekta veidnes, izmantojot pielāgoto darbību Projekta kopēšana.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286932"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="54b81-103">Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana</span><span class="sxs-lookup"><span data-stu-id="54b81-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="54b81-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="54b81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="54b81-105">Dynamics 365 Project Operations atbalsta iespēju kopēt projektu un pārveidot visus piešķīrumus atpakaļ par vispārīgajiem resursiem, kas norāda lomu.</span><span class="sxs-lookup"><span data-stu-id="54b81-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="54b81-106">Klienti var izmantot šo funkcionalitāti, lai veidotu vienkāršas projektu veidnes.</span><span class="sxs-lookup"><span data-stu-id="54b81-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="54b81-107">Atlasot **Projekta kopēšana**, tiek atjaunināts mērķa projekta statuss.</span><span class="sxs-lookup"><span data-stu-id="54b81-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="54b81-108">Izmantojiet **Statusa iemesls**, lai noteiktu, kad kopēšanas darbība ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="54b81-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="54b81-109">Atlasot **Projekta kopēšana**, tiek atjaunināts arī projekta sākuma datums uz pašreizējo sākuma datumu, ja mērķa projekta entītijā nav noteikts mērķa datums.</span><span class="sxs-lookup"><span data-stu-id="54b81-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="54b81-110">Pielāgotā darbība Projekta kopēšana</span><span class="sxs-lookup"><span data-stu-id="54b81-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="54b81-111">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="54b81-111">Name</span></span> 

<span data-ttu-id="54b81-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="54b81-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="54b81-113">Ievades parametri</span><span class="sxs-lookup"><span data-stu-id="54b81-113">Input parameters</span></span>
<span data-ttu-id="54b81-114">Ir trīs ievades parametri.</span><span class="sxs-lookup"><span data-stu-id="54b81-114">There are three input parameters:</span></span>

| <span data-ttu-id="54b81-115">Parametrs</span><span class="sxs-lookup"><span data-stu-id="54b81-115">Parameter</span></span>          | <span data-ttu-id="54b81-116">Veidi</span><span class="sxs-lookup"><span data-stu-id="54b81-116">Type</span></span>   | <span data-ttu-id="54b81-117">Vērtības</span><span class="sxs-lookup"><span data-stu-id="54b81-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="54b81-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="54b81-118">ProjectCopyOption</span></span>  | <span data-ttu-id="54b81-119">String</span><span class="sxs-lookup"><span data-stu-id="54b81-119">String</span></span> | <span data-ttu-id="54b81-120">**{"removeNamedResources":true}** vai **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="54b81-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="54b81-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="54b81-121">SourceProject</span></span>      | <span data-ttu-id="54b81-122">Entītijas atsauce</span><span class="sxs-lookup"><span data-stu-id="54b81-122">Entity Reference</span></span> | <span data-ttu-id="54b81-123">Avota projekts</span><span class="sxs-lookup"><span data-stu-id="54b81-123">Source Project</span></span> |
| <span data-ttu-id="54b81-124">Mērķis</span><span class="sxs-lookup"><span data-stu-id="54b81-124">Target</span></span>             | <span data-ttu-id="54b81-125">Entītijas atsauce</span><span class="sxs-lookup"><span data-stu-id="54b81-125">Entity Reference</span></span> | <span data-ttu-id="54b81-126">Mērķa projekts</span><span class="sxs-lookup"><span data-stu-id="54b81-126">Target Project</span></span> |


- <span data-ttu-id="54b81-127">**{"clearTeamsAndAssignments":true}**: Noklusējuma darbība Project tīmeklim, un tiks noņemti visi piešķīrumi un darba grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="54b81-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="54b81-128">**{"removeNamedResources":true}** Project Operations noklusējuma darbība, un tiks atjaunoti vispārīgie resursi.</span><span class="sxs-lookup"><span data-stu-id="54b81-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="54b81-129">Vairāk darbību noklusējuma vērtību skatiet sadaļā [Web API darbību izmantošana](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="54b81-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="54b81-130">Kopējamo lauku norādīšana</span><span class="sxs-lookup"><span data-stu-id="54b81-130">Specify fields to copy</span></span> 
<span data-ttu-id="54b81-131">Kad tiek izsaukta darbība, darbība **Projekta kopēšana** apskatīs projekta skatu **Projekta kolonnu kopēšana**, lai noteiktu, kuri lauki jākopē, pārkopējot projektu.</span><span class="sxs-lookup"><span data-stu-id="54b81-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="54b81-132">Piemērs</span><span class="sxs-lookup"><span data-stu-id="54b81-132">Example</span></span>
<span data-ttu-id="54b81-133">Šajā piemērā parādīts, kā izsaukt pielāgoto darbību **CopyProject** ar parametru kopu **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="54b81-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]