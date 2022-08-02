---
title: Projekta darba laika uzskaites tabulas mobilā programma
description: Šajā rakstā ir sniegta informācija par mobilo lietojumprogrammu Microsoft Dynamics 365 Project Timesheet. Projekta darba laika uzskaites tabulas mobilā programma ļauj lietotājiem iesniegt un apstiprināt darba laika uzskaites tabulas par projektiem savā mobilajā ierīcē.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110984"
---
# <a name="project-timesheet-mobile-application"></a>Projekta darba laika uzskaites tabulas mobilā programma

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Mobilā Microsoft Dynamics 365 Project Timesheet lietotne ļauj lietotājiem iesniegt un apstiprināt darba laika uzskaites tabulas projektiem savā mobilajā ierīcē (iPhone vai Android). Šī mobilā programma parāda darba laika uzskaites tabulas funkcionalitāti, kas atrodas Dynamics 365 Finance apgabalā Projektu pārvaldība un uzskaite. Tas palīdz uzlabot lietotāju produktivitāti un efektivitāti, kā arī ļauj savlaicīgi ievadīt un apstiprināt projekta darba laika uzskaites tabulas.

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana

Lejupielādējiet un instalējiet Microsoft Dynamics 365 Project Timesheet mobilo programmu, kas paredzēta Android vai ir iPhone no mobilā veikala jūsu ierīcei.

## <a name="enable-the-app"></a>Programmas iespējošana 

Finance ir jābūt iespējotai projekta darba laika uzskaites tabulas mobilajai programmai. Lai iespējotu funkcionalitāti, atveriet sadaļu **Projektu pārvaldības un grāmatvedības parametri \>darba laika uzskaites tabula** un atlasiet parametru **Iespējot Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Pierakstīšanās problēmu novēršana

**Problēma:** pierakstoties lietojumprogrammā Project Timeheet Mobile, lietotāji saņem kļūdas ziņojumu, kurā teikts, ka viņi "nevar piekļūt lietojumprogrammai "2bc50526-cdc3-4e36-a970-c284c34cbd6e" šajā nomniekā".

**Problēma:** pierakstoties lietojumprogrammā Project Timeheet Mobile, lietotāji saņem kļūdu, kas līdzinās kādam no šiem piemēriem:

- "AADSTS50020: lietotāja konts "[lietotājvārds]" no identitātes nodrošinātāja "https://sts.windows.net/[lietotnes id]" nepastāv nomniekā "[nomnieka ID]" un nevar piekļūt lietojumprogrammai "[lietotnes id]" šajā nomniekā."
- "Atlasītais lietotāja konts nepastāv nomnieka "[nomnieka ID]" un nevar piekļūt lietojumprogrammas "[lietotnes ID]" šajā nomniekā."

**Paskaidrojums:** Šīs problēmas izraisa izmaiņas, kas tika veiktas Azure Active Directory (Azure AD)2022. gada maijā un ir saistītas ar ārējiem lietotājiem. Tā kā šīs izmaiņas netika veiktas finansēšanas un darbības lietotnēs, tās var ietekmēt klientus jebkurā platformas vai lietojumprogrammas versijā.

