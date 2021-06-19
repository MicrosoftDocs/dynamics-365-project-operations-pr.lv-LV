---
title: Pārdošanas procesi
description: Šajā tēmā ir sniegta informācija par pamata pārdošanas procesiem.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f01ba14baa0a2378b0a230a46aed3a682342ce6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014215"
---
# <a name="sales-processes"></a>Pārdošanas procesi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pārdošanas procesi, kas tiek izmantoti uz projektu balstītā organizācijā, atšķiras no pārdošanas procesiem, kas tiek izmantoti uz preci balstītā organizācijā. Šī atšķirība rodas tāpēc, ka uz projektu balstītu organizāciju pārdošanas cikli ir garāki un tiem ir nepieciešamas pielāgotas novērtēšanas metodes, lai analizētu un izveidotu piedāvājumus katram darījumam. Dynamics 365 Project Service Automation izmanto daļu no tās pašas funkcionalitātes, kas tiek izmantota Dynamics 365 Sales pārdošanas procesā. Lūk, daži piemēri:

- Entītija Interesents tiek izmantota, lai izsekotu pārdošanas procesu.
- Kvalificētie interesenti tiek izsekoti kā iespējas. Pārdošanas process var sākties arī ar iespēju.
- Var piekļūt visiem ar iespēju saistītajiem artefaktiem. Šie artefakti ietver pārdošanas darba grupu, ieinteresētās puses, varbūtību, vērtējumu, pārdošanas posmus un biznesa procesus.
- Iespējai tiek izveidoti vairāki piedāvājumi.
- Piedāvājums tiek atzīmēts ar **Slēgts kā iegūts**, lai izveidotu pārdošanas pasūtījumu. Programmā PSA pārdošanas pasūtījums ir pielāgots, un to dēvē par projekta līgumu.

Tālāk esošajā attēlā ir parādīts tipisks pārdošanas process uz projektu balstītā organizācijā.

