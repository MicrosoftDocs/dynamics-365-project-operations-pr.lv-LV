---
title: Jaunumi Project Service Automation atjauninājuma laidienā 16, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 16, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753482"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation atjauninājumu izlaidums 16, V3
Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.

Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet rakstu [Vēlama risinājuma instalēšana un atjaunināšana](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 16. Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada janvāra pašatjauninājumu

## <a name="update-release-16"></a>Atjauninājumu izlaidums 16

### <a name="bug-fixes"></a>Kļūdu labojumi

-   Laiks un izdevumi

    -   Izlabots: lietotāji, kuri mēģina iesniegt apstiprināšanai dzēstus laika un izdevumu ierakstus, tagad saņems atbilstošus kļūdu ziņojumus.

-   Projekta pārvaldība

    -   Izlabots: darba grupas dalībniekiem veidnēs definētās resursu struktūrvienības tiek ievērotas, un veidnes tiek lietotas jaunajā projektā.

    -   Izlabots: uzlabots ieraksta īpašumtiesību atkārtotas piešķiršanas process.

    -   Izlabots: projektus, kas tiek kopēti, nevarēs kopēt, kamēr netiks pabeigtas visas kopēšanas darbības.

-   Resursu pārvaldība

    -   Izlabots: paplašinātā rezervācija tagad pareizi apstrādā īsus periodus un vairs neveido nulles stundas ilgākiem rezervējumiem.

    -   Izlabots: saskaņošanas skats tagad tiek atveidots, kad projekta laika josla ir +5:30 GMT, bet lietotāja laiks AOne ir atšķirīgs.

-   Sales

    -   Izlabots: ja tiek noņemts līguma rindā kartētais projekts un tiek kartēts jauns projekts, jaunā projekta faktiskie ieraksti netiek atkārtoti novērtēti, pamatojoties uz līguma rindā definētajām rēķina un cenu kārtulām. Šajā izlaidumā tas tika novērsts. Jaunajā kartētajā projektā cenas un faktiskie ieraksti tiks apgriezti un atkārtoti izveidoti, pamatojoties uz līguma rindas cenu un norēķinu kārtulām. Nekartētā projekta faktiskie ieraksti arī tiks atkārtoti novērtēti un atkārtoti izveidoti.

    -   Izlabots: papildu validācija tika pievienota novērtējuma rindas laukam **Summa**, lai nodrošinātu, ka nav iekļautas nulles vērtības.

    -   Izlabots: ja tika atjaunināti faktiskie projekta vērtības, projekta galvenajā veidlapā tika pievienota poga Atsvaidzināt, lai lietotāji varētu atkārtoti sinhronizēt faktiskās vērtības.

    -   Izlabots: ja lietotājs jauninās no versijas 2.X uz 3.X, tiks atļauti projekti ar vērtību NULL projekta nosaukumā.

