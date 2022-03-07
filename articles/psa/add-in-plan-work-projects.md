---
title: Plānojiet savu darbu programmā Microsoft Project ar Project Service pievienojumprogrammu
description: Šajā tēmā ir sniegta informācija par to, kā lietot Microsoft Project pievienojumprogrammu programmai Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014575"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Plānojiet savu darbu programmā Microsoft Project ar Project Service pievienojumprogrammu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] atvieglo projekta plānošanas posmu, tostarp prognozēšanu. Varat definēt darbu tā, lai izmaksas, pūles un pārdošanas vērtība būtu skaidri zināma, kad tiek iesniegts galīgais priekšlikums.  

Varat instalēt programmu [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] un plānot darbus ierastajā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vidē. Izmantojiet [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] stabilās plānošanas un pārvaldības iespējas un pēc tam atjauniniet savu projekta plānu pievienojumprogrammā Project Service Automation.  

> [!IMPORTANT]
> - Lai izmantotu SharePoint dokumentu pārvaldību, lai varētu saglabāt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failus, jūsu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratoram ir jāieslēdz dokumentu pārvaldība. 
> - Programma [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ir saderīga tikai ar izdevumu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Pievienojumprogrammas lejupielāde un instalēšana  
 Sagatavojiet [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pierakstīšanās informāciju. Šī informācija būs nepieciešama, lai pārietu no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] uz pievienojumprogrammu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Lejupielādes centrā varat lejupielādēt pievienojumprogrammu, kas paredzēta jūsu atbalstītajai Project Service versijai: [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) vai [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Atlasiet lejupielādes saiti.  

3.  Kad lejupielāde ir pabeigta, atlasiet **Jā**, lai instalētu pievienojumprogrammu.  

## <a name="configure-the-add-in"></a>Pievienojumprogrammas konfigurēšana  

1. Atveriet [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un atlasiet cilni **Project Service**.  

2. Atlasiet **Izveidot savienojumu**.  

3. Ievadiet savu pieteikšanās informāciju un atlasiet **Pierakstīties**.  

   Tagad varat sākt izmantojot pievienojumprogrammu.  

## <a name="read-from-a-template"></a>Nolasīšana no veidnes  
 Nolasiet no veidnes, ko izveidojāt pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] un kopējāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], lai sāktu projekta plānošanu. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projekta veidnes izveide (Project Service Automation)](../psa/create-project-template.md)  

1.  Cilnē **Project Service** atlasiet **Lasīt** > **Project Service Automation projekta veidne**.  

2.  Sarakstā izvēlieties projekta veidni un pēc tam atlasiet **Atvērt**.  

    > [!NOTE]
    >  Pēc noklusējuma uzdevumi, kas tiek kopēti no veidnes projektā, tiek iestatīti, kā manuāli ieplānoti.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lomu piešķiršana projekta resursiem  

1.  Atveriet projektu un atlasiet lenti **Uzdevums**.  

2. Atlasiet izvēlni **Ganta diagramma** un pēc tam izvēlieties **Resursa lapa**.  

3. Resursu lapā atlasiet nolaižamo izvēlni **Project Service resursa loma** un izvēlieties lomu Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Piešķiriet projektam resursus  

1.  Cilnē Project Service atlasiet rindu un atlasiet **Atrast resursus**.  

2.  Ekrānā **Rezervēt resursu** atlasiet resursu, kuru vēlaties lietot šim projektam.  

3.  Atlasiet **Rezervēt** un pēc tam atlasiet **Labi**.  

## <a name="publish-your-project"></a>Publicējiet savu projektu  
Kad projekta plānošana ir pabeigta, importējiet un publicēt to pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekts tiks importēts pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Tiek lietots cenu noteikšanas un komandas veidošanas process. Atveriet projektu pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], lai redzētu ģenerēto darba grupu, projekta aprēķinus un darba sadalījuma struktūru. Tālāk sniegtajā tabulā ir redzams, kur var atrast rezultātus.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganta diagramma**   | Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Darba sadalījuma struktūra**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resursa lapa** |   Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projekta darba grupas dalībnieki**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Lietojums**    |    Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projekta aprēķini**.     |

**Projekta importēšana un publicēšana**  
1. Cilnē **Project Service** dodieties uz **Publicēt** > **Jauns Project Service Automation projekts**.  

