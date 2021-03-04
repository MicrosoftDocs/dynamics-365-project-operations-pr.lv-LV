---
title: Projekta pārdošanas un izmaksu aprēķini, kad rezervējamam resursam projektā ir vairākas lomas
description: Šajā tēmā ir paskaidrots, kā izmantot cenu noteikšanas dimensijas, lai atbalstītu cenu un izmaksu aprēķinus resursam, kam projektā ir vairākas lomas.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531493"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Projekta pārdošanas un izmaksu aprēķini, kad rezervējamam resursam projektā ir vairākas lomas 

_**Attiecas uz:** Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem, Lite izvietošanu — darbu ar pro forma rēķiniem, Project Operations krājumu/ražošanas balstītiem scenārijiem_ 

Uz projektiem balstītiem uzņēmumiem bieži vien ir nepieciešams viens resurss ar vairākām lomām projektā. Katrai lomai var būt atšķirīga cena un izmaksas. Tas nozīmē, ka viena un tā paša resursa laiks projektā var iegūt dažādus finanšu novērtējumus atkarībā no katras lomas norēķinu un izmaksu likmes. Varat iestatīt vērtības nosauktā resursa darba grupas dalībnieka ierakstā ar dažādiem pārlabojumiem katram uzdevumam, kam ir piešķirts darba grupas dalībnieks.

Tālāk sniegtajā piemērā ir apskatīts, kā vienkārša vērtības pārlabošana ļauj projektā resursam izmantot vairākas lomas ar dažādām izmaksu un norēķinu likmēm.

## <a name="create-tasks"></a>Uzdevumu izveide
Lai izveidotu uzdevumus, jums ir jāpievieno uzdevumi, kā arī kopsavilkuma uzdevumi, un pēc tam pirms uzdevuma ilguma pievienošanas ir jāpiešķir uzdevums. 

### <a name="add-tasks-and-summary-tasks"></a>Uzdevumu un kopsavilkuma uzdevumu pievienošana
Lai pievienotu uzdevumu, izpildiet tālāk norādītās darbības.

1. Atveriet sadaļu **Projekti** un atveriet projektu, kuram vēlaties pievienot uzdevumus.
2. Atlasiet **Pievienot jaunu uzdevumu**. Piešķiriet uzdevumam nosaukumu un pēc tam nospiediet taustiņu **Enter**.
3. Ievadiet cita uzdevuma nosaukumu un nospiediet taustiņu **Enter**. Atkārtojiet šo darbību, līdz ir izveidots pilns uzdevumu saraksts.
3. Lai uzdevumiem izveidotu atkāpi zem uzdevumiem **Kopsavilkums**, atlasiet trīs vertikālos punktus blakus uzdevuma nosaukumam un pēc tam atlasiet **Izveidot apakšuzdevumu**. 

  > [!TIP]
  > Lai atlasītu vairāk nekā vienu uzdevumu, atlasiet uzdevumu, nospiediet un turiet nospiestu taustiņu **CTRL** un pēc tam atlasiet citu uzdevumu.
  >
  > Varat arī izvēlēties **Paaugstināt apakšuzdevumu**, lai uzdevumi vairs neatrastos zem uzdevumiem **Kopsavilkums**.

### <a name="assign-tasks"></a>Uzdevumu piešķiršana

Izpildiet tālāk norādītās darbības, lai piešķirtu uzdevumus.

1. Uzdevuma kolonnā **Piešķirts** atlasiet personas ikonu.
2. Sarakstā izvēlieties darba grupas dalībnieku vai ievadiet tekstu, lai meklētu vārdu un uzvārdu.

### <a name="add-task-duration-and-columns"></a>Uzdevuma ilguma un kolonnu pievienošana

Bieži projekta izveidi visvieglāk ir sākt, norādot ilgumu. Lai pievienotu uzdevuma ilgumu, izpildiet tālāk norādītās darbības.

1. Uzdevuma kolonnā **Ilgums** ierakstiet dienu skaitu, kas, jūsuprāt, ir nepieciešams uzdevuma izpildei. Ja vēlaties izmantot citu laika vienību, ievadiet skaitli un vārdu **stundas**, **nedēļas** vai **mēneši**.
2. Ja vēlaties, lai uzdevums skatā **Laika skala** būtu redzams kā dimanta formas atskaites punkts, kolonnā **Ilgums** ievadiet **0 dienu** .
3. Nospiediet taustiņu **Enter**, lai pārietu uz nākamā uzdevuma lauku **Ilgums** un turpinātu ievadīt ilgumus.

  > [!NOTE]
  > Kopsavilkuma uzdevumiem nevar ievadīt ilgumu.

Projektam var pievienot kolonnas, lai sniegtu detalizētāku informāciju. Lai to izdarītu, atlasiet **Pievienot kolonnu**. 

