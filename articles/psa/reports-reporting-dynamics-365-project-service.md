---
title: Atskaišu veidošanas sākumlapa
description: Šajā tēmā ir sniegta informācija par atskaišu veidošanu programmā Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 03/01/2019
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
ms.openlocfilehash: da9458741563aa918bc09259e35ba9002ff0ba13
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595967"
---
# <a name="reporting-home-page"></a>Atskaišu veidošanas sākumlapa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation ļauj projekta organizācijām efektīvi pārvaldīt savas biznesa operācijas. Jebkurā projektā darba grupas dalībniekiem ir jāpārvalda iespēja, jāizveido darba piedāvājums un plāns, jānodrošina resursi projektiem, jāpārvalda darbs atbilstoši plānam, jāizraksta rēķins par darbu un pēc tam jādara viss, lai pabeigtu projektu. Iespēja ziņot par operācijām ir būtiska, lai noteiktu organizācijas veselību un veiktu nepieciešamās korektīvās darbības. PSA izmanto Microsoft Dynamics 365 atskaišu izveides metodes un tehnoloģijas visu atskaišu izveidei. Papildinformāciju par atskaišu izveides iespējām skatiet: [Atskaišu rakstīšanas rokasgrāmata, Dynamics 365 Customer Engagement (on-premises)versija 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Atskaites vednis

Atskaites vednis ļauj lietotājiem, kas nav izstrādātāji, izveidot vienkāršas atskaites. Tā kā lietojumprogramma ir izveidota uz esošas platformas, lietošanas pieredze ir tāda pati kā pieredze, kas ir dokumentēta sadaļā [Atskaites izveide vai rediģēšana, izmantojot Atskaites vedni](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Taču būs jāizmanto risinājumam Project Service Automation raksturīgās entītijas.

## <a name="custom-sql-server-reporting-services-reports"></a>Pielāgotas SQL Server atskaišu izveides pakalpojumu atskaites

Ja uzņēmumam ir nepieciešama noteikta atskaite, ko nevar izveidot, izmantojot Atskaites vedni, varat izveidot pielāgotu atskaiti. Ir jābūt instalētam pakalpojumam Microsoft Visual Studio kopā ar atbilstošajiem Microsoft SQL Server Data Tools un atskaišu autorēšanas paplašinājumiem. Papildinformāciju par rīkiem un versijām skatiet sadaļā [Atskaišu izstrādes vide, izmantojot SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Informāciju par to, kā izveidot pielāgotu atskaiti, skatiet sadaļā [Jaunas atskaites izveide, izmantojot SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Power BI ieskatu lietojumprogrammas

Microsoft Power BI un Dynamics 365 nodrošina efektīvu veidu, kā strādāt ar datiem, izmantojot ieskatu programmas. Informāciju par ieskatu programmu pieejamību skatiet lapā [Power BI ieskatu programmas](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Papildu resursi
Papildinformāciju par atskaišu izveidi risinājumā PSA skatiet šādās tēmās:

- [Darbs ar Project Service datu modeli](reports-working-project-service-data-model.md)
- [Informācijas paneļi](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
