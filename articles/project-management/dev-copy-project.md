---
title: Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana
description: Šajā rakstā ir sniegta informācija par to, kā izveidot projekta veidnes, izmantojot pielāgoto darbību Projekta kopēšana.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923841"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektu veidņu izstrāde, izmantojot darbību Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations atbalsta iespēju kopēt projektu un pārveidot visus piešķīrumus atpakaļ par vispārīgajiem resursiem, kas norāda lomu. Klienti var izmantot šo funkcionalitāti, lai veidotu vienkāršas projektu veidnes.

Atlasot **Projekta kopēšana**, tiek atjaunināts mērķa projekta statuss. Izmantojiet **Statusa iemesls**, lai noteiktu, kad kopēšanas darbība ir pabeigta. Atlasot **Projekta kopēšana**, tiek atjaunināts arī projekta sākuma datums uz pašreizējo sākuma datumu, ja mērķa projekta entītijā nav noteikts mērķa datums.

## <a name="copy-project-custom-action"></a>Pielāgotā darbība Projekta kopēšana

### <a name="name"></a>Nosaukums/vārds 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Ievades parametri

Ir trīs ievades parametri.

- **ReplaceNamedResources** vai **ClearTeamsAndAssignments** — iestatiet tikai vienu no opcijām. Neiestatiet abus.

    - **\{"ReplaceNamedResources":true\}**  — Project Operations noklusējuma uzvedība. Visi nosauktie resursi tiek aizstāti ar vispārējiem resursiem.
    - **\{"ClearTeamsAndAssignments":true\}**  — Project for the Web noklusējuma uzvedība. Visi piešķīrumi un darba grupu dalībnieki tiek noņemti.

- **SourceProject** — avota projekta, no kura jākopē, entītijas atsauce. Šī parametra vērtība nevar būt nulle.
- **Target** — mērķa projekta, uz kuru jākopē, entītijas atsauce. Šī parametra vērtība nevar būt nulle.

Nākamajā tabulā ir sniegts šo trīs parametru kopsavilkums.

| Parametrs                | Tipi             | vērtība                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Patiess** vai **Aplams** |
| ClearTeamsAndAssignments | Boolean          | **Patiess** vai **Aplams** |
| SourceProject            | Entītijas atsauce | Avota projekts    |
| Mērķis                   | Entītijas atsauce | Mērķa projekts    |

Vairāk darbību noklusējuma vērtību skatiet sadaļā [Web API darbību izmantošana](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Pārbaudes

Tiek veiktas tālāk norādītās pārbaudes.

1. Tukšā pārbaude un avota un mērķa projektu izgūšana, lai apstiprinātu abu projektu esamību organizācijā.
2. Sistēma apstiprina, ka mērķa projekts ir derīgs kopēšanai, pārbaudot šādus nosacījumus:

    - Projektā nav iepriekšēju darbību (tostarp cilnes **Uzdevumi** atlase), un projekts ir jaunizveidots.
    - Tajā nav iepriekšēju kopiju, šajā projektā netika pieprasīta importēšana, un projekta statuss nav **Neizdevās**.

3. Operācija netiek izsaukta, izmantojot HTTP.

## <a name="specify-fields-to-copy"></a>Kopējamo lauku norādīšana

Kad tiek izsaukta darbība, darbība **Projekta kopēšana** apskatīs projekta skatu **Projekta kolonnu kopēšana**, lai noteiktu, kuri lauki jākopē, pārkopējot projektu.

### <a name="example"></a>Piemērs

Šajā piemērā parādīts, kā izsaukt pielāgoto darbību **CopyProjectV3** ar parametru kopu **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
