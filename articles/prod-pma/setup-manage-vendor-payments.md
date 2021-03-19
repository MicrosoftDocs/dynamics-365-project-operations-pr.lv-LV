---
title: Maksāt-kad-apmaksāts iestatīšana un izmantošana piegādātāja maksājumiem
description: Šajā tēmā ir paskaidrots, kā izveidot maksāt-kad-apmaksāts (PWP) nosacījumus, lai varētu atbrīvot daļējos piegādātāju maksājumus, pamatojoties uz klientu maksājumiem.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288612"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Maksāt-kad-apmaksāts iestatīšana un izmantošana piegādātāja maksājumiem

[!include [banner](../includes/banner.md)]

Kad apstiprināt, ka piegādātājs darbosies kā apakšuzņēmējs, iespējams, vēlēsities aizturēt maksājumu piegādātājam, līdz klients jums samaksās par projektu. Lai atbalstītu šo scenāriju, uzstādot iepirkuma pasūtījumu (PO) ar piegādātāju, var iestatīt maksāt-kad-apmaksāts (PWP) nosacījumus.

Piemēram, kad klients samaksā summu projekta rēķinā, varat izlaist daļu vai visu piegādātāja rēķina summu. Vienkārši iestatiet PWP nosacījumus, kas norāda, ka piegādātājs tiks apmaksāts pēc tam, kad saņemsit procentuālo daļu no saistītā maksājuma no klienta. Ja saņemat daļēju maksājumu no klienta, varat manuāli izlaist dažus saistītos piegādātāju rēķinus apmaksai.

Šajā piemērā ir izklāstīts process, lietojot PWP nosacījumus.

## <a name="example"></a>Piemērs

Jūsu organizācija piekrīt nodrošināt klientam 100 datoru, kuros ir instalēta programmatūra, par cenu 150,00 ASV dolāri (USD) par vienu vienību. Pēc tam jūs nolīgstat piegādātāju, kas jums nodrošina datorus, kuros instalēta programmatūra. Saskaņā ar līgumu klientam ir jāapstiprina datoru kvalitāte, pirms tas samaksā jūsu organizācijai. Jūsu organizācijas politika ir ieturēt maksājumu piegādātājiem, līdz klients jums ir samaksājis. Tādēļ iestatāt projektu, lai tā PWP procentu 100 procentu.

Piegādātājs nosūta jums 100 datoru, kuros ir instalēta programmatūra, kopā ar rēķinu par 10 000,00 ASV dolāriem. Tā kā PWP nosacījumi ir iestatīti jūsu projektam, jūs nemaksājat piegādātājam pēc datoru saņemšanas. Tā vietā nosūtāt datorus klientam kopā ar rēķinu par 15 000,00. Klients pārbauda datorus un apstiprina pilnu projekta rēķina summu.

Pēc tam, kad esat saņēmis pilnu maksājumu no klienta, jūs maksājat 10 000,00 rēķinu — pilnu piegādātāja rēķina summu.

## <a name="set-up-pwp-terms-for-a-project"></a>PWP nosacījumu iestatīšana projektam

Iestatot PWP nosacījumus projektam, kā procenti ir jānorāda minimālā summa, kas klientam ir jāmaksā par projektu, pirms maksājat piegādātājam. Sliekšņa summa tiek automātiski aprēķināta projekta klienta rēķiniem. Veiciet tālāk norādītās darbības, lai iestatītu PWP nosacījumu sliekšņa procentuālo vērtību.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Atrodiet un atveriet projektu, kuram vēlaties iestatīt PWP nosacījumus.
3. Kopsavilkuma cilnē **Piegādātāju līgumi** atlasiet **Pievienot rindu**.
3. Laukā **Konta kods** atlasiet vienu no tālāk minētajām opcijām.

    - **Tabula** — PWP nosacījumi attiecas uz vienu piegādātāju.
    - **Grupa** — PWP nosacījumi attiecas uz visiem piegādātāju grupas piegādātājiem.
    - **Visi** — PWP nosacījumi attiecas uz visiem piegādātājiem.

