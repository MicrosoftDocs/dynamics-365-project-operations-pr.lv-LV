---
title: Ārējā plānošana
description: Šajā rakstā ir sniegta informācija par ārējo plānošanu.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736989"
---
# <a name="external-scheduling"></a>Ārējā plānošana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Ārējās plānošanas režīms ļauj lokāli izveidot, atjaunināt un dzēst entītijas, kas saistītas ar darba sadalījuma struktūrām (WBS), bet bez pašreizējiem ierobežojumiem, kas ieviesti Microsoft Project for the Web. Tas arī nodrošina ierobežotu validāciju. Šo režīmu drīkst lietot tikai šādi klienti:

- klienti, kuriem ir rīki, kas nepieciešami, lai definētu WBS, kas atrodas ārpus Project Operations nodrošinātās plānošanas loģikas;
- klienti, kam jāpārvalda plānošanas hierarhija, atkarības vai uzdevuma ilgums.

> [!IMPORTANT]
> Dati, kas nav pareizi ievadīti ar WBS saistītajās entītijās, var nebūt atveidoti resursu saskaņošanas režģī, aprēķinu režģī, izsekošanas režģī vai resursu piešķiršanas režģī.

## <a name="configuration"></a>Konfigurācija

Šis līdzeklis ir iespējots pēc noklusējuma. Taču projektu standarta galvenajā lapā saistītais lauks pēc noklusējuma nav redzams. Lai iespējotu lauku, portālā Maker Portal atveriet projekta entītijas galveno lapu, atlasiet lauku **Plānošanas programma** un pēc tam mainiet lauku uz **Redzams pēc noklusējuma**. Ja neizmantojat standarta projekta galveno lapu, rediģējiet esošo lapu un pievienojiet tai lauku **Plānošanas programma**.

## <a name="settings"></a>Iestatījumi

Lai izmantotu ārējo plānošanas režīmu, vispirms ir jāizveido jauns projekts un projekta galvenajā lapā nolaižamajā sarakstā jāatlasa plānošanas programma **Ārēji plānots**. Kad šis režīms projektam ir iestatīts, to nevar mainīt.

## <a name="viewing-the-wbs"></a>WBS skatīšana

Ja projekts ir plānots ārēji, piekļuve Project for the Web tiek ierobežota šim projektam. Lai skatītu WBS, jāpāriet uz izsekošanas režģi, kur tiek parādīta pilnā WBS.

## <a name="creating-and-editing-the-wbs"></a>WBS rediģēšana un izveide

Ja projektam ir iespējota ārējā plānošana, ir jādefinē dati visām ar WBS saistītajām entītijām, tostarp uzdevumiem, darba grupas dalībniekiem, resursu piešķīrumiem un atkarībām.

Attēlā tālāk parādīts projektu plānošanas datu modelis.

![Projektu plānošanas datu modelis.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcionālie ierobežojumi

Ārēji plānotiem projektiem nav atļauts veikt tālāk norādītās operācijas.

### <a name="project-planning"></a>Projektu plānošana

- **Kopēt projektu** — šī darbība netiek atbalstīta ārēji ieplānotos projektos.
- **Pārvietot projektu** — izmaiņas projekta sākuma datumā nepārvieto uzdevumu sākuma datumu vai resursu piešķīrumus WBS.
- **Projekta vadītāja atjaunināšana** — projekta vadītājam veiktās izmaiņas projekta galvenajā lapā automātiski neizveido jaunu projekta darba grupas dalībnieku, kamēr projekts netiek pārvērsts.
- **Projekta darba stundu veidnes atjaunināšana** — projekta darba stundu veidnē veiktās izmaiņas nepārrēķina projekta grafiku.
- **Resursu piešķiršanas kontūras** — resursu piešķīrumu izveide automātiski neatjaunina lauku **mdyn\_PlannedWork**. Šo lauku izmanto, lai glabātu resursu piešķiršanas ieguldījuma kontūras. Ja resursu piešķiršanas režģī vai resursu saskaņošanas režģī tiek rādīts laika sadalījuma ieguldījums, ir jādefinē derīgas resursu piešķiršanas kontūras. Šīm kontūrām ir jābūt pareizi formatētām, lai tās izraisītu gan izmaksu kontūru, gan pārdošanas cenu kontūru aprēķināšanu. Ieteicams izveidot testa projektu, kas ieplānots programmā Project for the Web, un pēc tam pārskatīt saistītos datus, lai apstiprinātu prasības un formatējumu.

### <a name="resource-management"></a>Resursu pārvaldība

- **Vispārējā resursu piegāde** — vispārēja resursu piegāde netiek atbalstīta ārēji plānotiem projektiem. Mēģinot izpildīt aktīvās atvērtās prasības, tiks veidoti jauni projekta darba grupas dalībnieki, taču vispārējais darba grupas dalībnieks netiks dzēsts vai aizstāts nevienā no esošajiem resursu piešķīrumiem.
- **Dzēst darba grupas dalībnieku** — darba grupas dalībnieka dzēšana automātiski nedzēš resursu piešķīrumus.

### <a name="quoting-and-contracting"></a>Piedāvājumi un līgumu slēgšana

- **Piedāvājumu rindu un līguma rindu informācijas importēšana** — testēšanā apstiprināts, ka, importējot no projekta piedāvājuma vai līguma rindu informāciju, lietojumprogramma atbalsta ne vairāk kā 500 uzdevumus WBA, pamatojoties uz 20 piešķīrumu ierobežojumu katram uzdevumam.

### <a name="actuals-and-invoicing"></a>Faktiskie dati un rēķinu izrakstīšana

- Lai gan starp WBS un finanšu transakcijām nav veiktas izmaiņas esošajās validācijās, ir svarīgi ievērot atbilstību standarta datu modelim, lai nodrošinātu, ka visas lejupstraumes transakcijas darbojas, kā paredzēts.
