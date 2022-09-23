---
title: Kreditoru rēķinu pārbaude ar apstiprinātiem datiem
description: Šajā rakstā ir paskaidrots, kā Microsoft Dynamics 365 Project Operations ļauj projektu vadītājiem pārbaudīt kreditoru rēķinus, izmantojot faktiskos datus, kas tika apstiprināti, darbuzņēmējiem veicot darbu un reģistrējot laiku, kā arī izdevumus un materiālus, ko izmantoja projekta grupas dalībnieki.
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

Microsoft Dynamics 365 Project Operations verificēsim kreditoru rēķinu rindas šādos veidos:

- Izmantojiet **lauku Verifikācijas statuss** kreditora rēķina rindās.
- Ja kreditora rēķina rindās ir atsauce uz apakšuzņēmuma līgumu rindu, saistiet faktiskos izmaksu datus no apakšuzņēmēja darbībām ar šīm kreditora rēķina rindām. Saite tiek izveidota, saskaņojot faktiskos izmaksu datus ar kreditoru rēķina rindām.

    > [!NOTE]
    > Lai gan verifikācijas statusu var izsekot kreditora rēķina rindām, kurās nav atsauces uz apakšlīgumu, faktiskos izmaksu datus nevar saistīt ar šīm kreditoru rēķinu rindām.

## <a name="verification-status"></a>Verifikācijas statuss

Lauks Verifikācijas **statuss** kreditora rēķina rindā norāda šo verifikācijas statusu. Tiek atbalstīti šādi statusi:

1. Nav sākts
2. Norisē
3. Pabeigta

Var rediģēt kreditora rēķina rindas, kuru verifikācijas **statuss ir Nav sākts**.

Kreditora rēķina rindas, kuru verifikācijas **statuss ir Pašlaik,** vairs nevar rediģēt. Kreditora rēķina rindai, kas atsaucas uz apakšlīgumu, verifikācijas statuss tiek automātiski iestatīts uz **Notiek**, tiklīdz pirmās faktiskās izmaksas tiek saskaņotas ar kreditora rēķina rindu.

Kreditora rēķina rindas, kuru verifikācijas **statuss ir Pabeigts**, vairs nevar rediģēt. Ja visām kreditora rēķina rindām ir šāds verifikācijas statuss, kreditora rēķinu var apstiprināt.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Izmaksu faktisko vērtību saskaņošana ar kreditora rēķina rindām

Faktisko izmaksu saskaņošana palīdz verifikācijas procesā kreditora rēķina rindā. Lai izmaksu faktiskās izmaksas saskaņotu ar kreditora rēķina rindu, veiciet tālāk norādītās darbības.

1. Atveriet kreditora rēķina rindu un atlasiet **cilni Nesaskaņotās faktiskās** izmaksas. Režģī tiek parādīts saraksts ar faktisko izmaksu izmaksām, kas atsaucas uz to pašu apakšlīguma rindu, uz kuru attiecas kreditora rēķina rinda.
2. Atlasiet vienu vai vairākas faktiskās izmaksas un pēc tam rīkjoslā virs režģa atlasiet **Saskaņot**. Sistēma apstiprina, ka atlasītās izmaksu faktiskās vērtības var tikt saskaņotas. Kad validācija ir nokārtota, faktiskās izmaksas tiek saistītas ar kreditora rēķina rindu.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Validācijas kritēriji, kas tiek izmantoti, lai izmaksu faktiskos datus saistītu ar kreditoru rēķinu rindām

Atbilstības procesa laikā saikni starp faktisko izmaksu un kreditora rēķina rindu var noteikt tikai tad, ja ir izpildīti abi tālāk norādītie nosacījumi.

- Laukam **Korekcijas statuss** katrai atlasītajai faktiskajai izmaksu vērtībai ir jābūt tukšam. Citiem vārdiem sakot, faktiskās izmaksas nedrīkst būt aizstātas ar citām faktiskajām izmaksām atsaukšanas, apstiprinājuma atcelšanas vai labošanas žurnāla procesa laikā.
- Tālāk norādīto lauku vērtības tiek saskaņotas starp kreditora rēķina rindu un atlasītajām faktiskajām izmaksām. Ja kāds lauks nav iestatīts kreditora rēķina rindā, tas netiek ņemts vērā kā atbilstošs.

    - Projekta līgums
    - Projekta līguma rinda
    - Transakciju klase
    - Project
    - Uzdevums
    - Resursu kategorija
    - Transakciju kategorija
    - Produkts
    - Apakšuzņēmuma līgumu līnija
    - Rezervējamais resurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Izmaksu faktiskās vērtības atsaukšana no kreditora rēķina rindas

Izmaksu faktisko vērtību atmaskošana var arī palīdzēt kreditora rēķinā iekļautajā verifikācijas procesā, ļaujot noņemt iepriekš izveidotās saites. Faktiskos izmaksu datus var nesalīdzināt tikai no kreditoru rēķinu rindām, kuru verifikācijas **statuss ir Notiek**. Lai atceltu faktisko izmaksu atzīmi no kreditora rēķina rindas, veiciet tālāk norādītās darbības.

1. Atveriet kreditora rēķina rindu un atlasiet **cilni Atbilstošās izmaksu faktiskās** izmaksas. Režģī tiek parādīts to faktisko izmaksu saraksts, kurās ir atsauce uz kreditora rēķina rindu.
2. Atlasiet vienu vai vairākas faktiskās izmaksas un pēc tam rīkjoslā virs režģa atlasiet **Atmaskot**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
