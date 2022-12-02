---
title: Kreditoru rēķinu izveide
description: Šajā rakstā ir aprakstīts piegādātāju rēķinu jēdziens un izskaidrots, kā tos izveidot programmā Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475470"
---
# <a name="create-vendor-invoices"></a>Kreditoru rēķinu izveide

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai izmantotu šajā rakstā aprakstīto funkcionalitāti, ir jāiespējo līdzeklis **Iespējot apakšlīgumu faktisko datu apstrādi ar Project Operations resursos balstītiem scenārijiem** darbvietā **Līdzekļu pārvaldība**.

Piegādātāju rēķinu izrakstīšanu programmā Microsoft Dynamics 365 Project Operations var izmantot, lai ierakstītu izmaksas, kas saistītas ar pakalpojumu piegādi un/vai materiāliem projektā, ko izpilda piegādātāji.

Kad ar piegādātāju tiek noslēgts apakšlīgums par pakalpojumiem un/vai materiāliem, apakšlīgums atspoguļo līgumisku vienošanos ar šo piegādātāju. Kamēr piegādātājs nodrošina pakalpojumus vai tiek saņemti materiāli, kas tiek izmantoti projekta uzdevumiem, izmaksas tiek ierakstītas projektā. Pēc tam piegādātājs periodiski nosūta rēķinus. Šie rēķini tiek pārbaudīti un saskaņoti ar izmaksām, kas ir ierakstītas projektā. Pēc pārbaudes procesa pabeigšanas piegādātāja rēķins tiek apstiprināts un izlaists maksājumam.

## <a name="scenarios-for-use"></a>Scenāriji lietošanai

Piegādātāju rēķini programmā Project Operations var tikt izmantoti, lai atbalstītu divus atsevišķus scenārijus.

- Klienti izmanto pilnu apakšlīgumu pieredzi.
- Klienti neizmanto pilnu apakšlīgumu pieredzi, bet vēlas vienotu projektu izmaksu pārskatu programmā Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienti izmanto pilnu apakšlīgumu pieredzi

Piegādātāju rēķinu lietošanas iespējas nodrošina veidu, kā pārbaudīt laika ierakstus, materiālu lietojumu un izdevumu ierakstus, kas attiecas uz apakšlīguma komponentiem, un saskaņotu tos ar piegādātāja rēķina rindām. Šo procesu var izmantot, lai pārbaudītu piegādātāja rēķina rindu precizitāti. Pēc pārbaudes procesa pabeigšanas un piegādātāja rēķina apstiprināšanas sistēma apgriež faktiskos datus, kas tika ierakstīti apstiprinātajos laika, izdevumu un materiālu lietojuma žurnālos, un pēc tam izveido jaunas faktiskās izmaksas, izmantojot piegādātāja rēķina rindas.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienti neizmanto pilnu apakšlīgumu pieredzi, bet vēlas vienotu projektu izmaksu pārskatu programmā Project Operations

Ja izsekojat apakšlīguma procesu trešās puses sistēmā, varat ierakstīt izmaksas no šīs trešās puses sistēmas uz Project Operations, izveidojot piegādātāja rēķinus, kuriem nav atsauču uz apakšlīgumiem. Tādējādi projektu vadītājiem tiek nodrošināts viens, vienots visu konkrētā projekta izmaksu skats.

## <a name="create-vendor-invoices-in-project-operations"></a>Piegādātāju rēķinu izveidošana programmā Project Operations

Piegādātāju rēķini tiek izveidoti programmā Dynamics 365 Finance, izmantojot moduli **Kreditori**. Piegādātāju rēķinus nevar izveidot tieši programmā Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Piegādātāju rēķinu pārbaužu iestatīšana

Ja pārdevēja rēķins ir paredzēts apakšlīgumam programmā Dataverse, jāiespējo parametrs **Nepieciešams manuāls projekta vadītāja apstiprinājums**. Opcijas iestatījums nosaka, vai piegādātāju rēķins ir automātiski jāapstiprina programmā Dataverse, vai arī tam ir nepieciešams manuāls apstiprinājums. Katra projekta piegādātāja rēķina galvenē ir iekļauta opcija ar tādu pašu nosaukumu. Pēc noklusējuma opcijai visu projekta piegādātāja rēķinu galvenē tek iestatīta vērtība, ko iestatāt šeit. Tomēr šo vērtību pēc nepieciešamības var atjaunināt katra piegādātāja rēķina galvenē.

Ja opcijas iestatījums ir **Jā**, piegādātāja rēķins, kas izveidots programmā Finance un sinhronizēts ar Dataverse, ir ar statusu **Melnraksts**. Pēc tam projekta vadītājam rēķins ir jāpārbauda un jāapstiprina, pirms tas tiek apstrādāts un grāmatots konkrētajam projektam un virsgrāmatas kontos programmā Finance.

Ja ir iestatīta opcija **Nē**, piegādātāja rēķins tiek automātiski apstiprināts. Nav jāveic papildu darbības.

Lai iestatītu piegādātāja rēķina verifikāciju, veiciet tālāk norādītās darbības.

