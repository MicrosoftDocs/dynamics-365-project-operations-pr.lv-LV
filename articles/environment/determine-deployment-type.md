---
title: Nosakiet savu izvietošanas veidu
description: Šajā tēmā ir sniegta informācija, kas jums palīdzēs noteikt pareizo Project Operations izvietošanas tipu savam uzņēmumam.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479573"
---
# <a name="determine-your-deployment-type"></a>Nosakiet savu izvietošanas veidu

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

> [!IMPORTANT]
> Pēc licences iegādes sāciet šeit, lai noteiktu labāko izvietošanas modeli Dynamics 365 Project Operations, izmantojot elementu [Vadītā instalēšanas plūsma](https://aka.ms/provisionprojectoperations).
> Kad būsiet pabeidzis vadīto instalācijas plūsmu, tiksiet novirzīts uz atbilstošo pārvaldības portālu, lai pabeigtu instalēšanu. Lai pabeigtu instalēšanu, skatiet izvietošanas informāciju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Esošie Dynamics klienti, kas izmanto Dynamics 365 Project Service Automation
Project Operations ietver iespējas, kas piegādātas kopā ar Project Service Automation. Šiem klientiem jaunināšanas ceļš tiks izlaists 2021. gada 1. laidienā.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Esošie Dynamics 365 Finance klienti, kas izmanto Projektu pārvaldību un uzskaiti 

Esošie finanšu klienti, kas izmanto projekta pārvaldības un grāmatvedības funkcionalitāti, var turpināt to lietot bez izmaiņām. Skatiet [Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem](#pma).


## <a name="deployment-regions"></a>Izvietošanas reģions
Informāciju par to, kuri reģioni atbalsta Project Operations izvietošanu, skatiet sadaļā [Ģeogrāfiskā pieejamība Dynamics 365 un Power Platform atskaiti](https://dynamics.microsoft.com/en-us/geographic-availability/). Atlasiet vienumu **Skatīt atskaiti** un izvērsiet **Dynamics365 > Operations programmas > Dynamics 365 Project Operations**, lai skatītu atbalstītos reģionus.

## <a name="deployment-types"></a>Izvietojuma tipi
Project Operations atbalsta vairākas izvietošanas opcijas, lai atbilstu jūsu prasībām. Neatkarīgi no tā, vai esat jauns vai esošs Dynamics 365 klients, Project Operations var atbalstīt jūsu vajadzības.

Mūsu [Izvietošanas anketa](https://aka.ms/provisionprojectoperations) palīdzēs noteikt pareizo izvietošanas veidu. Rezultāti jums palīdzēs sasniegt kādu no tālāk norādītajiem izvietošanas tipiem.

- [Lite izvietošana — pāriet uz pro forma rēķina izrakstīšanu](#lite)
- [Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem](#integrated)
- [Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem](#pma)

Project Operations vienā un tajā pašā vidē atbalsta scenārijus, kas balstīti uz krājumiem un ražošanas pasūtījumiem, un scenārijus, kas ir balstīti uz resursiem/nav balstīti uz krājumiem, izmantojot juridiskās personas līmeņa konfigurācijas. Piemēram, Contoso var izmantot krājumu/ražošanas pasūtījumu iespējas savā ASV ražošanas objektā (juridiskā persona = Contoso Manufacturing United States). Contoso var izmantot iespējas, kas ir balstītas uz resursiem/nav balstītas uz krājumiem, savā Contoso Robotics Arms apkalpošanas objektā Lielbritānijā (juridiskā persona = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu

Lite izvietošana ietver tālāk norādītās iespējas.

- Pārdošanas process projektiem, kas paplašina Dynamics 365 Sales lietojumprogrammas lietošanas iespējas
- Projektu plānošana, izmantojot Microsoft Project tīmeklim
- Vairākdimensiju izcenojums
- Vienota resursu pārvaldība
- Laika izsekošana
- Pamata izdevumi
- Proforma un uz klientiem vērsti rēķini 

#### <a name="deployment-steps"></a>Izvietošanas darbības
Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).

Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](lite-preview-subscription-sign-up.md) un [Jaunas vides nodrošināšana](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
Project Operations scenāriji, kas balstīti uz resursiem/nav balstīti uz krājumiem, ietver tālāk norādītās iespējas.
 
- Pārdošanas process projektiem, kas paplašina Dynamics 365 Sales lietojumprogrammu
- Projektu plānošana, izmantojot Microsoft Project tīmeklim
- Vairākdimensiju izcenojums
- Vienota resursu pārvaldība
- Laika izsekošana
- Pamata izdevumi
- Pilnas izdevumi
- OCR apliecinājums
- Proforma un uz klientiem vērsti rēķini 
- Projektu ieņēmumu atzīšana

#### <a name="deployment-steps"></a>Izvietošanas darbības
Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).

Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](resource-sign-up-preview-subscription.md) un [Jaunas vides nodrošināšana](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem

- Projektu plānošana, izmantojot WBS
- Resursu pārvaldība
- Laika izsekošana
- Pilni izdevumi
- OCR apliecinājums
- Pilna rēķinu izrakstīšana
- Ieņēmumu atzinība
- Ražošanas pasūtījumi
- Materiālu atbalsts

#### <a name="deployment-steps"></a>Izvietošanas darbības
Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).

Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) un [Jaunas vides nodrošināšana](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
