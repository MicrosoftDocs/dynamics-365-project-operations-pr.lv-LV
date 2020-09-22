---
title: Kas jauns Project Service Automation atjauninājuma izlaidumā 12, 3. versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 12, 3. versijā
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753486"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation atjauninājuma izlaidums 12, versija 3
Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 12. Šai versijai ir būvējuma numurs V3.10.2.34, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2019. gada oktobrī.

## <a name="update-release-12"></a>Atjauninājumu izlaidums 12

### <a name="bug-fixes"></a>Kļūdu labojumi

- Laiks un izdevumi

    - Novērsts: laika ieraksta kļūdu ziņojumapmaiņa ir atjaunināta ar atbilstošāku kontekstu.
    - Novērsts: laika ievadņu režģis un grafiks pareizi parāda vertikālo ritjoslu, ja nepieciešams.
    - Novērsts: iesniegtus izdevumu un laika ierakstus nevar apstiprināt.
    - Novērsts: apstiprinājuma atcelšanas apstiprinājuma dialoglodziņš ir labots, lai atspoguļotu apstiprinājuma statusu, ja tas ir mainīts no **Apstiprināts** uz **Iesniegts**.
    - Novērsts **:** Cena **,** vienība un **daudzums** lauki tagad tiek bloķēti izdevumu ierakstā pēc tā apstiprināšanas.

- Projekta pārvaldība

    - Novērsts : **Jauna** darbība **Darba grupas** dalībnieka galvenajā veidlapā ir noņemta.
    - Novērsts: resursu piešķires ir atjauninātas uz kontu neprecīzām noapaļošanas kļūdām, kas izraisa uzdevuma beigu datuma maiņu.
    - Novērsts: uzdevumu režģī attiecīgās servera puses kļūdas tiks rādītas lietotājam.
    - Novērsts: darba grupas dalībnieka vārds tagad atveido uzdevumu lietotāju, nevis amata nosaukumu.

- Resursu pārvaldība

    - Novērsts: resursa prasību informācija projektiem, kas izveidoti no veidnes, tagad izmanto projekta kalendāru.
    - Novērsts: prasmes un kompetences, kas tagad ir noklusētas no lomu pamatdatiem līdz šai lomai izveidotajām resursu prasībām.

- Sales

    - Novērsts: **līguma galvenajā** veidlapā tiek dublēti atrasto objektu ID.
    - Novērsts: loģika ir atjaunināta, lai būtu redzama cilne **Piedāvājuma analīze**, lai tā parādītu cilnes metadatu iestatījumus.
    - Novērsts: faktiskā ieraksta uzskaites datums tagad ir no laika/izdevumu ieraksta datuma, nevis apstiprinājuma datuma.
