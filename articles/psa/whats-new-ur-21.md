---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 21, V3
description: Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami projektu pakalpojumu automatizācijas atjaunināšanas laidienā 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918827"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation atjauninājumu izlaidums 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).

Šajā rakstā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti project service automation V3, Update Release 21. Šīs versijas būvējuma numurs ir V 3.10.32.50, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.

## <a name="update-release-21"></a>Atjauninājumu izlaidums 21

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Kad tiek viesota **Laika ievadņu režģa vadīkla** informācijas paneļos, režģis neizmanto visu informācijas paneļa režģa konteinera platumu.
- Noteiktām laika zonām **Laika ieraksta** režģa vadīklā netiek rādīti ieraksti.
- Laika ieraksti, kas ir pēc 21:00, tiek rādīti nepareizā dienā.
- Lietotāji nevar iesniegt izdevumus, ja izdevumu kategorijai **Vajadzīga izdevumu kvīts** nav vērtības.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Neaktīvas rezervācijas tiek rādītas skatā **Saskaņošanas**.
- Vispārējai resursu izpildei trūkst validācijas, lai nodrošinātu, ka pastāv derīgs rezervācijas statuss.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- **Projekta** veidlapu režģi (**Resursu piešķiršana**, **Uzdevums**, skats **Saskaņošana**, **Izdevumu aprēķini**) paliek rediģējami pat tad, ja projekts nav aktīvs.
- Dublētos klientus nevar sapludināt ar klientiem, kas ir saistīti ar apstiprinātajiem projekta līgumiem.
- Ja tiek pievienots resurss, kam nav derīga kalendāra, sistēma neatgriež lietotājam draudzīgu kļūdas ziņojumu.
- Poga **Pievienot uzdevumu** poga uzdevuma režģī ir iespējota, ja projekts ir saistīts ar **Microsoft Project pievienojumprogrammu**.
- Intensitāte nekontrolējami pieaug, kad uzdevums ar kategoriju tiek piešķirts resursam, kura lomai ir definēta izmaksu cena.

**Sales**

Mēs esam veikuši šādus uzlabojumus:

- **Rēķinu biežums** un **Apmaksas sākums** ir pārvietoti uz cilni **Rēķinu grafiks**.

Ir novērstas tālāk norādītās problēmas.

- **Kopējā pārdošanas cena** ir nulle (0) attiecībā uz **Kategorija**, pat ja **Lomai** ir kopējā pārdošanas cena, kas nav nulle.
- Klienti nevar mainīt lauka **Rēķina statuss** vērtību uz **Gatavs rēķinu izrakstīšanai**, ja cits pielāgots process atjaunina papildu lauku.
- Poga **Atsvaidzināt rēķina rindas** atkārtoti tiek atlasīta, var izveidot vairākas dublētas rindas.
- Poga **Atjaunināt cenas** nedarbojas apakšrežģī **Lomas cena** veidlapā **Ātrais skats**.
- **Pārdošanas cenu saraksta risinājuma** loģika nepareizi uztver laika zonas, kas izraisa nepareizu cenrāžu atlasi.
- Projekta **Faktiskās kopējās izmaksas** var tikt dalītas ar frakcionētu summu pēc viena ieraksta apstiprināšanas.
- **Cenu atrisināšanas** loģika nenodrošina lietotājam draudzīgu kļūdas ziņojumu, ja **Izgūtā RolePrice** nav vērtību laukos **“Primārā vienība”** un **“Cena primārajās vienībās”**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
