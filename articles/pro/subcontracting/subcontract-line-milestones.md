---
title: Apakšlīguma rindas atskaites punkti
description: Šajā tēmā ir izskaidrots, kā izveidot un uzturēt uz atskaites punktiem balstītu rēķinu izrakstīšanas grafiku apakšlīgumam ar piegādātāju.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558511"
---
# <a name="subcontract-line-milestones"></a>Apakšlīguma rindas atskaites punkti

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lietojumprogrammā Dynamics 365 Project Operations apakšlīguma rindā ar fiksētas cenas norēķinu metodi var norādīt uz atskaites punktiem balstītu rēķinu izrakstīšanas grafiku ar piegādātāju.

Piegādātāja rēķinu izrakstīšanas atskaites punktus var ģenerēt automātiski, izmantojot iestatīto biežumu, vai arī tos var izveidot manuāli.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automātiska uz atskaites punktiem balstīta rēķinu izrakstīšanas grafika izveide apakšlīguma rindai

Veiciet tālāk norādītās darbības, lai automātiski ģenerētu uz atskaites punktiem balstītu rēķinu izrakstīšanas grafiku fiksētai vienādi izkliedētu atskaites punktu kopai.

1. Dodieties uz **Iestatījumi** > **Rēķinu izrakstīšanas biežums** un iestatiet rēķinu izrakstīšanas biežumu apakšlīguma rindām.
2. Atveriet lapu **Apakšlīgumi**, atveriet apakšlīgumu, ar kuru vēlaties strādāt, un pēc tam atveriet fiksētas cenas apakšlīguma rindu, kurai plānojat izveidot atskaites punktu grafiku.
3. Cilnē **Apakšlīguma rindas atskaites punkti** atlasiet **Izveidot periodiskus atskaites punktus**.
4. Dialoglodziņā ievadiet vai atlasiet datumu diapazonu, atskaites punktu skaitu un rēķinu izrakstīšanas biežumu. Varat atlasīt sākuma datumu vai atskaites punktu skaitu, kā arī rēķinu izrakstīšanas biežumu vai sākuma datumu, kā arī varat atlasīt beigu datumu un rēķinu izrakstīšanas biežumu. Nevar atlasīt beigu datumu un atskaites punktu skaitu.
Izmantojot šo informāciju, sistēma ģenerē atskaites punktus un ierakstus, kas tiek rādīti režģī **Atskaites punkti**.

   - **Atskaites punkta nosaukums** — iestatītais atskaites punkta nosaukums ir atskaites punkta datums, balstoties uz rēķinu izrakstīšanas biežumu.
   - **Atskaites punkta datums** — datums, balstoties uz rēķinu izrakstīšanas biežumu.
   - **Atskaites punkta summa** — tiek aprēķināta, dalot starpsummu apakšlīguma rindā ar atskaites punktu skaitu.

Ja apakšlīguma rindas laukā **Novērtētā nodokļu summa** ir vērtība, šī vērtība tiek pievienota katram atskaites punktam vienādi, ģenerējot periodiskos atskaites punktus.

Apakšlīguma rindas atskaites punktu summai jābūt vienādai ar apakšlīguma rindas vērtību. Ja tie nav vienādi, rodas kļūda. Varat izlabot kļūdu un pārbaudīt, vai atskaites punkta kopsumma ir vienāda ar apakšlīguma rindas vērtību, izveidojot, rediģējot vai dzēšot atskaites punktu un nodokļu summas. Pēc izmaiņu veikšanas saglabājiet un atsvaidziniet lapu, lai pārliecinātos, ka vairs nav kļūdu.

## <a name="manually-create-subcontract-line-milestones"></a>Apakšlīguma rindas atskaites punktu manuāla izveide

Fiksētas cenas atskaites punktus apakšlīguma rindā var ģenerēt manuāli, ja tie netiek periodiski sadalīti. Lai manuāli izveidotu apakšlīguma rindas atskaites punktu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un atveriet apakšlīgumu, ar kuru vēlaties strādāt.
2. Atveriet fiksētas cenas apakšlīguma rindu, kurai vēlaties izveidot atskaites punktu.
3. Cilnes **Apakšlīguma rindas atskaites punkti** apakšrežģī atlasiet **+ Jauns apakšlīguma rindas atskaites punkts**.
4. Lapā **Jauns apakšlīguma rindas atskaites punkts** ievadiet nepieciešamo informāciju, balstoties uz tālāk redzamo tabulu.

    | Lauks | Apraksts |Funkcionālā ietekme|
    | --- | --- |----------------------|
    | Atskaites punkta nosaukums | Atskaites punkta nosaukums. |Tas tiks parādīts kā pirmā kolonna visos uzmeklēšanas rezultātos, pamatojoties apakšuzņēmēja līguma rindas atskaites punktiem. Šī kreditora rēķina rinda, kas tika izveidota balstoties uz šo atskaites punktu, tiks saukta arī par apakšuzņēmēja līguma rindas atskaites punkts, kā noklusējuma nosaukums kreditora rēķina rindai.|
    | Apraksts | Atskaites punkta apraksts. |Šī kreditora rēķina rinda, kas tika izveidota balstoties uz šo atskaites punktu, tiks aprakstīta, kā apakšuzņēmēja līguma rindas atskaites punkts, kā noklusējuma apraksts kreditora rēķina rindai.|
    | Atskaites punkta datums | Datums, kurā automātiskās rēķinu izveides procesa datumam jāmeklē šī atskaites punkta statuss, lai izskatītu tā izrakstīšanu.| Šī vērtība tiks izmantota kā kreditora rēķina rindas noklusējuma datums, kad tiks izrakstīts rēķins šai apakšuzņēmēja līguma rindai. |
    | Apjoms | To atskaites punktu summa vai vērtība, par ko tiks izrakstīts rēķins klientam. |Šī vērtība ir izmantota kā kreditora rēķina rindas noklusējuma daudzums, kad tiek izrakstīts rēķins šai apakšuzņēmēja līguma rindai. |
    | Nodoklis | Atskaites punktam lietotā nodokļu summa.| Šī vērtība tiek izmantota, kā kreditora rēķina rindas noklusējuma nodoklis, kad tiek izrakstīts rēķins šai apakšuzņēmēja līguma rindai. |
    | Summa pēc nodokļiem | Šis tikai lasāmais lauks tiek aprēķināts kā summa + nodokļi.|Šī vērtība tiek izmantota, kā kreditora rēķina rindas noklusējums, kad tiek izrakstīts rēķins šai apakšuzņēmēja līguma rindai. |
    | Rēķina statuss | Izveidojot atskaites punktu, vienmēr tiek iestatīts statuss **Nav gatavs rēķina izrakstīšanai**.|  Kad statuss ir **Gatavs rēķina izrakstīšanai**, pārdevēja rēķina izveides laikā šis atskaites punkts tiek iekļauts pārdevēja rēķinā. |

5. Atlasiet vienumu **Saglabāt un aizvērt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
