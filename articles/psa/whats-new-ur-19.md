---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 19, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143615"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation atjauninājumu izlaidums 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 19. Šīs versijas būvējuma numurs ir V3.10.30.41, un tā ir vispārīgi pieejama, izmantojot 2020. gada maija pašatjauninājumu.

## <a name="update-release-19"></a>Atjauninājumu izlaidums 19

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas. 

- No laika ierakstu importēšanas atvasinātās kļūdas netiek pareizi apstrādātas.
- Laika ierakstu režģis neatbalsta lauka **Tikai datums** darbību.
- Projekta resursi projektā nevar izveidot izdevumus.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas. 

-  Otrā līmeņa atvasinātais uzdevums izraisa nepareizu ieguldījuma galīgo izmaksu novērtējumu pabeigšanas (EAC) aprēķināšanā.

**Sales**

Ir novērstas tālāk norādītās problēmas. 

- Darbība **Pārrēķināšana** nestrādā ar izdevumu līguma rindu detaļām vai piedāvājuma rindu detaļām.
- Izdevumu aplēsēm trūkst opcijas **Atjaunināt cenas**.
-  Klienti nevar atlasīt pielāgotus līguma statusa iemeslus lapā **Projekta līgums**.
- Veidojot pielāgotu cenrādi no piedāvājuma, klienti pieredz pasliktinātu darbību.
- Klienti pieredz nekonsekvenci, izmantojot noklusējuma **vienību** lapās **Piedāvājumu rindu informācija** un **Līgumu rindu informācija**.
- Rēķinā neiekļaujamo darbību kategorijas elementu pievienošana rēķinā iekļaujamā līguma rindai, neievēro darbību kategorijas norēķinu veidu **Rēķinā neiekļaujams**.
- Klienti nevar izmantot tikko pievienotās lomas un kategoriju iepriekš izveidotiem līgumiem.
- Klienti pieredz pasliktinātu darbību Nevajadzīgi izgūt failā PreValidateProjectTeamMemberUpdate.cs
- Lomas, kas sarakstā **Resursu kategorijas** ir iestatītas kā rēķinā neiekļaujamas, jāpievieno cilnei **Rēķinā iekļaujamās lomas** kā **Rēķinā neiekļaujamās** projekta līguma rindā.
- Klient var pieredzēt pasliktinātu darbību, veidojot projektu, jo **GetBookableResourceIdFromUser** izgūst visas rezervējamo resursu kolonnas, nevis tikai primāro ID.
- Entītijai **TransactionType** trūkst pirms validācijas atjauninājuma spraudnis, lai neļautu lietotājiem ievadīt **Vienības** un **UnitGroups**, kas transakciju tipiem nav derīgas.
- Darbība **Noņemt** laika ieraksta importēšanai nedarbojas.
