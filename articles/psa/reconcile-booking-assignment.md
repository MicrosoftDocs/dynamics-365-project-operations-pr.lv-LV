---
title: Rezervāciju un piešķiru saskaņošana
description: Šajā tēmā ir sniegta informācija par faktiskajām vērtībām.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 7ca6f4bb69322db08c413e076860e2ee9fdcc412
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080490"
---
# <a name="reconcile-bookings-and-assignments"></a>Rezervāciju un piešķiru saskaņošana

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta darba grupas dalībnieka projekta rezervācijas ir brīvi savienotas ar projekta uzdevumu piešķirēm. Tādēļ resursam var būt uzdevumu piešķires, kas neatbilst rezervācijām, un rezervācijas, kas neatbilst uzdevumu piešķirēm. Ideālā gadījumā projekta rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze savu uzdevumu piešķiru izpildīšanai. Taču realitātē rezervācijas var būt balstītas uz pieejamību, un projekta norises gaitā uzdevumu laiki var mainīties. Tādēļ brīvais savienojums pieļauj elastību.

Projektu rezervāciju un uzdevumu piešķiru brīvā savienojuma dēļ projekta entītijā ir cilne **Saskaņošana**. Šī cilne palīdz projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un viņu piešķires savām projekta darba grupām.

Katram nosauktajam darba grupas dalībniekam cilnē **Saskaņošana** rezervācijas un piešķires ir parādītas līdz atsevišķā uzdevuma piešķirei. Tur tiek rādītas stundas šūnās, kas var apzīmēt periodus no mēnešiem līdz dienām.

Laukā **Laika skala** varat atlasīt vienumu **Mēnesis** , **Nedēļa** vai **Diena**. Pēc noklusējuma ir atlasīts vienums **Nedēļa**. Taču šo noklusējuma vērtību varat mainīt, atlasot pogu **Iestatījumi**. Kad atverat cilni **Saskaņošana** , tiek rādīts pašreizējais datums, bet varat izmantot kalendāra vadīklu, lai pārietu laikā uz priekšu vai atpakaļ. Ja projekta sākuma datums ir nākotnē, šī cilne pēc atvēršanas rāda šo datumu. Kalendāra vadīklai ir arī opcijas, kas ļauj jums pāriet uz projekta sākuma un beigu datumiem.

Katram resursam varat izmantot izvērsēja vadīklas, lai parādītu detalizētu informāciju par šī resursa rezervācijām. Varat arī izvērst katra resursa piešķires līdz atsevišķā uzdevuma līmenim.

Cilnes **Saskaņošana** apakšā ir redzama attiecīgā projekta vispārējā neto kopsumma, un cilnē ir arī kolonnu kopsumma. Katram resursam šī cilne iegūst atšķirību starp grupas dalībnieka rezervācijām šim projektam un šī grupas dalībnieka uzdevumu piešķiru apkopojumu. Ideālā gadījumā atšķirībai vajadzētu būt 0 (nulle). Citiem vārdiem sakot — starp resursa rezervācijām un tā uzdevumu piešķirēm nevajadzētu būt nekādai starpībai. Visas atšķirības tiek norādītas ar krāsu un ēnojumu, lai izsauktu divus tālāk aprakstītos nosacījumus.

- **Rezervācijas deficīts** — rezervācijas deficīta gadījumi rodas, ja resursam ir vairāk piešķiru nekā rezervāciju. Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo deficītu.
- **Rezervāciju pārsniegšana** — rezervāciju pārsniegšana rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem. Šis apstāklis varētu būt pieņemams, piemēram, ja resurss tiek rezervēts, pirms notiek uzdevuma piešķiršana. Taču citos gadījumos šī resursa piešķiršana, iespējams, nemaz netiek plānota. Šādos gadījumos projektu vadītājam ir jāapsver resursa rezervācijas atcelšana, lai šo noslodzi varētu izmantot citam projektam.

> [!NOTE]
> Šo apstākļu apzīmējumi varētu būt slēpti, lai režģim atstātu vairāk vietas. Tādā gadījumā apzīmējumus varat padarīt redzamus, atlasot pogu **Iestatījumi**.

Reizēm, kad lauks **Laika skala** ir iestatīts uz līmeni, kas ir augstāks par **Diena** , atšķirības varētu tikt aprēķinātas kā 0 (nulle). Piemēram, līmenī **Mēnesis** neto starpība resursam varētu būt 0 (nulle), tā norādot, ka rezervācijas ir vienādas ar piešķirēm. Taču, ja skatāties līmenī **Nedēļa** , jūs varētu redzēt, ka mēneša pirmajā nedēļā piešķires ir 0 (nulle) stundu un rezervācijas ir 40 stundas, bet mēneša otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir 0 (nulle) stundu. Lai gan kopējās rezervācijas un piešķires mēnesim ir vienādas, tās atšķiras par nedēļu.

Kad skatāties augstākos laika līmeņos, cilnē **Saskaņošana** tiek rādīts šūnu indikators, lai jums ziņotu, ka pastāv atšķirības zemākos laika līmeņos. Piemēram, nākamajā ilustrācijā šūnas indikators ir redzams 2018. gada oktobra mēneša šūnā resursam, kura nosaukums ir Everita Liepa. Tādēļ varat redzēt, ka, lai gan resursa rezervācijas un piešķires ir vienādas, kad tās tiek apkopotas līmenī **Mēnesis** , tās nesaskan zemākos līmeņos.

![Neatbilstošas rezervācijas un piešķīrumi mēneša līmenī](media/reconcile-assignments-01.JPG)

