---
title: Pārdošanas tāmes un projekti
description: Šajā tēmā ir sniegta informācija par to, kā pārdošanas procesā izdevīgi izmantot plānošanu un tāmes.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753464"
---
# <a name="sales-estimates-and-projects"></a>Pārdošanas tāmes un projekti

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pārdošanas procesa laikā varat izveidot pārdošanas tāmes, sasaistot projektu un pārdošanas piedāvājumu. Šādi pārdošanas procesa laikā var rasties deterministisks novērtējums, lai izmantotu projekta plānošanas un tāmes noteikšanas iespējas. Ja pārdošanas darījums ir sekmīgs, pārdošanas tāmes vajadzībām izmantoto grafiku var izmantot kā pamatu turpmākai projekta plāna pilnveidošanai.

## <a name="linking-a-project-to-a-quote-line"></a>Projekta saistīšana ar piedāvājuma rindu

Kad izveidojat uz projektu balstītu piedāvājuma rindu, varat izveidot jaunu projektu vai saistīt jau esošu projektu lapā **Piedāvājuma rinda**. 

> ![Piedāvājuma rindas veidlapa](media/project-8.png)
 
Kad no piedāvājuma rindas informācijas veidojat jaunu projektu, varat izdevīgi izmantot projektu veidnes. Projektu veidnes ir modeļa projekti, kas pārstāv standarta projektu plānus un finanšu tāmes, kādas organizācijai ir tipiskas. Tās var pārstāvēt arī projektu plānu kopijas un tāmes no iepriekšējiem projektiem.

> ![Piedāvājuma rindas detaļas](media/project-9.png)
  
Kad projektu veidojat no piedāvājuma, šis projekts automātiski tiek saistīts ar piedāvājuma rindu.

## <a name="components-of-estimates-in-a-project"></a>Tāmju komponenti projektā

Grafiks ļauj jums sadalīt darbu uzdevumos, uzturēt uzdevumu hierarhiju, noteikt, kādi resursi ir nepieciešami uzdevuma izpildīšanai, un piešķirt piepūles tāmi, kas ir nepieciešama uzdevuma izpildīšanai.

Darba piepūli un grafika tāmes varat definēt, izmantojot laukus lapas **Projekts** cilnē **Grafiks**. Tā kā cenrādis ir saistīts ar projektu, finanšu tāmes tiek aprēķinātas, izmantojot cenrādī definētās izmaksas un pārdošanas cenas.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Tāmju importēšana no projekta uz piedāvājumu

Pēc projekta tāmju definēšanas varat tās importēt uz piedāvājuma rindu. Lapas **Piedāvājuma rindas informācija** lentē atlasiet vienumu **Importēt no tāmēm**, lai izveidotu projekta tāmju kopsavilkumu pēc transakcijas tipa, lomas vai uzdevuma līmeņa.
