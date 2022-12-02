---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 17, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 17, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915699"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation atjauninājumu izlaidums 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.  Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 17. Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada marta pašatjauninājumu.


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
