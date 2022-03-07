---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 32, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994870"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 32. Šīs versijas būvējuma numurs ir V3.10.53.108, un tas parasti ir pieejams, izmantojot 2021. gada jūnija pašatjauninājumu.

## <a name="update-release-32"></a>Atjauninājumu izlaidums 32

### <a name="bug-fixes"></a>Kļūdu labojumi

#### <a name="general"></a>VispārīgI

- Ja neizdodas veikt lielu jaunināšanu, ir jābloķē tikai galvenie lietojumprogrammas ieejas punkti, lai nodrošinātu, ka koplietojamās entītijas joprojām ir pieejamas.

#### <a name="time-and-expense"></a>Laiks un izdevumi

Ir novērstas tālāk norādītās problēmas.

- **TimeEntriesImportFromResourceAssignment** nesatur resursu piešķiršanas kontūru sadaļas sākuma un beigu laikus.
- Atlasot **Atvērt ierakstu** režģī **Laika ieraksts**, var nebūt atļauts atlasīt citas veidlapas.
- Importējot piešķires laika ierakstos, klienta koda vaicājums var ģenerēt garu URL, kas izraisa vaicājuma kļūmi.
- Režģī **Laika ieraksts**, dzēšot no šūnas vērtību, fokuss nepaliek režģī.
- Poga **Noraidīt** ir noņemta no skata **Apstrādē esošie apstiprinājumi** mūsdienīgiem apstiprinājumiem.
- Laika ierakstu lielapjoma apstiprinājuma stabilitāti un veiktspēju ietekmē savstarpēja bloķēšana, un nespēja atbilstoši apstrādāt pielāgojumus, kas ir saistīti ar entītiju **Laika ieraksts**.

#### <a name="project-planning"></a>Projektu plānošana

- Atjauninot projektu, kuram laukā **Līgumslēdzēja vienība** ir vērtība Null, tiek ģenerēts nulles atsauces izņēmums.
- Funkcija **Atsvaidzināt projekta kopsummas** nepareizi aprēķina projektā atlikušās izmaksas un atlikušos pārdošanas darījumus.
- Lieki cenu noteikšanas aprēķini ietekmē veiktspēju, kas saistīta ar resursu piešķiršanas kontūru atjauninājumiem.

#### <a name="resource-management"></a>Resursu pārvaldība

Ir novērsta šāda problēma:

- Ja rezervējama resursa kalendāra noslodze pārsniedz 1, funkcija Project Service Automation nepareizi atpazīst noslodzi kā 0 (nulli). Tāpēc plānošanas skatā rodas bezgalīga cilpa.

#### <a name="sales"></a>Pārdošana

Ir novērstas tālāk norādītās problēmas.

- Kad tiek izveidota žurnāla rinda, kurā ir pielāgots transakciju tips, rodas šāds nulles atsauces izņēmums: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Lomas un kategorijas, kas tiek deaktivizētas pirms piedāvājuma kopēšanas, nedrīkst pievienot tikko nokopētā piedāvājuma rēķinā iekļaujamajām lomām un kategorijām.
- Dokumenta datums un uzskaites datums nav saskaņoti ar sākuma datumu, kas ir norādīts tieši melnraksta rēķinā izveidotajā rēķina rindas informācijā.
- Scenārijos, kas ir saistīti ar lomu un kategoriju deaktivizēšanu pirms piedāvājuma kopēšanas, tiek ģenerēti nulles atsauces izņēmumi.
- Darbība **Atjaunināt cenas** lapā **Projekti** neatjaunina izdevumu aprēķinus un materiālu aprēķinus.