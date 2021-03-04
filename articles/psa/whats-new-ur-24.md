---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 24, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146717"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation atjauninājumu izlaidums 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 24. Šīs versijas būvējuma numurs ir V 3.10.42.43, un tas parasti ir pieejams, izmantojot 2020. gada oktobra pašatjauninājumu.

## <a name="update-release-24"></a>Atjauninājumu izlaidums 24

### <a name="bug-fixes"></a>Kļūdu labojumi

**Sales**

Ir novērstas tālāk norādītās problēmas.

- Problēma, iestatot produktu noklusējuma cenrādi.
- Piedāvājumu iegūšanas veiktspēja ir lēna, iebūvētā cenrāža un lomu cenu ierakstu kopijas dēļ.
- Pozīcijas **Projekta līgums / Pārdošanas centrs** > **Produkta rindas elements / Pasūtījuma rindas daudzums** tiek automātiski noapaļotas līdz tuvākajam veselajam skaitlim.
- Lasot cenrāžus, paaugstiniet līdz sistēmas privilēģijām.
- Kopējiet klienta adreses laukus **address1_freighttermscode** un **address1_shippingmethodcode** uz Piedāvājumu/pasūtījumu. 


**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

- **Laika ievades režģis** neatbalsta **Tikai datums** laika uzvedību.
- Vienums **Laika ievade** netiek automātiski atsvaidzināts. Ir nepieciešama manuāla atsvaidzināšana.
- Nevar importēt laika ierakstus no piešķīruma, ja resursu piešķīrumos ir pārtraukums (0 stundas).
- Veidojot laika ierakstu, iestatiet sākumu tādu pašu kā **msdyn_date**.
- Atkārtoti iespējojiet laika ievades lielapjoma rediģēšanu.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- Mēģinot atjaunināt sekojošu dienu rezervācijas statusu bez prasības, tiek izmests NullRef izņēmums.
- Ielādējot **Saskaņošanas skatu**, radās kļūda.


**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

- **Projekta grafikā**, mainot no **Manuāli** uz **Automātiski**, netiek veikta automātiska saglabāšana.
- Izdevumu izmaksām nevajadzētu tikt aprēķintam novirzes virzienā **Projekta izsekošanas režģī**.
- Nekonsekventa uzvedība **Novērtējuma tagu** kolonnu ielādes laikā un mainot **Laika sadalījuma** veidu.
- Faktiskās izmaksas projektā var neatspoguļot kopējās izmaksas no **Faktiskajām vērtībām**.
- **Novērtētais pabeigšanas datums** cilnē **Kopsavilkums** neatbilst **WBS grafikam**.
- **Faktisko stundu atjaunināšana** uz pārkaru atkāpes nedarbojas pareizi.
- Projekta vadītājs ārpus saknes **BU** nevar izveidot projektu.
- Uzdevuma vai kategorijas izmaiņas **Izdevumu novērtējumos** netiek saglabātas.
- **Līguma kopija** kopē rēķinu grafikus un izpildes statusu.
- Poga **Atsvaidzināt faktiskās vērtības** nepareizi aprēķina kopsavilkuma uzdevumus.
- Microsoft Project pievienojumprogramma: FixNull atsauces kļūda, ja kādam darba grupas dalībniekam ir tukša resursu plānošanas vienība.

