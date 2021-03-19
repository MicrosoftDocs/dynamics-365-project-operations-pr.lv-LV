---
title: Kā tīmekļa lietotnē piešķirt rezervējamu resursu uzdevumam
description: Pārskats par to, kā var piešķirt rezervējamus resursus.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286302"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kā tīmekļa programmā (Project Service v2.x) piešķirt rezervējamu resursu uzdevumam?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ir divi veidi, kā programmā Project Service resursu piešķirt uzdevumam. Varat rezervēt resursu kā darba grupas dalībnieku un pēc tam to piešķirt uzdevumam. Vai arī varat izveidot vispārējo grupas dalībnieku, izmantojot lomu piešķiršanu uzdevumos, izveidot darba grupu un pēc tam izpildīt dublējuma prasības ar nosauktu resursu.

Ņemiet vērā: ja vēlaties piešķirt uzdevumam rezervējamu resursu, rezervējamam resursu darba grupas dalībniekam ir jābūt pietiekami daudz pieejamām rezervācijām. Rezervācijas statusa saistību tipam ir jābūt Stingrs, bet statusam — Iesniegts. Ja resursam nav pietiekami daudz rezervāciju, Project Service noņem piešķiri un parādīta šādu kļūdas ziņojumu:

*Nevar piešķirt resursu uzdevumam — tālāk norādītajiem resursiem projektā nav pietiekami daudz rezervētu stundu*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervējiet resursu kā darba grupas dalībnieku un pēc tam to piešķirt uzdevumam

Izmantojot šo metodi, jūs pievienojat resursu projekta darba grupai un pēc tam piešķirat uzdevumus resursam projekta grafikā. Lūk, kā to paveikt:
1.  Darba grupas dalībnieku režģī pievienojiet jaunu darba grupas dalībnieku, atlasot **Jauns**.
2.  Darba grupas dalībnieku ātrās izveides ekrānā atlasiet rezervējamā resursa vārdu un iestatiet lomu.
3.  Atlasiet **sākuma** un **beigu** datumus.

    > [!div class="mx-imgBorder"] 
    > ![Ekrānuzņēmums: darba grupas dalībnieka pievienošana](media/FAQ-Resources-to-Tasks2-1.png "Ekrānuzņēmums: darba grupas dalībnieka pievienošana")
 
4.  Atlasiet kādu no šīm sadales metodēm resursa rezervēšanai:
    - **Pilna noslodze**: izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā (no sākuma līdz beigu datumam).
    - **Noslodzes procentuāla vērtība**: izmantojot šo metodi, tiek rezervēta resursa noslodzes procentuālā vertība norādītajā laika posmā (no sākuma līdz beigu datumam).
    - **Sadalīt vienmērīgi pa stundām**: rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā.
    - **Pa stundām — sākotnējā slodze**: rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā.

    Neatlasiet **Nav**, jo tā pievieno resursu darba grupai, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi.
5.  Atlasiet **Saglabāt**.

    Ņemiet vērā, ka rezervācijas stundām ir jāpietiek, lai segtu ieguldīto laiku un datumu diapazonu uzdevumiem, kuriem piešķirat šo resursu. Ja tās nav, nevarat piešķirt resursu uzdevumam.

6.  Uzdevuma darba sadalījuma struktūrā (WBS) noklikšķiniet uz resursu nolaižamajā šūnu sarakstā. Tad: 

    1. Atlasiet **Pievienot**.
    2. Sadaļā **Resursi** atlasiet nolaižamo sarakstu un atlasiet iepriekš pievienoto darba grupas dalībnieku.
    3. Atlasiet **Labi**. Grupas dalībnieks tagad ir piešķirts uzdevumam.

    > [!div class="mx-imgBorder"] 
    > ![Ekrānuzņēmums: resursu pievienošana ar WBS](media/FAQ-Resources-to-Tasks2-2.png "Ekrānuzņēmums: resursu pievienošana ar WBS")
 
Darba grupas dalībnieku režģa sadaļā Piešķirtās stundas jūs redzēsit resursam piešķirto stundu apkopojumu. Tas būs mazāks par vai vienāds ar resursam rezervēto stundu skaitu. 

> [!div class="mx-imgBorder"] 
> ![Ekrānuzņēmums: resursam piešķirtās stundas](media/FAQ-Resources-to-Tasks2-3.png "Ekrānuzņēmums: resursam piešķirtās stundas")
 
Ja uzdevums, ko mēģināt piešķirt resursam, sākas pēc resursa rezervāciju beigu datuma, resurss vairs netiek rādīts nolaižamajā izvēlnē.

