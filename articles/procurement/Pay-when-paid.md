---
title: Maksājiet, kad kreditors ir samaksājis par maksājumiem
description: Šajā tēmā ir paskaidrots, kā izmantot scenāriju "maksāšana pēc samaksas" (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525387"
---
# <a name="pay-when-paid-vendor-payments"></a>Maksājiet, kad kreditors ir samaksājis par maksājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir paskaidrots, kā izmantot scenāriju "maksāšana pēc samaksas" (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Tāda pirkšanas pasūtījuma izveide, kurā ir PWP nosacījumi

Kad grāmatojat rēķinu no kreditora, ja uz kreditoru attiecas PWP nosacījumi, šie nosacījumi tiek rādīti pirkšanas pasūtījuma (PO) rindās. Lai izveidotu PP, kam ir PWP nosacījumi, rīkojieties šādi:

1. Programmā Microsoft Dynamics 365 Finance veiciet vienu no šīm darbībām:

    - Dodieties uz **Sagāde un avoti** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**. Darbību rūtī atlasiet **Jauns**. Dialoglodziņā Pirkšanas **pasūtījuma** izveide atlasiet kreditoru, kuram projektā ir iestatīti PWP nosacījumi, ievadiet citu nepieciešamo informāciju un pēc tam atlasiet **Labi**.
    - Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**. Darbību rūts cilnē **Pārvaldība** atlasiet **Uzdevums Vienums**. Atlasiet pirkšanas pasūtījumu. Atlasiet kreditoru, kuram projektā ir iestatīti PWP nosacījumi, un pēc tam atlasiet **Labi**.

2. Lapas Pirkšanas **pasūtījums** cilnē Pirkšanas **pasūtījuma rindas** Ātrā cilne atlasiet **Pievienot rindu**, lai izveidotu pirkšanas pasūtījuma rindu.
3. Atlasiet krājuma numuru vai sagādes kategoriju un ievadiet citu nepieciešamo informāciju. Pārskatiet detalizētu informāciju par kreditora pirkšanas pasūtījuma rindiņu.

    Automātiski tiek atlasīta opcija **Maksāt-kad-apmaksāts**, un lauks **PWP sliekšņa procentuālā vērtība** automātiski tiek kopēts no lauka **PWP sliekšņa procentuālā vērtība** lapā **Projekti**.

4. Ja nevēlaties lietot PWP nosacījumus piegādātājam PP rindai, notīriet opciju **Maksāt-kad-apmaksāts**. Šajā gadījumā pirkšanas pasūtījuma rindas **PWP sliekšņa procentuālās** daļas lauks tiks atiestatīts uz **0** (nulle).
5. Lapas Pirkšanas **pasūtījums** darbību rūts **cilnē Pirkšana** atlasiet **Apstiprināt**, lai apstiprinātu pirkšanas pasūtījumu.
6. Darbību rūts cilnē Rēķins **atlasiet** **Rēķins**, lai ģenerētu rēķinu pirkšanas pasūtījumam.

## <a name="create-a-project-invoice-proposal"></a>Projekta rēķina priekšlikuma izveide

Projekta rēķinu priekšlikumi tiek izmantoti, lai izveidotu projekta rēķinus debitoram. PWP scenārijā kreditoru maksājumi ir atkarīgi no debitoru maksājumiem saskaņā ar PWP iestatījumiem. Tomēr ir iespējas, kas ļauj atbrīvot maksājumus bez debitoru maksājumiem, kā jums nepieciešams. Lai debitoram izveidotu projekta rēķinu, veiciet tālāk norādītās darbības.

1. Klientu iesaistes programmās dodieties uz **Project** \> **Projects** un atlasiet projektu.
2. **Cilnē Faktiskie** dati atlasiet faktisko rindu, ko ģenerē pirkšanas pasūtījums, kuram ir pirkšanas **unbilāro pārdošanas transakciju** tips. Pēc tam atlasiet **Gatavs rēķinam**.
3. Dodieties uz **Pārdošanas** \> **pārdošanas** \> **projekta līgums** un atlasiet projekta līgumu.
4. Darbību rūtī atlasiet **Rēķins**, lai ģenerētu debitora rēķinu.
5. Programmā Finance dodieties uz **Projektu pārvaldība un grāmatvedība** \> **Periodiskā** \> **importēšana no sagatavošanas tabulas** un atlasiet **Labi**, lai ģenerētu projektu operāciju integrācijas žurnālu.
6. Dodieties uz **Projektu vadība un uzskaite** \> **Projekta rēķini** \> **Projekta rēķina priekšlikums** un atlasiet **Izlikt ziņu**, lai grāmatotu projektam ģenerēto rēķina priekšlikumu.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Klienta maksājumu un piegādātāja apmaksu atjaunināšana

Kad kreditors ir pabeidzis darbu pie projekta un nosūta jums rēķinu, jums ir jāpārskata projekta statuss un debitoru rēķini, lai noteiktu, vai projektā ir izpildīti PWP nosacījumi. Ja tika izpildīti piegādātāja PWP nosacījumi, varat noteikt, kuras rindas piegādātāja rēķinā ir jāmaksā, pamatojoties uz klienta maksājumiem par projektu. Ja nolemjat maksāt piegādātājam pat tad, ja PWP nosacījumi nav izpildīti, varat ignorēt PWP nosacījumus lapā **Piegādātāja rēķins ar apmaksāto summu**.

1. Programmā Finance dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atlasiet projektu.
2. Darbību rūtī atlasiet **Vadīkla** un pēc tam atlasiet **Kreditoru rēķini**, lai parādītu visus projektam ģenerētos kreditoru rēķinus.
3. Lapas **Piegādātāja rēķins ar apmaksāto summu** meklēšanas laukā ievadiet vērtības, lai atrastu piegādātāja rēķinu, kuru vēlaties pārskatīt, un pēc tam atlasiet **Meklēt**.
4. Atlasiet opciju **Maksāt, kad maksājat**, lai skatītu tikai PWP rēķinus.
5. Ātrās **cilnes Kreditoru rēķinu rindās** atlasiet rindas, kuras vēlaties izlaist apmaksai.
6. Atlasiet **Atbrīvot kreditora maksājumu**. Opcija **Maksāt-kad-apmaksāts** tiek notīrīta, un lauka **Gatavs apmaksai** vērtība tiek mainīta uz **Jā**.
