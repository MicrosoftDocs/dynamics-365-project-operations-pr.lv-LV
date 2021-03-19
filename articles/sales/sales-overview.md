---
title: Pārdošanas norises pārskats
description: Šajā tēmā ir sniegta informācija par pamata pārdošanas procesiem.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277392"
---
# <a name="sales-process-overview"></a>Pārdošanas norises pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Pārdošanas procesi, kas tiek izmantoti uz projektu balstītā organizācijā, atšķiras no pārdošanas procesiem, kas tiek izmantoti uz preci balstītā organizācijā. Tas notiek tāpēc, ka uz projektu balstītu organizāciju pārdošanas cikli ir garāki un tiem ir nepieciešamas pielāgotas novērtēšanas metodes, lai analizētu un izveidotu piedāvājumus katram darījumam. Dynamics 365 Project Operations izmanto daļu no tālāk norādītās funkcionalitātes, kas tiek izmantota pārdošanas procesā:

- Lai izsekotu pārdošanas procesam, tiek izmantots Interesenta ieraksts.
- Kvalificētie interesenti tiek izsekoti kā iespējas.
- Var piekļūt visiem ar iespēju saistītajiem artefaktiem. Šie artefakti ietver pārdošanas darba grupu, ieinteresētās puses, varbūtību, vērtējumu, pārdošanas posmus un biznesa procesus.
- Iespējai tiek izveidoti vairāki piedāvājumi.
- Piedāvājumam tiek piešķirts statuss **Slēgts kā iegūts**, lai izveidotu pārdošanas pasūtījumu. Programmā Project Operations pārdošanas pasūtījums ir pielāgots, un to dēvē par projekta līgumu.

## <a name="estimate-a-sale"></a>Pārdošanas novērtēšana
Pārdošanas vērtību var novērtēt, pamatojoties uz iepriekš piegādātajiem projektiem un projektu sarežģītības. Projektiem, kas ietver iepriekšējo projektu pagarinājumus, vai projektiem, kuros kreditora zināšanu līmenis ir augsts un tiek izmantotas labi pazīstamas darba veidnes, varat izmantot vienkāršāku novērtēšanas procesu. Sarežģītākiem projektiem parasti ir ilgāks pirkšanas process. Tāpēc pārdošanas novērtēšanas procesā ir vairāk posmu. Procesa sākumā pārdošanas darba grupa izmanto uzņēmumu vadītāju un jomas speciālistu (SME) ieguldījumu, lai veidotu augsta līmeņa novērtējumu attiecībā uz katru atsevišķo piedāvājumā iekļauto darba komponentu. Šie darba komponenti ir norādīti piedāvājuma rindās. 

Varat izveidot augsta līmeņa piedāvājuma novērtējumu. Visbeidzot, šis augsta līmeņa novērtējums tiks aizstāts ar detalizētāku novērtējumu, kura pamatā ir projekta plāns, ko izveidojat, izmantojot standartizētas projekta veidnes. Šīs veidnes palīdz izveidot grafiku un noteikt piedāvājuma un tā komponentu (piedāvājuma rindu) naudas vērtības. 

Varat izveidot projektam vairākus piedāvājumus un grupēt tos, izmantojot vienu iespējas ierakstu. Visbeidzot, viens no piedāvājumiem tiek atzīmēts ar **Slēgts kā iegūts**, un tiek izveidots projekta līgums vai darba paziņojums (SOW). Projekta līgumā ir ietverta katra komponenta (līguma rindas) līguma vērtība, ko klients akceptējis piegādei. SOW parasti izveido kā Microsoft Word dokumentu. Visi rēķini, kas klientam nosūtīti projekta piegādes laikā, ietver atsauci uz projekta līgumu vai SOW.

Varat arī izveidot alternatīvus piedāvājumus ar vienu iespējas ierakstu vai iestatīt sistēmu tā, lai projekta līgums tiktu izveidots pēc piedāvājuma iegūšanas. Šajā gadījumā varat pievienot Word dokumentu, kas norāda SOW projekta līguma ierakstam.

