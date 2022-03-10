---
title: Project Operations duālās rakstīšanas kartes versijas
description: Šajā tēmā ir ietverts saraksts ar duālās rakstīšanas kartēm, kas ir nepieciešamas Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 452f9f16bfbae2d547afb9fcf4fc51595ea49890
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547118"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations duālās rakstīšanas kartes versijas

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai izmantotu Dynamics 365 Project Operations resursu/krājumos nebalstītiem scenārijiem, ir nepieciešams, lai vidē darbotos duālās rakstīšanas karšu kopa. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Priekšnosacījuma kartes: duālās rakstīšanas saskaņotais risinājums

Risinājumā Project Operations nepieciešamie priekšnosacījumi ir tālāk uzskaitītās kartes. Noteikti izmantojiet tālāk sniegtajā tabulā norādītās kartes un visas saistītās tabulu kartes savā vidē.

| Tabulas karte | Sākotnējā sinhronizācija |
| --- | --- |
| Virsgrāmata (msdyn_ledgers) | Tabulas kartei ir nepieciešama sākotnējā sinhronizācija un visi priekšnosacījumi. Sākotnējās sinhronizācijas šablons ir Finance and Operations programmas. |
| Juridiskas personas (cdm_companies) | Nav obligāta. Sistēma automātiski aizpilda šo entītiju, kad vides tiek saistītas, izmantojot duālo rakstīšanu. |
| Klienti V3 (accounts) | Nav nepieciešama nodrošināšanai. |
| Piegādātāji V2 (msdyn_vendors) | Nav nepieciešama nodrošināšanai. |

1. Karšu sarakstā atlasiet karti Virsgrāmata **(msdyn\_ledgers)** ar visiem priekšnosacījumiem un atzīmējiet izvēles rūtiņu **Sākotnējā sinhronizācija**. Laukā **Sākotnējās sinhronizācijas šablons** atlasiet **Finance and Operations programmas** gan virsgrāmatas kartei, gan visām priekšnosacījuma kartēm. Atlasiet **Izpildīt**.

![Virsgrāmatas kartes sinhronizācija.](media/DW6.png)

2. Veiciet tās pašas darbības visām pārējām tabulā iekļautajām tabulu kartēm, kas uzskaitītas iepriekš. Neatzīmējiet izvēles rūtiņu **Sākotnējā sinhronizācija**, palaižot šīs kartes.

## <a name="project-operations-dual-write-maps"></a>Project Operations duālās rakstīšanas kartes

Risinājumā Project Operations nepieciešamas tālāk uzskaitītās kartes. Ar 2021. gada maija atjauninājumu Project Operations versiju 4.10.0.186 ir uzskaitītas duālās rakstīšanas kartes.

| **Entītiju karte** | **Jaunākā versija** | **Sākotnējā sinhronizācija** |
| --- | --- | --- |
| Integrāciju entītija projekta transakciju relācijām (msdyn\_transactionconnections) | 1.0.0.0 | Nav nepieciešama nodrošināšanai. |
| Projektu līgumu galvenes (sales orders) | 1.0.0.1 | Nav nepieciešama nodrošināšanai. |
| Projekta līguma rindas (salesorderdetails) | 1.0.0.0 | Nav nepieciešama nodrošināšanai. |
| Projekta līdzekļu avots (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas tabula materiālu aprēķiniem (msdyn\_estimatelines) | 1.0.0.0 | Nav nepieciešama nodrošināšanai. |
| Projekta rēķinu priekšlikumi V2 (invoices) | 1.0.0.3 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas faktiskie dati (msdyn_actuals) | 1.0.0.14 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācija līguma rindas atskaites punktos (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas entītija izmaksu aprēķiniem (msdyn_estimatelines) | 1.0.0.2 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas entītija stundu aprēķiniem (msdyn_resourceassignments) | 1.0.0.5 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas projekta izdevumu kategorijas eksporta entītija (msdyn_expensecategories) | 1.0.0.1 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas projekta izdevumu eksporta entītija (msdyn_expenses) | 1.0.0.2 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.0 | Nav nepieciešama nodrošināšanai. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Nav nepieciešama nodrošināšanai. |
| Projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories) | 1.0.0.1 | Lai sinhronizētu projektu vadītāja un darba grupas dalībnieka resursu lomas, kas aizpildītas Dynamics 365 Dataverse vidē nodrošināšanas laikā, tabulas kartei ir nepieciešama sākotnējā sinhronizācija. Dataverse ir sākotnējās sinhronizācijas galvenais avots. |
| Projekta uzdevumi (msdyn_projecttasks) | 1.0.0.4 | Nav nepieciešama nodrošināšanai. |
| Projekta transakcijas kategorijas (msdyn_transactioncategories) | 1.0.0.0 | Nav nepieciešama nodrošināšanai. |
| Projekti V2 (msdyn_projects) | 1.0.0.2 | Nav nepieciešama nodrošināšanai. |

Izpildiet tālāk norādītās darbības, lai palaistu sarakstā norādītās kartes.

1. Iespējojiet projekta resursu lomas tabulas kartei **visi uzņēmumi (bookableresourcecategories)**, jo šai kartei ir nepieciešama sākotnējā sinhronizācija. Laukā **Sākotnējās sinhronizācijas šablons** atlasiet **Common data service**. 

 ![Resursu lomu tabulu karšu sinhronizācija.](media/6ResourceInitialSync.jpg)

 Pirms pāriešanas uz nākamo darbību nogaidiet, līdz kartes statuss ir **Darbojas**.

2. Atlasiet visas atlikušās nepieciešamās kartes. Varat tās filtrēt duālās rakstīšanas karšu sarakstā, izmantojot atslēgvārdu **Projekts** meklēšanas lodziņā augšējā labajā stūrī. Varat atlasīt visas kartes vienlaikus un tad tās palaist. Papildinformāciju skatiet sadaļā [Vairāku tabulas karšu pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Pārliecinieties, vai ir iespējotas un palaistas arī saistīto entītiju kartes.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations duālās rakstīšanas kartes versijas

Vienmēr palaidiet jaunāko kartes versiju savā vidē. Noteikti līdzekļi un iespējas var nedarboties pareizi, ja pastāv kāds no šiem nosacījumiem:

- karte nav aktivizēta;
- nav aktivizēta jaunākā kartes versija; 
- nav aktivizētas saistītās tabulas kartes.

Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Varat aktivizēt jaunu kartes versiju, atlasot **Tabulas kartes versijas**, atlasot jaunāko versiju un pēc tam saglabājot atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, izmaiņas būs jālieto atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
