---
title: Naudas avanss
description: Šajā tēmā ir sniegta informācija par naudas avansiem.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122758"
---
# <a name="cash-advance"></a>Naudas avanss

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Naudas avanss ļauj darbiniekiem aizņemties naudu no uzņēmuma pirms jebkādu izdevumu rašanās. Kad tiek apstiprināts un izmaksāts pieprasītais naudas avanss, darbinieks var izmantot šo naudu, lai segtu uzņēmuma izdevumus, kas tam varētu rasties. 

## <a name="create-and-submit-a-cash-advance-request"></a>Naudas avansa pieprasījuma izveide un iesniegšana

1. Sadaļā **Mani izdevumi** atlasiet **Naudas avansi** > **Jauns**, lai izveidotu jaunu naudas avansu. 
2. Lapā **Jauns naudas avansa pieprasījums** ievadiet izdevumu mērķi un atlasiet vietu, kurā radīsies izdevumi.
3. Ievadiet pieprasīto summu un valūtu un pēc tam atlasiet vienumu **Saglabāt**. 
4. Kad esat gatavs iesniegt naudas avansa pieprasījumu, lapā **Naudas avansa pieprasījums** atlasiet vienumu **Darbplūsma** > **Iesniegt**.

## <a name="modify-a-cash-advance-request"></a>Naudas avansa pieprasījuma modificēšana

Ja naudas avansa pieprasījums nav iesniegts apstiprināšanai, jūs varat to modificēt.

1. Sadaļā **Mani izdevumi: naudas avansi** atrodiet un atlasiet naudas avansu, ko vēlaties rediģēt.
2. Atlasiet **Rediģēt** un veiciet nepieciešamās izmaiņas naudas avansa pieprasījumā. 
3. Atlasiet **Saglabāt un aizvērt**.


## <a name="view-cash-advance-requests"></a>Naudas avansa pieprasījumu skatīšana
Varat pārskatīt visu to naudas avansu sarakstu, kas ir melnrakstā, iesniegti, tiek pārskatīti vai izmaksāti, sadaļā **Mani izdevumi: naudas avansi**. 

## <a name="approve-cash-advance-requests"></a>Naudas avansa pieprasījumu apstiprināšana

Vadītāji vai lietotāji, kas darbplūsmā konfigurēti kā apstiprinātāji, var apstiprināt naudas avansus, kas tiem iesniegti izskatīšanai. 

1. Lai apstiprinātu naudas avansu, sadaļā **Naudas avansu apstrāde** atlasiet vienumu **Naudas avansi manai izskatīšanai**.
2. Atlasiet naudas avansu, kas jums ir jāizskata, un atlasiet **Apstiprināt**.  

## <a name="pay-cash-advances"></a>Naudas avansu izmaksa 
Šo procedūru parasti izpilda grāmatvedis vai lietotājs ar grāmatvedības atļaujām.

1. Lai grāmatotu apstiprinātos naudas avansus, atlasiet vienumu **Apstiprinātie naudas avansi** un pēc tam atlasiet vienumu **Apmaksāt un pārsūtīt**.  
2. Norādiet žurnāla informāciju par naudas avansiem un pēc tam atlasiet **Labi**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Izdevumu atskaites iesniegšana par izmaksātu naudas avansu 

Kad izveidojat un iesniedzat izdevumu atskaiti par jau saņemtu naudas avansu, izdevumi tiek automātiski pielāgoti atbilstoši šim avansam. Ja jūsu saņemtais naudas avanss pārsniedz izdevumu summu, jums ir jāatgriež starpība uzņēmumam, izmantojot izmaksu kategoriju **Atgriezt naudu**. Ja uzņēmumam izmaksātais naudas avanss ir mazāks par izdevumu summu, uzņēmumam ir jāatlīdzina jums starpība. 

### <a name="example"></a>Piemērs
Jūs plānojat doties uz konferenci no Sietlas uz Ņujorku. Jūs izveidojat naudas avansa pieprasījumu par 3000,00 USD, jo esat aprēķinājis, ka konferenču biļetes, lidojumu, viesnīcu, ēdināšanas un taksometru izmaksu kopējā summa būs aptuveni šāda. Jums netiks izmaksāts avanss, ja jūsu vadītājs nebūs apstiprinājis šo pieprasījumu. Pēc jūsu vadītāja apstiprinājuma pieprasītais naudas avanss tiek izmaksāts kā 3000,00 USD jūsu bankas kontā. Pēc tam jūs apmeklējat konferenci. Pēc ceļojuma beigām jūs konstatējat, ka kopējie izdevumi ir tikai 2790,00 USD. Atlasiet vienumu **Nauda** laukā **Maksāšanas metode** un iesniedziet izdevumus par 2790,00 USD. Jūsu iesniegtā izdevumu summa tiek automātiski salīdzināta ar naudas avansa summu 3000,00 USD, kas jums tika aizdota. Tagad jūs esat parādā starpību 210,00 USD (3000,00-2790,00) apmērā uzņēmumam, ko var atgriezt uzņēmumam, izmantojot izdevumu kategoriju **Atgriezt naudu**. 
