---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643272"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation atjauninājumu izlaidums 26, V3
================================================

Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu. Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību. Šis laidiens ir saderīgs ar Dynamics 365 9. x. Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu. Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 26, V3. Šīs versijas būvējuma numurs ir V3.10.44.59, un tā ir pieejama 2020. gada decembra pašatjauninājumā.

<a name="update-release-26"></a>Atjauninājumu izlaidums 26
-----------------

### <a name="bug-fixes"></a>Kļūdu labojumi

**Laiks un izdevumi**

Ir novērstas tālāk norādītās problēmas.

-   Lietotāji var mainīt uzdevumu apstiprinātā/iesniegtā laika ierakstā.

-   Kļūda “Objekta atsauce nav piesaistīta”, saglabājot laika ierakstu.

-   Importējot laika ierakstu no resursu piešķirēm, tiek izveidoti laika ieraksti ar nepareizajām datuma un laika vērtībām.

-   Instalējot programmas Project Service Automation un Field Service, programmas Field Service komandjoslā laika ierakstiem divas reizes tiek parādīta poga **Jauns**.

-   Šūnu atjauninājumi **Atļaut vienību** un **Vienību grupa** tagad darbojas režģī **Izdevumu tāmes**.

-   Veidlapā **Laika ieraksta atjaunināšanas rediģēšana** ir ietverts vienums **Laika skala**.

-   Laiku apstiprināšana ar projektu nesaistītiem laika ierakstiem bloķē sistēmu, meklējot projekta apstiprinātāja lomu.

**Resursu pārvaldība**

Ir novērstas tālāk norādītās problēmas.

-   Pievienota validācija spraudnī **PostProjectCreate**, lai pirms izveidošanas pārbaudītu primāro prasību.

-   Ātrās izveides veidlapa **Projekta grupas dalībnieks** parāda atsauces izņēmumu Null, ja no veidlapas ir izņemti lauki.

-   Prasību ģenerēšana 12 stundām, kas pārsniedz 1 gadu, būs nesekmīga.

-   Uzlabots kļūdas ziņojums par atsauces izņēmumu Null resursu prasības izveides laikā.

**Projekta pārvaldība**

Ir novērstas tālāk norādītās problēmas.

-   Uzlabota validācija, lai risinātu atsauces izņēmumu Null, kas ģenerēts spraudnī **PreProjectUpdate**.

-   Projekti, ko publicē Microsoft Project darbvirsmas pievienojumprogramma, dzēš nepiešķirtās piešķires.

-   Pievienota jauna validācija, ja uzdevuma projekta atsauce nav derīga atsauces izņēmuma Null dēļ spraudnī **PreValidateProjectTaskUpdate**.

-   Team Member režģī nav redzamas atšķirīgas piešķires darba grupas dalībnieka ierakstā.

-   Pievienota jauna validācija un kļūdu ziņojumi atsauces izņēmuma Null dēļ spraudnī **PreProjectTaskDelete**.

**Sales**

Ir novērstas tālāk norādītās problēmas.

-   Atlasot projekta rindu piedāvājumā vai līgumā, pogai **Ieteikums** jābūt redzamai tikai tad, ja tiek atlasīta ar esošu produktu saistīta produkta rinda.

-   Nošķiriet atļauju **Create_Product** no atļaujas **Create_ProjectContract**.

-   Izdzēšot rēķina rindu, tiek izraisīta **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** atsauces Null kļūme.
