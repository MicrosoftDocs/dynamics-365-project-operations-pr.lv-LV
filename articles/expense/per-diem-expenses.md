---
title: Dienasnauda
description: Šajā rakstā sniegta informācija par to, kā strādāt ar dienasnaudu.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923197"
---
# <a name="per-diem-expenses"></a>Dienasnauda

> [!IMPORTANT] 
> Šajā rakstā aprakstītā funkcionalitāte ir pieejama lietotājiem kā daļa no priekšskatījuma laidiena.

Dienasnauda ir fiksēta, iepriekšnoteikta ikdienas summa, ko uzņēmums izmaksā darbiniekiem par naktsmītnēm (viesnīcām), ēdienreizēm un papildu izmaksām, kas darbiniekiem rodas, dodoties komandējumos. Uzņēmums šo summu izmaksā darbiniekiem tā vietā, lai apmaksātu faktiskās ceļa izmaksas. Darbinieki var izmantot savu **Papildu izmaksu / Citu** dienasnaudu, lai apmaksātu dzeramnaudas, apkalpošanu numurā, veļas mazgāšanas vai ķīmiskās tīrītavas pakalpojumus, apmeklējot būtiskas uzņēmēju sanāksmes. Dienasnaudas likme var atšķirties atkarībā no tā, vai darbinieks izvēlas atlīdzināt apvienotās naktsmītnes un ēdienreižu izmaksas, vai tikai izmaksas par ēdienreizēm un papildu izmaksām.

Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem. Kad izveidojat dienasnaudas kārtulu, varat norādīt, ka noteikta procentuālā dienasnaudas likme tiek ieturēta, ja darbinieks saņem bezmaksas maltītes vai pakalpojumus. Varat iestatīt arī minimālo un maksimālo stundu skaitu, kam var piemērot darba ņēmēja komandējuma dienasnaudas likmi.

Dienasnaudu aprēķina kā kopējo summu, kas tiek piedāvāta dienā, atskaitot atvilkumu par ēdienreizi (obligāto ēdienreižu izmaksas), kas tiek nodrošināta darbiniekam.

## <a name="configure-per-diems"></a>Dienasnaudas maksājumu konfigurēšana

Lai konfigurētu dienasnaudas maksājumus, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Izmaksu pārvaldība** \> **Iestatīšana** \> **Vispārīgi** \> **Izmaksu pārvaldības parametri**.
2. Lauka **Aprēķināt ēdienreizes atvilkumu pēc** cilnē **Dienasnauda** atlasiet, cik dienasnaudas maksājumus vajadzētu aprēķināt:

    - **Ēdienreizes veids katrā komandējumā** — aprēķiniet dienasnaudu, pamatojoties ievadītajā ēdienreizes veidā (brokastis, pusdienas vai vakariņas) un ēdienreizes atvilkumā, kas norādīts katram dienasnaudas ēdienreizes veidam komandējumā.
    - **Ēdienreizes veids dienā** — aprēķiniet dienasnaudu, pamatojoties ievadītajā ēdienreizes veidā (brokastis, pusdienas vai vakariņas) un ēdienreizes atvilkumā, kas norādīts katram dienasnaudas ēdienreizes veidam dienā.
    - **Ēdienreižu skaits dienā** — Aprēķina dienasnaudu, balstoties ēdienreižu skaitā, kas ievadīts dienā, un ēdienreižu atvilkumā par ēdienreižu skaitu, kas nodrošināts katru dienu.

3. Dodieties uz **Izmaksu pārvaldība** \> **Iestatīšana** \> **Aprēķini un kodi** \> **Dienasnaudas atrašanās vietas**.
4. Pievienojiet vietas, kurās var izmantot dienasnaudas maksājumus.
5. Katrai pievienotajai atrašanās vietai cilnē **Dienasnauda** atlasiet dienasnaudas likmi un valūtu, kas būs derīga no konkrēta sākuma datuma līdz beigu datumam par naktsmītni, ēdienreizēm un citiem izdevumiem. Lai konfigurētu dienasnaudas likmes un valūtas, dodieties uz **Izmaksu pārvaldība** \> **Iestatīšana** \> **Aprēķini un kodi** \> **Dienasnaudas maksājumi**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dienasnaudas maksājumi izmaksu saskarnē.

