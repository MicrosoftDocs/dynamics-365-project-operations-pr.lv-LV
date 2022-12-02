---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 36, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas pieejami Microsoft Dynamics 365 Project Service Automation 36. atjauninājumu laidienā, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924991"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 36, V3. Šai versijai ir būvējuma numurs V3.10.57.152, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2021. gada oktobrī.

## <a name="update-release-36"></a>Atjauninājumu izlaidums 36

### <a name="bug-fixes"></a>Kļūdu labojumi

Ir novērstas tālāk norādītās problēmas.

**VispārīgI**
- **Noklusējuma darba stundu veidnes** lauka nosaukums projekta parametru lapā **Projekta parametri** tiek nepareizi tulkots.
- Asinhronie spraudņi nepareizi apstrādā izņēmumus, kas ir saistīti ar **SharedManagerableService**.

**Laiks un izdevumi**
- Ja trūkst žurnāla rindas vai lietotājam nav pareizo atļauju lasīt žurnāla rindas, tad rodas nepareiza kļūda, kad tiek atcelti projekta apstiprinājumi.
- Lietotāji nevar atcelt apstiprinājumu, ja izmaksu vai laika ievadei ir vairāk nekā viens saistītais projekta apstiprinājums.
- **Prombūtne** un **Atvaļinājums** ir nepareizi tulkoti ķīniešu valodā ātrās izveides uzmeklēšanas lapā **Laika ieraksti**.

**Resursu pārvaldība**
- Lietotājs nevar meklēt resursus sadaļā **Plānošanas palīgs**, kad skata režīms ir iestatīts uz **Diena**, **Nedēļa** vai **Mēnesis**.
- Vispārējiem resursiem ir nepareizi atļauts izmantot tukšus pozīciju nosaukumus. 
- Slēdzot līgumu kā zaudētu netiek atceltas turpmākas rezervācijas.

**Pārdošana**
- Ja vidē ir daudz produktu, tad **Materiālu novērtēšanas** režģī veiktspēja samazinās.
- Veidojot projektu no veidnes, projekta valūta pēc noklusējuma netiek mainīta uz attiecīgo projekta vadītāja līguma slēgšanas vienību.
- Faktiskās summas ne vienmēr atbilst projekta termiņa atspoguļotajām summām vai arī īpašos scenārijos prognozētās summas kļūst negatīvas.
- Rodas kļūda, ja sasaistāt no projekta veidnes izveidotu projektu ar līguma rindu.
- Lietotāji var dzēst līguma rindu ar atskaites punktiem, **Gatavs rēķinam** un **Rēķins izveidots**. Tam nevajadzētu būt atļautam.
- Ja aprēķini tiek importēti no projekta, tad piedāvājuma rindas detalizētas iekļaujamības ir iestatītas nepareizi, ja piedāvājuma rindai ir iespējota no uzdevuma atkarīga rēķinu izrakstīšana.
- Kad pievienojat fiksētas cenas norēķinu atskaites punktam, tad atskaites punkts netiek atspoguļots atskaites punkta apakšrežģī, kamēr lapa netiek atsvaidzināta.
- Veidojot projekta līgumu ar piedāvājuma nosaukumu, kas ir Null, tiek ģenerēts atsauces izņēmums Null.
- Manuāla režīma uzdevumi, kuru projekta valūta atšķiras no resursa valūtas, izraisa nepareizus cenas aprēķinus.
- Lietotāji nevar atsaukt transakciju, kas tika veiksmīgi izlabota, izmantojot izlabotu rēķinu.
- Deaktivizētās transakciju kategorijas tiek rādītas **Izmaksu aprēķinu** režģī.