1. Programmā Finance dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un uzskaites parametri**.
1. Cilnē **Finanses** iestatiet opciju **Nepieciešams manuāls projekta vadītāja apstiprinājums** uz **Jā**, ja uzņēmuma politika pieprasa apakšuzņēmēju piegādātāju rēķinu verifikāciju. Ja projekta vadītāja veikta verifikācija nav nepieciešama programmā Dataverse, atstājiet opcijas iestatījumu **Nē**. Pēc noklusējuma šis iestatījums tiks izmantots lapā **Gaidošs piegādātāja rēķins**.

> [!NOTE]
> Piegādātāja rēķinus, kas tiek izveidoti apakšlīgumiem programmā Dataverse, var apstrādāt pareizi tikai tad, ja opcija **Nepieciešams manuāls projekta vadītāja apstiprinājums** ir iestatīta kā **Jā**. Projekta vadītājs var manuāli saskaņot laika, materiālu un izdevumu faktiskās izmaksas, ko rada apakšuzņēmēji, ar piegādātāja rēķina rindām tikai tad, ja šīs opcijas iestatījums ir **Jā**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Sagādes integrācijas konta iestatīšana piegādātāju rēķiniem

Kad piegādātāja rēķins tiek grāmatots Finance for Project Operations integrētajā vidē (nebalstīts uz krājumiem), finanšu rādītāji tiek grāmatoti sagādes integrācijas kontā. Sistēma ģenerē faktiskos datus programmā Dataverse grāmatotajam rēķinam. Šie faktiskie dati tiek grāmatoti programmā Finance, izmantojot projektu integrācijas žurnālu. Grāmatojot projektu integrācijas žurnālu, tiek grāmatota faktiskā summa un atgriezts sagādes integrācijas konts.

Lai iestatītu sagādes integrācijas kontu piegādātāju rēķiniem, veiciet tālāk norādītās darbības.

1. Programmā Finance dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un uzskaites parametri**.
1. Cilnē **Project Operations programmā Dynamics 365 Customer Engagement** atlasiet **Materiāli** \> **Sagādes integrācijas konts**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Apakšuzņēmēju piegādātāju rēķinu izveide un grāmatošana

Kad kreditoru darbinieks saņem rēķinu no apakšuzņēmēja, programmā Finance tiek izveidots jauns rēķins.

1. Programmā Finance dodieties uz **Kreditori** \> **Rēķini** \> **Gaidošie piegādātāju rēķini**.
1. Lai izveidotu piegādātāja rēķinu, **darbību rūtī** atlasiet **Jauns**.
1. Rēķina galvenes laukā **Rēķina konts** atlasiet **Apakšuzņēmējs**.
1. Atlasiet rēķina datumu.
1. Cilnē **Galvene** iestatiet opciju **Nepieciešams manuāls projekta vadītāja apstiprinājums** uz **Jā**. Šīs opcijas noklusējuma iestatījums nāk no lapas **Projektu pārvaldības un uzskaites parametri**. Tomēr to var mainīt piegādātāja rēķina līmenī.
1. Kopsavilkuma cilnē **Rēķina rinda** atlasiet **Pievienot rindu**, lai izveidotu piegādātāja rēķina rindu.
1. Atlasiet sagādes kategoriju, kas tika izveidota apakšlīguma rindām, un ievadiet vienības cenu, mērvienību un daudzumu.
1. Piegādātāju rēķinu rindu sadaļas cilnē **Projekts** atlasiet projektu, attiecībā uz kuru apakšuzņēmējs kopīgo apakšlīguma rēķinu.
1. Atlasiet projekta kategoriju. Tas var būt jebkurš tips: **Vienums**, **Izmaksas**, **Materiāli** vai **Stundas**.
1. Atlasiet lomu tikai tad, ja atlasītās projekta kategorijas tips ir **Stunda**.
1. Atlasiet **Grāmatot**, lai piegādātāja rēķinu grāmatotu.

Vai arī varat izveidot piegādātāja rēķinu, atverot **Kreditori** \> **Rēķini** \> **Atvērt piegādātāju rēķinus** un atlasot **Jauns**.

Kad pārdevēja rēķins ir iegrāmatots, tas kļūst pieejams programmā Dataverse, kur projekta vadītājs to var pārbaudīt un apstrādāt.

## <a name="vendor-invoice-processing-in-dataverse"></a>Piegādātāju rēķinu apstrāde programmā Dataverse

Piegādātāju rēķinā, kas tiek izveidots programmā Dataverse, dažu laiku vērtības tiek ņemtas no piegādātāja rēķina, kas ierakstīts programmā Finance. Citas vērtības ir noklusējuma vērtības, kas nāk no apakšlīguma.

Tālāk norādītie lauki un saistītie ieraksti tiks kopēti no apakšlīguma uz piegādātāja rēķina galveni.

- Valūta
- Līgumslēdzēja vienība
- Maksājumu nosacījumi

Piegādātāju rēķinu rindās programma Project Operations izmanto tālāk norādītās lauku vērtības, lai ievadītu noklusējuma apakšlīguma un apakšlīguma rindu atsauci.

- Transakciju klase
- Loma
- Transakciju kategorija
- Produktu lauki
- Project
- Uzdevums

> [!NOTE]
> Programmā Project Operations netiek atbalstītas fiksētas cenas apakšlīguma rindas.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
