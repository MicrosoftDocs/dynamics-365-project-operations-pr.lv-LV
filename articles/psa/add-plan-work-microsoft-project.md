---
title: Project Service pievienojumprogrammas izmantošana darba plānošanai programmā Microsoft Project | MicrosoftDocs
description: Šajā rakstā ir sniegta informācija par to, kā pievienot, konfigurēt un izmantot Microsoft Project pievienojumprogrammu programmai Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925543"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Izmantojiet pievienojumprogrammu Project Service Automation, lai plānotu savu darbu programmā Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] atvieglo projekta plānošanas posmu, tostarp prognozēšanu. Varat definēt darbu tā, lai izmaksas, pūles un pārdošanas vērtība būtu skaidri zināma, kad tiek iesniegts galīgais priekšlikums.  

 Tagad varat instalēt programmu [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] un plānot darbus ierastajā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vidē. Izmantojiet [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] stabilās plānošanas un pārvaldības iespējas un pēc tam atjauniniet savu projekta plānu pievienojumprogrammā Project Service Automation.  

> [!IMPORTANT]
> - Lai izmantotu SharePoint dokumentu pārvaldību, lai varētu saglabāt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failus, jūsu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratoram ir jāieslēdz dokumentu pārvaldība. 
> - Programma [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ir saderīga tikai ar izdevumu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Pievienojumprogrammas lejupielāde un instalēšana  
 Sagatavojiet [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pierakstīšanās informāciju. Šī informācija būs nepieciešama, lai pārietu no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] uz pievienojumprogrammu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Lejupielādes centrā varat lejupielādēt pievienojumprogrammu, kas paredzēta jūsu atbalstītajai Project Service versijai: [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) vai [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Noklikšķiniet uz lejupielādes saites.  

3.  Kad lejupielāde ir pabeigta, noklikšķiniet uz **Jā**, lai instalētu pievienojumprogrammu.  

## <a name="configure-the-add-in"></a>Pievienojumprogrammas konfigurēšana  

1. Atveriet [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un noklikšķiniet uz cilnes **Project Service**.  

2. Noklikšķiniet uz **Izveidot savienojumu**.  

3. Ievadiet savu pieteikšanās informāciju un noklikšķiniet uz **Pierakstīties**.  

   Tagad varat sākt izmantojot pievienojumprogrammu.  

## <a name="read-from-a-template"></a>Nolasīšana no veidnes  
 Nolasiet no veidnes, ko izveidojāt pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] un kopējāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], lai sāktu projekta plānošanu. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projekta veidnes izveide (Project Service Automation)](../psa/create-project-template.md)  

1.  Cilnē **Project Service** noklikšķiniet uz **Lasīt** > **Project Service Automation projekta veidne**.  

2.  Sarakstā izvēlieties projekta veidni un pēc tam noklikšķiniet uz **Atvērt**.  

    > [!NOTE]
    >  Pēc noklusējuma uzdevumi, kas tiek kopēti no veidnes projektā, tiek iestatīti, kā manuāli ieplānoti.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lomu piešķiršana projekta resursiem  

1.  Atveriet projektu un noklikšķiniet uz lentes **Uzdevums**.  

2.  Noklikšķiniet uz izvēlnes **Ganta diagramma** un pēc tam izvēlieties **Resursa lapa**.  

3.  Resursu lapā noklikšķiniet uz nolaižamās izvēlnes **Project Service resursa loma** un izvēlieties lomu Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Piešķiriet projektam resursus  

1.  Cilnē Project Service atlasiet rindu un noklikšķiniet uz **Atrast resursus**.  

2.  Ekrānā **Rezervēt resursu** atlasiet resursu, kuru vēlaties lietot šim projektam.  

3.  Noklikšķiniet uz **Rezervēt** un pēc tam noklikšķiniet uz **Labi**.  

## <a name="publish-your-project"></a>Publicējiet savu projektu  
Kad projekta plānošana ir pabeigta, importējiet un publicēt to pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekts tiks importēts pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Tiek lietots cenu noteikšanas un komandas veidošanas process. Atveriet projektu pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], lai redzētu ģenerēto darba grupu, projekta aprēķinus un darba sadalījuma struktūru. Tālāk sniegtajā tabulā ir redzams, kur var atrast rezultātus:

