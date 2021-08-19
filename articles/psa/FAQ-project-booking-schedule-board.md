---
title: Projekta rezervāciju izveide plānošanas panelī
description: Šajā tēmā ir sniegta informācija par to, kā plānošanas panelī izveidot projekta rezervāciju.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 513f7fe75cfb7b1658b4be71ed0a17da7b64a1023992e1dada9adca8f0dbf21e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987625"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Projekta rezervāciju izveide plānošanas panelī

[!include [banner](../includes/psa-now-project-operations.md)]

Jūs varat rezervēt resursu projektam tieši projekta cilnē **Darba grupa** vai izveidojot resursu prasību no vispārēja darba grupas dalībnieka piešķires un pēc tam izpildot izveidoto prasību ar projekta darba grupas dalībnieku.

Varat arī rezervēt resursu projektam tieši plānošanas panelī. To var izdarīt trīs tālāk minētajos veidos.

- **Rezervēt no izveidotās resursa prasības:** pēc vispārēja resursa izveides var izveidot resursu pieprasījumu un piešķirt uzdevumus projektā.

- **Rezervēt no primārajām prasībām:** primārās prasības tiek rādītas plānošanas paneļa cilnē **Projekts**. 

- **Rezervēt no jaunas resursu prasības:** varat izveidot no fragmentiem resursu prasību un saistīt to ar projektu. Plānošanas panelī resursa prasība tiek rādīta cilnē **Atvērtās prasības**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervēšana no izveidotas resursa prasības

Varat izveidot vispārēju resursu un piešķirt to vienam projekta uzdevumam vai vairākiem uzdevumiem. Pēc tam varat izveidot resursa prasību no vispārējā darba grupas dalībnieka. 

1.  Plānošanas panelī šis resurss tiks rādīts cilnē **Atvērtās prasības**. Ja jums ir daudz atvērtu prasību, iespējams, būs jāizmanto režģa kolonnu filtri. 

    ![Pieprasījuma cilnes atvēršana plānošanas panelim.](media/FAQ-Project-Booking-Schedule-Board-1.png "Rezervāciju un uzdevumu tabulas ekrānuzņēmums")

2. Atlasiet prasību. Atlasītās rindas augšdaļā tiek parādīta cilne **Atrast pieejamību**.
 
3. Atlasot šo cilni, tiek aktivizēts plānošanas paneļa režīms Plānošanas palīgs un tiek filtrēti pieejamie resursi, kas atbilst resursa prasībai. Pēc tam varat rezervēt resursu.

4. Varat arī vilkt un nomest atlasīto rindu no plānošanas paneļa apakšdaļas uz kāda resursa šūnu augstāk atrodamajā režģī. Kad to nometat, labajā pusē tiek atvērts panelis **Resursa rezervācijas izveide**.

    Atlasot **Rezervēt**, resurss tiek rezervēts projekta darba grupā.

![Resursa rezervāciju paneļa izveide.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervēšana no galvenās prasības

Izveidojot projektu programmā Project Service, tiek automātiski izveidota resursa prasība Galvenā prasība. Tā ir tukša prasība, kas tiek izmantota, lai ātri rezervētu resursu plānošanas panelī, neizveidojot prasību vai neizveidojot prasību no fragmentiem. Tā kā prasība ir tukša, ir nepieciešams norādīt datumus, kā arī piešķiršanas metodi un stundas, ja piemērojams. 

1. Lai rezervētu resursu ar galveno prasību, plānošanas panelī atlasiet cilni **Projekts**. Ja jums ir daudz projektu, iespējams, kolonnā **Projekts** būs jāizmanto filtrs.

   ![Kolonnu filtri plānošanas panelī.](media/FAQ-Project-Booking-Schedule-Board-2.png "Rezervāciju un uzdevumu tabulas ekrānuzņēmums")

2. Atlasiet prasību, kuras nosaukumā ir tikai projekta nosaukums un kuras ilgums ir nulle (0).

3. Atlasiet cilni **Atrast pieejamību**, kas tiek parādīta rindā. Šādi plānošanas panelī tiek aktivizēts režīms Plānošanas palīgs un tiek rādīti pieejamie resursi, kurus var rezervēt šim projektam.

4. Tā kā lauks **Primārā prasība** ir tukšs prasība ar nulles (0) ilgumu, atlasot un rezervējot resursu, panelī **Resursa rezervācijas izveide** ir jāiestata ilgums.

5. Varat arī atlasīt vienumu **Projekta primārā prasība** plānošanas paneļa apakšdaļā un vilkt un nomest to uz resursa, lai to rezervētu.
 
    Tā kā **Primārā prasība** ir tukša prasība ar nulles (0) ilgumu, atlasot un rezervējot resursu, panelī **Resursa rezervācijas izveide** ir jāiestata ilgums.
 
    Rezervējot resursu, izmantojot plānošanas paneļa lauku **Primārā prasība**, varat to pievienot projekta darba grupai bez piešķīrumiem.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervēšana no jaunas resursa prasības
Izpildiet tālāk aprakstītās darbības, lai rezervētu no jauna resursa prasības. 

1. Dodieties uz sadaļu **Resursu prasības** un atlasiet **Jauns**, lai izveidotu jaunu resursa prasību.

2. Cilnē **Projekts** atlasiet projektu, lai prasību saistītu ar šo projektu.
 
    Šī jaunizveidotā prasība plānošanas panelī tiek parādīta kā **Atvērta prasība**, ko varat izpildīt.

3. Rezervējiet resursu, lai to pievienots projekta darba grupai.

4. Tagad, kad resurss ir rezervēts, ir manuāli jāpiešķir uzdevumi.



[!INCLUDE[footer-include](../includes/footer-banner.md)]