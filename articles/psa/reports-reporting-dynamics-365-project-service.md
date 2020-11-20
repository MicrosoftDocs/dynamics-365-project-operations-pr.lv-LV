---
title: Atskaišu veidošanas sākumlapa
description: Šajā tēmā ir sniegta informācija par atskaišu veidošanu programmā Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: e1a645b157c56066e56b22ea8cf0324fbc1ddd2c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120327"
---
# <a name="reporting-home-page"></a>Atskaišu veidošanas sākumlapa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation ļauj projekta organizācijām efektīvi pārvaldīt savas biznesa operācijas. Jebkurā projektā darba grupas dalībniekiem ir jāpārvalda iespēja, jāizveido darba piedāvājums un plāns, jānodrošina resursi projektiem, jāpārvalda darbs atbilstoši plānam, jāizraksta rēķins par darbu un pēc tam jādara viss, lai pabeigtu projektu. Iespēja ziņot par operācijām ir būtiska, lai noteiktu organizācijas veselību un veiktu nepieciešamās korektīvās darbības. PSA izmanto Microsoft Dynamics 365 atskaišu izveides metodes un tehnoloģijas visu atskaišu izveidei. Papildinformāciju par atskaišu izveides iespējām skatiet: [Atskaišu rakstīšanas rokasgrāmata, Dynamics 365 Customer Engagement (on-premises)versija 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Atskaites vednis

Atskaites vednis ļauj lietotājiem, kas nav izstrādātāji, izveidot vienkāršas atskaites. Tā kā lietojumprogramma ir izveidota uz esošas platformas, lietošanas pieredze ir tāda pati kā pieredze, kas ir dokumentēta sadaļā [Atskaites izveide vai rediģēšana, izmantojot Atskaites vedni](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Taču būs jāizmanto risinājumam Project Service Automation raksturīgās entītijas.

## <a name="custom-sql-server-reporting-services-reports"></a>Pielāgotas SQL Server atskaišu izveides pakalpojumu atskaites

Ja uzņēmumam ir nepieciešama noteikta atskaite, ko nevar izveidot, izmantojot Atskaites vedni, varat izveidot pielāgotu atskaiti. Ir jābūt instalētam pakalpojumam Microsoft Visual Studio kopā ar atbilstošajiem Microsoft SQL Server Data Tools un atskaišu autorēšanas paplašinājumiem. Papildinformāciju par rīkiem un versijām skatiet sadaļā [Atskaišu izstrādes vide, izmantojot SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Informāciju par to, kā izveidot pielāgotu atskaiti, skatiet sadaļā [Jaunas atskaites izveide, izmantojot SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Power BI ieskatu lietojumprogrammas

Microsoft Power BI un Dynamics 365 kopā nodrošina efektīvu veidu, kā strādāt ar datiem, izmantojot ieskatu programmas. Informāciju par ieskatu programmu pieejamību skatiet lapā [Power BI ieskatu programmas](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Papildu resursi
Papildinformāciju par atskaišu izveidi risinājumā PSA skatiet šādās tēmās:

- [Darbs ar Project Service datu modeli](reports-working-project-service-data-model.md)
- [Informācijas paneļi](reports-dashboards.md)

