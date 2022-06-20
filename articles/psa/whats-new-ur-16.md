---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 16, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation Update Release 16, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926509"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation atjauninājumu izlaidums 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.  Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet rakstu [Vēlama risinājuma instalēšana un atjaunināšana](/dynamics365/project-service/upgrade-psa-home-page).
Šajā rakstā ir uzskaitītas funkcijas un labojumi, kas ir jauni vai mainīti PSA V3, 16. atjauninājuma laidienam. Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada janvāra pašatjauninājumu.


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
