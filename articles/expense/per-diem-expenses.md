---
title: Dienasnauda
description: Šajā rakstā ir sniegta informācija par to, kā strādāt ar dienasnaudas izdevumiem.
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
> Šajā rakstā aprakstītā funkcionalitāte ir pieejama mērķa lietotājiem kā daļa no priekšskatījuma laidiena.

Dienasnaudas maksājums ir fiksēta, iepriekš noteikta dienas nauda, ko uzņēmums maksā saviem darbiniekiem par izmitināšanu (viesnīcām), ēdināšanu un nejaušiem izdevumiem, kas šiem darbiniekiem rodas, ceļojot uz darbu. Uzņēmums maksā šo pabalstu darbiniekiem, nevis maksā faktiskos ceļa izdevumus. Darbinieki var izmantot savu **Nejaušo/citu** dienasnaudas pabalstu, lai segtu padomus, apkalpošanu numurā, veļas mazgātavu vai ķīmiskās tīrīšanas pakalpojumus svarīgām biznesa sanāksmēm. Dienasnaudas likme var atšķirties atkarībā no tā, vai darba devējs izvēlas atlīdzināt kopējās izmitināšanas un ēdināšanas izmaksas, vai tikai ēdināšanas un neparedzēto izdevumu izmaksas.

Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem. Veidojot dienasnaudas kārtulu, var norādīt, ka dienasnaudas likmes procentuālā daļa tiks ieturēta, ja darbinieks saņems bezmaksas maltītes vai pakalpojumus. Varat arī iestatīt minimālo stundu skaitu un maksimālo stundu skaitu, ko dienasnaudas likme var attiecināt uz darbinieka komandējumu.

Dienasnauda tiek aprēķināta kā kopējais pabalsts, kas tiek piedāvāts dienā, atskaitot ēdienreizes samazinājumu (bezmaksas ēdināšanas izmaksas), kas tiek nodrošināts darbiniekam.

## <a name="configure-per-diems"></a>Konfigurēt dienasnaudu

Lai konfigurētu dienasnaudas izdevumus, rīkojieties šādi.

1. Dodieties uz **Izdevumu pārvaldības** \> **iestatīšanas** \> **vispārīgie** \> **izdevumu pārvaldības parametri.**
2. Cilnes **Dienas nauda** **laukā Aprēķināt maltītes samazinājumu pa** atlasiet, kā jāaprēķina dienas nauda:

    - **Maltītes veids vienā ceļojumā** – aprēķiniet dienasnaudu, pamatojoties uz ievadītās maltītes veidu (brokastis, pusdienas vai vakariņas) un ēdienreizes samazinājumu, kas katram ēdienreizes veidam ir norādīts dienasnaudai par ceļojuma laiku.
    - **Ēdienreizes veids dienā** – aprēķiniet dienasnaudu, pamatojoties uz ievadītās maltītes veidu un ēdienreizes samazinājumu, kas katram ēdienreizes veidam norādīts dienasnaudai dienā.
    - **Ēdienreižu skaits dienā** – aprēķiniet dienas naudu, pamatojoties uz dienā ievadīto ēdienu skaitu un ēdienreižu skaita samazināšanu par katru dienu nodrošināto ēdienreižu skaitu.

3. Dodieties uz **Izdevumu pārvaldības** \> **uzstādījumi** \> **Aprēķini un kodi** \> **pa dienasnaudas novietojumiem.**
4. Pievienojiet vietas, kur var izmantot dienasnaudu.
5. Katrai pievienotajai **vietai cilnē Dienas nauda atlasiet dienasnaudas** likmi un valūtu, kas ir spēkā starp noteiktiem naktsmītņu, maltīšu un citu izdevumu sākuma un beigu datumiem. Lai konfigurētu dienasnaudas likmes un valūtas, dodieties uz **Izdevumu pārvaldības** \> **uzstādījumi** \> **Aprēķini un kodi** \> **Dienasnaudai.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dienasnauda pārveidotajā izdevumu interfeisā