| Project | Detalizēta informācija |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganta diagramma**   | Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Darba sadalījuma struktūra**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resursa lapa** |   Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projekta darba grupas dalībnieki**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Lietojums**    |    Importē ekrānā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projekta aprēķini**.     |

**Projekta importēšana un publicēšana**  
1. Cilnē **Project Service** noklikšķiniet uz **Publicēt** > **Jauns Project Service Automation projekts**.  

2. Dialoglodziņā **Publicēt jaunā Project Service projektā** ievadiet vērtību laukā **Projekta nosaukums** un atlasiet vienumu **Klients**.  

3. Varat arī atzīmēt izvēles rūtiņu **Saistīt projekta plānu ar Project Service Automation**, lai piesaistītu plānotā projekta failu pievienojumprogrammai Project Service Automation.  

4. Noklikšķiniet uz **Publicēt**.  

   Piesaistot projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projekta fails tiek iestatīts kā galvenais un darba sadalījuma struktūra pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tiek iestatīta kā tikai lasāma.  Lai veiktu izmaiņas projekta plānā, tās ir jāveic programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un jāpublicē kā atjauninājumi pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Importēta projekta rediģēšana  
 Lai veiktu izmaiņas projekta plānā, kas tika importēts programmā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ir divas iespējas.  

- Atveriet galveno failu un rediģējiet to pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Atsaistiet failu un rediģējiet to tieši pievienojumprogrammā Project Service. Pēc noklusējuma projekts, kas tika augšupielādēts no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], tiek bloķēts un to var rediģēt tikai projektā. Lai failu rediģētu pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], fails ir jāatsaista.  

### <a name="edit-in-pn_microsoft_project"></a>Rediģēšana programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Galvenajā izvēlnē noklikšķiniet uz **Project Service** > **Projekti**.  

2. Projektu sarakstā atveriet projektu, ko izveidojāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. No lentes noklikšķiniet uz **Atvērt programmā MS Project**. Tādējādi piesaistītais galvenais fails tiks atvērts pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Failu atsaistīšana un rediģēšana pievienojumprogrammā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Galvenajā izvēlnē noklikšķiniet uz **Project Service** > **Projekti**.  

2. Projektu sarakstā atveriet projektu, ko izveidojāt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. No lentes noklikšķiniet uz **Atcelt saistību ar MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Projekta faila augšupielāde risinājumā SharePoint vai Office grupās  
 Varat augšupielādēt savu projekta failu risinājumā SharePoint un piekļūt tam sava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekta sadaļā Saistītie dokumenti.  Jūsu administratoram ir jākonfigurē SharePoint dokumentu pārvaldība, un tā jāieslēdz projekta entītijai. 

 Projekta failu varat augšupielādēt arī programmā [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], ja ir iestatīs pakalpojums Office grupas.

### <a name="upload-a-file-for-sharepoint"></a>Augšupielādējiet SharePoint failu  

1. Galvenajā izvēlnē noklikšķiniet uz **Project Service** > **Augšupielādēt**.  

2. Atlasiet **Project Service Automation projekta dokumentiem**.  