2. Dialoglodziņā **Publicēt jaunā Project Service projektā** ievadiet vērtību laukā **Projekta nosaukums** un atlasiet vienumu **Klients**.  

3. Varat arī atlasīt **Saistīt projekta plānu ar Project Service Automation**, lai piesaistītu plānotā projekta failu pievienojumprogrammai Project Service Automation.  

4. Atlasiet **Publicēt**.  

   Piesaistot projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projekta fails tiek iestatīts kā galvenais un darba sadalījuma struktūra pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tiek iestatīta kā tikai lasāma.  Lai veiktu izmaiņas projekta plānā, tās ir jāveic programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un jāpublicē kā atjauninājumi pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Importēta projekta rediģēšana  
 Lai veiktu izmaiņas projekta plānā, kas tika importēts programmā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ir divas iespējas.  

- Atveriet galveno failu un rediģējiet to pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Atsaistiet failu un rediģējiet to tieši pievienojumprogrammā Project Service. Pēc noklusējuma projekts, kas tika augšupielādēts no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], tiek bloķēts un to var rediģēt tikai projektā. Lai failu rediģētu pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], fails ir jāatsaista.  

### <a name="edit-in-pn_microsoft_project"></a>Rediģēt pakalpojumā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Galvenajā izvēlnē dodieties uz **Project Service** > **Projekti**.  

2. Projektu sarakstā atveriet projektu, ko izveidojāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Lentē atlasiet **Atvērt programmā MS Project**. Tādējādi piesaistītais galvenais fails tiks atvērts pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Failu atsaistīšana un rediģēšana pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Galvenajā izvēlnē dodieties uz **Project Service** > **Projekti**.  

2. Projektu sarakstā atveriet projektu, ko izveidojāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Lentē atlasiet **Atcelt saistību ar MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Projekta faila augšupielāde risinājumā SharePoint vai Office grupās  
 Varat augšupielādēt savu projekta failu risinājumā SharePoint un piekļūt tam sava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekta sadaļā Saistītie dokumenti.  Jūsu administratoram ir jākonfigurē SharePoint dokumentu pārvaldība, un tā jāieslēdz projekta entītijai. 

 Projekta failu varat augšupielādēt arī programmā [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], ja ir iestatīs pakalpojums Office grupas.

### <a name="upload-a-file-for-sharepoint"></a>Augšupielādējiet SharePoint failu  

1. Galvenajā izvēlnē dodieties uz **Project Service** > **Augšupielādēt**.  

2. Atlasiet **Project Service Automation projekta dokumentiem**.  

