---
title: "\"Apmaksāt pēc apmaksas\" tipa piegādātāju maksājumi"
description: Šajā tēmā izskaidrots, kā izmantot "apmaksāt pēc apmaksas" (PWP) scenāriju.
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
# <a name="pay-when-paid-vendor-payments"></a>"Apmaksāt pēc apmaksas" tipa piegādātāju maksājumi

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā izskaidrots, kā izmantot "apmaksāt pēc apmaksas" (PWP) scenāriju.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Pirkuma pasūtījuma ar PWP nosacījumiem izveide

Grāmatojot rēķinu no piegādātāja, ja uz piegādātāju attiecas PWP nosacījumi, šie nosacījumi tiek parādīti pirkšanas pasūtījuma (PO) rindās. Lai izveidotu PP, kam ir PWP nosacījumi, rīkojieties šādi:

1. Programmā Microsoft Dynamics 365 Finance izpildiet vienu no turpmāk uzskaitītajām darbībām:

    - Dodieties uz **Sagāde un avoti** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**. Darbību rūtī atlasiet **Jauns**. Dialoglodziņā **Izveidot pirkuma pasūtījumu** atlasiet piegādātāju, kuram projektā tiek sagatavoti PWP nosacījumi, ievadiet pārējo vajadzīgo informāciju un atlasiet **Labi**.
    - Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**. Darbību rūts cilnē **Pārvaldīt** atlasiet **Vienības uzdevums**. Atlasiet pirkšanas pasūtījumu. Atlasiet piegādātāju, kuram projektā tiek sagatavoti PWP nosacījumi un atlasiet **Labi**.

2. Laukā **Pirkšanas pasūtījums**, kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai izveidotu pirkšanas pasūtījuma rindu.
3. Atlasiet elementa numuru vai iepirkuma kategoriju un ievadiet pārējo vajadzīgo informāciju. Pārskatiet piegādātāja PO rindas informāciju.

    Automātiski tiek atlasīta opcija **Maksāt-kad-apmaksāts**, un lauks **PWP sliekšņa procentuālā vērtība** automātiski tiek kopēts no lauka **PWP sliekšņa procentuālā vērtība** lapā **Projekti**.

4. Ja nevēlaties lietot PWP nosacījumus piegādātājam PP rindai, notīriet opciju **Maksāt-kad-apmaksāts**. Šādā gadījumā PO rindas lauks **PWP sliekšņa procentuālā vērtība** tiks atiestatīts uz **0** (nulle).
5. Darbību rūts lapā **Pirkšanas pasūtījums**, cilnē **Pirkums** atlasiet **Apstiprināt**, lai apstiprinātu pirkšanas pasūtījumu.
6. Darbību rūts cilnē **Rēķins** atlasiet **Rēķins**, lai ģenerētu pirkuma pasūtījuma rēķinu.

## <a name="create-a-project-invoice-proposal"></a>Projekta rēķina priekšlikuma izveide

Projekta rēķinu priekšlikumus izmanto, lai klientam izveidotu projekta rēķinus. PWP scenārijā piegādātāju maksājumi ir atkarīgi no klienta maksājumiem atbilstoši PWP iestatījumiem. Taču ir iespējas, ar kurām maksājumus varat pēc vajadzības veikt, neraugoties uz klienta maksājumiem. Lai klientam izveidotu projekta rēķinu, izpildiet turpmāk uzskaitītās darbības.

1. Klientu iesaistes programmā atveriet **Projekts**\>**Projekti** un atlasiet projektu.
2. Cilnē **Dati** atlasiet PO ģenerēto datu rindu, kurai ir transakcijas tipa **Rēķinā neiekļautā pārdošana**. Pēc tam atlasiet **Gatavs rēķinam**.
3. Dodieties uz **Pārdošana** \>**Pārdošana** \>**Projekta līgums** un atlasiet projekta līgumu.
4. Darbību rūtī atlasiet **Rēķins**, lai ģenerētu klienta rēķinu.
5. Pakalpojumā Finance dodieties uz **Projektu pārvaldībva un uzskaite** \>**Periodiski** \>**Importēt no izstādīšanas tabulas** un atlasiet **Labi**, lai ģenerētu Project Operations integrācijas žurnālu.
6. Dodieties uz **Projektu pārvaldība un uzskaite** \> **Projekta rēķini** \> **Projekta rēķina priekšlikums** un atlasiet **Grāmatot**, lai grāmatotu projektam ģenerēto rēķina priekšlikumu.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Klienta maksājumu un piegādātāja apmaksu atjaunināšana

Kad piegādātājs pabeidz darbu ar projektu un nosūta jums rēķinu, ir jāpārskata projekta statuss un klientu rēķini, lai noteiktu, vai projektam tika izpildīti PWP nosacījumi. Ja tika izpildīti piegādātāja PWP nosacījumi, varat noteikt, kuras rindas piegādātāja rēķinā ir jāmaksā, pamatojoties uz klienta maksājumiem par projektu. Ja nolemjat maksāt piegādātājam pat tad, ja PWP nosacījumi nav izpildīti, varat ignorēt PWP nosacījumus lapā **Piegādātāja rēķins ar apmaksāto summu**.

1. Sadaļā Finance dodieties uz **Projektu pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti** un atlasiet projektu.
2. Darbību rūtī atlasiet **Vadība** un pēc tam atlasiet **Piegādātāju rēķini**, lai redzētu visus projektam ģenerētos piegādātāju rēķinus.
3. Lapas **Piegādātāja rēķins ar apmaksāto summu** meklēšanas laukā ievadiet vērtības, lai atrastu piegādātāja rēķinu, kuru vēlaties pārskatīt, un pēc tam atlasiet **Meklēt**.
4. Lai skatītu tikai PWP rēķinus, atlasiet opciju **Apmaksāt pēc apmaksas**.
5. Kopsavilkuma cilnē **Piegādātāja rēķina rindas** atlasiet rindas, kurām vēlaties veikt maksājumu.
6. Atlasiet **Veikt piegādātāja maksājumu**. Opcija **Maksāt-kad-apmaksāts** tiek notīrīta, un lauka **Gatavs apmaksai** vērtība tiek mainīta uz **Jā**.