Dienasnaudas līdzeklis tiek atbalstīts pārveidotajā **Izmaksu pārvaldības** darbvietā pakalpojuma Microsoft Dynamics 365 Finance 10.0.25. versijā un jaunākās versijās.

Lai iespējotu dienasnaudas maksājumus, veiciet tālāk uzskaitītās darbības.

1. Darbvietā **Līdzekļu pārvaldība** sarakstā atrodiet un atlasiet līdzekli **Pārveidotās izmaksu atskaites** un atlasiet **Iespējot tagad**.
2. Sarakstā atrodiet un atlasiet līdzekli **Dienasnauda izmaksu atskaites pārveidotajai saskarnei** un atlasiet **Iespējot tagad**.

## <a name="how-the-feature-works"></a>Kā darbojas līdzeklis

Šajā sadaļā sniegti piemēri trim konfigurāciju gadījumiem. Katrā piemērā lauks **Aprēķināt ēdienreižu atvilkumu par** ir iestatīts uz atšķirīgu vērtību. Visos trijos piemēros kopējā izmaksājamā summa ir vienā, līdz tiek piemērots atvilkums par ēdienreizēm. Pēc tam kopējā izmaksājamā summa katrā piemērā atšķiras.

Lai izveidotu dienasnaudas izdevumus, kas tiek izmantoti visos trijos piemēros, veiciet tālāk uzskaitītās darbības.

1. Atveriet sadaļu **Darbvietas** \> **Izmaksu pārvaldība**.
2. Atlasiet **Jauna izdevumu atskaite** vai sarakstā atlasiet esošu izdevumu atskaiti.
3. Pievienojiet jaunus izdevumus. Laukā **Kategorija** atlasiet **Dienasnauda**. Atlasiet komandējuma vietu un beigu un sākuma datumu. Dienasnauda par naktsmītni, ēdienreizēm un papildu (citiem) izdevumiem tiek aprēķināta, pamatojoties ikdienas summā, kas tiek iestatīta atlasītajai atrašanās vietai.

    Piemēram, kā atrašanās vietu iestatāt **Redmonda (ASV)**. Ikdienas summa šai vietai ir 150 ASV dolāru (USD 150) par naktsmītni, 75 USD par ēdienreizēm un 5 USD papildu izdevumiem. Sākuma datums ir 10. janvāris, bet beigu datums — 14. janvāris. Tāpēc atlasītais ilgums ir piecas dienas, kurā atlasītā konfigurācija ir kalendāra dienas ar laiku, bet atlasītais laiks sākas un beidzas sākuma un beigu datumu plkst. 12:00. Aprēķini:

    - Kopējā izmaksājamā summa = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Kopējās summas ēdienreižu un papildu izdevumu daļa = 5 × (75 + 5) = USD 400

Ja komandējuma laikā ir nodrošinātas brokastis, pusdienas un vakariņas, šīs ēdienreizes jāiekļauj ēdienreižu atvilkumā.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. piemērs: Dienasnauda, kurā ēdienreižu atvilkumi tiek balstīti ēdienreizes veidā katrā komandējumā.

Šajā piemērā ēdienreizes atvilkums ir 30 procentu brokastīm, 30 procentu pusdienām un 40 procentu vakariņām. Lapā **Izmaksu pārvaldības parametri** lauks **Aprēķināt ēdienreizes atvilkumu pēc** ir iestatīts uz **Ēdienreizes veids katrā komandējumā**. Tālāk sniegti aprēķini, ja darbiniekam tika nodrošinātas trīs brokastis, trīs pusdienas un trīs vakariņas:

- Ēdienreižu atvilkums = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67.50 + 45 + 0 = USD 112,50
- Ēdienreizes un papildu izdevumi = 400 – 112,50 = USD 287,50
- Kopējā izmaksājamā summa = Kopējā summa - ēdienreižu atvilkums = 1150 – 112,50 = USD 1037,50

