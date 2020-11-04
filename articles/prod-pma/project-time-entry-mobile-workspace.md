---
title: Projekta laika ieraksta mobilā darbvieta
description: Šajā tēmā ir sniegta informācija par to, kā izmantot projekta laika ieraksta mobilā darbvietu. Šī darbvieta lietotājiem ļauj ievadīt un saglabāt laiku attiecībā pret projektu, izmantojot savu mobilo ierīci.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080425"
---
# <a name="project-time-entry-mobile-workspace"></a>Projekta laika ieraksta mobilā darbvieta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par **Projekta laika ierakstu** mobilo darbvietu. Šī darbvieta lietotājiem ļauj ievadīt un saglabāt laiku attiecībā pret projektu, izmantojot savu mobilo ierīci.

Šo mobilo darbvietu ir paredzēts izmantot kopā ar Dynamics 365 Unified OPS mobilo programmu. 

## <a name="overview"></a>Pārskats
Kā daļa no ikdienas darba projekta resursi bieži vien atrodas uz vietas vai ceļojumā. **Projekta laika ieraksts** mobilo darbvietu lietotājiem ļauj ievadīt apmaksājamu vai nemaksājamu laiku attiecībā uz projektu, izmantojot savu izvēlēto mobilo ierīci. Tāpēc projekta resursi var ierakstīt laika ierakstus jebkurā laikā un vietā. Viņi var arī apskatīt jau ierakstītos laika ierakstus. 

Konkrēti **Projekta laika ieraksts** mobilajā darbvietā lietotāji var veikt šādus uzdevumus:

-   Atlasītajā datumā ievadiet stundu skaitu, kas patērēts noteiktam uzdevumam.
-   Meklējiet pēc projekta nosaukuma vai klienta, lai atrastu projektu laika ievadīšanai.
-   Norādiet kategoriju un darbību patērētajam laikam.
-   Ierakstiet laiku kā apmaksājamu vai neapmaksājamu šim projektam.
-   Ja vēlaties, ievadiet ārējos vai iekšējos komentārus.

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no tā, kāda versija ir Microsoft Dynamics 365, kas ir izvietota jūsu organizācijā.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Priekšnosacījumi, ja izmantojat Dynamics 365 Finance
Ja jūsu organizācijai ir izvietots Finance, sistēmas administratoram ir jāpublicē **Projekta laika ieraksts** mobilajai darbvietai. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat versiju 1611 ar platformas atjauninājumu 3 vai jaunāku versiju
Ja jūsu organizācijai ir izvietota versija 1611 ar platformas atjauninājumu 3 vai jaunāku versiju, sistēmas administratoram ir jāizpilda tālāk minētie priekšnosacījumi. 

<table>
<thead>
<tr class="header">
<th>Priekšnosacījums</th>
<th>Loma</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>KB 4018050 ieviešana.</td>
<td>Sistēmas administrators</td>
<td>KB 4018050 ir X + + atjaunināšanas vai metadatu labojumfails, kurā ir iekļauts <strong>Projekta laika ieraksts</strong> mobilajām darbvietā. Lai ieviestu KB 4018050, jūsu sistēmas administratoram ir jāizpilda šīs darbības.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni</a>, kurā ir <strong>ApplicationSuite</strong> un <strong>ProjectMobile</strong> modeļi, un pēc tam augšupielādējiet izvēršamo paku uz LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Izmantojiet izvēršamo pakotni</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicējiet <strong>Projekta laika ierakstu</strong> mobilajai darbvietai.</td>
<td>Sistēmas administrators</td>
<td>Skatiet <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicēt mobilo darbvietu</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana

Lejupielādējiet un instalējiet Finance and Operations mobilo programmu:

-   [Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstieties mobilajā programmā
1.  Startējiet programmu savā mobilajā ierīcē.
2.  Ievadiet savu Dynamics 365 URL.
3.  Pirmo reizi pierakstoties sistēmā, tiek parādīts aicinājums ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
4.  Pēc pierakstīšanās programmā tiek rādītas pieejamās darbvietas jūsu uzņēmumam. Ņemiet vērā, ka tad, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, būs jāatsvaidzina mobilo darbvietu saraksts.

[![Izvilkšana, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Laika ievadīšana, izmantojot projekta laika ierakstu mobilajai darbvietai
1.  Mobilajā ierīcē atlasiet **Projekta laika ieraksts** darbvietai.
2.  Atlasiet vienumu **Laika ieraksts**. Tiek parādīti pašreizējās nedēļas kalendāra datumi.
3.  Izvēlētajam datumam atlasiet vienumu **Darbības** &gt; **Jauns ieraksts**.
4.  Ievadiet stundu skaitu, kas jāieraksta.
5.  Atlasiet projektu laika ierakstam. Sarakstā redzami projekti, kas ielādēti jūsu programmā izmantošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju skatiet sadaļā [Mobilā platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Ja jūsu projekts nav iekļauts sarakstā, atlasiet **Meklēt**. Meklējiet pēc nosaukuma vai pārslēdzieties uz meklēšanu pēc projekta nosaukuma vai klienta.
7.  Atlasiet kategoriju. Sarakstā redzamas kategorijas, kas ielādētas jūsu programmā izmantošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju skatiet sadaļā [Mobilā platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Ja jūsu kategorija nav iekļauta sarakstā, atlasiet **Meklēt**. Meklējiet pēc kategorijas vai pārslēdzieties uz meklēšanu pēc kategorijas nosaukuma.
9.  Atlasiet darbību. Sarakstā redzamas darbības, kas ielādētas jūsu programmā izmantošanai bezsaistē. Pēc noklusējuma tiek ielādēti 50 elementi, taču izstrādātājs šo skaitu var mainīt. Papildinformāciju skatiet sadaļā [Mobilā platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Ja jūsu darbība nav iekļauta sarakstā, atlasiet **Meklēt**. Meklējiet pēc darbības numura vai pārslēdzieties uz meklēšanu pēc mērķa.

11. Atlasiet rindas rekvizītu.
12. Ja vēlaties: ievadiet ārējos un iekšējos komentārus.
13. Atlasiet **Gatavs**.
