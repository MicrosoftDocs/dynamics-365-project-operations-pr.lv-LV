---
title: Izdevumu politiku iestatīšana
description: Varat iestatīt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus risinājumā Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271272"
---
# <a name="set-up-expense-policies"></a>Izdevumu politiku iestatīšana

Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.         
Izdevumu politiku ieviešana var palīdzēt efektīvi pārvaldīt izdevumus.         

Piemēram, varat iestatīt politiku viesnīcas izdevumiem Ņujorkā, kuri nosaka, ka izdevumi par nakti nedrīkst pārsniegt 250 USD.       
Ja darbinieks iesniedz izdevumu atskaiti vai komandējuma pieprasījumu, kur numura likme pārsniedz šo summu, sistēma to paziņos        
darbiniekam, ka ir pārsniegta izdevumu politikas summa. Varat konfigurēt ziņojumu, kuru darbinieks saņems, kad        
definēsit politiku.      
        
Varat definēt triju veidu politikas:         
        
- Brīdinājums — ļauj darbiniekam iesniegt izdevumu atskaiti vai komandējuma pieprasījumu, taču izdevumi tiks atzīmēti visiem apstiprinātājiem un        
  vēlākai ziņošanai.        

- Kļūda — darbiniekam ir jāpārskata izdevumi, lai tie atbilstu politikai, pirms viņš iesniedz izdevumu atskaiti vai komandējuma pieprasījumu.       
 
 - Pamatojums — darbiniekam vai vadītājam ir jāievada pamatojums politikas apmēra pārsniegšanai, pirms tiek iesniegta izdevumu atskaite vai komandējuma pieprasījums.        

## <a name="policy-tips"></a>Politikas padomi
Tālāk sniegti daži ierosinājumi, kas var jums palīdzēt, veidojot jaunas izdevumu pārvaldības politikas. 
* Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiks izveidota ar datumu pēc izdevumu rašanās datuma. Piemēram, ja šodien izveidojat jaunu politiku, lai īstenotu 50 ASV dolāru vērtus maksimālo maltīšu izdevumus, tad jebkādas no vakardienas esošām izmaksām netiks pārbaudītas attiecībā pret šo politiku.
* Veidojot politiku izdevumu kategorijai, kuru nevar uzskaitīt, apsveriet pievienot izdevumu rindas veida nosacījumu. Dažas politikas, piemēram, ieejas plūsmas pieprasīšana, var nebūt noderīgas detalizētām rindām, un tās ir jālieto tikai galvenes rindai vai neiekļautai rindai. 
* Izdevumu pārvaldības politikas pēc noklusējuma tiek novērtētas attiecībā pret avota entitīju. Starpuzņēmumu scenārijos varat iestatīt, ka politika tiek novērtēta attiecībā pret mērķa entitīju (aizņēmuma entitīju). Lai palaistu politiku pret mērķa entītīju, ieslēdziet līdzekli “Novērtēt Izdevumu politiku attiecībā pret aizņēmuma juridisko entītiju” darbvietā **Līdzekļu pārvaldība**.

## <a name="when-to-evaluate-policies"></a>Kad novērtēt politikas

Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad tiek saglabāta rinda vai tiek iesniegts izdevumu pārskats. Ja izvēlaties novērtēt, kad tiek saglabāta rinda, tiek nodrošināts, ka lietotājiem ir iepriekš redzama informācija par to, kas jādara, lai pabeigtu izdevumu pārskatu visu uzreiz. Pretējā gadījumā var aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija notiek beigās, iesniegšanas darbplūsmā laikā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]