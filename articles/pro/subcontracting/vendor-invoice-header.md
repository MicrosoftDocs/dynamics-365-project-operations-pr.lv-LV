---
title: Informācija par piegādātāju rēķiniem
description: Šajā rakstā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Microsoft kreditora rēķina galvenē Dynamics 365 Project Operations.
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

Šajā rakstā ir izskaidrota funkcionalitāte, kas tiek nodrošināta Microsoft kreditora rēķina galvenē Dynamics 365 Project Operations.

Tā kā projektu vadītāji plāno un īsteno projektus, viņi var nodarbināt apakšuzņēmējus un iegādāties produktus un pakalpojumus no piegādātājiem. Projekta izpildes laikā izmaksas rodas no pakalpojumiem, materiāliem un izdevumu kategorijām, kas tiek iepirktas apakšuzņēmuma līgumos ar piegādātājiem. Kreditori izraksta rēķinus par šīm izmaksām projektiem, izveidojot kreditoru rēķinus.

Šajā tabulā ir sniegta informācija par laukiem kreditoru rēķinu galvenēs programmā Project Operations.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina nosaukums. | Visos kreditoru rēķinu nolaižamajās sarakstos kreditora rēķina nosaukums ir norādīts pirmajā kolonnā, lai palīdzētu identificēt kreditora rēķinu. Pēc noklusējuma, kad kreditora rēķins tiek izveidots no apakšuzņēmuma līguma, **kreditora rēķina laukam Nosaukums** tiek iestatīta vērtība, kas sastāv no apakšuzņēmuma līguma nosaukuma un pašreizējā datuma. |
| Apraksts | Īss apraksts par pakalpojumiem un precēm, par kurām tiek izrakstīts rēķins kreditora rēķinā. | Nevienu |
| Kreditors | Tā uzņēmuma nosaukums, kas izraksta rēķinus par produktiem un pakalpojumiem. Šim uzņēmumam ir jābūt konta ierakstam, kura relāciju tips ir Kreditors **vai** **Piegādātājs**. | <p>Pamatojoties uz atlasīto kreditoru, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul> |
| Apakšuzņēmēja līgums | Atsauce uz apakšlīgumu par kreditora rēķinu. | <p>Pamatojoties uz atlasīto apakšuzņēmuma līgumu, noklusējuma vērtības tiek automātiski ievadītas tālāk norādītajos laukos.</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul><p>Apakšlīgums, kas ir atlasīts kreditora rēķina galvenē, pēc noklusējuma tiek ievadīts kreditora rēķina rindās, un tur to nevar mainīt.</p> |
| Rēķina datums | Faktisko izmaksu datums, kas tiks izveidots, apstiprinot kreditora rēķinu. | Rēķina datums tiek izmantots arī, lai atlasītu pareizo pirkšanas cenrādi vai nu no cenrāžiem, kas ir pievienoti saistītajam kreditoram, vai no projekta parametriem. |
| Statusa iemesls | Kreditora rēķina statuss. | <p>Statuss nosaka, kur kreditora rēķins atrodas biznesa procesā un vai to var rediģēt. Tālāk ir norādītas dažas no pieejamajām vērtībām.</p><ul><li>**Melnraksts** — kreditora rēķinu var rediģēt.</li><li>**Apstiprināts** — kreditora rēķins tika pārbaudīts un apstiprināts. Kreditoru rēķinus šajā statusā nevar rediģēt vai dzēst.</li><li>**Procesā** — tiek pārskatīts kreditora rēķins. Kreditoru rēķinus šajā statusā var rediģēt, bet tos nevar izdzēst.</li><li>**Atcelts** — kreditora rēķins tika atcelts. Kreditoru rēķinus šajā statusā nevar rediģēt vai dzēst.</li></ul> |
| Valūta | Valūta, par kuru kreditors izraksta rēķinus par precēm un pakalpojumiem kreditora rēķinā. | Kreditora rēķinā, kurā ir atsauce uz apakšlīgumu, apakšuzņēmuma līguma valūta pēc noklusējuma tiek ievadīta kā kreditora rēķina valūta. Kreditora rēķinā, kurā nav atsauces uz apakšlīgumu, noklusējuma vērtība tiek ievadīta kreditora konta ierakstā un var tikt mainīta. Pēc kreditora rēķina saglabāšanas valūtu vairs nevar rediģēt. |
| Līgumslēdzēja vienība | Uzņēmuma nodaļa, kas ir atbildīga par pakalpojumu un/vai produktu saņemšanu no pārdevēja. | Nevienu |
| Maksājumu nosacījumi | Apmaksas noteikumi izrakstītajos kreditoru rēķinos. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājuma nosacījumi no apakšuzņēmuma līguma tiek kopēti uz visiem kreditoru rēķiniem, kas ir saistīti ar apakšlīgumu. Maksājuma nosacījumus var atjaunināt, ja kreditora rēķinam ir melnraksta **statuss**. |
| Maksājuma adrese | Piegādātāja adrese, uz kuru ir jānosūta maksājumi. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Maksājuma adrese no apakšuzņēmuma līguma tiek kopēta kā maksājuma adrese visiem kreditoru rēķiniem, kas ir izveidoti šim apakšlīgumam. Maksājuma adresi var atjaunināt, ja kreditora rēķinam ir melnraksta **statuss**. |
| Starpsumma | Ja kreditora rēķinam nav rindu, pirms nodokļu nomaksas ievadiet rēķina starpsummu. Ja kreditora rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir starpsummu summa no visām rindām kreditora rēķinā. | Nevienu |
| Kopējais nodoklis | Ja kreditora rēķinā nav rindu, ievadiet kopējos nodokļus apakšuzņēmuma līgumā. Ja kreditora rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir nodokļu summu summa no visām rindām kreditora rēķinā. | Nevienu |
| Kopsumma | Šajā aprēķinātajā laukā tiek parādīta kreditora rēķina kopējā summa pēc nodokļu iekļaušanas. | Nevienu |

> [!NOTE]
> Pēc kreditora rēķina saglabāšanas nevar mainīt šādus kreditora rēķina laukus: Kreditors **, Apakšlīgums**, **Valūta** **,** Līgumslēdzēja struktūrvienība **un** Maksājuma nosacījumi **.** Ja šajos laukos kreditora rēķinā ir nepieciešamas kādas izmaiņas, jums ir jāizdzēš kreditora rēķins un jāizveido jauns kreditora rēķins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