## <a name="configure-the-sales-process"></a>Pārdošanas procesa konfigurēšana
Varat izmantot biznesa procesa plūsmas, lai konfigurētu pārdošanas procesu. Šīs plūsmas nodrošina virzītu vizuālo interfeisu, lai pārvietotu darījumus uz priekšu pa pārdošanas procesa posmiem.

Jūsu uzņēmumā var būt, piemēram, tālāk norādītie seši pārdošanas procesa posmi.

1. Kvalificēt
2. Novērtējums
3. Iekšējā pārskatīšana
4. Līgums
5. Piegādāt
6. Aizvēršana
 
Jūsu organizācija var izmantot dažādas entītijas, lai apzīmētu to pašu darījumu dažādās tā attīstības fāzēs. Pārdošanas procesa sākumā darījumu apzīmē entītija Iespēja. Laika gaitā, kad parādās papildinformācija, varat izmantot augsta līmeņa novērtējumus, lai izveidotu vienu vai vairākus piedāvājumus. Ja kādu no šiem piedāvājumiem pārskata iekšējās un klienta ieinteresētās puses, darījumu apzīmē entītija Piedāvājums. Pēc tam, kad klients ir akceptējis piedāvājumu, darījumu apzīmē projekta līgums vai SOW. Lai atbalstītu šo uzvedību, BPF ir strukturēts tā, lai katrs procesa posms tiktu saistīts ar citu datu bāzes tabulu.

Posmu **Kvalificēšana** pārdošanas procesā var atbalstīt ar entītiju Iespēja. Posmus **Novērtējums** un **Iekšējā pārskatīšana** var atbalstīt ar entītiju Piedāvājums. Posmus **Līgums**, **Piegāde** un **Slēgšana** var atbalstīt ar entītiju Projekta līgums.

Virzot darījumus cauri posmiem, saņemsit aicinājumu izveidot atbilstošo entītijas ierakstu, kas palīdzēs izpildīt procesu un vadīs to. Posmi var būt nosacījuma. Piemēram, ja piedāvājumam iekšēja pārskatīšana ir nepieciešama tikai tad, ja piedāvājumā ir izmantots pielāgots cenrādis, varat šo nosacījumu konfigurēt atbilstošajā biznesa procesa posmā. Šādi posms **Iekšējā pārskatīšana** tiek rādīts tikai piedāvājumiem, kas izmanto pielāgotu cenrādi. Attiecībā uz visiem citiem darījumiem un piedāvājumiem pēc posma **Novērtējums** seko posms **Līgums**.

> [!NOTE]
> Project Operations ir īpašas lapas iespējas, piedāvājuma, pasūtījuma un rēķina entitīju ierakstiem. Šie ieraksti ir jāizveido, izmantojot šo entītiju projekta informācijas lapas. Pretējā gadījumā jūs nevarēsit atvērt ierakstus no lapas **Projekta informācija**. Ja vēlaties atvērt ierakstu no lapas **Projekta informācija**, ir jādzēš ieraksts un tas jāizveido no jauna, izmantojot lapu **Projekta informācija**, kurā katra entitījas veida biznesa loģika nodrošina, ka ieraksta lauks **Veids** ir iestatīts pareizi un ka visi obligātie koncepti tiek pareizi inicializēti.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Pārskatījumu izsekošana attiecībā uz piedāvājumiem un projekta plāniem pārdošanas ciklā
Programmā Project Operations nevar izsekot pārskatījumus, kas veikti piedāvājumā. Tā vietā ir jāatzīmē, ka esošais piedāvājums ir **Slēgts kā zaudēts**, un pēc tam jāizveido jauns piedāvājums. Varat kopēt piedāvājumu vai klonēt uz projektu balstītu piedāvājumu.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Piedāvājumu un projekta līgumu komentāru un apstiprinājumu izsekošana
Varat pārvaldīt piedāvājumu un projekta līgumu pārskatīšanu un apstiprināšanu, izmantojot Record Wall un ziņas. Jūsu organizācija var izveidot pielāgotas darbplūsmas un spraudņus, lai piešķirtu, pārvirzītu, eskalētu un pārvaldītu paziņojumus par darba vienumu pārskatīšanu un apstiprināšanu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]