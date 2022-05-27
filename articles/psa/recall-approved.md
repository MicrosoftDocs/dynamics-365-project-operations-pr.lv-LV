---
title: Apstiprinātu laika vai izdevumu ierakstu atsaukšana
description: Šajā tēmā ir sniegta informācija par to, kā atsaukt iepriekš apstiprinātu laika un izdevumu transakciju.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578809"
---
# <a name="recall-approved-time-or-expense-entries"></a>Apstiprinātu laika vai izdevumu ierakstu atsaukšana

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta darba grupas dalībnieks vai cita persona, kas iesniedz laika vai izdevumu ierakstu, pēc tā apstiprināšanas šo laika vai izdevumu ierakstu var atsaukt. Apstiprināta laika vai izdevumu ieraksta atsaukšanas procedūra sastāv no divām tālāk norādītajām darbībām.

1. Iesniedzējs pieprasa atsaukšanu.
2. Apstiprinātājs apstiprina atsaukšanu.

## <a name="request-a-recall"></a>Atsaukšanas pieprasīšana

Lai pieprasītu apstiprināta laika vai izdevumu ieraksta atsaukšanu, ir jāizpilda tālāk aprakstītās darbības.

1. Laika ierakstu gadījumā dodieties uz **Projekti** \> **Mani darbi** \> **Laika ieraksts**.

    –vai–

    Izdevumu ierakstu gadījumā dodieties uz **Projekti** \> **Mani darbi** \> **Izdevumi**.

2. Laika ierakstu gadījumā atlasiet visus laika ierakstus noteiktai projekta un uzdevuma kombinācijai. Vai arī režģī atlasiet atsevišķās šūnas laikam noteikta projekta noteiktā datumā.

    –vai–

    Izdevumu ierakstu gadījumā atlasiet rindu tam izdevumu ierakstam, kuru vēlaties atsaukt.

3. Atlasiet **Atsaukt**. Tiek atvērts apstiprinājuma dialoglodziņš. Ja atlasītie laika un izdevumu ieraksti jau bija apstiprināti, tiek parādīta uzvedne ar aicinājumu ievadīt atsaukšanas iemeslu.
4. Ievadiet atsaukšanas iemeslu un pēc tam atlasiet **Labi**, lai apstiprinātu šo operāciju. Personai, kas apstiprināja šos ierakstus, sistēma nosūta pieprasījumu apstiprināt atsaukšanu.

> [!NOTE]
> Lai gan apstiprinātos laika un izdevumu ierakstus var atsaukt, ja klientam jau ir izrakstīts rēķins par apstiprināto laiku vai izdevumiem, atsaukšanas pieprasījumu nevar izveidot. Lietotājs, kurš mēģina izveidot atsaukšanas pieprasījumu, saņems ziņojumu, kurā teikts, ka šo laiku vai izdevumus nevar atsaukt, jo rēķins par tiem jau ir izrakstīts.

## <a name="approve-or-reject-a-recall-request"></a>Atsaukšanas pieprasījuma apstiprināšana vai noraidīšana

Lai apstiprinātu vai noraidītu atsaukšanas pieprasījumu, izpildiet tālāk aprakstītās darbības.

1. Atveriet sadaļu **Projekti** \> **Mani darbi** \> **Apstiprinājumi**.
2. Saraksta lapā **Apstiprinājumi** mainiet skatu uz **Atsaukšanas pieprasījumi apstiprināšanai**. Tiek parādīts iesniegto atsaukšanas pieprasījumu saraksts.
3. Atlasiet vienu vai vairākus ierakstus un pēc tam atlasiet vai nu **Apstiprināt**, vai **Noraidīt**.
4. Ja atlasījāt **Apstiprināt**, jūs saņemat brīdinājuma ziņojumu, kurā ir paskaidrota šī apstiprinājuma ietekme. Atlasiet **Labi**, lai apstiprinātu šo operāciju. Atsaukšanas pieprasījums tiek apstiprināts.

    –vai–

    Ja atlasījāt **Noraidīt**, atsaukšanas pieprasījums tiek noraidīts.

> [!NOTE]
> Tāpat kā laikā, kad atsaukšana tiek pieprasīta, arī laikā, kad atsaukšana tiek apstiprināta, sistēma pārbauda visas norēķinu darbības laika vai izdevumu ierakstos. Ja par ierakstu jau ir izrakstīts rēķins vai ja tas atrodas melnraksta rēķinā, apstiprinātājs saņem kļūdas ziņojumu, kurā ir teikts, ka šo laiku vai izdevumus nevar apstiprināt atsaukšanai, jo par tiem jau ir izrakstīts rēķins.

## <a name="impact-of-a-recall-request"></a>Atsaukšanas pieprasījuma ietekme

Kad apstiprinājums tiek atsaukts, tam ir gan operatīva, gan finansiālā ietekme.

### <a name="operational-impact"></a>Operatīva ietekme

Ja atsaukšanas pieprasījums tiek apstiprināts, apstiprinājuma ieraksts tiek atzīmēts kā **Noraidīts**. Atkarībā no tā, vai tas ir laika ieraksts vai izdevumu ieraksts, ieraksta statuss mainās uz **Atgriezts** vai uz **Noraidīts**.

Projekta darba grupas dalībnieks var apskatīt ierakstus, rediģēt un atkārtoti iesniegt ierakstus vai izdzēst ierakstus pilnībā.

Ja atsaukšanas pieprasījums tiek noraidīts, ieraksta statuss paliek **Apstiprināts** un projekta darba grupas dalībnieks un projekta apstiprinātājs šo ierakstu nevar rediģēt.

### <a name="financial-impact"></a>Finansiālā ietekme

Ja atsaukšanas pieprasījums tiek apstiprināts, atbilstošās faktiskās vērtības izmaksām un pārdošanai tiek atjauninātas tālāk norādītajā veidā.

- Lauks **Korekcijas statuss** tiek atjaunināts uz **Koriģēts**.
- Lauks **Norēķinu statuss** tiek atjaunināts uz **Atcelts**.

Tālāk tiek izveidotas anulēšanas ievadnes tabulā Esošie. Lai izveidotu atgrieztos ierakstus, sistēma pārkopē lauka vērtības no sākotnējiem esošajiem. Vienīgās vērtības, kas nav pārkopētas, ir daudzuma vērtības. Šīs vērtības tiek atgrieztas. Atgrieztie esošie tiek izveidoti gan sadaļā **Izmaksas**, **gan Nerēķina pārdošana** esošajos izdevumos. Anulētajām faktiskajām vērtībām lauks **Korekcijas statuss** tiek iestatīts uz **Nekoriģējams** un lauks **Norēķinu statuss** tiek iestatīts uz **Atcelts**. Šo izmaiņu dēļ ierakstītie nepabeigtie tēriņi un ieņēmumi projektā vairs neveido summas, kuras šīs faktiskās vērtības pārstāv.

Ja atsaukšanas pieprasījums tiek noraidīts, uz projektu nav nekādas finansiālas ietekmes.

## <a name="changes-to-time-entry-records"></a>Laika ierakstu reģistru izmaiņas

Nākamajā ilustrācijā ir parādītas izmaiņas, kas rodas apstiprinātiem laika ierakstiem, kad tie tiek atsaukti.

![Laika ierakstu stāvokļa pārejas.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Izmaiņas izdevumu ierakstu reģistros

Nākamajā ilustrācijā ir parādītas izmaiņas, kas rodas apstiprinātiem izdevumu ierakstiem, kad tie tiek atsaukti.

![Izdevumu ierakstu stāvokļa pārejas.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