3. Dialoglodziņā **Iespējot atvēršanu programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** atlasiet **Jā** vai **Nē**.  

   - Noklikšķinot uz **Jā**, jūs varēsit atlasīt pogu **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** Project Service Automation, palaist [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un ielādēt projekta failu no SharePoint dokumentu bibliotēkas.  

   - Ja noklikšķināsit uz **Nē**, pogas **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** saite nedarbosies.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failu var atrast līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sadaļā **Dokumenti** konkrētajam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektam.  

### <a name="upload-a-file-for-office-groups"></a>Faila augšupielāde pakalpojumā Office grupām  

1. Galvenajā izvēlnē noklikšķiniet uz **Project Service** > **Augšupielādēt**.  

2. Atlasiet **Project Service Automation projekta dokumentiem**.  

3. Dialoglodziņā **Iespējot atvēršanu programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** atlasiet **Jā** vai **Nē**.  

   - Noklikšķinot uz **Jā**, varēsit atlasīt pogu **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** Project Service Automation, palaist [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un ielādēt projekta failu no SharePoint dokumentu bibliotēkas.  

   - Ja noklikšķināsit uz **Nē**, pogas **Atvērt programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** saite nedarbosies.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] failu var atrast līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sadaļā **Dokumenti** konkrētajam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektam.  

## <a name="publish--your-project-as-a-template"></a>Projekta veidnes publicēšana  
 Var saglabāt jūsu projektu un atkārtoti saglabājiet to kā veidni projekta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projekta veidnes ir projektu plāni, kas ir atkārtoti izmantojami līdzeklī [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projekta veidnes izveide (Project Service Automation)](../psa/create-project-template.md)  

1. Cilnē **Project Service** noklikšķiniet uz **Publicēt** > **Jauna Project Service Automation projekta veidne**.  

2. Dialoglodziņā **Publicēt jaunā Project Service projekta veidnē** ievadiet vērtību laukā **Projekta veidnes nosaukums**.  

3. Varat arī atzīmēt izvēles rūtiņu **Saistīt projekta plānu ar Project Service Automation**, lai piesaistītu plānotā projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Noklikšķiniet uz **Publicēt**.  

Piesaistot projekta failu pievienojumprogrammai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projekta fails tiek iestatīts kā galvenais un darba sadalījuma struktūra pievienojumprogrammas [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]veidnē  tiek iestatīta kā tikai lasāma.  Lai veiktu izmaiņas projekta plānā, tās ir jāveic programmā [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] un jāpublicē kā atjauninājumi pievienojumprogrammā [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Resursa ielādētā grafika lasīšana

Kad tiek lasīts Project Service Automation projekts, resursa kalendārs netiek sinhronizēts ar darbvirsmas klientu. Ja atšķiras uzdevumu ilgums, ieguldījums vai beigas, iespējams, resursu un darbvirsmas klienta projektiem ir lietoti dažādi darba stundu veidnes kalendāri.


## <a name="data-synchronization"></a>Datu sinhronizācija

Tālāk sniegtajā tabulā ir aprakstīta datu sinhronizācija starp Project Service Automation un Microsoft Project darbvirsmas pievienojumprogrammu.

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Projekta uzdevums | Termiņš | ● | - |
| Projekta uzdevums | Paredzamais ieguldījums | ● | - |
| Projekta uzdevums | MS Project klienta ID | ● | - |
| Projekta uzdevums | Pamata uzdevums | ● | - |
| Projekta uzdevums | Project | ● | - |
| Projekta uzdevums | Projekta uzdevums | ● | - |
| Projekta uzdevums | Projekta uzdevuma nosaukums | ● | - |
| Projekta uzdevums | Resursu vienība (novecojis — v3.0) | ● | - |
| Projekta uzdevums | Plānotais ilgums | ● | - |
| Projekta uzdevums | Sākuma datums | ● | - |
| Projekta uzdevums | WBS ID | ● | - |

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Grupas dalībnieks | MS Project klienta ID | ● | - |
| Grupas dalībnieks | Amata nosaukums | ● | - |
| Grupas dalībnieks | projekts | ● | ● |
| Grupas dalībnieks | Projekta grupa | ● | ● |
| Grupas dalībnieks | Resursu vienība | - | ● |
| Grupas dalībnieks | Loma | - | ● |
| Grupas dalībnieks | Darba laiks | Netiek sinhronizēts | Netiek sinhronizēts |

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Resursu piešķiršana | No datuma | ● | - |
| Resursu piešķiršana | stundas | ● | - |
| Resursu piešķiršana | MS Project klienta ID | ● | - |
| Resursu piešķiršana | Plānotais darbs | ● | - |
| Resursu piešķiršana | Project | ● | - |
| Resursu piešķiršana | Projekta grupa | ● | - |
| Resursu piešķiršana | Resursu piešķiršana | ● | - |
| Resursu piešķiršana | Uzdevums | ● | - |
| Resursu piešķiršana | Līdz datumam | ● | - |

| **Entītija** | **Lauks** | **Microsoft Project ar Project Service Automation** | **Project Service Automation ar Microsoft Project** |
| --- | --- | --- | --- |
| Projekta uzdevuma atkarības | Projekta uzdevuma atkarība | ● | - |
| Projekta uzdevuma atkarības | Saites veids | ● | - |
| Projekta uzdevuma atkarības | Pirmstecīgais uzdevums | ● | - |
| Projekta uzdevuma atkarības | Project | ● | - |
| Projekta uzdevuma atkarības | Pēctecīgais uzdevums | ● | - |

### <a name="see-also"></a>Skatiet arī  
 [Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