> ![Pārdošanas process uz projektu balstītā organizācijā](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Pārdošanas novērtēšana
Pārdošanas vērtību var novērtēt, pamatojoties uz iepriekš piegādātajiem projektiem un projektu sarežģītības. Projektiem, kas ietver iepriekšējo projektu pagarinājumus, vai projektiem, kuros kreditora zināšanu līmenis ir augsts un tiek izmantotas labi pazīstamas darba veidnes, varat izmantot vienkāršāku novērtēšanas procesu. Sarežģītākiem projektiem parasti ir ilgāks pirkšanas process. Tāpēc pārdošanas novērtēšanas procesā ir vairāk posmu. Procesa sākumā pārdošanas darba grupa izmanto uzņēmumu vadītāju un jomas speciālistu (SME) ieguldījumu, lai sāktu veidot augsta līmeņa novērtējumu attiecībā uz katru atsevišķo piedāvājumā iekļauto darba komponentu. Šie darba komponenti ir norādīti piedāvājuma rindās. 

Varat izveidot augsta līmeņa piedāvājuma novērtējumu. Visbeidzot, šis augsta līmeņa novērtējums tiks aizstāts ar detalizētāku novērtējumu, kura pamatā ir projekta plāns, ko izveidojat, izmantojot standartizētas projekta veidnes. Šīs veidnes palīdz izveidot grafiku un noteikt piedāvājuma un tā komponentu (piedāvājuma rindu) naudas vērtības. 

Varat izveidot projektam vairākus piedāvājumus un grupēt tos, izmantojot vienu iespējas entītijas tipu. Visbeidzot, viens no šiem piedāvājumiem tiek atzīmēts ar **Slēgts kā iegūts**, un tiek izveidots projekta līgums vai darba paziņojums (SOW). Projekta līgumā ir ietverta katra komponenta (līguma rindas) līguma vērtība, ko klients akceptējis piegādei. SOW parasti izveido kā Microsoft Word dokumentu. Visi rēķini, kas klientam nosūtīti projekta piegādes laikā, ietver atsauci uz projekta līgumu vai SOW.

Varat arī izveidot alternatīvus piedāvājumus ar vienu iespējas entītijas tipu vai iestatīt sistēmu tā, lai projekta līgums tiktu izveidots pēc piedāvājuma iegūšanas. Šajā gadījumā varat pievienot Word dokumentu, kas norāda SOW projekta līguma ierakstam.

![Piedāvājuma slēgšana, lai izveidotu projekta līgumu](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Pārdošanas procesa konfigurēšana
Varat izmantot biznesa procesa plūsmas (BPF) programmā Microsoft Dynamics 365, lai konfigurētu pārdošanas procesu. BPF piešķiriet pārdošanas personālam vadītu vizuālo interfeisu, ko tas var izmantot, lai virzītu darījumus cauri posmiem, kas ir tipiski jūsu uzņēmumā.

Jūsu uzņēmumā var būt, piemēram, tālāk norādītie seši pārdošanas procesa posmi.

1. Kvalificēšana
2. Novērtējums
3. Iekšējā pārskatīšana
4. Līgums
5. Piegādāt
6. Aizvērt

Šos sešus posmus apzīmē skujiņas (\>), ko atlasāt, lai izvērstu katru jūsu izveidoto iespējas entītijas tipu.

![Biznesa procesu konfigurācija programmā Dynamics 365](media/basic-guide-3.png)
 
Jūsu organizācija var izmantot dažādas entītijas, lai apzīmētu to pašu darījumu dažādās tā attīstības fāzēs. Pārdošanas procesa sākumā darījumu apzīmē entītija Iespēja. Laika gaitā, kad parādās papildinformācija, varat izmantot augsta līmeņa novērtējumus, lai izveidotu vienu vai vairākus piedāvājumus. Ja kādu no šiem piedāvājumiem pārskata iekšējās un klienta ieinteresētās puses, darījumu apzīmē entītija Piedāvājums. Pēc tam, kad klients ir akceptējis piedāvājumu, darījumu apzīmē projekta līgums vai SOW. Lai atbalstītu šo uzvedību, BPF ir strukturēts tā, lai katrs procesa posms tiktu saistīts ar citu datu bāzes tabulu.

Posmu **Kvalificēšana** pārdošanas procesā var atbalstīt ar entītiju Iespēja. Posmus **Novērtējums** un **Iekšējā pārskatīšana** var atbalstīt ar entītiju Piedāvājums. Posmus **Līgums**, **Piegāde** un **Slēgšana** var atbalstīt ar entītiju Projekta līgums.

Virzot darījumus cauri posmiem, saņemsit aicinājumu izveidot atbilstošo entītijas ierakstu, kas palīdzēs izpildīt procesu un vadīs to. Posmi var būt nosacījuma. Piemēram, ja piedāvājumam iekšēja pārskatīšana ir nepieciešama tikai tad, ja piedāvājumā ir izmantots pielāgots cenrādis, varat šo nosacījumu konfigurēt atbilstošajā biznesa procesa posmā. Šādi posms **Iekšējā pārskatīšana** tiek rādīts tikai piedāvājumiem, kas izmanto pielāgotu cenrādi. Attiecībā uz visiem citiem darījumiem un piedāvājumiem pēc posma **Novērtējums** seko posms **Līgums**.

> [!NOTE]
> Programmā PSA ir entītijām Iespēja, Piedāvājums, Pasūtījums un Rēķins paredzētas lapas. Jums ir jāizveido projekta pakalpojumu iespējas, piedāvājumi, pasūtījumi un rēķini, izmantojot šo entītiju projekta informācijas lapas. Ja ieraksta izveidei izmantosit citu lapu, nevarēsit atvērt šo ierakstu lapā **Projekta informācija**. Ja vēlaties ierakstu atvērt lapā **Projekta informācija**, jums ir jādzēš ieraksts un tas atkārtoti jāizveido, izmantojot lapu **Projekta informācija**. Lapā **Projekta informācija** katra šo entītiju tipu biznesa loģika nodrošina, ka ieraksta lauks **Tips** ir iestatīts pareizi un visas obligātās koncepcijas ir pareizi inicializētas.

> ![Jauna pasūtījuma projekta informācija](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Atšķirības starp Project Service Automation un Sales
Lai gan pārdošanas process programmā PSA izmanto programmā Sales pieejamās pārdošanas procesa pamata iespējas, tam ir dažas būtiskas atšķirības, jo uz projektu balstītās organizācijās pastāv dažādas biznesa prakses. Lūk, daži piemēri:

- **Projekta piedāvājumi** — programmā Project Service Automation piedāvājums tiek slēgts, kad no piedāvājuma tiek izveidots projekta līgums. Programmā Sales piedāvājumu var saglabāt atvērtu pēc tam, kad tas ir iegūts. Šīs atšķirības iemesls ir tāds, ka piedāvājuma un projekta līguma atbilstība ir piemērotāka uz projektu balstītām organizācijām. 
- **Aktivizēšana un pārskatījumi** — programmā PSA aktivizēšana un pārskatījumi netiek atbalstīti projekta piedāvājumiem. Programmā Sales piedāvājumu var bloķēt, lai neļautu veikt papildu rediģēšanu.
- **Zaudēta vai iegūta piedāvājuma slēgšana** — kad programmā PSA projekta piedāvājums tiek slēgts kā iegūts vai zaudēts, iespēja paliek atvērta. Visi pārējie iespējas piedāvājumi tiek slēgti kā zaudēti. Kad programmā Sales piedāvājums tiek slēgts kā iegūts vai zaudēts, lietotājam tiek parādīts aicinājums veikt darbību iespējā. Atkarībā no lietotāja ievades pamatā esošā iespēja var tikt slēgta vai saglabāta atvērta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Pārskatījumu izsekošana attiecībā uz piedāvājumiem un projekta plāniem pārdošanas ciklā
Programmā PSA nevar izsekot pārskatījumus, kas veikti piedāvājumā. Tā vietā ir jāatzīmē, ka esošais piedāvājums ir **Slēgts kā zaudēts**, un pēc tam jāizveido jauns piedāvājums. Izmantojot PSA, varat kopēt piedāvājumu vai klonēt uz projektu balstītu piedāvājumu.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Piedāvājumu un projekta līgumu komentāru un apstiprinājumu izsekošana
Varat pārvaldīt piedāvājumu un projekta līgumu pārskatīšanu un apstiprināšanu, izmantojot Record Wall un ziņas. Jūsu organizācija var izveidot pielāgotas darbplūsmas un spraudņus, lai piešķirtu, pārvirzītu, eskalētu un pārvaldītu paziņojumus par darba vienumu pārskatīšanu un apstiprināšanu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]