Dienasnaudas līdzeklis tiek atbalstīts **pārveidotajā izdevumu pārvaldības** darbvietā Microsoft Dynamics 365 Finance versijā 10.0.25 un jaunākā versijā.

Lai iespējotu dienasnaudu, veiciet tālāk norādītās darbības.

1. Līdzekļu pārvaldības **darbvietā sarakstā atrodiet un atlasiet** līdzekli Izdevumu pārskati, kas pārveidoti **, un pēc tam atlasiet** Iespējot tūlīt **.**
2. Sarakstā atrodiet un atlasiet **Izdevumu pārskata atkārtoti iedomātā interfeisa** līdzekli Dienas nauda un pēc tam atlasiet **Iespējot tūlīt**.

## <a name="how-the-feature-works"></a>Kā līdzeklis darbojas

Šajā sadaļā sniegti piemēri trim konfigurācijas scenārijiem. Katram piemēram lauks **Aprēķināt maltītes samazinājumu pēc** ir iestatīts uz citu vērtību. Visiem trim piemēriem kopējā maksājamā summa ir vienāda līdz ēdienreizes samazinājuma piemērošanai. Pēc tam kopējā maksājamā summa katram piemēram atšķiras.

Lai izveidotu dienasnaudas izdevumus, kas tiek izmantoti visiem trim piemēriem, rīkojieties šādi.

1. Dodieties uz **Darbvietu** \> **izdevumu pārvaldība.**
2. Atlasiet **Jauns izdevumu pārskats** vai atlasiet esošu izdevumu pārskatu.
3. Pievienojiet jaunus izdevumus. Laukā **Kategorija** atlasiet **Dienas nauda**. Atlasiet ceļojuma atrašanās vietu un sākuma un beigu datumus. Dienas nauda par izmitināšanu, ēdināšanu un neparedzētiem izdevumiem (citiem izdevumiem) tiek aprēķināta, pamatojoties uz dienas naudu, kas ir noteikta izvēlētajai vietai.

    Piemēram, kā atrašanās vietu tiek atlasīta **Redmonda (ASV).** Dienas nauda par šo vietu ir 150 ASV dolāri (USD 150) par izmitināšanu, USD 75 maltītēm un USD 5 nejaušiem gadījumiem. Sākuma datums ir 10. janvāris, bet beigu datums ir 14. janvāris. Tāpēc atlasītais ilgums ir piecas dienas, kad atlasītā konfigurācija ir kalendārās dienas ar laiku, un atlasītais laiks sākas un beidzas sākuma un beigu datumos pulksten 12:00. Šeit ir aprēķini:

    - Kopējā maksājamā summa = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Maltīte un nejaušā daļa no kopējā daudzuma = 5 × (75 + 5) = USD 400

Ja ceļojuma laikā tika nodrošinātas brokastis, pusdienas un vakariņas, šīs maltītes ir jāuzskaita kā ēdienreizes samazināšana.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. piemērs: Dienasnauda, kad ēdienreižu samazinājums ir balstīts uz ēdienreizes veidu vienā ceļojumā

Šajā piemērā ēdienreizes samazinājums ir 30 procenti brokastīm, 30 procenti pusdienām un 40 procenti vakariņām. **Lapā** Izdevumu pārvaldības parametri **lauks Aprēķināt maltītes samazinājumu pa** laukiem ir iestatīts uz **Maltītes tips vienā braucienā**. Šeit ir aprēķini, ja darbiniekam tika nodrošinātas trīs brokastis, divas pusdienas un nulles vakariņas:

- Ēdienreizes samazināšana = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Maltītes un nejaušības = 400 – 112,50 = USD 287.50
- Kopējā maksājamā summa = Kopējais pabalsts – Ēdienreizes samazinājums = 1150 – 112,50 = USD 1,037.50

