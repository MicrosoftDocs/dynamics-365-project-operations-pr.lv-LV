---
title: Starpuzņēmumu rēķinu izrakstīšanas pārskats
description: Šajā tēmā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002650"
---
# <a name="intercompany-invoicing-overview"></a>Starpuzņēmumu rēķinu izrakstīšanas pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Jūsu organizācijā var būt vairākas nodaļas, meitasuzņēmumi un citas juridiskas personas, kas pārsūta produktus un pakalpojumus cita citai projektu ietvaros. Juridiskā persona, kas nodrošina pakalpojumu vai produktu, tiek saukta par *aizdevuma juridisko personu*. Juridiskā persona, kas saņem pakalpojumu vai produktu, tiek saukta par *aizņēmuma juridisko personu*.

Nākamajā attēlā parādīts tipisks scenārijs, kad divas juridiskās personas, Contoso Robotics USA (aizņemošā juridiskā persona) un Contoso Robotics UK (aizdodošā juridiskā persona), koplieto resursus klienta Adventure Works projekta izpildei. Šajā scenārijā Ir noslēgts līgums ar Contoso Robotics USA, lai izpildītu darbu Adventure Works.

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