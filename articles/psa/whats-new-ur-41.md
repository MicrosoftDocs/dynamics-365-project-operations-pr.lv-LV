---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 41, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 41. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930557"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 41, V3. Šīs versijas būvējuma numurs ir V3.10.62.162, un tas parasti ir pieejams, izmantojot 2022. gada marta pašatjauninājumu.

## <a name="update-release-41"></a>Atjauninājumu izlaidums 41

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**Projekta pārvaldība**
- Mēģinot izveidot projektu no veidnes, kuras pamatā ir projekts, kas izveidots no darbvirsmas pievienojumprogrammas, tiek parādīts šāds kļūdas ziņojums: “Resursu piešķiršanas lauka Plānotais darbs validācija: katra resursa piešķiršanas laika slāņa beigu datums nedrīkst būt agrāks par tā sākuma datumu”.

**Laiks un izdevumi**
- Mēģinot dzēst laika ierakstu, tiek parādīts šāds kļūdas ziņojums: “Rodas neparedzēta kļūda no ISV koda”.

**Pārdošana**
- Izveidojot rēķinu fiksētas cenas atskaites punktam, netiek aizpildīti lauki **Apraksts** un **Ārējais apraksts**. 
