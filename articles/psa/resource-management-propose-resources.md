---
title: Projekta resursu piedāvāšana
description: Šajā tēmā ir sniegta informācija par projekta resursu piedāvāšanu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997970"
---
# <a name="propose-project-resources"></a>Projekta resursu piedāvāšana

[!include [banner](../includes/psa-now-project-operations.md)]

Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.

1. Pieprasījumu režģī vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.
2. Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam rūtī **Izveidot resursu rezervāciju**, laukā **Rezervācijas statuss** atlasiet **Rezervēt**.

    ![Piedāvātais resurss atlasīts](media/Resource-Management-image62.png)

Tiek veikti šādi statusa atjauninājumi:

- Lapā **Plānošanas palīgs** statusa indikatori tiek atjaunināti, lai norādītu, ka rezervācija ir piedāvāta, nevis stingri rezervēta.

    ![Piedāvātās rezervācijas statusa indikatori lapā Plānošanas palīgs](media/Resource-Management-image63.png)

- Resursa pieprasījumā statuss tiek mainīts uz **Nepieciešama pārskatīšana**.

    ![Resursu pieprasījumā statuss mainīts uz Nepieciešama pārskatīšana](media/Resource-Management-image64.png)

- Projekta cilnē **Darba grupa** vērtība vispārējā darba grupas dalībnieka vienumam **Pieprasījuma statuss** ir mainīta uz **Nepieciešama pārskatīšana**.

    ![Vispārējā darba grupas dalībnieka pieprasījuma statusa vērtība mainīta uz Nepieciešama pārskatīšana cilnē Darba grupa](media/Resource-Management-image48.png)

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

![Skats Resursa izmantojums](media/Resource-Management-image65.png)

Katra režģa šūna norāda resursa apmaksājamās izmantošanas procentuālo vērtību periodā, piemēram, dienā, nedēļā vai mēnesī. Šūnu iekrāsošanai lieto šādas formulas:

- **Zaļa:** Apmaksājamā izmantošana \>= Resursa mērķa lietojums
- **Dzeltena:** Mērķa lietojums – 20 \<= Apmaksājamā izmantošana \< Mērķa lietojums
- **Sarkana:** Apmaksājamā izmantošana \< Mērķa lietojums – 20

Tā kā skats **Apmaksājamā izmantošana** ir atkarīgs no plānošanas paneļa, varat izmantot plānošanas paneļa filtrēšanas iespējas, lai filtrētu rezultātus.

Režģim ir jāiestata mērķa lietojums lomai vai atsevišķam resursam. Lai veiktu šo iestatīšanu, atveriet **Resursi** \> **Resursu lomas**.

Turklāt katram rezervējamajam resursam ir jāpiešķir noklusējuma loma. Atveriet sadaļu **Resursi** \> **Resursi.** Cilnē **Project Service** pārbaudiet, vai resursa loma ir definēta un vai laukā **Ir noklusējuma** ir iestatīta vērtība **Jā**. Varat pievienot papildu lomas, kurām iestatīta opcija **Ir noklusējuma = Nē**. Loma, kurai iestatīta opcija **Ir noklusējuma = Jā**, tiek izmantota, lai novērtētu resursa izmantojumu atbilstoši attiecīgās mērķim.

![Noklusējuma loma iestatīta](media/Resource-Management-image67.png)

Cilnē **Project Service** resursam var iestatīt arī atsevišķu mērķa lietojumu. Šādā gadījumā lietojuma aprēķinā tiek izmantots mērķa lietojums, lai novērtētu resursa mērķi, nevis resursa noklusējuma lomas mērķi.

Resursa lietojums tiek rādīts tikai tad, ja šis resurss ir apstiprinājis rēķinā iekļaujamu laiku periodā, kas ir norādīts režģī.

## <a name="resource-availability"></a>Resursu pieejamība

Ir ļoti svarīgi, lai resursu vadītāji varētu apskatīt resursu pieejamību un atjaunināt rezervācijas. Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma), bet resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas rodas, izmantojot tādus kanālus kā e-pasts, tālruņa saruna vai tūlītējais ziņojums. Resursu vadītāji izmanto plānošanas paneli, lai atjauninātu resursus un rezervācijas.

Resursa darba stundas tiek izmantotas par pamatu resursa pieejamības aprēķināšanai. Resursu rezervēšana patērē resursu noslodzi.

![Plānošanas panelis](media/Resource-Management-image68.png)

Plānošanas panelī tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību un rezervēšanas pārsniegšanu, kā arī rezervāciju statusu. Iestatījums plānošanas paneļa iestatījumos ļauj rādīt apzīmējumus.

Ja blakus atsevišķiem rezervējamiem resursiem plānošanas panelī tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.

![Rezervējamais resurss izvērsts plānošanas panelī](media/Resource-Management-image69.png)

Tā kā Dynamics 365 Project Service Automation izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.

![Detalizēta informācija par resursu rezervēšanu projektiem un darba pasūtījumiem](media/Resource-Management-image70.png)

Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.

![Resursa karte](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]