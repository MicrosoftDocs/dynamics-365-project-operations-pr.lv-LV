---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 14, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 14, 3. versijā
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124827"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation atjauninājumu izlaidums 14, V3
Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 14. Šai versijai ir kompilācijas numurs V 3.10.4.21, un tas ir pieejams šādā grafikā:

- **Vispārēja pieejamība (pašregulācija):** 2020. gada janvāris
- **Automātiskā atjaunināšana:** 2020. gada februāris

## <a name="update-release-14"></a>Atjauninājumu izlaidums 14

### <a name="enhancements"></a>Uzlabojumi

- Sales

     - Pielāgotas lauku vērtības no **Piedāvājuma rindas detalizētā informācija** tiek kopētas **Projekta līgumu rindu detalizētā informācija**, kad piedāvājums tiek **Slēgts kā iegūts**.
     - Apstiprinātie projekti var būt **Slēgti kā zaudēti**.

- Resursu pārvaldība

     - Pagarinot rezervācijas, lietotājiem tiks piedāvāts apstiprinājuma dialoglodziņš, lai apkopotu rezervācijas rezultātus un nodrošinātu saiti, lai uzturētu rezervācijas.


### <a name="bug-fixes"></a>Kļūdu labojumi

- Laiks un izdevumi

     - Novērsts: uzlabota lietotāja pieredze kad lietotājs nav atlasījis nevienu ierakstu, kas jālabo.

- Resursu pārvaldība

     - Novērsts: resursa vairākkārtēja rezervācija pārsniedz iegrāmatoto resursa nosaukumu.

- Sales

     - Novērsts: kopējā pārdošanas cena netiek aprēķināta, kamēr lietotājs neievada arī izmaksu cenu projekta izdevumu aplēsēm.
     - Novērsts: piedāvājuma slēgšana kā **Iegūts** nerodas, ja saistītais projekta līgums nav statusā **Melnraksts**.