Ņemiet vērā, ka varat resursam piešķirt vairāk stundu nekā tā rezervētās stundas, ja resursam ir atlikusi nepiešķirta noslodze. Šajā gadījumā resurss tiek tikai daļēji piešķirts rezervācijām. Atlikušās nepiešķirtās uzdevuma stundas varat skatīt, darba sadalījuma struktūrai pievienojot kolonnu Stundas bez personāla.

Ja resursi tiek piešķirti to rezervētajām stundām (rezervētās stundas ir vienādas ar piešķirtajām stundām) un jūs mēģināsiet piešķirt tiem papildu uzdevumus, redzēsiet šādu kļūdas ziņojumu:

*Nevar piešķirt resursu uzdevumam — tālāk norādītajiem resursiem projektā nav pietiekami daudz rezervētu stundu.*

Turklāt noklusējuma projektu vadītāju darba grupas dalībnieks, kas tiek pievienots darba grupai, kad izveidojat projektu, tiek pievienots bez rezervācijām un to nevar piešķirt nevienam uzdevumam. Tas netiks rādīts uzdevumu resursu nolaižamajā izvēlnē.

Ja vēlaties piešķirt šo resursu, jums ir nepieciešams noņemt to no darba grupas un pēc tam atkārtoti pievieno to ar sadalījuma metodi, izņemot Nav. Resurss tiek pievienots darba grupai, kad projekts ir izveidots, tāpēc ka projektam pēc noklusējuma ir nepieciešams vismaz viens projekta apstiprinātājs.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Vispārējā darba grupas dalībnieka izveide, izmantojot lomu piešķiri uzdevumos

Šī metode nodrošina, ka resursiem uzdevumos ir pietiekami daudz rezervāciju. Vispirms izveidojiet vietturi vai vispārējo resursu, kas apraksta tā nosauktā resursa īpašības, kuram būtu vēlams strādāt pie uzdevumiem, izveidojot darba grupu pēc lomu piešķiršanas uzdevumiem. Lūk, kā to paveikt:

1. Darba sadalījuma struktūrā atlasiet uzdevumu.
2. Resursa šūnā atlasiet nolaižamā saraksta ikonu **Piešķirta loma**.
3. Atlasiet nolaižamo sarakstu **Loma** un atlasiet lomu vispārējam resursam.
4. Atlasiet **Labi**.

    > [!div class="mx-imgBorder"] 
    > ![Ekrānuzņēmums: WBS izmantošana resursa piešķiršanai](media/FAQ-Resources-to-Tasks2-4.png "Ekrānuzņēmums: WBS izmantošana resursa piešķiršanai")
 
Kad WBS esat pabeidzis piešķirt lomas uzdevumiem, atlasiet **Izveidot darba grupu**. Project Service izveido vispārējās darba grupas dalībnieku minimālo skaitu atbilstoši lomām, resursu organizācijas vienībām un projekta kalendāram, apkopojot uzdevumu piešķiri.

> [!div class="mx-imgBorder"] 
> ![Ekrānuzņēmums: projekta komandas ģenerēšana](media/FAQ-Resources-to-Tasks2-5.png "Ekrānuzņēmums: projekta komandas ģenerēšana")
 
Darba grupas dalībnieku režģī jūs redzēsiet resursus ar vispārējā resursa tipu un to lomas un pozīciju nosaukumus. Ja darba veikšanai vienai lomai ir nepieciešami divi resursi, līdzeklis Izveidot darba grupu izveido divus darba grupas dalībniekus un izmanto pozīcijas nosaukumu, lai tos atšķirtu.

> [!div class="mx-imgBorder"] 
> ![Ekrānuzņēmums: divu vispārējo resursu pievienošana](media/FAQ-Resources-to-Tasks2-6.png "Ekrānuzņēmums: divu vispārējo resursu pievienošana")
 
Varat atvērt vispārēja darba grupas dalībnieka resursa dublējuma prasību, atlasot saiti sadaļā Resursa prasības.

> [!div class="mx-imgBorder"] 
> ![Ekrānuzņēmums: dublēta resursa pieprasījuma atvēršana](media/FAQ-Resources-to-Tasks2-7.png "Ekrānuzņēmums: dublēta resursa pieprasījuma atvēršana")

Vispārejam resursam atlasiet **Rezervēt** un pēc tam varat izmantot plānošanas paneli, lai atrastu un rezervētu reālu resursu. Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam, atlasot **Iesniegt pieprasījumu**.

Kad vispārējais resurss ir aizpildīts ar nosauktu resursu, vispārējais resurss tiek noņemts no darba grupas un vispārējam resursam piešķirtie uzdevumi tiek piešķirti nosauktajam resursu, kas izpildīja vispārējā resursa prasības.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]