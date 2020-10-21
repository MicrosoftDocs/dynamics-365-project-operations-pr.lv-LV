---
title: Laika ieraksta UI uzvedība
description: Šajā tēmā ir sniegta informācija par laika ieraksta UI uzvedību.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961727"
---
# <a name="time-entry-ui-behavior"></a>Laika ieraksta UI uzvedība

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Režģis **Nedēļas laika ieraksts** ir pielāgota vadīkla, kurā ir divas galvenās sadaļas: **Dimensijas** un **Ilgums**.

## <a name="dimensions"></a>Dimensijas
Sadaļā **Dimensijas** tiek rādītas dimensijas, kurām var ievadīt laiku. Sākotnēji atbalstītas tiek šādas dimensijas:

  - Project
  - Projekta uzdevums
  - Loma
  - Veidi
  - Ieraksta statuss

Sadaļā **Dimensijas** iekļautā rediģēšana nav atļauta. Šīs sadaļas pamatā ir skats, kas iespējo pielāgotus laukus pievienošanai iknedēļas laika ierakstu režģim.

## <a name="duration"></a>Ilgums
Sadaļā Ilgums ir parādītas nedēļas dienas kā kolonnu virsraksti. Šajā sadaļā iekļautā rediģēšana ir atļauta. Pēc tam, kad tiek izveidota laika ieraksta rinda ar atbilstošajām dimensijām, lietotāji var ātri ievadīt laika periodu, ko viņi patērējuši šīm dimensijām.

## <a name="create-a-new-time-entry"></a>Jauna laika ieraksta izveide

1. Laika ierakstu režģī atlasiet **Jauns**. 
2. Dialoglodziņā **Laika ieraksta ātrā izveide** atlasiet laika ieraksta datumu.
3. Ievadiet dimensiju **Projekts**, **Projekta uzdevums**, **Loma**un **Ilgums** datus. Šī informācija ir jāpievieno minūtēs, stundās vai dienās, kopā ar skaitli ierakstot **h**, **m** vai **d**. 
4. Ievadiet ieraksta aprakstu un jebkādus komentārus, ko var ārēji kopīgot par laika ierakstu. 

Saglabājot ierakstu, ievadītās vērtības tiek parādītas sadaļā **Dimensijas**. Laukā **Ilgums** ievadītā informācija tiek parādīta laika ieraksta izveidošanas datumā.

Uzmeklēšanas laukus atbalsta sistēmas skati. Piemēram, pēc tam, kad lietotājs ievada projektu, lauks **Projekta uzdevums** pēc noklusējuma tiek iestatīts uz **Kopēšanas** skatu. Lai izveidotu laika ierakstus uzdevumiem, kas nav piešķirti lietotājam, uzmeklēšanas dialoglodziņā atlasiet **Mainīt skatu** un pēc tam atlasiet skatu **Visi aktīvi projekta uzdevumi**.

## <a name="edit-a-time-entry"></a>Laika ieraksta rediģēšana 
Detalizēta informācija no dažiem laukiem laika ieraksta lapā, piemēram, **Apraksts** un **Ārējie komentāri**, netiek rādīti iknedēļas laika ierakstu režģī. Tā vietā šūnās **Ilgums**, kurās ir šāda papildinformācija, parādās neliels trīsstūra indikators. 

1. Lai rediģētu laika ierakstu, laika ierakstā atlasiet šūnu, kuru vēlaties atjaunināt.
2. Atlasiet **Rediģēt informāciju**, lai atjauninātu datus rūtī **Laika ieraksta galvenā veidlapa**. 

## <a name="copy-a-time-entry-row"></a>Laika ieraksta rindas kopēšana
Pēc rindas izveides varat atlasīt **Kopēt rindu**, lai kopētu visu rindu jaunā rindā. Ja rinda tiek kopēta šādā veidā, tiek kopētas arī dimensijas un ilgums. Varat arī atlasīt opciju **Rediģēt rindu**, lai atjauninātu dimensiju vērtības un ilgumus sadaļā **Ilgums**.

