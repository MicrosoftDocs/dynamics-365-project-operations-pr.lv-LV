---
title: Izdevumu atskaišu publicēšana
description: Šajā rakstā ir izskaidrots, kā grāmatot izdevumu atskaites.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524879"
---
# <a name="post-expense-reports"></a>Izdevumu atskaišu publicēšana

Pēc izdevumu atskaites apstiprināšanas un pārsūtīšanas uz vispārējo žurnālu to var iegrāmatot. Grāmatojot izdevumu atskaiti, tiek identificēti izdevumi, par kuriem var atgūt pievienotās vērtības nodokli (PVN). Uzdevums pārbaudīt un atgūt PVN maksājumus tiek piešķirts darbiniekam, kurš ir atbildīgs par izdevumu atskaites verificēšanu.

Ja izdevumi izdevumu atskaitē tiek iekasēti citam uzņēmumam, nevis uzņēmumam, kas nodarbina šo darbinieku, ir jāpārbauda gan uzņēmums, kuram šie izdevumi tiks atmaksāti, gan uzņēmums, no kura tie tiks segti. Piemēram, darbinieks, kurš iesniedzis izdevumu atskaiti, strādā uzņēmumā DAT, bet pieprasīja izdevumu atmaksu uzņēmumam DIR. Šajā gadījumā DAT ir uzņēmums, kuram izdevumi tiks atmaksāti, un DIR ir uzņēmums, no kura izdevumi tiks segti. Pēc šo žurnāla rindu verificēšanas varat grāmatot izdevumu rindas virsgrāmatā.

Lai grāmatotu izdevumu atskaiti, lapā **Apstiprinātās izdevumu atskaites** atlasiet izdevumu atskaiti un pēc tam darbību rūtī atlasiet vienumu **Grāmatot**.

Varat arī grāmatot visas sarakstā esošās izdevumu atskaites vienlaicīgi. Atlasiet visas izdevumu atskaites un pēc tam atlasiet vienumu **Grāmatot**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Iespējot iespēju grāmatot izdevumu atbildību piegādātāja valūtai attiecībā uz skaidras naudas maksājuma metodes līdzekli

Līdzeklis **Iespēja grāmatot izdevumu atbildību piegādātāja valūtā maksājumiem skaidrā naudā** ļauj grāmatot izdevumu atskaites piegādātāja valūtā, ja tiek izmantota skaidras naudas maksājuma metode.

Pašlaik, iesniedzot skaidras naudas izdevumus, izdevumu atskaites tiek grāmatots uzskaites valūtā. Tā kā summa tiek pārvērsta starp transakcijas valūtu, grāmatvedības valūtu un piegādātāja valūtu, piegādātājiem tiek samaksāta nepareiza summa, ja rēķina transakcijas datumam un faktiskajam maksājuma datumam ir atšķirīgs valūtas kurss.

Šis līdzeklis nodrošinās to, ka piegādātāja bilance tiek ierakstīta piegādātāja valūtā, kad tiek grāmatota izmaksu atskaite.

1. Atveriet sadaļu **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Sarakstā atrodiet un atlasiet **Iespēja grāmatot izdevumu atbildību piegādātāja valūtā maksājumam skaidrā naudā**, pēc tam atlasiet **Iespējot tagad**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
