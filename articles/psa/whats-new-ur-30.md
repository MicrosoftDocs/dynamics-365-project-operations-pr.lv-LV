---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 30, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852873"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 30. Šīs versijas būvējuma numurs ir V 3.10.51.61, un tā ir vispārīgi pieejama, izmantojot 2021. gada aprīļa pašatjauninājumu.

## <a name="update-release-30"></a>Atjauninājumu izlaidums 30

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Rodas kļūda, kad lapā **Ātrā izveide** izveidojat un saglabājat laika ierakstu, ja ir noņemts lauks **Loma**.
- Filtrs Laika ievade lieto nepareizo filtra operatoru.
- Kad laika ievades vadīklā atlasāt **Kopēt nedēļu**, kopētās laika uzskaites tabulas netiek automātiski parādītas.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Paplašinot rezervāciju, rezervācijas statuss, kas piešķirts stingrajai rezervācijai, ir nepareizs. Paplašinot rezervāciju, tiek ņemts vērā rezervācijas statuss, kas rezervācijas iestatīšanas metadatos definēts kā **Iesniegts**.
- Ja nav norādīts derīgs rezervācijas statuss, kļūdas ziņojums nav pareizi lokalizēts.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Nevar izveidot projektus vienā valūtā un ietvert saistītos uzdevumus citā valūtā.

**Pārdošana**

Ir novērstas tālāk norādītās problēmas.

- Veicot cenrāža kopēšanu, cenas netiek atjauninātas.
- Neizdodas slēgt piedāvajumu kā uzvarētu, ja izmaksu detalizētai informācijai ir izcelsmes vērtība.
- Entītijā **Projekta uzdevums** **Izmaksu aprēķins** ir pārdēvēts par **Plānotās izmaksas (pamatvalūtā)**.
- Izveidojot vai dzēšot rēķinus, tiek ģenerēts nulles atsauces izņēmums.
