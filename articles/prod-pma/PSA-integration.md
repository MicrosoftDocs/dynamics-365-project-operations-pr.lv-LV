---
title: Project Service Automation pārskats
description: Šajā tēmā ir sniegta informācija par Dynamics 365 Project Service Automation integrācijas risinājumu Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685525"
---
# <a name="project-service-automation-overview"></a>Project Service Automation pārskats

[!include[banner](../includes/banner.md)]


Project Service Automation to Finance integration risinājums izmanto datu integrācijas līdzekli, lai sinhronizētu datus starp Dynamics 365 Finance gadījumiem un Dynamics 365 Project Service Automation izmantojot Common Data Service. Integrēšanas veidnes, kas ir pieejamas ar datu integrācijas līdzekli, iespējo projektu plūsmu, projekta līgumus, projekta līguma rindas, projekta līgumu rindu atskaites punktus, projekta uzdevumus, izdevumu darbību kategorijas, stundu aprēķinus un izdevumu tāmes no Project Service Automation uz Finance.

> [!NOTE]
> - Ja izmantojat versiju 7.3.0, ir jāinstalē KB 4074835. Tad varēsit integrēt fiksētas cenas projektus.
> - Ja izmantojat versiju 7.3.0 un no Project Service Automation ir jāievieš maksas transakcijas, jums ir jāinstalē KB 4345320, lai projekta rēķinā iekļautu šīs maksas.
> - Ja izmantojat versiju 8.0, varēsit izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.
> - Ja izmantojat versiju 8.0.1 vai jaunāku versiju, jūs varēsit sinhronizēt faktiskos datus.

Lai varētu integrēt Project Service Automation sistēmā Finance, ir jākonfigurē Project Service Automation integrācijas parametri. Papildinformācija: [Project Service Automation integrācijas parametri](PSA-parameters.md).

Šis integrācijas risinājums nodrošina tiešu sinhronizāciju šādos gadījumos:

- Project Service Automation uzturēt projekta līgumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Project Service Automation izveidot projektus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Project Service Automation uzturēt projekta līguma rindas, kā arī sinhronizēt tās tieši no Project Service Automation uz Finance.
- Project Service Automation uzturēt projekta līguma rindu atskaites punktus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Project Service Automation uzturēt projekta uzdevumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Uzturēt izdevumu transakciju kategorijas sistēmā Finance, kā arī sinhronizēt tās tieši no Finance uz Project Service Automation.
- Project Service Automation izveidot projekta stundu novērtējumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Project Service Automation izveidot projekta izdevumu novērtējumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.
- Veidot projekta laika, izdevumu un maksas faktiskos datus Project Service Automation, un Project Service Automation integrācijas žurnālā veidot projekta darbības, lai tās varētu grāmatot sistēmā Finance.

## <a name="data-synchronization"></a>Datu sinhronizācija

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti kā daļa no integrēšanas starp Project Service Automation un Finance.

> [!NOTE]
> Pašlaik nav pieejamas visas veidnes. Veidnes tiks izlaistas, kad tās būs pabeigtas.

[![Project Service Automation integrācija ar Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance sistēmas prasības

Lai izmantotu Project Service Automation uz Finance integrācijas risinājumu, ir jāinstalē Enterprise Edition 7.3 ar platformas atjauninājumu 12 vai jaunāku versiju.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation sistēmas prasības

Lai izmantotu Project Service Automation uz Finance integrācijas risinājumu, ir jāinstalē šādi komponenti:

- Dynamics 365 Project Service Automation versija 9.0.0.0 vai jaunāka versija
- Izredzes uz naudas risinājumu pakalpojumam Dynamics 365 Sales, versija 1.14.0.0 (V14) vai jaunāka versija
- Project Service Automation uz Finance risinājums Dynamics 365 Project Service Automation 1.0.0.0 vai jaunākai versijai

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instalējiet Project Service Automation uz Finance integrācijas risinājumu savā Project Service Automation instancē

Lejupielādējiet Project Service Automation uz Finance integrācijas risinājumu no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=57016) un izpildiet risinājumā iekļautos norādījumus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]