---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 33, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601487"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Tas ir saderīgs ar Dynamics 365 9.x. Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 33. Šai versijai būvējuma numurs ir V3.10.54.98, un tā ir vispārīgi pieejama ar pašatjauninājumu 2021. gada jūlijā.

## <a name="update-release-33"></a>Atjauninājumu izlaidums 33

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Divi bloķēti lauki, **msdyn_description** un **msdyn_externaldescription** var rediģēt pēc iesniegšanas.
- Kļūdas ziņojums tiek parādīts, izveidojot izmaksas, kas nav saistītas ar projektu.
- Izveidojot laika ierakstu, resursa loma pēc noklusējuma tiek aktivizēta kā neaktīva loma.
- Netiek dzēstas žurnāla rindas, kas saistītas ar atsauktiem un dzēstiem izdevumiem.
- **Laika ieraksta ātrās izveides formā** atjauniniet **Projekta uzdevumu saraksta** skatu, lai mainītu pēc noklusējuma parādīto datumu uz uzdevuma sākuma datumu.
- Izveidojot laika ierakstu no rezervējamā resursa cilnes **Saistīts**, pierakstītajam lietotājam, nevis galvenajam rezervējamam resursam laika ieraksts tiek izveidots nepareizi.
- Jauni lauki tiek pievienoti dialoglodziņam **Lielapjoma apstiprinājuma MDD**.

**Projektu plānošana**

Ir novērstas tālāk norādītās problēmas.
- Lēna projekta izveides veiktspēja, lietojot projekta darba stundu veidnes sarežģītos kalendāros.
- Ja sākuma datums ir lielāks par beigu datumu, kopēšanas projekta veidnē tiek rādīta kļūda, jo katra lauka laika komponents atšķiras.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.
- Resursu lietojuma vaicājumā tiek izmantots nepareizs parametrs, bet XML rada nepareizus filtrēšanas rezultātus **Resursu lietojuma** režģī.
- Apstiprinājums **Rezervāciju pagarināšana** parāda nepareizu rezervāciju beigu datumu.

**Pārdošana**

Ir novērstas tālāk norādītās problēmas.
- Rodas kļūdas ziņojums, ja kategorijas cena tiek izveidota ar trūkstošām vērtībām.
- Rodas kļūdas ziņojums, ja līguma rindas atskaites punkts tiek izveidots bez pasūtījuma rindas.