![Dienasnaudas izdevumi, ja ēdienreizes samazinājums ir atkarīgs no ēdienreizes veida vienā braucienā.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. piemērs: Dienasnauda, kad ēdienreizes samazinājums ir atkarīgs no ēdienreizes veida dienā

Šajā piemērā ēdienreizes samazinājums ir 30 procenti brokastīm, 30 procenti pusdienām un 40 procenti vakariņām. **Lapā** Izdevumu pārvaldības parametri **lauks Aprēķināt maltītes samazinājumu pa** laukiem ir iestatīts uz **Ēdienreizes tips dienā**. Šādā gadījumā dialoglodziņa **Izdevumu** rediģēšana **režģī** Maltītes notīriet izvēles rūtiņas, lai norādītu, kuras maltītes jums tika nodrošinātas ceļojuma laikā.

Piemēram, šeit ir aprēķini, ja brokastis tika nodrošinātas pirmajām trim ceļojuma dienām:

- Ēdienreizes samazināšana katru dienu katrā no pirmajām trim dienām = 75 × 30% = USD 22.50
- Kopējais ēdienreizes samazinājums = 3 × 22,50 = USD 67.50
- Maltītes un nejaušība no 1. līdz 3. dienai = 75 – 22,50 = USD 57.50
- Kopējais ēdienreizes un nejaušības gadījumu skaits = ēdienreižu un nejaušību summa piecās dienās = 400 – 67,50 = USD 332.50
- Kopējā maksājamā summa = Kopējā summa – Ēdienreizes samazinājums = 1150 – 67,50 = USD 1,082.50

![Dienasnaudas izdevumi, ja ēdienreizes samazinājums ir atkarīgs no ēdienreizes veida dienā.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. piemērs: dienasnauda, kad ēdienreižu samazinājums ir atkarīgs no ēdienreižu skaita dienā

Šajā piemērā ēdienreizes samazinājums tiek aprēķināts, pamatojoties uz dienā sniegto ēdienu skaitu (tas ir, **lapas Izdevumu pārvaldības parametri lauks Aprēķināt maltītes samazinājumu pa** laukiem **ir** iestatīts uz **Maltīšu skaits dienā**). Dialoglodziņa **Izdevumu** rediģēšana režģī **Maltītes** notīriet izvēles rūtiņas, lai norādītu, kuras maltītes tika nodrošinātas.
Šajā gadījumā ēdienreizes samazināšana ir balstīta tikai uz piedāvāto ēdienu #, nevis uz nodrošināto maltītes veidu ( brokastis / pusdienas / vakariņas).

Šeit ir aprēķini par dienas naudu, kad dienas nauda ir USD 150 izmitināšanai, USD 75 ēdienreizēm un USD 5 nejaušiem gadījumiem:

- **Kopējā maksājamā** summa = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Viena ēdienreize:** ēdienreizes samazināšana = 20% = USD 15
- **Divas ēdienreizes:** ēdienreizes samazināšana = 50% = USD 37.50
- **Trīs ēdienreizes:** ēdienreizes samazināšana = 100% = USD 75

Šeit ir aprēķini par **ēdienreizēm un nejaušo pabalstu**, kas ietver USD 5 nejaušiem gadījumiem:

- 1. diena – nodrošinātas divas ēdienreizes = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. diena – nodrošinātas divas ēdienreizes = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. diena – nodrošināta viena ēdienreize = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. diena – nulles ēdienreizes = (75-0) + 5 = 75 + 5 = USD 80
- 5. diena – nodrošinātas trīs ēdienreizes = (75 – 75) + 5 = 0 + 5 = USD 5

- Kopējais ēdienreižu un nejaušību gadījumu skaits = ēdienreizes un nejaušības 1. dienā+ 2. dienā +3. diena+4. diena+ 5. diena = USD 235
- Kopējais ēdienreizes samazinājums = ēdienreizes samazināšana 1. dienā+ 2. dienā +3. dienā+4. dienā+ 5. dienā= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Kopējā maksājamā summa = Kopējais pabalsts – Kopējais ēdienreižu samazinājums = USD 1,150 – USD 165 = USD 985

![Dienasnaudas izdevumi, ja ēdienreizes samazinājums ir atkarīgs no ēdienreižu skaita dienā.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Finance versijā 10.0.23, ja izmantojat pārveidoto izdevumu interfeisu, nevar izveidot dienasnaudas izdevumus, kuru datumi pārklājas. Ja mēģināsit, saņemsit kļūdas ziņojumu.
