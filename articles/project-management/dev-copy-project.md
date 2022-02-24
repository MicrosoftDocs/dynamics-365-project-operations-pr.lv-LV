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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045018"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations atbalsta iespēju kopēt projektu un pārveidot visus piešķīrumus atpakaļ par vispārīgajiem resursiem, kas norāda lomu. Klienti var izmantot šo funkcionalitāti, lai veidotu vienkāršas projektu veidnes.

Atlasot **Projekta kopēšana**, tiek atjaunināts mērķa projekta statuss. Izmantojiet **Statusa iemesls**, lai noteiktu, kad kopēšanas darbība ir pabeigta. Atlasot **Projekta kopēšana**, tiek atjaunināts arī projekta sākuma datums uz pašreizējo sākuma datumu, ja mērķa projekta entītijā nav noteikts mērķa datums.

## <a name="copy-project-custom-action"></a>Pielāgotā darbība Projekta kopēšana 

### <a name="name"></a>Nosaukums/vārds, uzvārds 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Ievades parametri
Ir trīs ievades parametri.

| Parametrs          | Veidi   | Vērtības                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** vai **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entītijas atsauce | Avota projekts |
| Mērķis             | Entītijas atsauce | Mērķa projekts |


- **{"clearTeamsAndAssignments":true}**: Noklusējuma darbība Project tīmeklim, un tiks noņemti visi piešķīrumi un darba grupas dalībnieki.
- **{"removeNamedResources":true}** Project Operations noklusējuma darbība, un tiks atjaunoti vispārīgie resursi.

Vairāk darbību noklusējuma vērtību skatiet sadaļā [Web API darbību izmantošana](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Kopējamo lauku norādīšana 
Kad tiek izsaukta darbība, darbība **Projekta kopēšana** apskatīs projekta skatu **Projekta kolonnu kopēšana**, lai noteiktu, kuri lauki jākopē, pārkopējot projektu.


### <a name="example"></a>Piemērs
Šajā piemērā parādīts, kā izsaukt pielāgoto darbību **CopyProject** ar parametru kopu **removeNamedResources**.
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
