---
title: Projektā balstītu piedāvājumu unikālās koncepcijas
description: Šajā rakstā ir sniegta informācija par projektu piedāvājumiem korporācijā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824337"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Projektā balstītu piedāvājumu unikālās koncepcijas

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Pirms sākat izmantot projektu citātus korporācijā Microsoft Dynamics 365 Project Operations, jums jāzina šādi galvenie jēdzieni.

## <a name="owning-company"></a>Atbildīgais uzņēmums

Piederošais uzņēmums pārstāv juridisko personu, kurai pieder projekta piegāde. Debitoram piedāvājumā ir jābūt derīgam klientam šajā juridiskajā personā Finance and Operations programmās. Piederošā uzņēmuma valūtai un līgumslēdzējas struktūrvienības valūtai, kas atlasīta uz projektu balstītā piedāvājumā, ir jāatbilst.

## <a name="contracting-unit"></a>Līgumslēdzēja vienība

Līgumslēdzēja struktūrvienība pārstāv nodaļu vai praksi, kurai pieder projekta īstenošana. Katrai līgumslēdzējai vienībai var iestatīt resursu izmaksas. Norādot resursu izmaksas resursam līgumslēdzēja struktūrvienībā, varat iestatīt dažādas izmaksu likmes resursiem, no kuriem līgumslēdzēja struktūrvienība aizņemas, vai citām nodaļām vai praksēm uzņēmumā. Šīs izmaksu likmes sauc par transfertcenām, resursu aizņēmumu vai biržas cenām. Iestatot resursu aizņemšanās izmaksas no citām nodaļām, varat iestatīt izmaksu likmes kreditēšanas nodaļas valūtā.

## <a name="cost-currency"></a>Izmaksu valūta

Izmaksu valūta programmā Project Operations ir valūta, kurā tiek uzrādītas izmaksas. Šī valūta tiek atvasināta no valūtas, kas ir pievienota **kotējuma, līguma un projekta laukam Līgumslēdzēja vienība** . Izmaksas pret projektu var reģistrēt jebkurā valūtā. Tomēr notiek valūtas konvertēšana no valūtas, kurā izmaksas tika reģistrētas, uz projekta izmaksu valūtu.

Tā kā valūtas maiņas kursi Dataverse platformā nevar būt spēkā no datuma, ekrānā redzamās izmaksu kopsummas laika gaitā var mainīties, ja atjaunināt valūtas maiņas kursus. Tomēr izmaksas, kas tiek reģistrētas datu bāzē, paliek nemainīgas, jo summas tiek glabātas valūtā, kurā tās radušās.

## <a name="sales-currency"></a>Pārdošanas valūta

Pārdošanas valūta projekta operācijās ir valūta, kurā tiek reģistrētas un rādītas aplēstās un faktiskās pārdošanas summas. Tā ir arī valūta, par kuru klientam tiek izrakstīts rēķins par darījumu. Projekta piedāvājumam tiek iestatīta noklusējuma pārdošanas valūta no debitora vai uzņēmuma ieraksta, un to var mainīt, kad piedāvājums tiek izveidots. Tomēr pēc piedāvājuma saglabāšanas pārdošanas valūtu nevar mainīt. Noklusējuma produktu un projektu cenrāži tiek iestatīti, pamatojoties uz piedāvājuma pārdošanas valūtu.

Atšķirībā no izmaksām pārdošanas vērtības var ierakstīt **tikai** pārdošanas valūtā.

## <a name="billing-method"></a>Rēķinu izrakstīšanas metode

Projektiem parasti ir fiksētas maksas un patēriņa līgumu modeļi. Sadaļā Projekta operācijas projekta līguma modelis tiek attēlots ar norēķinu metodi. Norēķinu metodei ir divas vērtības: laiks un materiāls un fiksēta cena.

- **Laiks un materiāli**  — uz patēriņu balstīts līgumu slēgšanas modelis, kurā visas radušās izmaksas tiek segtas ar atbilstošiem ieņēmumiem. Aprēķinot vai radot vairāk izmaksu, palielinās arī aplēstais un faktiskais pārdošanas apjoms. Varat norādīt nepārsniedzamos ierobežojumus to piedāvājumu rindās, kam ir šī norēķinu metode. Tādā veidā jūs varat ierobežot faktiskos ieņēmumus. Aprēķinātos ieņēmumus neietekmē ierobežojumi, kas nepārsniedz ierobežojumus.
- **Fiksēta cena**  — fiksētas maksas līgumu modelis, kurā pārdošanas vērtības nav atkarīgas no izmaksām, kas radušās. Pārdošanas vērtība ir fiksēta un nemainās, aplēšot vai radot vairāk izmaksu.

## <a name="project-price-lists"></a>Projekta cenrāži

