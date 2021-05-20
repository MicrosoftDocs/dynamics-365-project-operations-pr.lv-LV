---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 17, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949238"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation atjauninājumu izlaidums 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.  Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 17. Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada marta pašatjauninājumu.


## <a name="update-release-17"></a>Atjauninājumu izlaidums 17

### <a name="bug-fixes"></a>Kļūdu labojumi

**Vispārīgi**

- Izlabots: atjauniniet pakalpojumu Project Service Automation, lai ieviestu darba grupas dalībnieku licences (projekta resursu centrmezgls iekļaus darba grupas dalībnieku pakalpojumu plānu metadatiem 3.x)
 
**Laiks un izdevumi**

- Izlabots: nav iespējams mainīt izdevumu aplēses no cenas, kas nav nulle, uz nulli (0). Izmaiņas tiek ignorētas.

**Projekta pārvaldība**

- Izlabots: darba grupas dalībnieka amata nosaukumam ir pievienota nulle vērtības pārbaude.
- Izlabots: entītijas **msdyn_resourceassignment** lauks **msdyn_userresourceid** vairs nav pieejams.
- Izlabots: jauninot no versijas 2.x uz 3.x, tagad uzdevumu piešķirēs tiek apstrādātas tukšas ieguldījumu kontūras.

**Sales**

- Izlabots: parametrs **Invoice.PreValidateInvoiceUpdate** tagad atbilstoši apstrādā ieraksta īpašnieku atkārtotu piešķiršanu.
- Izlabots: ja transakcijas klase ir **Laiks**, parametrs **UnitGroup** nav rediģējams visām entītijām, tostarp **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** un **ContractLineDetails**. Taču parametrs **Vienība** nav rediģējams tikai entītijai **JournalLine** un **InvoiceLineDetails.**




[!INCLUDE[footer-include](../includes/footer-banner.md)]