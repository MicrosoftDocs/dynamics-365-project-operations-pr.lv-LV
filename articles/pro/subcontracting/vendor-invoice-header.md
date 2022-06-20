---
title: Informācija par piegādātāju rēķiniem
description: Šajā rakstā ir izskaidrota funkcionalitāte, kas norādīta Microsoft kreditora rēķina virsrakstā Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929867"
---
# <a name="header-details-for-vendor-invoices"></a>Informācija par piegādātāju rēķiniem

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā ir izskaidrota funkcionalitāte, kas norādīta Microsoft kreditora rēķina virsrakstā Dynamics 365 Project Operations.

Tā kā projektu vadītāji plāno un izpilda projektus, viņi var nodarbināt apakšuzņēmējus un iegādāties produktus un pakalpojumus no piegādātājiem. Projekta izpildes laikā izmaksas rodas no pakalpojumu, materiālu un izdevumu kategorijām, kas tiek iepirktas apakšlīgumos ar kreditoriem. Kreditori izraksta rēķinus par šīm izmaksām projektiem, veidojot kreditoru rēķinus.

Šajā tabulā ir sniegta informācija par laukiem kreditoru rēķinu virsrakstos projektu operācijās.

| Kolonna | Apraksts | Funkcionālā ietekme |
| --- | --- | --- |
| Nosaukums/vārds | Kreditora rēķina nosaukums. | Visos piegādātāju rēķinu nolaižamajos sarakstos kreditora rēķina nosaukums ir norādīts pirmajā kolonnā, lai palīdzētu identificēt kreditora rēķinu. Pēc noklusējuma, kad kreditora rēķins tiek izveidots no apakšuzņēmuma, **kreditora rēķina lauks Nosaukums** ir iestatīts uz vērtību, kas sastāv no apakšuzņēmuma nosaukuma plus pašreizējais datums. |
| Apraksts | Īss to pakalpojumu un produktu apraksts, par kuriem tiek izrakstīts rēķins kreditora rēķinā. | Nevienu |
| Kreditors | Tā uzņēmuma nosaukums, kas izraksta rēķinus par produktiem un pakalpojumiem. Šim uzņēmumam ir jābūt konta ierakstam, kura attiecību tips **ir Kreditors** vai **Piegādātājs**. | <p>Pamatojoties uz atlasīto kreditoru, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul> |
| Apakšuzņēmēja līgums | Atsauce uz kreditora rēķina apakšuzņēmuma līgumu. | <p>Pamatojoties uz atlasīto apakšuzņēmuma līgumu, noklusējuma vērtības tiek automātiski ievadītas šādos laukos:</p><ul><li>Valūta</li><li>Cenrāži</li><li>Maksājumu nosacījumi</li><li>Maksājuma adrese</li></ul><p>Apakšuzņēmuma līgums, kas atlasīts kreditora rēķina virsrakstā, pēc noklusējuma tiek ievadīts kreditora rēķina rindās, un tur to nevar mainīt.</p> |
| Rēķina datums | Izmaksu faktiskās vērtības datums, kas tiks izveidots, apstiprinot kreditora rēķinu. | Rēķina datums tiek izmantots arī, lai atlasītu pareizo pirkšanas cenrādi vai nu cenrāžos, kas pievienoti saistītajam kreditoram, vai no projekta parametriem. |
| Statusa iemesls | Kreditora rēķina statuss. | <p>Statuss nosaka, kur atrodas kreditora rēķins biznesa procesā un vai to var rediģēt. Tālāk ir norādītas dažas no pieejamajām vērtībām.</p><ul><li>**Melnraksts** — kreditora rēķinu var rediģēt.</li><li>**Apstiprināts** – kreditora rēķins tika pārbaudīts un apstiprināts. Kreditora rēķinus ar šādu statusu nevar rediģēt vai dzēst.</li><li>**Notiek** – kreditora rēķins tiek pārskatīts. Kreditoru rēķinus ar šādu statusu var rediģēt, bet tos nevar dzēst.</li><li>**Atcelts** – kreditora rēķins tika atcelts. Kreditora rēķinus ar šādu statusu nevar rediģēt vai dzēst.</li></ul> |
| Valūta | Valūta, kurā kreditors izraksta rēķinus par precēm un pakalpojumiem kreditora rēķinā. | Kreditora rēķinā, kas atsaucas uz apakšuzņēmuma līgumu, apakšuzņēmuma valūta pēc noklusējuma tiek ievadīta kā kreditora rēķina valūta. Kreditora rēķinā, kurā nav atsauces uz apakšuzņēmuma līgumu, noklusējuma vērtība tiek ievadīta no kreditora konta ieraksta, un to var mainīt. Pēc kreditora rēķina saglabāšanas valūtu vairs nevar rediģēt. |
| Līgumslēdzēja vienība | Tā uzņēmuma nodaļa, kas ir atbildīga par pakalpojumu un/vai produktu saņemšanu no kreditora. | Nevienu |
| Maksājumu nosacījumi | Apmaksas nosacījumi izrakstītajiem kreditoru rēķiniem. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Apmaksas nosacījumi no apakšuzņēmuma tiek kopēti uz visiem kreditoru rēķiniem, kas ir saistīti ar apakšuzņēmuma līgumu. Apmaksas nosacījumus var atjaunināt, ja kreditora rēķinam ir melnraksta **statuss**. |
| Maksājuma adrese | Piegādātāja adrese, uz kuru ir jānosūta maksājumi. Noklusējuma vērtība tiek automātiski ievadīta no piegādātāja konta ierakstiem. | Apakšlīguma maksājuma adrese tiek kopēta kā maksājuma adrese visiem kreditoru rēķiniem, kas izveidoti šim apakšuzņēmējam. Maksājuma adresi var atjaunināt, ja kreditora rēķina statuss ir **Melnraksts**. |
| Starpsumma | Ja kreditora rēķinā nav rindu, ievadiet rēķina starpsummu pirms nodokļu nomaksas. Ja kreditora rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir starpsumma no visām kreditora rēķina rindām. | Nevienu |
| Kopā nodokļi | Ja kreditora rēķinā nav rindu, ievadiet apakšuzņēmēja kopējos nodokļus. Ja kreditora rēķinā ir rindas, šis lauks ir tikai lasāms. Šajā gadījumā parādītā summa ir nodokļu summu summa no visām kreditora rēķina rindām. | Nevienu |
| Kopsumma | Šajā aprēķinātajā laukā norādīta kreditora rēķina kopējā summa pēc nodokļu nomaksas. | Nevienu |

> [!NOTE]
> Pēc kreditora rēķina saglabāšanas piegādātāja rēķinā nevar mainīt šādus laukus: Kreditors, Apakšlīgums **,** Valūta **,** Līguma vienība **un** Apmaksas nosacījumi **.** **·** Ja šajos kreditora rēķina laukos ir nepieciešamas kādas izmaiņas, ir jāizdzēš kreditora rēķins un jāizveido jauns kreditora rēķins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
