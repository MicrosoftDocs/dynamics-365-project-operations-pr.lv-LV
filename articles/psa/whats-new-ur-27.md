---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 27, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146672"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 27. Šīs versijas būvējuma numurs ir V3.10.45.98, un tas parasti ir pieejams, izmantojot 2021. gada janvāra pašatjauninājumu.

## <a name="update-release-27"></a>Atjauninājumu izlaidums 27

### <a name="bug-fixes"></a>Kļūdu labojumi

**Vispārīgi**

Ir novērstas tālāk norādītās problēmas.

- Project Service Automation spraudņu ģenerētos žurnālus nevar iestatīt uz automātisku dzēšanu.
- Automātiskā atjaunināšana neizdodas, jo Project Service Automation risinājums satur mantoto mantoto tukšo NavBarArea un nosaukuma elementu.

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- Režģis **Laika ieraksts** rāda nepareizus datus **No laika joslas neatkarīgo** datu darbībai.
- Režģis **Laika ieraksts** izveido nepareizu laiku **No laika joslas neatkarīgo** datu darbībai.
- Uzdevumu uzmeklēšana neaprobežojas ar atlasīto projektu lapā **Rediģēt laika ievadi**.
- Laiku apstiprināšana ar projektu nesaistītiem laika ierakstiem ir bloķēta, jo sistēma meklē projekta apstiprinātāja lomu.
- Pareizie ieraksti par faktiskajiem datiem rāda nepareizu kļūdas ziņojumu.
- Kad uzdevums satur tukšu vērtību faktiskām izmaksām un projekta kopsummas tiek atsvaidzinātas, tiek rādīta šāda kļūda "Dotās atslēgas vārdnīcā nav".
- Noteiktos gadījumos cilnes **Projekta novērtējums** filtri **Grupēt pēc** nerāda izdevumu aprēķinus.
- **Vasaras laika** intervāls netiek labots laika ierakstiem.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Kešdarbes uzlabojumi, kuri uzlabo veiktspēju, kas saistīta ar **Projekta** lapas ielādi.
- Novecojusi biznesa kārtula, kas neļauj pabeigt projekta uzdevumus.
- Microsoft Project pievienojumprogrammas kontūras neievēro pievienojumprogrammas kalendāru, kā dēļ rodas nepareizas resursu prasības.
- Izveidojot projektus no veidnēm, tiek nepareizi iestatīti piešķires datumi un tiek novērsta iespēja ģenerēt resursu prasības.
- Lietotājs nevar piekļūt opcijām **Kategorija**, **Apraksts** un **Statuss**, izmantojot tastatūru.
- Faktiskās projekta pārdošanas vērtības neiekļauj papildmaksu un materiālu pārdošanas vērtības.
- Faktiskās pārdošanas un faktisko izmaksu apkopošana notiek nepareizi ar atšķirīgiem valūtas kursiem.
- **Noklusējuma darba stundu veidnes** apraksts ir maldinošs.
- Veidojot atkāpi uzdevumam, netiek noņemta **Kategorija** lietotāja interfeisā, kamēr tā netiek atsvaidzināta.
- Trūkst validācijas, lai nodrošinātu savu beigu datumu pārsnieguša projekta pārvietošanu, nav atļauta.

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Projekta piedāvājuma rindā tiek ģenerēts tukšās atsauces izņēmums, jo ir redzams **Importēt no projekta aprēķina**, ja projekts nav atlasīts.
- Aizverot piedāvājumu kā **Iegūtu**, tiek rādīta šāda kļūda "Objekta atsauce nav iestatīta uz objekta instanci".
- Pielāgojuma statuss netiek iestatīts faktiskās maiņas laikā, atsaistot projektu no līguma rindas.
- Ja ir instalēts gan Dynamics 365 Field Service, gan Project Service Automation, opcijas **Bloķēt cenu noteikšanu** un **Izmantot pašreizējo cenu noteikšanu** netiek vienlaikus rādītas lapā **Rēķins**.
- Japāņu valodā tulkojums nesaskan ar citām kalendāra lapām.
- **Aktivizēt** un **Deaktivizēt** ir noņemtas no **Cenrāža saistību** entitījas programmā Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]