Projekta cenrāži ir cenrāži, kas tiek izmantoti, lai ievadītu noklusējuma cenas, nevis izmaksu likmes laikam, izdevumiem un citiem ar projektu saistītiem komponentiem. Var būt vairāki cenrāži, un katram no tiem var būt savs datums katram projekta piedāvājumam. Project Operations neatbalsta pārklājošos datumu efektivitāti projekta cenrāžiem.

## <a name="product-price-lists"></a>Produktu cenrāži

Produktu cenrāži ir cenrāži, kas tiek izmantoti, lai piedāvājumā ievadītu noklusējuma cenas, nevis izmaksu likmes uz precēm balstītām rindām. Katram piedāvājumam ir tikai viens produktu cenrādis.

## <a name="transaction-classes"></a>Transakciju klases

Project Operations atbalsta četru veidu transakciju klases:

- Laiks
- Izdevumi
- Materiāls
- Maksa

Izmaksu un pārdošanas vērtības var aplēst un radīt klasēs **Laiks**, **Izdevumi** un **Materiālu** transakcijas. **Maksa** ir darījumu klase, kas attiecas tikai uz ieņēmumiem.

## <a name="work-entities-and-billing-entities"></a>Darba entītijas un norēķinu entītijas

Projekti un Uzdevumi ir entītijas, kas pārstāv darbu. Piedāvājuma rindas un Līguma rindas ir entītijas, kas apzīmē norēķinus. Varat saistīt dažādas darba entītijas ar norēķinu opcijām, saistot tās ar piedāvājuma rindām vai līguma rindām.

## <a name="multi-customer-deals"></a>Vairāku klientu darījumi

Vairāku klientu darījumi notiek, ja vienā rēķinā ir vairāk nekā viens klients. Šeit ir daži tipiski piemēri:

- **Oriģinālā aprīkojuma ražotāja (OEM) uzņēmumi un to partneri**  – Partneri un tālākpārdevēji pārdod produktu, kas ietver pievienotās vērtības pakalpojumus. Darījuma laikā ar klientu OEM parasti piedāvā finansēt daļu no projekta.
- **Publiskā sektora projekti**  – Vairāki pašvaldības departamenti piekrīt finansēt projektu un tiek izrakstīti rēķini saskaņā ar iepriekš saskaņotu sadalījumu. Piemēram, skolas rajons un pilsēta vai vietējās pašvaldības departaments vienojas par peldbaseina būvniecības finansēšanu.

## <a name="invoice-schedules"></a>Rēķina izrakstīšanas grafiki

Rēķinu grafiki ir specifiski katrai piedāvājuma rindai un nav obligāti. Rēķinu grafiki tiek izveidoti, pamatojoties uz konkrētiem sākuma un beigu datumiem un rēķinu biežumu. Tie tiek izmantoti līguma posmā, kad ir konfigurēts automātiskais rēķinu izveides process. Piedāvājuma posmā rēķinu grafiki nav obligāti. Ja tie tiek izveidoti piedāvājuma stadijā, tie tiek kopēti uz projekta līgumu, kas tiek izveidots, kad tiek uzvarēts projekta piedāvājums.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Atšķirības no Dynamics 365 pārdošanas piedāvājumiem

Project Operations piedāvājumi ir balstīti uz Dynamics 365 Sales piedāvājumiem. Tomēr ir dažas būtiskas atšķirības funkcionalitātē, kas jāņem vērā.

- Projekta operāciju piedāvājumiem ir divu veidu rindas: viena projektiem un otra precēm.
- Project Operations piedāvājumiem ir savi lapas un lietotāja interfeisa (User Interface — UI) elementi, biznesa kārtulas, biznesa loģika spraudņos un klienta puses skripti, kas padara tos atšķirīgus no pārdošanas piedāvājumiem.
- Sadaļā Pārdošana vienam pārdošanas piedāvājumam varat pievienot vairākus pasūtījumus. Sadaļā Project Operations projekta piedāvājumam varat pievienot tikai vienu projekta līgumu.
- Vinnējot pārdošanas piedāvājumu, saistītā iespēja var palikt atvērta. Pēc tam, kad projekta piedāvājums ir iegūts, saistītā iespēja tiek slēgta.
- Pārdošanas piedāvājumā nav iekļauti daži lauki un koncepcijas, kas iekļautas projekta piedāvājumā. Šie lauki ir, piemēram, **Līgumslēdzēja struktūrvienība**, **Uzņēmumu pārvaldnieks** un **Rēķina saņēmēja kontaktpersonas vārds**.
- Pārdošanas piedāvājumi un projektu piedāvājumi tiek identificēti pēc lauka opciju kopa **Tips** . Pārdošanas piedāvājumam šī lauka vērtība ir **balstīta** uz krājumu. Projekta piedāvājumam vērtība ir **Uz darbu balstīta**.

Šo atšķirību dēļ mēs neiesakām pārdošanas piedāvājumus un Project Operations piedāvājumus izmantot pamīšus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
