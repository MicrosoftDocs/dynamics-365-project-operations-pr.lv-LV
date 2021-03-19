---
title: Starpuzņēmumu rēķinu izrakstīšanas pārskats
description: Šajā tēmā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287337"
---
# <a name="intercompany-invoicing-overview"></a>Starpuzņēmumu rēķinu izrakstīšanas pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Jūsu organizācijā var būt vairākas nodaļas, meitasuzņēmumi un citas juridiskas personas, kas pārsūta produktus un pakalpojumus cita citai projektu ietvaros. Juridiskā persona, kas nodrošina pakalpojumu vai produktu, tiek saukta par *aizdevuma juridisko personu*. Juridiskā persona, kas saņem pakalpojumu vai produktu, tiek saukta par *aizņēmuma juridisko personu*.

Tālāk sniegtajā ilustrācijā ir parādīts tipisks scenārijs, kurā divas juridiskās personas, Contoso Robotics USA (aizņēmuma juridiskā persona) un Contoso Robotics UK (aizdevuma juridiskā persona) koplieto resursus, lai nodrošinātu projektu klientam Adventure Works. Šajā scenārijā uzņēmums Contoso Robotics USA ir noslēdzis līgumu, lai izpildītu klientam Adventure Works piegādājamo darbu.

![Starpuzņēmumu rēķinu izrakstīšana](./media/IntercompanyScenario.png) 

Programmā Dynamics 365 Project Operations tiek izmantota tālāk aprakstītā starpuzņēmumu darbību apstrādes plūsma.

1. Resursi no aizņēmuma juridiskās personas reģistrē starpuzņēmumu laika vai izdevumu darbības, grāmatojot laiku un izdevumus aizņēmuma juridiskās personas projektos.
2. Laika un izdevumu izmaksas aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.
3. Starpuzņēmumu rēķinā neiekļautās pārdošanas darbības aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.
4. Rēķinā neiekļautie ieņēmumi tiek reģistrēti aizņēmuma uzņēmumā, izmantojot projekta līguma pārdošanas cenrādi. Klientam rēķinu var izrakstīt, kad ir reģistrēti rēķinā neiekļautie ieņēmumi. Klientam nav jāgaida, kamēr tiek pabeigta starpuzņēmumu rēķinu apstrāde.
5. Starpuzņēmumu klientu rēķini tiek periodiski izveidoti aizdevuma uzņēmumā. Rēķini tiek izveidoti manuāli vai izmantojot periodisku, automatizētu procesu. Var izveidot vienu rēķinu katrai aizņēmuma juridiskajai personai vai arī var izveidot atsevišķus rēķinus projektiem.
6. Kad aizdevuma juridiskajā personā tiek grāmatots starpuzņēmumu klienta rēķins, aizņēmuma juridiskajā personā tiek izveidots atbilstošais gaidošais piegādātāja rēķins. Izmaksas gaidošajā piegādātāja rēķinā tiks reģistrētas projekta apakšgrāmatā, kad būs iegrāmatots rēķins.

Tālāk sniegtajā diagrammā ir parādīta starpuzņēmumu rēķinu izrakstīšana saistībā ar uzskaites notikumiem un paredzētajiem grāmatojumiem virsgrāmatā.

![Starpuzņēmumu plūsma](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Papildu resursi

- [Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana](configure-intercompany-invoicing.md)
- [Starpuzņēmumu darbību reģistrēšana](create-intercompany-transactions.md)
- [Starpuzņēmumu klientu un piegādātāju rēķinu izveide](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]