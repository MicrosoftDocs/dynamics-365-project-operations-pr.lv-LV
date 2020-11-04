---
title: Piedāvāto resursu pārskats
description: Šajā tēmā ir sniegta informācija par to, kā piedāvāt projekta resursus.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080411"
---
# <a name="review-proposed-resources"></a>Piedāvāto resursu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.

1. Pieprasījumu režģī vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.
2. Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam rūtī **Izveidot resursu rezervāciju** , laukā **Rezervācijas statuss** atlasiet **Rezervēt**.

Tiek veikti šādi statusa atjauninājumi:

- Lapā **Plānošanas palīgs** statusa indikatori tiek atjaunināti, lai norādītu, ka rezervācija ir piedāvāta, nevis stingri rezervēta.
- Resursa pieprasījumā statuss tiek mainīts uz **Nepieciešama pārskatīšana**.
- Projekta cilnē **Darba grupa** vērtība vispārējā darba grupas dalībnieka vienumam **Pieprasījuma statuss** ir mainīta uz **Nepieciešama pārskatīšana**.

Projekta vadītājs var pieņemt vai noraidīt piedāvājumu.

Kad resursu vadītāji apstrādā resursu pieprasījumus, viņi var izmantot jebkuru no tālāk minētajām metodēm.

- Piedāvāt vairākus resursus, lai apmierinātu pieprasījumu, ja nepieciešamo stundu izpildei nav pieejams viens resurss. Piedāvātās stundas tiek sadalītas starp vairākiem resursiem, kas var apmierināt nepieciešamo stundu skaitu. Šādā gadījumā stundas nevar pārklāties.
- Piedāvāt mazāk resursu, nekā nepieciešams. Šādā gadījumā paredzētā resursa noslodze ir mazāka nekā prasītāja norādītais nepieciešamo stundu laiks. Tāpēc, kad prasītājs pieņem piedāvātos resursus, tiek izveidota neizpildīta resursa vajadzība, lai norādītu atlikušo pieprasījumu.
- Rezervēt vairākus resursus, lai apmierinātu pieprasījumu, ja darba izpildei nav pieejams viens resurss.
- Rezervēt mazāk resursu, nekā nepieciešams. Šādā gadījumā rezervēto stundu skaits ir mazāks par nepieciešamo stundu skaitu. Sistēma palīdz piedāvāt resursus, nevis rezervācijas, lai pieprasītājs varētu pārbaudīt un sekot līdzi atlikušajām vajadzībām.

## <a name="billable-utilization"></a>Apmaksājamā izmantošana

Resursiem var būt mērķa apmaksājamā izmantošana. Šī mērķa izmantošana tiek definēta kā atribūts resursa noklusējuma lomā vai iestatīta atsevišķa rezervācijas resursa ierakstā. Izmantošanas aprēķini ir balstīti uz faktiskajām stundām, par kurām resursi ir paziņojuši, izmantojot apstiprinātos laika ierakstus.

Izmantošanas aprēķināšanai lieto šādas formulas:

- Apmaksājamā izmantošana = Rēķinā iekļaujamās stundas ÷ Resursa noslodze
- Neapmaksājamā izmantošana = Faktiskais laiks ar norēķinu tipa ID = Rēķinā neiekļaujams, Papildu vai Nav pieejams ÷ Resursa noslodze
- Iekšējs = Faktiskais laiks bez pārdošanas līguma ÷ Resursa noslodze
- Resursa noslodze = Resursa darba stundas – Ārpus biroja – Brīvdienas

Skatu **Resursa izmantojums** var atrast rūtī **Resursi**.

Katra režģa šūna norāda resursa apmaksājamās izmantošanas procentuālo vērtību periodā, piemēram, dienā, nedēļā vai mēnesī. Šūnu iekrāsošanai lieto šādas formulas:

- **Zaļa:** Apmaksājamā izmantošana \>= Resursa mērķa lietojums
- **Dzeltena:** Mērķa lietojums – 20 \<= Apmaksājamā izmantošana \< Mērķa lietojums
- **Sarkana:** Apmaksājamā izmantošana \< Mērķa lietojums – 20

Tā kā skats **Apmaksājamā izmantošana** ir atkarīgs no plānošanas paneļa, varat izmantot plānošanas paneļa filtrēšanas iespējas, lai filtrētu rezultātus.

Režģim ir jāiestata mērķa lietojums lomai vai atsevišķam resursam. Lai veiktu šo iestatīšanu, atveriet **Resursi** \> **Resursu lomas**.

Turklāt katram rezervējamajam resursam ir jāpiešķir noklusējuma loma. Atveriet sadaļu **Resursi** \> **Resursi.** Cilnē **Project Service** pārbaudiet, vai resursa loma ir definēta un vai laukā **Ir noklusējuma** ir iestatīta vērtība **Jā**. Varat pievienot papildu lomas, kurām iestatīta opcija **Ir noklusējuma = Nē**. Loma, kurai iestatīta opcija **Ir noklusējuma = Jā** , tiek izmantota, lai novērtētu resursa izmantojumu atbilstoši attiecīgās mērķim.

Cilnē **Project Service** resursam var iestatīt arī atsevišķu mērķa lietojumu. Šādā gadījumā lietojuma aprēķinā tiek izmantots mērķa lietojums, lai novērtētu resursa mērķi, nevis resursa noklusējuma lomas mērķi.

Resursa lietojums tiek rādīts tikai tad, ja šis resurss ir apstiprinājis rēķinā iekļaujamu laiku periodā, kas ir norādīts režģī.

## <a name="resource-availability"></a>Resursu pieejamība

Ir ļoti svarīgi, lai resursu vadītāji varētu apskatīt resursu pieejamību un atjaunināt rezervācijas. Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma), bet resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas rodas, izmantojot tādus kanālus kā e-pasts, tālruņa saruna vai tūlītējais ziņojums. Resursu vadītāji izmanto plānošanas paneli, lai atjauninātu resursus un rezervācijas.

Resursa darba stundas tiek izmantotas par pamatu resursa pieejamības aprēķināšanai. Resursu rezervēšana patērē resursu noslodzi.

Plānošanas panelī tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību un rezervēšanas pārsniegšanu, kā arī rezervāciju statusu. Iestatījums plānošanas paneļa iestatījumos ļauj rādīt apzīmējumus.

Ja blakus atsevišķiem rezervējamiem resursiem plānošanas panelī tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.

Tā kā Dynamics 365 Project Operations izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.

Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.

