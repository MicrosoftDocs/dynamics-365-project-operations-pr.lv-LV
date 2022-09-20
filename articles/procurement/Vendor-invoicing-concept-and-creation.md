---
title: Kreditoru rēķinu izveide
description: Šajā rakstā ir aprakstīts kreditoru rēķinu jēdziens un paskaidrots, kā tos izveidot korporācijā Microsoft Dynamics 365 Project Operations.
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

Lai izmantotu šajā rakstā aprakstīto funkcionalitāti, ir jāiespējo **līdzeklis Iespējot apakšlīgumu faktisko apstrādi ar Project Operations resursu scenārijiem** darbvietā **Līdzekļu pārvaldība**.

Kreditoru rēķinus korporācijā Microsoft Dynamics 365 Project Operations var izmantot, lai reģistrētu izmaksas, kas saistītas ar pakalpojumu un/vai materiālu piegādēm projektā, kuru ir pabeiguši piegādātāji.

Ja pakalpojumi un/vai materiāli ir noslēgti ar pārdevēju, apakšlīgums ir līgums ar šo pārdevēju. Kad pārdevējs sniedz pakalpojumus vai kad materiāli tiek saņemti un izmantoti projekta uzdevumos, izmaksas tiek reģistrētas projektā. Pēc tam kreditors periodiski sūta rēķinus. Šie rēķini tiek pārbaudīti un saskaņoti ar izmaksām, kas ir reģistrētas projektā. Kad verifikācijas process ir pabeigts, kreditora rēķins tiek apstiprināts un izlaists apmaksai.

## <a name="scenarios-for-use"></a>Lietošanas scenāriji

Kreditoru rēķinus programmā Project Operations var izmantot, lai atbalstītu divus atšķirīgus scenārijus:

- Klienti izmanto pilnu apakšuzņēmuma līgumu slēgšanas pieredzi.
- Klienti neizmanto pilnas apakšuzņēmuma līgumu slēgšanas iespējas, bet vēlas iegūt vienotu skatījumu uz izmaksām par projektu izmaksām programmā Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienti izmanto visas apakšuzņēmuma līgumu slēgšanas iespējas

Kreditoru rēķinu pieredze nodrošina veidu, kā pārbaudīt laika ierakstus, materiālu lietojumu un izdevumu ierakstus, kuros ir atsauces uz apakšuzņēmuma līguma komponentiem, un saskaņot tos ar kreditoru rēķinu rindām. Šo procesu var izmantot, lai pārbaudītu kreditora rēķina rindu rindu precizitāti. Kad verifikācijas process ir pabeigts un kreditora rēķins ir apstiprināts, sistēma apvērš faktiskos datus, kas tika reģistrēti apstiprinātajos laika, izdevumu un materiālu lietojuma žurnālos, un pēc tam izveido jaunas faktiskās izmaksas, izmantojot kreditora rēķina rindas.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienti neizmanto pilnas apakšuzņēmuma līgumu slēgšanas iespējas, bet vēlas iegūt vienotu priekšstatu par projektu izmaksām project darbībās

Ja izsekojat apakšuzņēmuma līgumu slēgšanas procesu trešās puses sistēmā, varat reģistrēt izmaksas no šīs trešās puses sistēmas uz Project Operations, izveidojot kreditoru rēķinus, kuros nav atsauces uz apakšuzņēmuma līgumiem. Tādā veidā jūsu projektu vadītājiem var būt vienots, vienots skatījums uz visām izmaksām konkrētā projektā.

## <a name="create-vendor-invoices-in-project-operations"></a>Kreditoru rēķinu izveide programmā Project Operations

Kreditoru rēķini tiek izveidoti Dynamics 365 Finance, izmantojot **kreditoru parādu** moduli. Kreditoru rēķinus nevar izveidot tieši sadaļā Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Kreditora rēķina verifikācijas iestatīšana

Ja kreditora rēķins ir paredzēts apakšuzņēmuma līgumam, Dataverse jums ir jāiespējo parametrs **Pm manuāla verifikācija.** Opcijas iestatījums nosaka, vai kreditora rēķins ir automātiski jāapstiprina, Dataverse vai arī tam ir nepieciešams manuāls apstiprinājums. Katra projekta kreditora rēķina galvenē ir iekļauta tāda paša nosaukuma opcija. Pēc noklusējuma opcijai visu projektu kreditoru rēķinu galvenē ir iestatīta vērtība, kuru iestatījāt šeit. Tomēr varat atjaunināt vērtību, kā tas ir nepieciešams atsevišķu kreditoru rēķinu galvenē.

Ja opcija ir iestatīta uz **Jā**, kreditora rēķinam, kas ir izveidots programmatūrā Finance un sinhronizēts ar to, Dataverse ir **melnraksta** statuss. Pēc tam rēķins ir jāapstiprina un jāapstiprina projekta vadītājam, un tas ir jāapstiprina, pirms tas tiek apstrādāts un grāmatots konkrētā projekta un virsgrāmatas kontos programmā Finance.

Ja opcija ir iestatīta uz **Nē**, kreditora rēķins tiek automātiski apstiprināts. Turpmāka rīcība nav nepieciešama.

Lai iestatītu kreditora rēķina verifikāciju, veiciet tālāk norādītās darbības.

