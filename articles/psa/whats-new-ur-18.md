---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 18, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: b35c2f8f67e1bb75493a8787f1c4d8c2baf74d51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280767"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation atjauninājumu izlaidums 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 18. Šīs versijas būvējuma numurs ir V 3.10.8.12, un tā ir vispārīgi pieejama, izmantojot 2020. gada aprīļa pašatjauninājumu.

## <a name="update-release-18"></a>Atjauninājumu izlaidums 18

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

- Izlabots: plūsmās **Atsaukums**, **Pieprasījums** un **Atcelšanas apstiprinājums** rodas izņēmumi ar neskaidriem kļūdu ziņojumiem.
- Izlabots: ja **Atcelšanas apstiprinājums** netiek piemērots izdevumiem, netiek parādīta atbilstoša kļūda.
- Izlabots: laika ievadnes režģis nepareizi apstrādā brīvdienas Austrālijā pēc ziemas/vasaras laika (DST) maiņas oktobrī.
- Izlabots: nepareiza noklusējuma loģika neļauj iesniegt izdevumus.
- Izlabots: ja neizdodas laika ieraksta apstiprinājums, apstiprinājums paliek stāvoklī **Gaida**.
- Izlabots: SQL kļūdas lielapjoma apstiprinājumos (strupsaķere/taimauts).
- Izlabots: būtiskas veiktspējas problēmas lietotāju pieredzē, ko izraisa darba grupu dalībnieku atjaunināšana laika ierakstu apstiprināšanas laikā.

**Projekta pārvaldība**

- Izlabots: laika zonas paziņojums ir pārvietots no **saskaņošanas** skata uz **projekta** galveno veidlapu.
- Izlabots: kalendāra veidne netiek pareizi iestatīta uz noklusējumu, atverot jaunu projekta veidlapu.
- Izlabots: uz chromium bāzes izstrādātām pārlūkprogrammām lietotāji nevar viegli atlasīt pirmstecīgos uzdevumus dzēšanai.
- Izlabots: projekta izveide vai kopēšana **no tukšas veidnes** ielādē nesaistītus uzdevumus.
- Izlabots: noteiktos lietojuprogrammas Edge gadījumos, jauna piešķīruma no uzdevumu režģa izveidošanas laikā tiek izveidoti dublikāta ieraksti.
- Izlabots: manuālajā režīmā lietotāji nevar atjaunināt uzdevumu sākuma datumus, lai tie būtu vēlāki par pašreiz saglabātajiem datumiem.

**Resursu pārvaldība**

- Izlabots: **saskaņošanas** skata kopsummas rinda nepareizi aprēķina rezervācijas dispersiju pēc rezervācijas pagarināšanas.
- Izlabots: **saskaņošanas** skats nepareizi parāda resursu piešķīrumus, ja rezervācijas resursam ir kalendārs, kas neatbilst projekta kalendāram.

**Sales**

- Izlabots: ja laika ieraksti tiek atkārtoti apstiprināti (**Apstiprināt > Atcelt >** apstiprināt vēlreiz), tiek izveidots rēķinā neiekļaujams dublikāts.


[!INCLUDE[footer-include](../includes/footer-banner.md)]