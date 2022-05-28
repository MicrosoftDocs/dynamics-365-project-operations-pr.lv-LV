---
title: Piedāvāto resursu pārskats
description: Šajā tēmā ir sniegta informācija par to, kā piedāvāt projekta resursus.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584973"
---
# <a name="review-proposed-resources"></a>Piedāvāto resursu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.

Lai pārskatītu piedāvātos resursus, izpildiet šīs darbības.

1. Režģī **Pieprasījums** vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.
2. Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam apstipriniet, ka piedāvātajā rezervācijā ir iekļautas visas piedāvātās stundas.
3. Rūtī **Izveidot resursa rezervāciju** iestatiet laukam **Rezervācijas statuss** vērtību **Ierosināts** un pēc tam atlasiet **Rezervēt**.

    > [!NOTE]
    > Iestatot laukam **Rezervācijas statuss** vērtību **Ierosināts**, netiek veikta resursa stingrā rezervācija, un vispārējais resurss netiek aizstāts ar nosaukto darba grupas dalībnieku.

    Tiek veikti šādi statusa atjauninājumi:

    - Lapā **Plānošanas palīgs** statusa indikatori tiek atjaunināti, lai norādītu, ka rezervācija ir piedāvāta, nevis stingri rezervēta.
    - Resursa pieprasījumā statuss tiek mainīts uz **Nepieciešama pārskatīšana**.
    - Projekta cilnē **Darba grupa** vērtība vispārējā darba grupas dalībnieka vienumam **Pieprasījuma statuss** ir mainīta uz **Nepieciešama pārskatīšana**.

Projekta vadītājs var pieņemt vai noraidīt piedāvājumu.

Kad resursu vadītāji apstrādā resursu pieprasījumus, viņi var izmantot jebkuru no tālāk minētajām metodēm.

- Piedāvāt vairākus resursus, lai apmierinātu pieprasījumu, ja nepieciešamo stundu izpildei nav pieejams viens resurss. Piedāvātās stundas tiek sadalītas starp vairākiem resursiem, kas var apmierināt nepieciešamo stundu skaitu. Šādā gadījumā stundas nevar pārklāties.
- Piedāvāt mazāk resursu, nekā nepieciešams. Šādā gadījumā paredzētā resursa noslodze ir mazāka nekā prasītāja norādītais nepieciešamo stundu laiks. Kad prasītājs pieņem piedāvātos resursus, tiek izveidota neizpildīta resursa vajadzība, lai norādītu atlikušo pieprasījumu.
- Rezervēt vairākus resursus, lai apmierinātu pieprasījumu, ja darba izpildei nav pieejams viens resurss.
- Rezervēt mazāk resursu, nekā nepieciešams. Šādā gadījumā rezervēto stundu skaits ir mazāks par nepieciešamo stundu skaitu. Sistēma palīdz piedāvāt resursus, nevis rezervācijas, lai pieprasītājs varētu pārbaudīt un sekot līdzi atlikušajām vajadzībām.

## <a name="resource-availability"></a>Resursu pieejamība

Resursu vadītājiem ir jāapskata resursu pieejamība un jāatjaunina rezervācijas. Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma). Tomēr resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas tiek nosūtīts, izmantojot citus kanālus, piemēram, e-pasta ziņojumus, tālruņa zvanus vai tūlītējos ziņojumus. Resursu vadītāji izmanto **plānošanas paneli**, lai atjauninātu resursus un rezervācijas.

Resursa darba stundas tiek izmantotas, lai aprēķinātu resursa pieejamību. Resursu rezervēšana patērē resursu noslodzi.

**Plānošanas panelī** tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību, rezervēšanas pārsniegšanu un rezervāciju statusu. Iestatījums **plānošanas panelī** ļauj parādīt apzīmējumus.

Ja blakus atsevišķiem rezervējamiem resursiem **plānošanas panelī** tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.

Tā kā Dynamics 365 Project Operations izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.

Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