1. Programmā Finance dodieties uz Sadaļu **Projektu vadības un grāmatvedības** \> **iestatīšana** \> **Projektu vadība un grāmatvedības parametri.**
1. Cilnē Finanses **iestatiet** opciju **Pm obligātā manuālā verifikācija uz** Jā **, ja uzņēmuma politikai ir** nepieciešama apakšuzņēmēju kreditoru rēķinu pārbaude. Ja projekta vadītāja veikta verifikācija nav nepieciešama Dataverse, atstājiet opciju kopa uz **Nē**. Pēc noklusējuma šis iestatījums tiks izmantots **lapā Gaida kreditoru rēķins**.

> [!NOTE]
> Kreditoru rēķinus, kas ir izveidoti apakšuzņēmuma līgumiem Dataverse, var pareizi apstrādāt tikai tad, **ja ir nepieciešama** opcija Manuāla verifikācija, ko veic PM, ir iestatīta uz **Jā**. Laika, materiālu un izdevumu faktiskos datus, ko veido apakšuzņēmēji, projekta vadītājs var manuāli saskaņot ar kreditoru rēķinu rindām tikai tad, ja šī opcija ir iestatīta uz **Jā**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Sagādes integrācijas konta iestatīšana kreditoru rēķiniem

Kad kreditora rēķins ir grāmatots programmatūrā Finance for Project Operations — integrētā vide (kas nav krājums), finanses tiek grāmatotas sagādes integrācijas kontā. Sistēma ģenerē faktiskos Dataverse datus par izlikto rēķinu. Šie faktiskie dati tiek grāmatoti programmatūrā Finance, izmantojot projektu integrācijas žurnālu. Publicējot projektu integrācijas žurnālu, tiek publicētas faktiskās izmaksas un anulēts sagādes integrācijas konts.

Lai iestatītu sagādes integrācijas kontu kreditoru rēķiniem, veiciet tālāk norādītās darbības.

1. Programmā Finance dodieties uz Sadaļu **Projektu vadības un grāmatvedības** \> **iestatīšana** \> **Projektu vadība un grāmatvedības parametri.**
1. **Cilnē Project operations vietnē Dynamics 365 customer engagement** atlasiet **Materiālu sagādes integrācijas** \> **konts**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Apakšuzņēmēju kreditoru rēķinu izveide un grāmatošana

Kad kreditoru parādu pārzinis saņem rēķinu no apakšuzņēmēja, programmatūrā Finance tiek izveidots jauns rēķins.

1. Programmā Finance dodieties uz **Kreditoru parādu rēķini** \> **·** \> **Gaida kreditoru rēķinus**.
1. **Darbību rūtī** atlasiet **Jauns**, lai izveidotu kreditora rēķinu.
1. Rēķina galvenes laukā **Rēķina konts** atlasiet **Apakšuzņēmējs**.
1. Atlasiet rēķina datumu.
1. Cilnē **Galvene** iestatiet opciju **Pm obligātā manuālā verifikācija** uz **Jā**. Šīs opcijas noklusējuma iestatījums nāk no **lapas Projektu vadība un uzskaites parametri**. Tomēr to var mainīt kreditora rēķina līmenī.
1. Kopsavilkuma cilnē Rēķins **atlasiet** **Pievienot rindu**, lai izveidotu kreditora rēķina rindu.
1. Atlasiet sagādes kategoriju, kas tika izveidota apakšlīgumu rindām, un ievadiet vienības cenu, mērvienību un daudzumu.
1. Sadaļas **Kreditora rēķina rindas cilnē Projekts** atlasiet projektu, pret kuru apakšuzņēmējs koplieto apakšlīguma rēķinu.
1. Atlasiet projekta kategoriju. Tas var būt jebkura veida **postenis**, **izdevumi**, **materiāli** vai **stundas**.
1. Atlasiet lomu tikai tad, ja atlasītā projekta kategorija atbilst **tipam Stunda**.
1. Atlasiet **Izlikt ziņu**, lai grāmatotu kreditora rēķinu.

Varat arī izveidot kreditora rēķinu, dodoties uz **Sadaļu Kreditoru** \> **rēķini** \> **Atvērt kreditoru rēķinus** un atlasot **Jauns.**

Kad kreditora rēķins ir grāmatots Dataverse, tas kļūst pieejams projektu vadītāja verifikācijai un apstrādei.

## <a name="vendor-invoice-processing-in-dataverse"></a>Kreditoru rēķinu apstrāde Dataverse

Kreditora rēķinā, kas ir izveidots programmā Dataverse, dažas lauka vērtības tiek iegūtas no kreditora rēķina, kas ir ierakstīts programmatūrā Finance. Citas vērtības ir noklusējuma vērtības, kas nāk no apakšuzņēmuma līguma.

Tālāk norādītie lauki un saistītie ieraksti tiks kopēti no apakšuzņēmuma līguma uz kreditora rēķina galveni:

- Valūta
- Līgumslēdzēja vienība
- Maksājumu nosacījumi

Kreditora rēķina rindās Project Operations izmanto tālāk norādītās lauku vērtības, lai ievadītu noklusējuma apakšuzņēmuma līgumu un apakšuzņēmuma līgumu rindas atsauci:

- Transakciju klase
- Loma
- Transakciju kategorija
- Produktu lauki
- Project
- Uzdevums

> [!NOTE]
> Fiksētas cenu apakšlīgumu rindas netiek atbalstītas project operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