Papildinformāciju skatiet sadaļā [Projekta izveide](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Lomas un organizācijas vienības iestatīšana vispārējam projekta darba grupas dalībniekam
Izpildiet tālāk aprakstītās darbības, lai iestatītu lomu un organizācijas vienību vispārējam darba grupas dalībniekam.

1. Lapā **Uzdevumi** atlasiet rindu **Uzdevums** vienumam **A uzdevums**. 
2. Sadaļā **Piešķirts** atlasiet **Pievienot vispārēju resursu**. Tiks atvērta lapa **Darba grupas dalībnieku ātrā izveide**.
3. Lapā **Darba grupas dalībnieka ātrā izveide** lapā norādiet tā vispārīgā darba grupas dalībnieka, kas var veikt šo uzdevumu, atribūtus.
4. Atlasiet atbilstošo lomu un organizācijas vienību un pēc tam atlasiet vienumu **Saglabāt un aizvērt**. Vispārīgs darba grupas dalībnieks tiek izveidots un piešķirts šim uzdevumam. 
5. Atkārtojiet 1–4. darbību vienumam **B uzdevums**. Taču vienuma **B uzdevums** lomai un organizācijas vienībai, kas piešķirtas vispārējam darba grupas dalībniekam, ir jāatšķiras no vienuma **A uzdevums** lomas un organizācijas vienības. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Lomas un organizācijas vienības iestatīšana projekta uzdevumam
Izpildiet tālāk aprakstītās darbības, lai iestatītu lomu un organizācijas vienību uzdevumam.

1. Pēc vienuma **A uzdevums** izveides atlasiet uzdevumu un pēc tam atlasiet **i** ikonu, lai atvērtu rūti **Detalizēta informācija par uzdevumu**. 
2. Rūtī **Detalizēta informācija par uzdevumu** ritiniet līdz apakšai un atlasiet **Skatīt detalizētu informāciju**, lai atvērtu lapu **Detalizēta informācija par uzdevumu**.
3. Lapas **Detalizēta informācija par uzdevumu** sadaļās **Loma** un **Organizācijas vienība** pievienojiet vērtības, kas resursam nepieciešamas šī uzdevuma izpildei. 

  > [!NOTE]
  > Ja šī scenārija izpildei izmantojat Project Operations demonstrācijas datus, kā lomu atlasiet **Interesenta konsultēšana**, bet kā organizācijas vienību — **Fabrikam US**.

4. Atlasiet **B uzdevums** un pēc tam atlasiet uzdevumu.
5. Atlasiet **i** ikonu, lai atvērtu rūti **Detalizēta informācija par uzdevumu**. 
6. Rūtī **Detalizēta informācija par uzdevumu** ritiniet līdz apakšai un atlasiet **Skatīt detalizētu informāciju**, lai atvērtu lapu **Detalizēta informācija par uzdevumu**.
7. Lapas **Detalizēta informācija par uzdevumu** sadaļās **Loma** un **Organizācijas vienība** pievienojiet tā resursa vērtības, kas izpildīs šo uzdevumu. Vērtībām vienuma **B uzdevums** sadaļās **Loma** un **Organizācijas vienība** ir jāatšķiras no vērtībām, kas ievadītas vienumam **A uzdevums**. 

  > [!NOTE]
  > Ja šī scenārija izpildei izmantojat Project Operations demonstrācijas datus, kā lomu atlasiet **Tīkla tehniķis**, bet kā organizācijas vienību — **Fabrikam US**.

8. Saglabājiet un aizveriet lapu **Uzdevuma dati**. 

## <a name="team-member-and-estimates-behavior"></a>Darba grupas dalībnieka režģa un aprēķinu uzvedība 
Lai saprastu režģa **Darba grupas dalībnieks** un aprēķinu uzvedību, veiciet tālāk norādītās darbības.

1. Režģī **Darba grupas dalībnieks** atlasiet abus vispārējos darba grupas dalībniekus un pēc tam atlasiet **Ģenerēt prasības**. Tādējādi tiks ģenerētas resursu prasības. 
2. Atlasiet darba grupas dalībnieka rindu vienumam **Interesenta konsultēšana**, un pēc tam atlasiet **Rezervēt**. Tiek atvērts plānošanas panelis ar resursu sarakstu. Atlasiet resursu un pēc tam atlasiet **Rezervēt**, lai rezervētu resursu šai prasībai.
3. Atlasiet darba grupas dalībnieka rindu vienumam **Tīkla tehniķis**, un pēc tam atlasiet **Rezervēt**. Tiek atvērts plānošanas panelis ar resursu sarakstu. Atlasiet to pašu resursu, ko iepriekš, un pēc tam atlasiet **Rezervēt**, lai rezervētu resursu šai prasībai.

### <a name="team-member-grid"></a>Darba grupas dalībnieka režģis 

Režģī **Darba grupas dalībnieks** abi vispārējo darba grupas dalībnieku ieraksti tiek dzēsti un aizstāti ar tikai vienu resursu. Šim resursam ir viena vērtību kopa, kas ir vienumu **Loma** un **Organizācijas vienība** noklusējuma vērtību kopa.

Izvēršot šī darba grupas dalībnieka ieraksta rindu, abiem uzdevumiem darba grupas dalībnieka ierakstā var redzēt atšķirīgus piešķīrumus. Katrai piešķīruma rindai ir uzdevumam specifiskas vienumu **Loma** un **Organizācijas vienība** vērtības. 

### <a name="estimates-grid"></a>Novērtējumu režģis 

Režģī **Aprēķini** abiem viena resursa piešķīrumiem atšķiras cenas. Vienuma **A uzdevums** resursa piešķīrumam cena tiek noteikta, izmantojot vienuma **Loma** atribūta vērtību laukā **Interesenta konsultēšana**. Vienuma **B uzdevums** tā paša resursa piešķīruma cena tiek noteikta, izmantojot vienuma **Loma** atribūta vērtību laukā **Tīkla tehniķis**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]