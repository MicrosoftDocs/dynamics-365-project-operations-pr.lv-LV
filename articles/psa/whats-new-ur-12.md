---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 12, V3
description: Šajā rakstā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 12, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922645"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation atjauninājumu izlaidums 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 12. Šai versijai ir būvējuma numurs V3.10.2.34, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2019. gada oktobrī.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