4. Ja iepriekšējā darbībā atlasījāt **Tabula** vai **Grupa**, laukā **Piegādātājs/piegādātāju grupa** piegādātāju vai piegādātāju grupu, uz kuru attiecas PWP nosacījumi. Ja iepriekšējā darbībā atlasījāt **Visi**, lauku **Piegādātājs/piegādātāju grupa** nevar rediģēt.
5. Ja piegādātāja ieturējumu nosacījumi piegādātājam ir iestatīti projektā, laukā **Piegādātāja ieturējumu nosacījumi** atlasiet noteikuma ID saglabāšanas nosacījumiem.
6. Laukā **PWP sliekšņa procentuālā vērtība** ievadiet projekta sliekšņa procentuālo vērtību. Projektam ievadītā procentuālā vērtība nosaka minimālo summu, kas klientam ir jāmaksā pirms samaksas piegādātājam.

## <a name="create-a-po-that-has-pwp-terms"></a>PP izveide, kuram ir PWP nosacījumi

Grāmatojot rēķinu no piegādātāja, ja uz piegādātāju attiecas PWP nosacījumi, šie nosacījumi tiek parādīti PP rindās. Lai izveidotu PP, kam ir PWP nosacījumi, rīkojieties šādi:

1. Dodieties uz **Sagāde un avoti** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**. Pēc tam dialoglodziņā **Izveidot pirkšanas pasūtījumu** ievadiet nepieciešamo informāciju un atlasiet **Labi**.

    Vai arī atveriet esošu PP saraksta lapā **Visi**.

4. Lapas **Pirkšanas pasūtījums** kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas** pārskatiet detalizētu informāciju par piegādātāja PP rindu. Automātiski tiek atlasīta opcija **Maksāt-kad-apmaksāts**, un lauks **PWP sliekšņa procentuālā vērtība** automātiski tiek kopēts no lauka **PWP sliekšņa procentuālā vērtība** lapā **Projekti**.
6. Ja nevēlaties lietot PWP nosacījumus piegādātājam PP rindai, notīriet opciju **Maksāt-kad-apmaksāts**. Šādā gadījumā PP rinda laukā **PWP sliekšņa procentuālā vērtība** tiks atiestatīta uz 0 (nulle).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Klienta maksājumu un piegādātāja apmaksu atjaunināšana

Kad piegādātājs pabeidz darbu ar projektu un nosūta jums rēķinu, ir jāpārskata projekta statuss un klientu rēķini, lai noteiktu, vai projektam ir izpildīti PWP nosacījumi. Ja tika izpildīti piegādātāja PWP nosacījumi, varat noteikt, kuras rindas piegādātāja rēķinā ir jāmaksā, pamatojoties uz klienta maksājumiem par projektu. Ja nolemjat maksāt piegādātājam pat tad, ja PWP nosacījumi nav izpildīti, varat ignorēt PWP nosacījumus lapā **Piegādātāja rēķins ar apmaksāto summu**.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Pieprasījumi un atskaites** \> **Ieturējumu pieprasījumi** \> **Piegādātāja rēķins ar apmaksāto summu**.
2. Lapas **Piegādātāja rēķins ar apmaksāto summu** meklēšanas laukā ievadiet vērtības, lai atrastu piegādātāja rēķinu, kuru vēlaties pārskatīt, un pēc tam atlasiet **Meklēt**.
3. Kopsavilkuma cilnē **Piegādātāja rēķina rindas** atlasiet rindas, kuras vēlaties mainīt.
4. Ja rēķina rindai **Maksāt-kad-apmaksāts** ir izpildīti nosacījumi, atlasiet **Izpildīt piegādātāja maksājumu**. Opcija **Maksāt-kad-apmaksāts** tiek notīrīta, un lauka **Gatavs apmaksai** vērtība tiek mainīta uz **Jā**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]