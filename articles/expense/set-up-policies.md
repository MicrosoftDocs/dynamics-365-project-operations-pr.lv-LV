---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001885"
---
# <a name="define-expense-policies"></a>Izdevumu politiku definēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.         
Izdevumu politiku ieviešana var palīdzēt efektīvi pārvaldīt izdevumus.         

Piemēram, varat iestatīt politiku viesnīcas izdevumiem Ņujorkā, kuri nosaka, ka izdevumi par nakti nedrīkst pārsniegt 250 USD.       
Ja darbinieks iesniedz izdevumu atskaiti vai komandējuma pieprasījumu, kurā numura likme pārsniedz šo summu sistēma paziņos         
darbiniekam, ka ir pārsniegta izdevumu politikas summa. Varat konfigurēt ziņojumu, kuru darbinieks saņems, kad        
definēsit politiku.      
        
Varat definēt triju veidu politikas:         
        
- **Brīdinājums**: Ļauj darbiniekam iesniegt izdevumu atskaiti vai komandējuma pieprasījumu, taču izdevumi tiks atzīmēti visiem apstiprinātājiem un         
  vēlākai ziņošanai.        

- **Kļūda**: Darbiniekam ir jāpārskata izdevumi, lai tie atbilstu politikai, pirms viņš iesniedz izdevumu atskaiti vai komandējuma pieprasījumu.        
 
 - **Pamatojums**: Darbiniekam vai vadītājam ir jāievada pamatojums politikas apmēra pārsniegšanai, pirms tiek iesniegta izdevumu atskaite vai komandējuma pieprasījums.        

## <a name="policy-tips"></a>Politikas padomi
Tālāk sniegti daži ierosinājumi, kas var jums palīdzēt, veidojot jaunas izdevumu pārvaldības politikas: 

- Politikām ir spēkā stāšanās datums, kas nozīmē, ka tās nestāsies spēkā, ja tiks izveidotas datumā, kas ir vēlāks par datumu, kad radās izdevumi. Piemēram, jūs izveidojat jaunu politiku šodien, lai noteiktu, ka maksimālie maltīšu izdevumi ir 50$. Jebkuri izdevumi, kas ievadīti no vakardienas, netiks pārbaudīti attiecībā pret šo politiku.
- Veidojot politiku izdevumu kategorijai, kuru nevar uzskaitīt, apsveriet pievienot izdevumu rindas veida nosacījumu. Dažas politikas, piemēram, nepieciešamība pēc kvīts, var nebūt loģiskas attiecībā uz uzskaitītajām rindām. Šādā gadījumā politika tiek piemērota vienīgi virsraksta rindai vai neuzskaitītajai rindai. 
- Izdevumu pārvaldības politikas pēc noklusējuma tiek novērtētas attiecībā pret avota entitīju. Starpuzņēmumu scenārijos varat iestatīt, ka politika tiek novērtēta attiecībā pret mērķa entitīju (aizņēmuma entitīju). Lai palaistu politiku pret mērķa entitīju, ieslēdziet līdzekli **Novērtēt Izdevumu politiku attiecībā pret aizņēmuma juridisko personu** darbvietā **Līdzekļu pārvaldība**.

## <a name="when-to-evaluate-policies"></a>Kad novērtēt politikas

Izdevumu pārvaldības parametros varat atlasīt izvērtēt izdevumu pārvaldības politikas, ja tiek saglabāta rinda vai ja tiek iesniegta izdevumu atskaite. Ja izvēlaties izvērtēt, kad rinda tiek saglabāta, lietotajiem būs agrāka redzamība par to, kas viņiem ir jādara, lai vienlaikus aizpildītu visu izdevumu atskaiti. Pretējā gadījumā varat aizkavēt politikas novērtējumu un ietaupīt laiku beigās, iesniedzot darbplūsmā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]