3. Dialoglodziņā **Iespējot atvēršanu programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izvēlieties **Jā** vai **Nē**.  

   - Atlasot **Jā**, jūs varēsit atlasīt Project Service Automation pogas **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, lai palaistu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un ielādētu projekta failu no SharePoint dokumentu bibliotēkas.  

   - Atlasot **Nē** saite **Atvērt[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nedarbosies.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failu var atrast līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sadaļā **Dokumenti** konkrētajam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektam.  

### <a name="upload-a-file-for-office-groups"></a>Faila augšupielāde pakalpojumā Office grupām  

1. Galvenajā izvēlnē dodieties uz **Project Service** > **Augšupielādēt**.  

2. Atlasiet **Project Service Automation projekta dokumentiem**.  

3. Dialoglodziņā **Iespējot atvēršanu programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izvēlieties **Jā** vai **Nē**.  

   - Atlasot **Jā**, jūs varēsit atlasīt Project Service Automation pogas **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, lai palaistu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un ielādētu projekta failu no SharePoint dokumentu bibliotēkas.  

   - Atlasot **Nē** saite **Atvērt[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nedarbosies.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failu var atrast līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sadaļā **Dokumenti** konkrētajam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektam.  

## <a name="publish--your-project-as-a-template"></a>Projekta veidnes publicēšana  
 Var saglabāt jūsu projektu un atkārtoti saglabājiet to kā veidni projekta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projekta veidnes ir projektu plāni, kas ir atkārtoti izmantojami līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Papildinformāciju skatiet sadaļā [Projekta veidnes izveide (Project Service Automation)](../psa/create-project-template.md). 

1. Cilnē **Project Service** dodieties uz **Publicēt** > **Jauna Project Service Automation veidne**.  

2. Dialoglodziņā **Publicēt jaunā Project Service projekta veidnē** ievadiet vērtību laukā **Projekta veidnes nosaukums**.  

3. Varat arī atlasīt izvēles rūtiņu **Saistīt projekta plānu ar Project Service Automation**, lai piesaistītu projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Atlasiet **Publicēt**.  

Piesaistot projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projekta fails tiek iestatīts kā galvenais un darba sadalījuma struktūra pievienojumprogrammas [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]veidnē  tiek iestatīta kā tikai lasāma.  Lai veiktu izmaiņas projekta plānā, tās ir jāveic programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un jāpublicē kā atjauninājumi pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Resursa ielādētā grafika lasīšana

Kad tiek lasīts Project Service Automation projekts, resursa kalendārs netiek sinhronizēts ar darbvirsmas klientu. Ja atšķiras uzdevumu ilgums, ieguldījums vai beigas, iespējams, resursu un darbvirsmas klienta projektiem ir lietoti dažādi darba stundu veidnes kalendāri.


## <a name="data-synchronization"></a>Datu sinhronizācija
Šis sadaļas tabulās sniegta informācija par entitījas datu sinhronizāciju starp Project Service Automation un Microsoft Project datora pievienojumprogrammu.

### <a name="project-task-entity-table"></a>Projekta uzdevuma entitīja tabulu
Tālāk sniegtajā tabulā ir aprakstīta projekta uzdevuma entitījas datu sinhronizācija starp Project Service Automation un Microsoft Project darbvirsmas pievienojumprogrammu.

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Projekta uzdevums | Izpildes datums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Paredzamais ieguldījums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | MS Project klienta ID | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Pamata uzdevums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Project | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Projekta uzdevums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Projekta uzdevuma nosaukums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Resursu vienība (novecojis — v3.0) | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Plānotais ilgums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | Sākuma datums | Synchronized | Nav sinhronizēts |
| Projekta uzdevums | WBS ID | Synchronized | Nav sinhronizēts |

### <a name="team-member-entity-table"></a>Darba grupas dalībnieka entītijas tabula
Tālāk sniegtajā tabulā ir aprakstīta darba grupas dalībnieka entitījas sinhronizācija starp Project Service Automation un Microsoft Project darbvirsmas pievienojumprogrammu.

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Grupas dalībnieks | MS Project klienta ID | Synchronized | Nav sinhronizēts |
| Grupas dalībnieks | Amata nosaukums | Synchronized | Nav sinhronizēts |
| Grupas dalībnieks | projekts | Synchronized | Synchronized |
| Grupas dalībnieks | Projekta grupa | Synchronized | Synchronized |
| Grupas dalībnieks | Resursu vienība | Nav sinhronizēts | Synchronized |
| Grupas dalībnieks | Loma | Nav sinhronizēts | Synchronized |
| Grupas dalībnieks | Darba laiks | Nav sinhronizēts | Nav sinhronizēts |

### <a name="resource-assignment-entity-table"></a>Resursu piešķires entitījas tabula
Tālāk sniegtajā tabulā ir aprakstīta resursu piešķires entitījas datu sinhronizācija starp Project Service Automation un Microsoft Project darbvirsmas pievienojumprogrammu.

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Resursu piešķiršana | No datuma | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | stundas | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | MS Project klienta ID | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Plānotais darbs | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Project | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Projekta grupa | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Resursu piešķiršana | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Uzdevums | Synchronized | Nav sinhronizēts |
| Resursu piešķiršana | Līdz datumam | Synchronized | Nav sinhronizēts |

### <a name="project-task-dependencies-entity-table"></a>Projekta uzdevuma atkarību entitījas tabula
Tālāk sniegtajā tabulā ir aprakstīta projekta uzdevumu atkarības entitījas datu sinhronizācija starp Project Service Automation un Microsoft Project darbvirsmas pievienojumprogrammu.

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Projekta uzdevuma atkarības | Projekta uzdevuma atkarība | Synchronized | Nav sinhronizēts |
| Projekta uzdevuma atkarības | Saites veids | Synchronized | Nav sinhronizēts |
| Projekta uzdevuma atkarības | Pirmstecīgais uzdevums | Synchronized | Nav sinhronizēts |
| Projekta uzdevuma atkarības | Project | Synchronized | Nav sinhronizēts |
| Projekta uzdevuma atkarības | Pēctecīgais uzdevums | Synchronized | Nav sinhronizēts |

### <a name="additional-resources"></a>Papildu resursi
 [Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]