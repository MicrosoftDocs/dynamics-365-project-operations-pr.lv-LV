---
title: Kreditoru rēķinu pārbaude ar apstiprinātiem datiem
description: Šajā rakstā paskaidrots, kā Microsoft Dynamics 365 Project Operations projektu vadītāji pārbaudīs piegādātāju rēķinus ar faktiskajiem datiem, kas tika apstiprināti kā darbuzņēmēji, kas veica darbu un reģistrēja laiku, kā arī izdevumus un materiālus, ko izmantoja projekta grupas dalībnieki.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914227"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Kreditoru rēķinu pārbaude ar apstiprinātiem datiem

[!include [banner](../../includes/dataverse-preview.md)]

_ **Attiecas uz:** Lite izvietošana - darījums ar proforma rēķinu izrakstīšanu

Microsoft Dynamics 365 Project Operations projektu vadītāji pārbaudīs kreditora rēķina rindas šādos veidos:

- **Izmantojiet kreditora rēķina rindu lauku Pārbaudes statuss**.
- Ja kreditora rēķina rindas atsaucas uz apakšuzņēmuma rindu, saistiet izmaksu faktiskos datus no apakšuzņēmēja darbības uz šīm kreditora rēķina rindām. Saite tiek izveidota, saskaņojot izmaksu faktiskās vērtības ar kreditora rēķina rindām.

    > [!NOTE]
    > Lai gan pārbaudes statusu var izsekot kreditora rēķina rindām, kas neatsaucas uz apakšuzņēmuma līgumu, izmaksu faktiskās nevar saistīt ar šīm kreditora rēķina rindām.

## <a name="verification-status"></a>Pārbaudes statuss

Kreditora **rēķina rindas lauks Verifikācijas statuss** norāda šo pārbaudes statusu. Tiek atbalstīti šādi statusi:

1. Nav sākts
2. Norisē
3. Pabeigta

Kreditora rēķina rindas, kuru pārbaudes statuss **ir Nav startēts**, var labot.

Kreditora rēķina rindas, kuru pārbaudes statuss **ir Notiek**, vairs nevar labot. Kreditora rēķina rindai, kas atsaucas uz apakšuzņēmuma līgumu, pārbaudes statuss tiek automātiski iestatīts uz **Notiek,** tiklīdz pirmās faktiskās izmaksas tiek saskaņotas ar kreditora rēķina rindu.

Kreditora rēķina rindas, kuru pārbaudes statuss ir **Pabeigts**, vairs nevar labot. Ja visām kreditora rēķina rindām ir šāds pārbaudes statuss, kreditora rēķinu var apstiprināt.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Saskaņot izmaksu faktiskos ar kreditora rēķina rindām

Izmaksu faktisko saskaņošana palīdz veikt pārbaudes procesu kreditora rēķina rindā. Lai izmaksu faktisko atbilstību kreditora rēķina rindai saskaņotu ar kreditora rēķina rindu, rīkojieties šādi.

1. Atveriet kreditora rēķina rindu un atlasiet **cilni Nesaskaņotās izmaksu faktiskās** vērtības. Režģis parāda izmaksu faktisko sarakstu, kas atsaucas uz to pašu apakšuzņēmuma rindu kā kreditora rēķina rinda.
2. Atlasiet vienu vai vairākus izmaksu faktiskos lielumus un pēc tam rīkjoslā virs režģa atlasiet **Saskaņot**. Sistēma apstiprina, ka atlasītos izmaksu faktiskos lielumus var saskaņot. Pēc pārbaudes pabeigšanas izmaksu faktiskās izmaksas tiek saistītas ar kreditora rēķina rindu.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Pārbaudes kritēriji, ko izmanto, lai izmaksu faktiskos datus sasaistītu ar kreditora rēķina rindām

Saskaņošanas procesa laikā saiti starp faktisko pašizmaksu un kreditora rēķina rindu var izveidot tikai tad, ja ir izpildīti abi šie nosacījumi:

- Laukam **Korekcijas statuss** katrai faktiskajai atlasītajai pašizmaksai jābūt tukšam. Citiem vārdiem sakot, atsaukšanas, apstiprināšanas atcelšanas vai labošanas žurnāla procesa laikā izmaksu faktiskās izmaksas nedrīkst aizstāt ar citām izmaksu izteiksmēm.
- Šo lauku vērtības tiek saskaņotas starp kreditora rēķina rindu un faktiskajām atlasītajām izmaksām. Ja kreditora rēķina rindā nav iestatīts kāds lauks, tas netiek ņemts vērā saskaņošanai.

    - Projekta līgums
    - Projekta līguma rinda
    - Transakciju klase
    - Project
    - Uzdevums
    - Resursu kategorija
    - Transakciju kategorija
    - Produkts
    - Apakšuzņēmuma līnija
    - Rezervējamais resurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Atmatīt izmaksu faktiskās vērtības no kreditora rēķina rindas

Izmaksu faktisko attiecību atcelšana var palīdzēt arī kreditora rēķina pārbaudes procesā, ļaujot noņemt iepriekš izveidotās saites. Izmaksu faktiskos lielumus var nesaskaņot tikai no kreditora rēķina rindām, kuru pārbaudes statuss **ir Notiek**. Lai noņemtu izmaksu faktiskos rādītājus no kreditora rēķina rindas, rīkojieties šādi.

1. Atveriet kreditora rēķina rindu un atlasiet **cilni Saskaņoto izmaksu faktiskās** vērtības. Režģis parāda izmaksu faktisko sarakstu, kas atsaucas uz kreditora rēķina rindu.
2. Atlasiet vienu vai vairākus izmaksu faktiskos lielumus un pēc tam rīkjoslā virs režģa atlasiet **Noņemt** atlasi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
