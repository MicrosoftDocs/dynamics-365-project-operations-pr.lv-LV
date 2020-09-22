---
title: Bieži uzdotie jautājumi par resursu pārvaldību
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par resursu pārvaldību.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753537"
---
# <a name="resource-management-faq"></a>Bieži uzdotie jautājumi par resursu pārvaldību

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Kāda ir atšķirība starp darba grupas dalībnieku un resursu vajadzību?

Projekta darba grupas dalībniekam var piešķirt uzdevumus, to var rezervēt, tam var pārsniegt rezervācijas, kā arī to var iestatīt kā apstiprinātāju. Resursa vajadzība var pastāvēt bez projekta darba grupas dalībnieka kā pieprasījuma melnraksts. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Kāda ir atšķirība starp piedāvātajām un viegli rezervētajām stundām?

Piedāvātās stundas un viegli rezervētās stundas atšķiras to redzamības ziņā. Piedāvātās stundas ir redzamas tikai resursu vadītājiem un projektu vadītājam, kas uzsāka pieprasījumu, izmantojot resursa pieprasījumu. Viegli rezervētās stundas ir redzamas ikvienam, kas var piekļūt plānošanas panelim.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kā var redzēt viegli rezervētās stundas resursiem darba grupā?

Vieglās rezervācijas var veikt, rezervējot resursa vajadzību. Resursi, kas ir viegli rezervēti projekta darba grupā, tiek parādīti kā darba grupas dalībnieki, kuriem ir viegli rezervētas stundas. Tie parādās arī plānošanas panelī.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kā mainīt nepieciešamās stundas un sākuma un beigu datumus attiecībā uz resursu (vispārēju vai nosauktu), kuru esmu rezervējis?

Kad resursi ir rezervēti, atlasiet opciju **Uzturēt rezervācijas**, lai veiktu vajadzīgās izmaiņas.

## <a name="what-resources-types-does-project-service-automation-support"></a>Kādus resursu tipus atbalsta Project Service Automation?

**Lietotājs** un **Kontaktpersona** ir vienīgie resursu tipi, kuri tiek atbalstīti programmā Dynamics 365 Project Service Automation. Lai gan var izveidot citus resursu tipus (piemēram, **Aprīkojums** un **Grupa**), tiem netiek atbalstīta visaptveroša lietošana.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Kāda ir atšķirība starp piešķiri un rezervāciju?

Piešķires ir resursu piešķiršana projekta uzdevumiem projekta grafikā. Resursi var būt vai reāli vai vispārēji. Rezervācijas ir resursu stingra vai viegla piešķiršana projektam. Stingrās rezervācijas patērē resursu noslodzi. Ideālā gadījumā attiecībā uz reāliem resursiem rezervācijām būtu jāatbilst piešķirēm, jo tās neatšķiras. Tomēr PSA neparedz obligātu šādu atbilstību. Saskaņošanas skats norāda projekta vadītājiem gadījumus, kad resursu rezervācijas neatbilst piešķirēm.
