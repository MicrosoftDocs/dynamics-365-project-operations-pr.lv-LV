---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 16, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143642"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation atjauninājumu izlaidums 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.  Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet rakstu [Vēlama risinājuma instalēšana un atjaunināšana](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 16. Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada janvāra pašatjauninājumu.


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



[!INCLUDE[footer-include](../includes/footer-banner.md)]