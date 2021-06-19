---
title: Project Service Automation integrācijas parametri
description: Šajā tēmā izskaidrots, kā konfigurēt noklusējuma datu ievadīšanu, kad veicat Microsoft Dynamics 365 for Project Service Automation integrēšanu ar Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9793b680fc2be3b300689c4aded8005470f30519
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006430"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation integrācijas parametri

[!include[banner](../includes/banner.md)]

Lapā **Project Service Automation integrācijas parametri** var konfigurēt, kā tiek ievadīti noklusējuma dati, integrējot Dynamics 365 Project Service Automation programmā Dynamics 365 Finance. Lai projektus veiksmīgi sinhronizētu no Project Service Automation to Finance, ir jāiestata tālāk norādītie lauki.

Lai atvērtu lapu **Project Service Automation integrācijas parametri**, atveriet sadaļu **Projekta pārvaldība un grāmatvedība** \> **Iestatīšana** \> **Dynamics 365 for Project Service Automation integrācijas parametri**. 

> [!NOTE]
> - 8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.
> - Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.


| Cilnes                    | Lauks                | Apraksts |
|------------------------|----------------------|-------------|
| Vispārīgs                | Noklusējuma projekta tips | Atlasiet noklusējuma projekta tipu. Kad projekti tiek sinhronizēti no Project Service Automation, šī vērtība tiek izmantota, ja integrācijas veidnē nav norādīta noklusējuma vērtība. Sinhronizācijas laikā jaunu projektu lauks **Projekta tips** tiek iestatīts uz šo vērtību. Tomēr šī vērtība var tikt atjaunināta, kad projekta līguma rindas tiek sinhronizētas no Project Service Automation. |
|                        | Laika kategorija        | Atlasiet laika noklusējuma kategoriju. Šī vērtība tiek izmantota, kad stundu aprēķini tiek sinhronizēti no Project Service Automation. Kad stundu aprēķini un stundu faktiskie dati tiek sinhronizēti no Project Service Automation, **Kategorija** jauno projektu stundu prognožu lauks Finance sistēmā ir iestatīts uz šo vērtību. |
|                        | Maksas kategorija         | Atlasiet maksas noklusējuma kategoriju. Šī vērtība tiek izmantota, kad maksas dati tiek sinhronizēti no Project Service Automation. Kad maksas dati tiek sinhronizēti no Project Service Automation, **Kategorija** jauno maksas darījumu lauks Finance sistēmā ir iestatīts uz šo vērtību. |
| Projekta grupas noklusējumi | Projekta veids         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kur var atlasīt projekta tipu, lai iestatītu noklusējuma projekta grupu. Noteiktu projekta tipu var atlasīt tikai vienu reizi konfigurācijā. |
|                        | Projekta grupa        | Atlasiet atlasītā projekta tipa noklusējuma projektu grupu. Kad jauni projekti tiek sinhronizēti no Project Service Automation, lauks **Projekta grupa** tiek iestatīts kā projekta tipa noklusējuma vērtība, ja integrācijas veidnē nav norādīta noklusējuma vērtība. |
| Rēķina tipa noklusējuma iestatījumi  | Norēķinu tips         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kur var atlasīt norēķinu tipu, lai iestatītu noklusējuma rindas rekvizītu. Noteiktu norēķinu tipu var atlasīt tikai vienu reizi konfigurācijā. |
|                        | Rindas rekvizīts        | Atlasiet atlasītā norēķinu tipa noklusējuma rindas rekvizītu. Kad jauni stundu aprēķini, jauni izdevumu novērtējumi vai jauni faktiskie dati tiek sinhronizēti no Project Service Automation, lauks **Rindas rekvizīts** tiek iestatīts uz noklusējuma vērtību norēķinu tipam. |
| Funkcionalitātes bloķēšana  | Nav piemērojams       | Atlasiet funkcionalitāti, lai atspējotu Finance projektiem un līgumiem, kas cēlušies no Project Service Automation. Piemēram, varat izslēgt iespēju rediģēt līgumus un projektus, izveidot darba sadalījuma struktūras un ievadīt darba laika uzskaites tabulas Finance sistēmā. Ar grāmatvedību saistītie lauki joprojām tiks iespējoti pat tad, ja tie nav pieejami, izmantojot parametru iestatījumu. Pēc noklusējuma ir iespējota visa funkcionalitāte. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]