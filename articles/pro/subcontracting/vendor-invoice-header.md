---
title: Informācija par piegādātāju rēķiniem
description: Šajā rakstā ir izskaidrota funkcionalitāte, kas tiek nodrošināta piegādātāja rēķina galvenē programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261670"
---
# <a name="header-details-for-vendor-invoices"></a>Informācija par piegādātāju rēķiniem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā ir izskaidrota funkcionalitāte, kas tiek nodrošināta piegādātāja rēķina galvenē programmā Microsoft Dynamics 365 Project Operations.

Kamēr projektu vadītāji plāno un izpilda projektus, viņi var nodarbināt apakšuzņēmējus un iegādāties produktus un pakalpojumus no piegādātājiem. Projekta izpildes laikā izmaksas rodas no pakalpojumu, materiālu un izmaksu kategorijām, kas tiek iepirktas ar apakšlīgumiem no piegādātājiem. Piegādātāji izraksta rēķinu par šīm izmaksām projektā, izveidojot piegādātāju rēķinus.

Šajā tabulā ir informācija par piegādātāja rēķina galvenēm programmā Project Operations.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Piegādātāja rēķina nosaukums. | Visos piegādātāja rēķina nolaižamajos sarakstos piegādātāja rēķina nosaukums tiek norādīts pirmajā kolonnā, lai palīdzētu jums identificēt piegādātāja rēķinu. Pēc noklusējuma, izveidojot piegādātāja rēķinu no apakšlīguma, piegādātāja rēķina laukā **Nosaukums** tiek iestatīta vērtība, kas sastāv no apakšlīguma nosaukuma un pašreizējā datuma. |
| Apraksts | Īss pakalpojumu un produktu apraksts, par kuriem tiek izrakstīts piegādātāja rēķins. | Nevienu |
| Kreditors | Uzņēmuma nosaukums, kas izraksta rēķinu par produktiem un pakalpojumiem. Šim uzņēmumam ir nepieciešams uzņēmuma ieraksts, kam ir attiecību tips **Pārdevējs** vai **Piegādātājs**. | <p>Pamatojoties uz atlasīto piegādātāju, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul> |
| Apakšuzņēmēja līgums | Atsauce uz piegādātāja rēķina apakšlīgumu. | <p>Pamatojoties uz atlasīto apakšlīgumu, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul><p>Apakšlīgums, kas tiek atlasīts piegādātāja rēķina galvenē, tiek ievadīts pēc noklusējuma piegādātāja rēķina rindās, un to tur nevar mainīt.</p> |
| Rēķina datums | Faktisko izmaksu datums, kas tiks izveidots, kad tiks apstiprināts piegādātāja rēķins. | Rēķina datums tiek arī izmantots, lai atlasītu pareizo cenrādi no cenrāžiem, kas ir pievienoti saistītajam piegādātājam, vai no projekta parametriem. |
| Statusa iemesls | Piegādātāja rēķina statuss. | <p>Statuss nosaka, kur atrodas piegādātāja rēķins uzņēmējdarbības procesā, un to var rediģēt. Šīs ir dažas no pieejamajām vērtībām:</p><ul><li>**Melnraksts** — piegādātāja rēķinu var rediģēt.</li><li>**Apstiprināts** — piegādātāja rēķins tika pārbaudīts un apstiprināts. Šajā statusā piegādātāja rēķinus nevar rediģēt vai dzēst.</li><li>**Procesā** — piegādātāja rēķins tiek pārskatīts. Šajā statusā piegādātāja rēķinus var rediģēt, bet nevar dzēst.</li><li>**Atcelts** — piegādātāja rēķins tika atcelts. Šajā statusā piegādātāja rēķinus nevar rediģēt vai dzēst.</li></ul> |
| Valūta | Valūta, kurā piegādātājs izraksta rēķinu par produktiem un pakalpojumiem piegādātāja rēķinā. | Piegādātāja rēķinā, kas atsaucas uz apakšlīgumu, apakšlīguma valūta pēc noklusējuma tiek ievadīta tāda pati kā piegādātāja rēķina valūta. Piegādātāja rēķinā, kam nav atsauces uz apakšlīgumu, noklusējuma vērtība tiek ievadīta no piegādātāja uzņēmuma ieraksta, un to var mainīt. Pēc piegādātāja rēķina saglabāšanas valūtu vairs nevar rediģēt. |
| Līgumslēdzēja vienība | Uzņēmuma nodaļa, kas ir atbildīga par pakalpojumu un/vai produktu saņemšanu no piegādātāja. | Nevienu |
| Maksājumu nosacījumi | Maksājumu nosacījumi par piegādātāju rēķiniem, kas tiek izsniegti. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājumu nosacījumi no apakšuzņēmēja līguma tiek kopēti uz visiem ar apakšlīgumu saistītajiem piegādātāja rēķiniem. Maksājumu nosacījumus var atjaunināt, ja piegādātāja rēķina statuss ir **Melnraksts**. |
| Maksājuma adrese | Piegādātāja adrese, uz kuru ir jānosūta maksājumi. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājumu adrese no apakšuzņēmēja līguma tiek kopēta, kā maksājuma adrese visiem šim apakšlīgumam izveidotajiem piegādātāja rēķiniem. Maksājumu adresi var atjaunināt, ja piegādātāja rēķina statuss ir **Melnraksts**. |
| Starpsumma | Ja piegādātāja rēķinā nav rindu, ievadiet rēķinu starpsummu pirms nodokļiem. Ja piegādātāja rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir starpsumma no visām piegādātāja rēķina rindām. | Nevienu |
| Kopā nodokļi | Ja piegādātāja rēķinā nav rindu, ievadiet nodokļu kopsummu apakšlīgumā. Ja piegādātāja rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir nodokļu summu kopsumma no visām piegādātāja rēķina rindām. | Nevienu |
| Kopsumma | Šajā aprēķinātajā laukā ir redzama piegādātāja rēķina kopsumma pēc nodokļu iekļaušanas. | Nevienu |

> [!NOTE]
> Pēc piegādātāja rēķina saglabāšanas piegādātāja rēķinā nevar mainīt šādus laukus: **Piegādātājs**, **Apakšlīgums**, **Valūta**, **Līgumslēdzēja vienība** un **Maksājumu nosacījumi**. Ja šajos laukos piegādātāja rēķinā ir vajadzīgas izmaiņas, piegādātāja rēķins ir jāizdzēš un jāizveido jauns piegādātāja rēķins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
