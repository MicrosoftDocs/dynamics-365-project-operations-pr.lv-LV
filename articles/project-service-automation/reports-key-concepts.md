---
title: Galvenie jēdzieni
description: Šajā tēmā ir sniegta informācija par galvenajiem resursu pārvaldības jēdzieniem programmā Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f5f96f65-c191-493a-aef7-df7deb52a9cb
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4a839b828d5e1da1e5a8d8a378197b3d4932e529
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753541"
---
# <a name="key-concepts"></a>Galvenie jēdzieni

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nākamajā tabulā ir definēti galvenie jēdzieni, kas tiek izmantoti Dynamics 365 Project Service Automation programmā.

| Jēdziens                    | Definīcija |
|----------------------------|------------|
| Projekta darba grupas dalībnieks        | Projekta darba grupas dalībnieks ir kā daļa no projekta darba grupas, un tas var būt nosaukts resurss, kam ir rezervācijas, nosaukts resurss, kam nav rezervāciju, vai vispārējs resurss. Vispārējiem resursiem nav rezervāciju, tie projektam ir lokāli, un tiem nav noslodzes ierobežojumu dažādos projektos. |
| Projekta vispārējais resurss   | Resursa vietturis, kas ļauj jums veidot darba grupu un komplektēt personālu projekta plānam bez nepieciešamības zināt nosaukto resursu. Projekta kalendārs tiek izmantots kā vispārējais resursu kalendārs. Vispārējos resursus var pievienot projekta darba grupai un piešķirt uzdevumiem. |
| Rezervētās stundas               | Resursu stundas projektam tiek stingri rezervētas, lai palīdzētu garantēt, ka projekta darbs tiek izpildīts. Rezervētās stundas tiek patērētas no resursa vispārējās noslodzes. Rezervācijas tiek veiktas tikai nosauktajiem resursiem, bet ne vispārējiem resursiem. |
| Piešķirtās stundas             | Resursu stundas tiek piešķirtas uzdevumiem projekta grafikā. Piešķires var būt gan nosauktajiem resursiem, gan vispārējiem resursiem. Piešķires var būt neatkarīgas no rezervācijām. |
| Nepieciešamās stundas             | Noslodze, kas ir nepieciešama, bet kas vēl nav izpildīta ar nosaukto resursu. Nepieciešamās stundas attiecas tikai uz vispārējiem darba grupas dalībniekiem, kuriem ir ģenerētas resursu vajadzības. |
| Pieprasījums                     | Pašreizējā un ienākošā darba slodze. Programmā Project Service Automation pieprasījums tiek rādīts kā resursu vajadzības vai resursu pieprasījumi. |
| Resursu prasība       | Entītija, kas tiek izmantota, lai nepieciešamajiem resursiem tvertu nepieciešamās stundas, sākuma un beigu datumus, prasmes, ģeogrāfiju un citas cenu noteikšanas dimensijas. Resursu vajadzības vai nu tiek ģenerētas no projekta darba grupas dalībniekiem, vai tiek izveidotas atsevišķi. |
| Resursu pieprasījums           | Entītija, kas tiek izmantota kā “aploksne”, lai nodotu resursu vajadzību, kura resursu pārvaldniekam ir jāizpilda. |
| Resursa noklusējuma loma      | Loma, kuras grupai resurss tiek piešķirts lietojuma aprēķināšanai. Tiek pieņemts, ka resursam ir šai lomai nepieciešamās prasmes un ka tas atbilst šīs lomas mērķa lietojumam. |
| Resursa organizācijas struktūrvienība | Organizācijas struktūrvienība, kurai šis resurss ir piešķirts. |
| Kontūra                    | Uzdevuma, vajadzības vai piešķires stundas, tās iedalot dienas sadalē. Piemēram, piecu dienu, 40 stundu uzdevumu var konturēt uz astoņām stundām dienā piecu dienu ilgumā. |
| Skats Saskaņošana        | Skats, kurā tiek rādītas rezervācijas un piešķires katram projekta darba grupas dalībniekam. Šis skats ļauj projektu vadītājam meklēt jebkādas neatbilstības starp rezervācijām un piešķirēm, un veikt korekcijas, ja rodas kāda neatbilstība. |
| darba stundas                 | Entītija, kas tiek izmantota, lai identificētu resursu noslodzi, kā arī darba stundas un brīvās stundas. Šī entītija tiek saukta arī par resursu kalendāru. |
