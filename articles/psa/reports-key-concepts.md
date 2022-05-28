---
title: Galvenie jēdzieni
description: Šajā tēmā ir sniegta informācija par galvenajiem resursu pārvaldības jēdzieniem programmā Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3a0305ab35a28348798f9d9c7452b3bee75412e4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601257"
---
# <a name="key-concepts"></a>Galvenie jēdzieni

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
