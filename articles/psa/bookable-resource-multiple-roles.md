---
title: Projekta pārdošanas un izmaksu aprēķini, kad rezervējamam resursam projektā ir vairākas lomas
description: Šajā tēmā sniegta informācija par to, kā var izmantot cenu noteikšanas dimensijas, lai atbalstītu cenu un izmaksu aprēķinus resursam, kam projektā ir vairākas lomas.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013270"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Projekta pārdošanas un izmaksu aprēķini, kad rezervējamam resursam projektā ir vairākas lomas 

[!include [banner](../includes/psa-now-project-operations.md)]

Uz projektiem balstītiem uzņēmumiem bieži vien ir nepieciešams viens resurss, lai strādātu ar vairākām lomām projektā. Katrai no šīm lomām var veikt atšķirīgu izcenojuma un izmaksu aprēķināšanu, kas nozīmē to, ka vienam resursa laikam projektā var būt dažādi finanšu aprēķini atkarībā no rēķina un izmaksu likmes katrai lomai. Project Service Automation ļauj iestatīt vērtības darba grupas dalībnieka ierakstā par nosaukto resursu, kā arī ļauj veikt dažādus pārlabojumus katrā no darba grupas dalībniekam piešķirtajiem uzdevumiem.

Tālāk sniegtajā piemērā ir paskaidrots, kā šīs vērtības vienkārša pārlabošana ļauj piešķirt resursam vairākas lomas projektā ar dažādām izmaksu un rēķina likmēm.

## <a name="create-tasks"></a>Uzdevumu izveide
Izveidojiet divus projekta uzdevumus, katru pa 40 stundām, A uzdevumu un B uzdevumu. Atlasiet A uzdevumu kā B uzdevuma priekšteci.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Lomas un organizācijas vienības iestatīšana vispārīgam projekta darba grupas dalībniekam

1. Lapā **Plānošana** atlasiet A uzdevumam rindu **Uzdevums**. 
2. Laukā **Resursi** nolaižamajā sarakstā atlasiet **Izveidot**.
3. Lapā **Darba grupas dalībnieka ātrā izveide** lapā norādiet tā vispārīgā darba grupas dalībnieka, kas var veikt šo uzdevumu, atribūtus.
4. Atlasiet atbilstošo lomu un organizācijas vienību un pēc tam atlasiet vienumu **Saglabāt un aizvērt**. Vispārīgs darba grupas dalībnieks tiek izveidots un piešķirts šim uzdevumam. 

Atkārtojiet šīs darbības B uzdevumam un pārliecinieties, vai B uzdevumam izveidotā vispārīgā darba grupas dalībnieka loma un organizācijas vienība ir citāda nekā A uzdevumam. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Lomas un organizācijas vienības iestatīšana projekta uzdevumam

1. Pēc A uzdevuma izveidošanas atlasiet šo uzdevumu un pēc tam atlasiet vienumu **Rediģēt uzdevumu**.
2. Lapā **Uzdevuma dati** atrodiet laukus **Loma** un **Organizācijas vienība**, pievienojiet nepieciešamās vērtības no resursa, kurš veiks šo uzdevumu. 

  > [!NOTE]
  > Ja izpildīsiet šos scenārijus, izmantojot Project Service Automation demonstrācijas datus, lomai atlasiet **Konsultāciju interesents** un **Fabrikam US** kā organizācijas vienību.

3. Atlasiet B uzdevumu un pēc tam atlasiet **Rediģēt uzdevumu**.
4. Lapā **Uzdevuma dati** atrodiet laukus **Loma** un **Organizācijas vienība**, pievienojiet nepieciešamās vērtības no resursa, kurš veiks šo uzdevumu. Pārliecinieties, ka laukos **Loma** un **Organizācijas vienība** norādītās vērtības atšķiras Uzdevumam B no Uzdevuma A. 

  > [!NOTE]
  > Ja izpildīsiet šos scenārijus, izmantojot Project Service Automation demonstrācijas datus, lomai atlasiet **Tīkla tehniķis** un **Fabrikam US** kā organizācijas vienību.

5. Saglabājiet un aizveriet lapu **Uzdevuma dati**. 

## <a name="team-member-and-estimates-behavior"></a>Darba grupas dalībnieka režģa un aprēķinu uzvedība 

1. Lapā **Uzdevuma dati** pie **Darba grupas dalībnieks** atlasiet divus vispārīgus darba grupas dalībniekus un pēc tam atlasiet **Ģenerēt prasības**. 
2. Atlasiet darba grupas dalībnieka rindu, lai izvēletos **Konsultāciju interesentu**, un pēc tam atlasiet **Rezervēt**. Tiek atvērts plānošanas panelis, un šai prasībai tiek rezervēts resurss.
3. Atlasiet darba grupas dalībnieka rindu, lai izvēletos vienumu **Tīkla tehniķis**, un pēc tam atlasiet **Rezervēt**. Tiek atvērts plānošanas panelis, un šai prasībai tiek rezervēts tas pats resurss.

### <a name="team-member-grid"></a>Darba grupas dalībnieka režģis 
Ņemiet vērā, ka **Darba grupas dalībnieka** režģī abi vispārīgā darba grupas dalībnieka ieraksti ir dzēsti un ir aizstāti kā viens resurss. Šim resursam ir viena vērtību kopa, kurā tiek parādīta **Lomas** un **Organizācijas vienības** noklusējuma vērtību kopa.
Izvēršot šī darba grupas dalībnieka ieraksta rindu, abiem šiem uzdevumiem darba grupas dalībnieka ierakstā redzami atšķirīgi piešķīrumi. Katrai piešķīruma rindai ir uzdevumam specifiskas vienumu **Loma** un **Organizācijas vienība** vērtības. 

### <a name="estimates-grid"></a>Novērtējumu režģis 
Naviģējot uz **Novērtējumu** režģi, pamanīsiet, ka viena un tā paša resursa diviem uzdevumiem ir atšķirīgs cenas aprēķins.
A uzdevuma resursa piešķīrumam cena tiek noteikta, izmantojot **Lomas** atribūta vērtību no **Konsultāciju interesenta**. B uzdevuma tā paša resursa piešķīrumam cena tiek noteikta, izmantojot **Lomas** atribūtu no **Tīkla tehniķa**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]