**Labojums:** visi ārējie lietotāji ir jāaicina uz nomnieku, izmantojot Azure AD. Papildinformāciju skatiet rakstā [To lietotāju uzaicināšana, kuriem ir sadarbība ar Azure Active Directory B2B](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Pierakstieties programmā

1.  Startējiet programmu savā mobilajā ierīcē.

2.  Ievadiet savu Finance URL.

3.  Pirmo reizi pierakstoties sistēmā, tiek parādīts aicinājums ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.

4. Jūs tiksit pieteicies savā noklusējuma uzņēmumā.

## <a name="submit-a-project-timesheet"></a>Projekta darba laika uzskaites tabulas iesniegšana

Programmā var izveidot un iesniegt projekta darba laika uzskaites tabulu. Jaunu darba laika uzskaites tabulu var balstīt uz informāciju no iepriekšējās darba laika uzskaites tabulas, saglabātās rindas vai projekta piešķires. Ja esat norādīts kā pārstāvis, varat arī ievadīt darba laika uzskaites tabulu citam darbiniekam. Lai kā pārstāvis izveidotu darba laika uzskaites tabulu, atlasiet **pogu Izvēlne** un pēc tam atlasiet resursa nosaukumu.

Darba laika uzskaites tabulas lapa izveidos jaunu darba laika uzskaites tabulu par darba laika uzskaites tabulas periodu, pamatojoties uz šīsdienas datumu. Tiks parādīta darba nedēļa. Ja darba laika uzskaites tabulas periods attiecas uz vairākām nedēļām, varat atlasīt citu darba nedēļu no darba nedēļu cilnēm.
Ja pašreizējam datumam ir darba laika uzskaites tabula, tā tiks parādīta. Ja ir nepieciešams izveidot jaunu darba laika uzskaites tabulu citā darba laika uzskaites tabulas periodā, atlasiet pogu **Izvēlne** un pēc tam atlasiet **Jauna darba laika uzskaites tabula**.

Projekta informāciju var ievadīt, noklikšķinot uz darbības **Pievienot laiku** vai **Kopēt laiku no**. **Kopēt laiku no** darbība kopēs projekta rindas informāciju, bet ne stundas. Izvēlnē **Kopēt laiku no** ir šādas opcijas:

- **Kopēt no esošas darba laika uzskaites tabulas** — kopēt darba laika uzskaites tabulas rindas no esošas darba laika uzskaites tabulas.

- **Kopēt no izlases** — izveidot jaunas darba laika uzskaites tabulas rindas, izmantojot darba laika uzskaites tabulas iestatījumus, ko izvēlējāties kā izlasi.

- **Kopēt no piešķires** — izveidojiet jaunas darba laika uzskaites tabulas rindas no piešķirtajiem projektiem.

Parādītā projekta informācija ir atkarīga no lapā **Projektu pārvaldības un grāmatvedības parametri** definētajiem mobilajiem parametriem.

Laukā **Juridiskā entītija** atlasiet to juridisko personu, kurai veicāt projekta darbu. Lauks **Juridiskā entītija** ir pieejams tikai tad, ja jūsu juridiskajai personai ir iespējots starpuzņēmumu darba laika uzskaites tabulas atbalsts.

Atlasiet klientu, kurš ir saistīts ar darba laika uzskaites tabulas projektu. Sākotnējam laidienam Android klienta ieraksts netiek atbalstīts, jo vispirms ir jāatlasa projekts. Ja pirmo reizi atlasījāt projektu, lauks **Klients** tiek aizpildīts automātiski.

**Laukā Projekts** atlasiet projektu, kuram ievadāt laiku. Lauks **Klients** tiek aizpildīts automātiski.

Klientu un projektu uzmeklējumos tiek iespējota meklēšana, izmantojot gan klientus, gan projektus.

Pēc nepieciešamības atlasiet informāciju laukos **Kategorija**, **Darbība**, **Rindas rekvizīts**, **PVN grupa** un **Krājumu PVN grupa**. Šos laukus var ignorēt.

Lauks **Rindas rekvizīts** tiks iestatīts kā noklusējuma vērtība, pamatojoties uz projekta pārvaldības un grāmatvedības parametriem. Ja ir iespējoti projekta/kategorijas un kategorijas/resursa parametri, vērtība **Rindas statuss** tiek iestatīta uz šīs validācijas definēto noklusējuma vērtību. Ja projekta/kategorijas un kategorijas/resursa parametri nav iespējoti, rekvizīta **Līnija** vērtība pēc noklusējuma tiek noklusēta atbilstoši **laukam Iespējot noklusējuma rindas rekvizītu** **lapā Projektu pārvaldība un uzskaites parametri**. Vērtību **Rindas rekvizīts** var ignorēt.

Atlasiet dienu, lai pievienotu laiku. Ievadiet stundu skaitu, kas tika izstrādāts katru dienu.

Lai pievienotu komentārus par stundām, kurās ievadāt, noklikšķiniet uz **Pievienot komentārus** un pēc tam ievadiet komentārus iekšējai auditorijai, klientu auditorijai vai abiem.
Iekšējos komentārus var skatīt projekta pārvaldnieki. Klientu komentāri tiek iekļauti rēķinos.

Lai rindu saglabātu kā izlasi, atzīmējiet izvēles rūtiņu un pēc tam noklikšķiniet uz **Saglabāt kā izlasi**.

Finanšu dimensija un piesaistes atbalsts mobilajā lietojumprogrammā netiek nodrošināts.

Turpiniet pievienot projekta rindas, kas nepieciešamas, lai izpildītu darba laika uzskaites tabulu.

Lai nosūtītu darba laika uzskaites tabulu apstiprināšanas darbplūsmai, noklikšķiniet uz **Iesniegt**.

## <a name="review-timesheets"></a>Pārskatīt darba laika uzskaites tabulas

Izvēlnē ir pieejams saraksts ar laika uzskaites tabulām, kas jāpārskata. Šī opcija ir pieejama tikai tad, ja esat norādīts kā darbplūsmas apstiprinātājs. Tiek atbalstīti gan virsrakstu, gan rindu apstiprinājumi. Rindas līmeņa apstiprinājums piedāvā iespēju atzīmēt vienu vai vairākas rindas apstiprināšanai. Pēc darba laika uzskaites tabulas informācijas pārskatīšanas noklikšķiniet uz **Apstiprināt**, **Deleģēt** vai **Atgriezties**, lai turpinātu darbplūsmu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
