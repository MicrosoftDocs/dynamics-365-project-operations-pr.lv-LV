---
title: Piedāvāto resursu pārskats
description: Šajā tēmā ir sniegta informācija par to, kā piedāvāt projekta resursus.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401182"
---
# <a name="review-proposed-resources"></a>Piedāvāto resursu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.

1. Pieprasījumu režģī vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.
2. Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam rūtī **Izveidot resursu rezervāciju**, laukā **Rezervācijas statuss** atlasiet **Rezervēt**.

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

## <a name="resource-availability"></a>Resursu pieejamība

Ir ļoti svarīgi, lai resursu vadītāji varētu apskatīt resursu pieejamību un atjaunināt rezervācijas. Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma), bet resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas rodas, izmantojot tādus kanālus kā e-pasts, tālruņa saruna vai tūlītējais ziņojums. Resursu vadītāji izmanto plānošanas paneli, lai atjauninātu resursus un rezervācijas.

Resursa darba stundas tiek izmantotas par pamatu resursa pieejamības aprēķināšanai. Resursu rezervēšana patērē resursu noslodzi.

Plānošanas panelī tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību un rezervēšanas pārsniegšanu, kā arī rezervāciju statusu. Iestatījums plānošanas paneļa iestatījumos ļauj rādīt apzīmējumus.

Ja blakus atsevišķiem rezervējamiem resursiem plānošanas panelī tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.

Tā kā Dynamics 365 Project Operations izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.

Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.

