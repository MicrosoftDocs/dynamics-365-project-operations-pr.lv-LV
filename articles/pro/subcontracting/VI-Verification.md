---
title: Kreditoru rēķinu pārbaude ar apstiprinātiem datiem
description: Šajā rakstā ir izskaidrots, kā Microsoft Dynamics 365 Project Operations ļauj projektu vadītājiem pārbaudīt piegādātāju rēķinus ar faktiskajiem datiem, kas tika apstiprināti, kad darbuzņēmēji izpildīja darbu un reģistrēja laiku, kā arī ar izdevumiem un materiāliem, ko izmantoja projekta darba grupas dalībnieki.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522947"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Kreditoru rēķinu pārbaude ar apstiprinātiem datiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Microsoft Dynamics 365 Project Operations ļauj projektu vadītājiem pārbaudīt piegādātāja rēķina rindas tālāk norādītajos veidos.

- Izmantojiet piegādātāja rēķina rindu lauku **Pārbaudes statuss**.
- Ja piegādātāja rēķina rindās ir atsauce uz apakšlīguma rindu, saistiet faktiskās izmaksas no apakšlīguma darbības ar šīm piegādātāja rēķina rindām. Saite tiek izveidota, salīdzinot faktisko izmaksu atbilstību piegādātāja rēķina rindām.

    > [!NOTE]
    > Kaut arī pārbaudes statusu var izsekot tām piegādātāja rēķina rindām, kurās nav atsauces uz apakšlīgumu, faktiskās izmaksas nevar saistīt ar šīm piegādātāja rēķina rindām.

## <a name="verification-status"></a>Verifikācijas statuss

Piegādātāja rēķina rindas lauks **Pārbaudes statuss** norāda šo pārbaudes statusu. Tiek atbalstīti šādi statusi:

1. Nav sākts
2. Norisē
3. Pabeigta

Piegādātāja rēķina rindas ar pārbaudes statusu **Nav sākts** var rediģēt.

Piegādātāja rēķina rindas ar pārbaudes statusu **Norisē** vairs nevar rediģēt. Piegādātāja rēķina rindai, kurā ir atsauce uz apakšlīgumu, pārbaudes statuss automātiski tiek iestatīts uz **Norisē**, tiklīdz pirmās faktiskās izmaksas ir saskaņots ar piegādātāja rēķina rindu.

Piegādātāja rēķina rindas ar pārbaudes statusu **Pabeigts** vairs nevar rediģēt. Kad visas rindas piegādātāja rēķinā ir ar šo pārbaudes statusu, var apstiprināt piegādātāja rēķinu.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Faktisko izmaksu atbilstības noteikšana piegādātāja rēķina rindām

Faktisko izmaksu atbilstības salīdzināšana palīdz veikt pārbaudes procesu piegādātāja rēķina rindai. Lai salīdzinātu faktisko izmaksu atbilstību piegādātāja rēķina rindai, veiciet tālāk minētās darbības.

1. Atveriet piegādātāja rēķina rindu un atlasiet cilni **Faktiskās izmaksas bez atbilstības**. Režģis parāda sarakstu ar faktiskajām izmaksām, kam ir atsauce uz to pašu apakšlīguma rindu kā piegādātāja rēķina rindai.
2. Atlasiet vienu vai vairākas faktiskās izmaksas un pēc tam rīkjoslā virs režģa atlasiet **Saskaņot**. Sistēma apstiprina, ka atlasītās faktiskās izmaksas var saskaņot. Pēc apstiprināšanas beigām faktiskās izmaksas tiek saistītas ar piegādātāja rēķina rindu.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Apstiprināšanas kritēriji, ko izmanto, lai saistītu faktiskās izmaksas ar piegādātāja rēķina rindām

Saskaņošanas laikā starp faktisko izmaksu vienumu un piegādātāja rēķina rindu var izveidot saiti tikai tad, ja ir izpildīti abi tālāk minētie nosacījumi.

- Katra atlasītā faktisko izmaksu vienuma laukam **Pielāgojuma statuss** ir jābūt tukšam. Citiem vārdiem, faktiskās izmaksas nedrīkst būt aizstātas ar citām faktiskajām izmaksām atsaukšanas, apstiprinājuma atcelšanas vai korekciju procesa laikā.
- Tālāk norādīto lauku vērtības ir saskaņotas starp piegādātāja rēķina rindu un atlasīto faktisko izmaksu vienumu. Ja piegādātāja rēķina rindā nav iestatīts kāds lauks, tas saskaņošanā netiek ņemts vērā.

    - Projekta līgums
    - Projekta līguma rinda
    - Transakciju klase
    - Project
    - Uzdevums
    - Resursu kategorija
    - Transakciju kategorija
    - Produkts
    - Apakšlīguma rinda
    - Rezervējamais resurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Faktiskās izmaksas bez atbilstības piegādātāja rēķina rindai

Faktisko izmaksu atbilstības atcelšana var arī palīdzēt veikt pārbaudes procesu piegādātāja rēķinā, iepriekš izveidotu saišu noņemšanu. Faktisko izmaksu atbilstību var noņemt tikai no tām piegādātāja rēķina rindām, kam ir pārbaudes statuss **Norisē**. Lai noņemtu faktisko izmaksu atbilstību no piegādātāja rēķina rindas, veiciet tālāk minētās darbības.

1. Atveriet piegādātāja rēķina rindu un atlasiet cilni **Faktiskās izmaksas ar atbilstību**. Režģis parāda sarakstu ar faktiskajām izmaksām, kam ir atsauce uz piegādātāja rēķina rindu.
2. Atlasiet vienu vai vairākas faktiskās izmaksas un pēc tam rīkjoslā virs režģa atlasiet **Atcelt atbilstību**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
