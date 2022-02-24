---
title: Jaunumi 2021. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada februāra laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8270214d47f712cdb0942991b0ffb5baff64cbfb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948023"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. februārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vidē 4.7.0.95
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.16 

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| **Cenu noteikšana un norēķini** | 2053736 | Rēķina rindas informācijai tagad var piekļūt, dodoties uz **Rēķins** > **Saistīta informācija**. |
| **Cenu noteikšana un norēķini** | 2122613 | No **Cenu saraksta** saistītajām entitījām tika noņemtas darbības **Aktivizēt** un **Deaktivizēt**. |
| **Cenu noteikšana un norēķini** | 2128606 | Atrisināta problēma ar **ullReferenceException** spraudnī **GetEstimatesForProject** . |
| **Izvietošana un konfigurācija** | 2139346 | Atrisiniet problēmu, importējot nepārvaldīto lēmumu **Dynamics365ProjectOperationsDualWrite**. |
| **Izvietošana un konfigurācija** | 2140569 | Projekta risinājumu nedrīkst instalēt Dataverse Teams vidēs. |
| **Izvietošana un konfigurācija** | 2086991 | Ierobežota tīmekļu resursu pielāgošanas lokalizācija. |
| **Iespēju pārvaldība** | 2136794 | Rādiet pareizo kļūdas ziņojumu, kad neizdodas process **Apstiprināt rēķinu** vai **Atzīmēt rēķinu kā apmaksātu**. |
| **Iespēju pārvaldība** | 2139330 | Mainot projekta vadītāju vai projektu, nedrīkst atiestatīt īpašnieku uzņēmumu atpakaļ uz noklusējuma vērtību. |
| **Iespēju pārvaldība** | 2146376 | Izlabota nodokļu summa rēķinā neiekļaujamā faktiskajā summā tiek izveidota no rēķina apstiprinājuma. |
| **Projektu plānošana un izsekošana** | 2099879 | Dataverse vides izvietošanai jāizveido noklusējuma transakcijas kategorija ar statisku ID, nevis nejauši tas jāģenerē katrai videi. |
| **Projektu plānošana un izsekošana** | 2128577 | Izlabotas projekta pakalpojumu lietotāju privilēģijas, lai resursa piešķirē atjauninātu transakcijas kategoriju. |
| **Projektu plānošana un izsekošana** | 2164035 | Novērstas problēmas ar funkciju **Kopēt projektu**. |
| **Laika ieraksts** | 2129161 | Ir piemēroti stingrāki ierobežojumi, lai nodrošinātu, ka lietotāji nevar mainīt un atjaunināt laika ierakstu, kas ir iesniegts vai apstiprināts. |
| **Laika ieraksts** | 2103572 | Laika apstiprināšanai ar projektu nesaistītiem laika ierakstiem nav nepieciešama projekta apstiprinātāja loma. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Dynamics 365 Finance 

Papildinformāciju par projektu pārvaldību un grāmatvedību programmā Dynamics 365 Finance skatiet tēmā [Jaunumi 2021. gada februārī — Project Operations resursu/nekrājumu scenārijiem](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Vēl viens veids, kā uzzināt par regulatīviem atjauninājumiem, ir pieteikties pakalpojumā Lifecycle Services (LCS) un apskatīt plānotos regulatīvos atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]