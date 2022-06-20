---
title: Apakšsadarbību pārvaldība projekta operācijās
description: Šajā rakstā sniegts pārskats par visaptverošu apakšuzņēmuma līgumu pārvaldības procesu, kas parasti notiek uz projektiem balstītās organizācijās.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f5e025b5f741935494349fb1bdfd3a19bacb5e1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911514"
---
# <a name="subcontract-management-in-project-operations"></a>Apakšsadarbību pārvaldība projekta operācijās

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā sniegts pārskats par apakšuzņēmuma pārvaldības procesu no gala līdz galam uz projektiem balstītās organizācijās. Pakalpojumu apakšlīgumu slēgšana parasti ietilpst biznesa procesu plūsmā, kas parādīta tālāk redzamajā diagrammā.

![Apakšlīgumu slēgšanas procesa plūsma](../media/SubcontractingProcessFlow.png)

Tālāk redzamajā sarakstā ir sniegts detalizēts apakšlīgumu slēgšanas procesa apraksts.

1. Projekta vadītājs izveido apakšlīgumu ar pārdevēju. Pēc noklusējuma apakšlīgumam tiek izmantoti pārdevēja ierakstam pievienotie cenrāži. Pārdevēja uzņēmuma attiecību tips ir **Pārdevējs** vai **Piegādātājs**.
2. Projekta vadītājs var norādīt visus pirkumus kā apakšlīguma rindas elementus. Apakšlīguma rindas var būt laiks, izmaksas vai produkti. Apakšlīguma rindas transakciju klase nosaka, kam šī rinda ir paredzēta.
3. Pārdevēja uzņēmuma pārvaldnieks un projekta vadītājs var atkārtoti veikt darbības apakšlīgumā. Cenu noteikšanu var pielāgot apakšlīgumam pievienotajos pirkumu cenrāžos.
4. Šajā posmā vai vēlāk procesā, ja apakšlīguma rinda paredzēta laikam, pārdevēja uzņēmuma pārvaldnieks saista pārdevēja kontaktpersonas ar katru apakšlīguma rindu. Šī saistība nodrošina informāciju projekta vadītājam, kurš strādā pie apakšlīguma izveides. Kad pārdevēja kontaktpersona ir saistīta ar apakšlīguma rindu, sistēma automātiski izveido rezervējamu resursu no kontaktpersonas, ja rezervējamais resurss vēl nepastāv.
5. Katras apakšlīguma rindas norēķinu metode var būt **Fiksēta cena** vai **Laiks un materiāli**. Fiksētas cenas apakšlīgumu rindām tiek iestatīts uz atskaites punktu balstīts rēķinu grafiks.
6.  Pēc apakšlīguma iestatīšanas un apspriešanas noslēgšanas tas tiek apstiprināts. Apstiprinātos apakšlīgumus nevar rediģēt, bet, ja rodas izmaiņas, apakšlīgumu var “atkārtoti atvērt rediģēšanai”, tādējādi iestatot statusu no **Apstiprināts** atpakaļ uz **Melnraksts**, un var atkārtoti uzsākt apspriešanu. 
7.  Veidojot vispārīgu darba grupas dalībnieku projektā, darba grupas dalībnieku var saistīt ar apakšlīguma rindu. Tas norāda, ka ir nepieciešams piešķirt vispārīgajam darba grupas dalībniekam apakšlīguma noslodzi.
8.  Nosauktos darba grupas dalībniekus var izveidot tieši projektā vai rezervējot, izmantojot resursu plānošanas iespējas. Ja nosauktais projekta darba grupas dalībnieks ir līgumdarbinieks, to var saistīt ar apakšlīguma līguma rindu. Tādējādi pieejamā noslodze tiek pārvietota uz apakšlīguma rindu.
9.  Apakšlīguma resursi var reģistrēt laiku, izdevumus un materiālu lietojumu projektos un projektu uzdevumos, un pēc tam iesniegt apstiprināšanai. Tas ir līdzīgi kā darbiniekiem. Reģistrējot laiku, līgumdarbinieks var atlasīt noteiktu apakšlīgumu un apakšlīguma rindu.
10. Pēc apstiprināšanas apakšlīgumos apstiprinātais laiks tiek reģistrēts projekta izmaksu faktiskajos datos, pamatojoties uz līgumdarbinieka pirkšanas cenu vai lomu, ko tas pilda projektā.
11. Pārdevēja rēķinus un pārdevēja rēķinu rindu vienumus var reģistrēt sistēmā gan par darbu, ko izpildījuši pārdevēja resursi, gan par produktiem, ko piegādājis pārdevējs. Pārdevēja rēķina rindām ir jāatbilst konkrētam projektam un laika, izmaksu, produktu/materiālu, atskaites punktu vai nodevu transakciju klasei. Pēc vēlēšanās pārdevēja rēķina rindās var norādīt atsauci uz apakšlīguma rindu.
12. Sistēma automātiski saista visus izmaksu faktiskos datus, kas atbilst apakšlīguma rindai un projektam, ar pārdevēja rēķinu. Tas atvieglo 3 virzienu saskaņošanas un pārbaudes procesu.
13. Pēc tam projekta vadītājs var pārskatīt automātiski saskaņotos projekta faktiskos datus, noņemt vai pievienot citus projekta izmaksu faktiskos datus un pabeigt pārbaudes procesu.
14. Veicot pārbaudes procesu visās rindās, pārdevēja rēķins tiek atzīmēts kā **Gatavs maksājumam**. Šajā posmā pārdevēja rēķinu un rindas var pārsūtīt uz uzskaites vai kreditoru sistēmu, lai apstrādātu maksājumu pārdevējam. Iepriekš ierakstītās projekta izmaksas tiek mainītas, un projektā tiek reģistrētas faktiskās pārdevēja rēķina rindā esošās izmaksas.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Uz daudzumu balstītas apakšlīguma rindas un uz darbu balstītas apakšlīgumu rindas

Apakšlīguma rinda var būt balstīta uz daudzumu vai uz darbu. 

Ja apakšlīguma rinda ir **balstīta uz daudzumu**, tad daudzumu, kas tiek iegādāts apakšlīguma laika, izdevumu vai materiāla rindā, var izmantot jebkurā projektā.

Ja apakšlīguma rinda ir **balstīta uz darbu**, apakšlīguma rinda ir kartēta uz darba vienību, ko atspoguļo mezgls projekta plānā. Apakšlīguma rindas vērtība ir visu to komponentu summa, kas nepieciešami, lai nodrošinātu šīs darba vienības izpildi. Tās tiek modelētas kā apakšlīguma rindas detaļas un var būt laika, izdevumu vai materiālu kolekcija. Uz darbu balstītām apakšlīguma rindām apakšlīguma rinda ir arī paredzēta atsevišķam projektam. Šāda veida apakšuzņēmuma līgumi ir aktuāli, ko neatbalsta projekta operācijas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