## <a name="open-a-time-entry-behavior"></a>Laika ieraksta atvēršanas uzvedība
Lai nodrošinātu optimālu un ātru ievadi svarīgākajos laukos, nedēļas laika ieraksta režģī tiek rādīta atlasīto dimensiju un laika ilgumu apakškopa. Lai skatītu visu papildinformāciju par vienu laika ierakstu, sadaļā **Rediģēt ierakstu** atlasiet **Atvērt**.

## <a name="submit-a-time-entry"></a>Laika ieraksta iesniegšana
Varat iesniegt vienu laika ierakstu vai laika ierakstu grupu, atlasot šūnu bloku vai visu laika ierakstu rindu un pēc tam atlasot **Iesniegt**. Iesniegtie laika ieraksti tiek rādīti kā vēl neapstiprināti ieraksti apstiprinātāja **Apstiprinājuma** lapā. Pēc laika ierakstu sekmīgi iesniegšanas tos vairs nevar rediģēt.

## <a name="recall-a-time-entry"></a>Laika ieraksta atsaukšana
Iesniegtos laika ierakstus var atsaukt. Varat atsaukt vienu laika ierakstu, laika ierakstu bloku vai veselu laika ierakstu rindu. Atsauktos laika ierakstus var rediģēt.

## <a name="time-entry-status"></a>Laika ieraksta statuss

- **Melnraksts**: jauniem laika ierakstiem automātiski tiek piešķirts statuss **Melnraksts**. Var dzēst tikai tos laika ierakstus, kuriem ir statuss **Melnraksts**.
- **Iesniegts**: iesniedzot laika ierakstu, statuss tiek atjaunināts uz **Iesniegts**. 
- **Apstiprināts**: kad iesniegtais laika ieraksts ir apstiprināts, statuss tiek atjaunināts uz **Apstiprināts**. 
- **Atgriezts**: ja laika ieraksts ir noraidīts, statuss tiek atjaunināts uz **Atgriezts**, un ieraksts kļūst pieejams labošanai un atkārtotai iesniegšanai. 

## <a name="view-rejection-comments"></a>Noraidīšanas komentāru skatīšana
Kad apstiprinātājs noraida laika ierakstu, apstiprinātājs var pievienot komentārus, lai palīdzētu resursam izprast noraidīšanas iemeslu. Lai skatītu atteikuma komentārus laika ierakstam, atlasiet **Atvērt ierakstu**. Atteikuma komentāri tiks parādīti laika skalā. Lietotājs var atbildēt uz noraidīšanas komentāriem, pirms viņš atkārtoti iesniedz ierakstu.

## <a name="copy-week"></a>Nedēļas kopēšana
Kad ir izveidots pāris laika ierakstu, lietotāji vienlaikus var izveidot vairākus laika ierakstus.

1. Veidlapā **Laika ieraksti** atlasiet **Kopēt nedēļu**, lai lielapjomā izveidotu papildu laika ierakstus. 
2. Dialoglodziņa **Kopēt** sadaļā **Periodā no** izmantojiet laukus **Sākuma datums** un **Beigu datums**, lai definētu datumu diapazonu, no kura kopēt laika ierakstus. 
3. Sadaļā **Līdz periodam**, laukā **Sākuma datums** norādiet datumu, kuram veidot laika ierakstus. 
4. Atlasiet **Kopēt**. Laukā **Līdz periodam** norādītajam datumam tiek izveidota laika ierakstu kopija atbilstošajai nedēļas dienai laukā **Periodā no**. Piemēram, pagājušās nedēļas pirmdienas laika ieraksts tiek kopēts uz nedēļas pirmdienu, kura norādīta kā **Līdz periodam**.

## <a name="import"></a>Importēšana
To pašu pamata procesu izmanto importēšanai no rezervācijām, uzdevumiem un apmaiņām. Varat norādīt datumu diapazonu, no kura tiek importētas rezervācijas, un pēc tam tieši atlasīt rezervācijas, kas jākopē melnraksta laika ierakstos. 