![Dienasnaudas izdevums, kurā ēdienreizes atvilkums ir balstīts ēdienreizes veidā katrā komandējumā.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. piemērs: Dienasnauda, kurā ēdienreižu atvilkumi tiek balstīti ēdienreizes veidā dienā.

Šajā piemērā ēdienreizes atvilkums ir 30 procentu brokastīm, 30 procentu pusdienām un 40 procentu vakariņām. Lapā **Izmaksu pārvaldības parametri** lauks **Aprēķināt ēdienreizes atvilkumu pēc** ir iestatīts uz **Ēdienreizes veids dienā**. Šajā gadījumā dialoglodziņa **Rediģēt izdevumus** režģī **Ēdienreizes** tiek notīrītas izvēles rūtiņas, lai norādītu, kuras ēdienreizes komandējuma laikā tika nodrošinātas.

Piemēram, šeit ir aprēķini, ja brokastis tika nodrošinātas ceļojuma pirmajās trīs dienās:

- Ēdienreizes ikdienas samazinājums par katru no pirmajām trim dienām = 75 × 30% = USD 22,50
- Kopējais ēdienreižu atvilkums = 3 × 22,50 = USD 67,50
- Ēdienreizes un papildu izmaksas par 1.-3. dienu = 75 – 22,50 = USD 57,50
- Kopējās ēdienreizes un papildu izdevumi = Ēdienreižu un papildu izdevumu summa visās piecās dienās 400 – 67,50 = USD 332,50
- Kopējā izmaksājamā summa = Kopējā summa - ēdienreižu atvilkums = 1,150 – 67,50 = USD 1.082,50

![Dienasnaudas izdevums, kurā ēdienreizes atvilkums ir balstīts ēdienreizes veidā dienā.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. piemērs: Dienasnauda, kurā ēdienreižu atvilkumi tiek balstīti ēdienreižu skaitā dienā

Šajā piemērā ēdienreižu samazinājums ir aprēķināts, pamatojoties ēdienreižu skaitā, kas tika nodrošinātas dienā (t.i. lauka **Aprēķināt ēdienreižu atvilkumu pēc** lapā **Izmaksu pārvaldības parametri** ir iestatīts uz **Ēdienreižu skaits dienā**). Dialoglodziņa **Rediģēt izdevumus** režģī **Ēdienreizes** tiek notīrītas izvēles rūtiņas, lai norādītu, kuras ēdienreizes tika nodrošinātas.
Šajā gadījumā ēdienreižu atvilkums tiek balstīts tikai nodrošināto ēdienreižu skaitā, bet ne ēdienreizes veidā (brokastis/pusdienas/vakariņas).

Tālāk sniegti dienasnaudas aprēķini, ja ikdienas summa ir 150 USD par naktsmītni, 75 USD par ēdienreizi un 5 USD papildu izdevumiem:

- **Kopējā izmaksājamā summa** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Viena ēdienreize:** Ēdienreizes atvilkums = 20% = USD 15
- **Divas ēdienreizes:** Ēdienreizes atvilkums = 50% = USD 37,50
- **Trīs ēdienreizes:** Ēdienreizes atvilkums = 100% = USD 75

Tālāk sniegti aprēķini **ēdienreižu un papildu izmaksām**, kas ietver 5 USD par papildu izmaksām:

- 1. diena — nodrošinātas divas ēdienreizes =(75–37,50) +5=37,50+5=USD 42,50
- 2. diena — nodrošinātas divas ēdienreizes =(75–37,50) +5=37,50+5=USD 42,50
- 3. diena — viena nodrošinātā ēdienreize =(75–15) +5=60+5=USD 65
- 4. diena — netiek nodrošinātas ēdienreizes =(75–0) +5=75+5=USD 80
- 5. diena — nodrošinātas trīs ēdienreizes =(75–75) +5=0+5=USD 5

- Ēdienreizes un papildu izdevumi kopā = ēdienreizes un papildu izdevumi par 1. + 2. + 3. + 4. + 5. dienu = 235 USD
- Kopējais ēdienreižu atvilkums = ēdienreižu atvilkums par 1. + 2. + 3. + 4. + 5. dienu = 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Kopējā izmaksājamā summa = Kopējā summa - Kopējais ēdienreižu atvilkums = USD 1,150 – USD 165 = USD 985

![Dienasnaudas izdevums, kurā ēdienreizes atvilkums ir balstīts ēdienreižu skaitā dienā.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> No Finance versijas 10.0.23., ja lietojat pārveidoto izdevumu saskarni, nevarat izveidot dienasnaudas izdevumus, kuriem pārklājas datumi. Ja to mēģināt darīt, saņemsit kļūdas ziņojumu.
