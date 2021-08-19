---
title: Naudas avanss
description: Šajā tēmā ir sniegta informācija par naudas avansiem.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988525"
---
# <a name="cash-advance"></a>Naudas avanss

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Naudas avanss ļauj darbiniekiem aizņemties naudu no uzņēmuma pirms jebkādu izdevumu rašanās. Kad tiek apstiprināts un izmaksāts pieprasītais naudas avanss, darbinieks var izmantot šo naudu, lai segtu uzņēmuma izdevumus, kas tam varētu rasties. 

## <a name="create-and-submit-a-cash-advance-request"></a>Naudas avansa pieprasījuma izveide un iesniegšana
Lai izveidotu jaunu skaidras naudas avansu un skaidras naudas avansa pieprasījumu, veiciet šādas darbības: 

1. Sadaļā **Mani izdevumi** atlasiet **Skaidras naudas avansi** > **Jauns**. 
2. Lapā **Jauns naudas avansa pieprasījums** ievadiet izdevumu mērķi un atlasiet vietu, kurā radīsies izdevumi.
3. Ievadiet pieprasīto summu un valūtu un pēc tam atlasiet vienumu **Saglabāt**. 
4. Kad esat gatavs iesniegt naudas avansa pieprasījumu, lapā **Naudas avansa pieprasījums** atlasiet vienumu **Darbplūsma** > **Iesniegt**.

## <a name="modify-a-cash-advance-request"></a>Naudas avansa pieprasījuma modificēšana

Ja naudas avansa pieprasījums nav iesniegts apstiprināšanai, jūs varat to modificēt.

1. Sadaļā **Mani izdevumi: skaidras naudas avansi** atrodiet un atlasiet to skaidras naudas avansu, kuru vēlaties rediģēt.
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

Izveidojot un iesniedzot jau saņemta skaidras naudas avansa atskaiti, izdevumi tiks automātiski pielāgoti atbilstoši šim avansam. Ja jūsu saņemtais naudas avanss pārsniedz izdevumu summu, jums ir jāatgriež starpība uzņēmumam, izmantojot izmaksu kategoriju **Atgriezt naudu**. Ja uzņēmuma izmaksātais skaidras naudas avanss ir mazāks par jūsu izdoto summu, uzņēmumam jums ir jāatlīdzina bilance. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Atlasiet saviem izdevumiem piemērotu naudas avansu
Pirms izdevumu atskaites iesniegšanas varat atlasīt naudas avansu, kas atbilst atskaitē iekļautajiem izmaksu darījumiem. Lai izmantotu šo funkcionalitāti, darbvietā **Līdzekļu pārvaldība** ir jāiespējo divi līdzekļi:

  - Atjaunotas izdevumu atskaites
  - Spēja kartēt naudas avansu izdevumu rindām
 
 Ja ir iespējoti šie līdzekļi:
 
  - Katrai izdevumu rindai varat pievienot vienu vai vairākus naudas avansus.
  - Pieejamā naudas avansa bilance ir redzama reāllaikā, kad tiek saglabāta izdevumu atskaite. Tas ļauj vienlaikus apstrādāt izdevumu transakcijas un atgriezt naudas transakciju.
  - Vienai izdevumu transakcijai varat atlasīt vairākus naudas avansus.
  - Izmantojot vaicājumu, ir pieejami naudas avansa saskaņošanas dati. 
 
Ja neizmantojat šos līdzekļus, funkcionalitāte nemainīsies, esošos naudas avansus automātiski samazinot pēc izdevumu atskaites iesniegšanas.

### <a name="example"></a>Piemērs 
Jūs plānojat doties no Sietlas uz Ņujorku, lai apmeklētu konferenci. Jūs izveidojat skaidras naudas avansa pieprasījumu par 3000,00 USD, balstoties novērtētajās izmaksās par konferences biļeti, lidojumiem, viesnīcu, maltītēm un taksometru. Jums netiks samaksāts, kamēr vadītājs neapstiprinās šo pieprasījumu. Pēc jūsu vadītāja apstiprinājuma pieprasītais naudas avanss tiek izmaksāts kā 3000,00 USD jūsu bankas kontā. Pēc tam jūs apmeklējat konferenci. Pēc ceļojuma beigām jūs konstatējat, ka kopējie izdevumi ir tikai 2790,00 USD. Laukā **Maksājuma metode** atlasiet **Skaidrā naudā** un iesniedziet savus izdevumus 2790,00 USD apmērā. Jūsu iesniegtā izdevumu summa tiek automātiski salīdzināta ar naudas avansa summu 3000,00 USD, kas jums tika aizdota. Tagad jūs esat parādā bilanci 210,00 USD (3000,00-2790,00) apmērā, kuru varat atgriezt uzņēmumam, izmantojot izdevumu kategoriju **Atgriezt skaidro naudu**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
