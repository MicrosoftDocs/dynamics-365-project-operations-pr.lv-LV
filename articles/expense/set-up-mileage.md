---
title: Nobraukuma iestatīšana, izmantojot nobraukuma likmes pakāpes
description: Šajā tēmā ir sniegta informācija par nobraukuma likmēm un nobraukuma likmju pakāpēm.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083680"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Nobraukuma iestatīšana, izmantojot nobraukuma likmes pakāpes

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Kad tiek ziņots par izdevumiem un atlasītā izdevumu kategorija ir **Nobraukums**, šīs izdevumu rindas summa tiek aprēķināta atbilstoši *nobraukuma likmes* summai. Šo summu nosaka, izmantojot definētās nobraukuma pakāpes, vai, ja nobraukuma pakāpes nav iestatītas, lietojot standarta nobraukuma likmi. 

Nobraukuma likmju pakāpes var iestatīt, dodoties uz **Izdevumu pārvaldība** > **Iestatīšana** > **Vispārīgi** > **Izdevumu kategorijas** > **Nobraukums** > **Kategorijas iestatīšana**.

Ja jūsu organizācija izmanto nobraukuma izdevumu kategoriju, pārskatiet tālāk izklāstītās dizaina izmaiņas un pēc jaunināšanas uz versiju 10.0.18 apsveriet nobraukuma līdzekļa iespējošanu. 

Jaunais nobraukuma likmju pakāpju dizains ietekmē, kā tiek apstrādāta lauka **Daudzums** vērtība. Pirms 10.0.18 izlaišanas vērtība laukā **Daudzums** tika uzskatīta par apakšējo robežu. Ja uzkrātā summa pārsniedza šo vērtību, tika izmantota atbilstošā likme.  Sākot ar versiju 10.0.18, lauka **Daudzums** vērtība tiek uzskatīta par augšējo robežu. Atbilstošā likme tiek lietota tad, kad uzkrātā nobraukuma vērtība ir mazāka nekā vērtība laukā **Daudzums**.  Jaunais nobraukuma pakāpju modelis palīdz nodrošināt konsekvenci starp dažādām nobraukuma pakāpēm un labāku lietojamību.   

Atbilstoši jaunajam dizainam visas apstiprinātās izdevumu atskaites grāmatošanas laikā tiek pārrēķinātas.

## <a name="example"></a>Piemērs
 
### <a name="before-version-10018"></a>Pirms versijas 10.0.18
Ar divām nobraukuma likmju pakāpēm lauks **Daudzums** katrā pakāpē parāda apakšējo nobraukuma robežu. Pašlaik pirmās pakāpes vērtība ir nulle (0) un likme ir 0,45, bet otrās pakāpes vērtība ir 1000 un likme ir 0,25. Ja uzkrāto jūdžu vai kilometru skaits pārsniedz laukā norādīto vērtību, tiek izmantota saistītā likme. Ja nav rindas ar nulles daudzumu, sistēma izmanto nobraukuma likmi, kas ir definēta izdevumu pārvaldības sadaļā. 
 
Ja darbinieks iesniedz izdevumu atskaiti ar 1500 jūdzēm, abas nobraukuma rindas iegrāmatotajā izdevumu atskaitē būtu šādas: 1000 (likme 0,45) + 500 (likme 0,25) = 575,00.

### <a name="after-version-10018"></a>Pēc versijas 10.0.18
Versijā 10.0.18 lauks **Daudzums** parāda katras likmes augšējo robežu. Pašlaik pirmās pakāpes vērtība ir 999 un likme ir 0,45, bet otrās pakāpes vērtība ir 999 999 999,00 un likme ir 0,25. Ja uzkrāto jūdžu vai kilometru skaits pārsniedz laukā **Daudzums** norādīto vērtību, tiek izmantota saistītā likme. Ja tiek pārsniegtas visas augšējās robežas, sistēma izmanto nobraukuma likmi, kas ir definēta izdevumu pārvaldības sadaļā. 
 
Lai pareizi aprēķinātu to pašu scenāriju, ir jāmaina iestatītā pakāpe. Lauka **Daudzums** vērtība pirmajā likmē ir 999,00, bet otrajā likmē vērtība ir 999 999 999,00. Ja darbinieks pārsniedz kopējo jūdžu vai kilometru daudzumu pirmajā pakāpē, sistēma izmanto nobraukuma likmi, kas ir definēta izdevumu pārvaldības sadaļā. 
  
Ja darbinieks iesniedz izdevumu atskaiti ar 1500 jūdzēm, abas nobraukuma rindas iegrāmatotajā izdevumu atskaitē būtu šādas: 1000 (likme 0,45) + 500 (likme 0,25) = 575.

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Nobraukuma summas aprēķina iespējošana vairākām nobraukuma pakāpēm ar vienu likmi

Līdzeklis **Nobraukuma summas aprēķina iespējošana vairākām nobraukuma pakāpēm ar vienu likmi** uzlabo nobraukuma likmju aprēķinu. Lai iespējotu šo līdzekli, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Darbvietas** > **Līdzekļu pārvaldība**. 
2. Sarakstā atrodiet un atlasiet **Nobraukuma summas aprēķina iespējošana vairākām nobraukuma pakāpēm ar vienu likmi** un pēc tam atlasiet **Iespējot tūlīt**.

Pēc līdzekļa iespējošanas atiestatiet nobraukuma likmes, lai pareizi atspoguļotu lauka **Daudzums** vērtību. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