Veiciet dubultklikšķi uz šūnas, lai tuvinātu uz nākamo zemāko līmeni un apskatītu atšķirību. Piemēram, ja veicat dubultklikšķi uz 2018. gada oktobra atšķirību Everitai Liepai, tiek detalizēti parādīts līmenis **Nedēļa**. Tad varat redzēt, ka pirmajās divās oktobra nedēļās šim resursam ir rezervācijas 16 stundām, bet nav nevienas piešķires, un trešajā oktobra nedēļā ir 16 stundu piešķires, bet nav nevienas rezervācijas.

![Neatbilstošas rezervācijas un piešķīrumi nedēļas līmenī](media/reconcile-assignments-02.JPG)

Varat uz šūnas noklikšķināt ar peles labo pogu, lai tālinātu uz nākamo augstāko līmeni. Varat arī izslēgt šūnas indikatoru, atlasot pogu **Iestatījumi**. 

Varat arī izmantot virs režģa esošās pogas **Iepriekšējais** un **Nākamais** , lai pārvietotos pa visām projektā esošajām atšķirībām. Lai izmantotu šīs pogas, jums vispirms ir jāatlasa kāds resurss. Atlasiet **Nākamais** , lai pārietu uz nākamo atšķirību starp rezervācijām un piešķirēm šim resursam. Atlasiet **Iepriekšējais** , lai pārietu uz iepriekšējo atšķirību.

Gadījumos, kad jums ir uzdevumu piešķires kādam resursam, bet nav rezervāciju, varat atlasīt rezervācijas deficītu un pēc tam atlasīt **Paplašināt rezervāciju**. Pēc tam varat skatīt rezervāciju, kas ir nepieciešama, lai novērstu resursa deficītu. Varat arī apskatīt resursu rezervācijas pašreizējam projektam un citiem projektiem. Atlasiet **Labi** , lai izveidotu rezervāciju resursam, neņemot vērā pašreizējo pieejamību. Pēc tam projektu vadītājs vai resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu situācijas, kur resursa rezervācija pārsniedz tā noslodzi, jo tā rezervācijas bija paplašinātas.

## <a name="managing-with-time-zones"></a>Laika joslu pārvaldība
Lai nodrošinātu precīzus un prognozējamus rezultātus, izmantojot rezervācijas pagarinājumu, ir jāizpilda divi galvenie priekšnosacījumi.  

- Lietotājam ir jākonfigurē savas ierīces laika josla, lai tā atbilstu sistēmas personalizēšanas iestatījumos definētajai laika joslai.
 
  ![Laika joslu iestatījumi operētājsistēmā Windows 10](media/reconcile-assignments-03.png)

  ![Laika joslu iestatījumi personalizēšanas iestatījumos](media/reconcile-assignments-04.png)
 
- Rezervējamam resursam ir jābūt vismaz vienai minūtei no darba laika, kas pārklājas ar kontūrām, kas tiek izmantotas pieprasītā paplašinājuma definēšanai. Piemēram, šajā piemērā parādīts, kā pārskatīt resursus, kas atbilst darba stundām, kas ir no 9:00 līdz 19:00. 

  ![Resursu kontūru salīdzinājums](media/reconcile-assignments-05.png)

Tālāk sniegtajā tabulā ir norādīts:

- Projekta kalendāra veidne.
- Resurss A: šim resursam ir viens un tas pats kalendārs, un tas atrodas vienā laika joslā ar projektu. Rezervācijas sākuma laiks būs 9:00.
- Resursi B: šis resurss atrodas citā laika joslā, nevis tajā, kurā projekts; tāpēc sākas ar 7:00 resursa laika joslā. Tomēr rezervācijas tiks sāktas ar 9:00, jo tas ir visagrākais piešķiršanas kontūras sākuma laiks.
- Resursi C un D: resursi ir atrodami arī dažādās laika joslās, un tie atšķiras cits no cita un projekta, un to rezervācijas tiek sāktas ne agrāk kā to attiecīgie pieejamie sākuma laiki.

|Entītija  |Kalendārs  |
|-|-|
|Projekta kalendāra veidne   | ![projekta kalendārs](media/reconcile-assignments-06.png) |
|Resurss A  | ![Resursa A kalendārs](media/reconcile-assignments-06.png) |
|Resurss B  |  ![Resursa B kalendārs](media/reconcile-assignments-07.png) |
|Resurss C  |  ![Resursa C kalendārs](media/reconcile-assignments-08.png) |
|Resurss D  | ![Resursa D kalendārs](media/reconcile-assignments-09.png)  |
 
Pārejot uz saskaņošanas skatu, tiks parādīti resursa piešķīrumi un ar to saistītie rezervācijas trūkumi.
 ![Saskaņošanas skats pirms paplašinājuma](media/reconcile-assignments-10.png)

Pēc tam, kad katram resursam ir izpildīta paplašinājuma funkcionalitāte, rezervācijas tiek veiksmīgi paplašinātas attiecībā uz katru resursu. Tas ir tāpēc, ka katra resursa darba stundas pārklājas ar deficīta kontūrām.
 ![Saskaņošanas skats pēc rezervācijas paplašinājuma](media/reconcile-assignments-11.png) 

Taču sīkāka informācija par rezervācijām rāda atšķirības rezervācijas sākuma laikā. Rezervācijas tiks sāktas ne agrāk kā piešķiršanas sākuma laiks un ne agrāk kā resursam pieejamais sākuma laiks.
 ![Jaunas resursa rezervācijas plānošanas panelī](media/reconcile-assignments-12.png)
