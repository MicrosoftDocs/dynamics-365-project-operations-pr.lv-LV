---
title: Projekta kategoriju iestatīšana
description: Šajā tēmā ir sniegta informācija par projekta kategoriju iestatīšanu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080340"
---
# <a name="configure-project-categories"></a>Projekta kategoriju iestatīšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Project Operations nodrošina robustas ieņēmumu un izdevumu kategorizācijas iespējas projektiem. Kategorijas nodrošina iespēju ziņot par projekta darījumiem un tos analizēt, kā arī vadīt grāmatošanu virsgrāmatā.

Tālāk sniegtajā shēmā parādīta korelācija starp darījumu kategorijām, koplietojamām kategorijām un projekta kategorijām. 

Darījumu kategorijas ir projekta darījumu pamata grupas. Šajās grupās ir koplietojamu kategoriju kopums, ko var kopīgot programmās un moduļos. Konkrētāk — projekta kategorijas ir detalizētākais kategoriju līmenis. Projekta kategorijas ir noteiktas konkrētai juridiskai personai, modulim un programmai.

![Korelācija starp darījumu kategorijām, koplietojamām kategorijām un projekta kategorijām](media/project-categories.png)

## <a name="transaction-categories"></a>Transakcijas kategorijas

Darījumu kategorijas ataino projekta darījumu pamatgrupas, un tās neattiecas uz konkrētu uzņēmuma vai darījumu veidu. Piemēram, uzņēmums Contoso Robotics" izmanto darījumu kategorijas Projektēšana, Ceļojumi, Uzstādīšana un Apkope, kurās grupē Projekta darījumus.

Darījumu kategorijas tiek definētas Project Operations modulī. 
1. Lai atvērtu veidlapu, dodieties uz **Iestatījumi** \> **Darījumu kategorijas**. 
2. Izveidojiet jaunu darījumu kategoriju, atlasot vienumu **Jauns** vai atlasot **Importēt no Excel**.

## <a name="shared-categories"></a>Koplietotās kategorijas

Dynamics 365 izmanto Koplietoto kategoriju koncepciju, lai kategorizētu izdevumus dažādās programmās, piemēram, Dynamics 365 Finance, Dynamics 365 Supply Chain un Dynamics 365 Project Operations. Katrai izveidotajai Darījumu kategorijai Project Operations automātiski izveido četras saistītas Koplietotās kategorijas: Stundas, Izdevumi, Maksas un Vienums. Varat pārskatīt un pielāgot koplietotās kategorijas, atverot **Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Koplietotās kategorijas**.

## <a name="project-categories"></a>Projektu kategorijas

Projekta kategorijas ir detalizētākais kategoriju konfigurācijas līmenis, un tās ir jākonfigurē Projekta grāmatvedim atsevišķi un katram uzņēmumam individuāli.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Projekta kategorijas**.
2. Atlasiet **Jauns**.
3. Atlasiet tās Koplietotās kategorijas **Kategorijas ID** , ko izveidojāt iepriekšējā sadaļā. Project Operations ļauj izmantot tikai tās koplietotās kategorijas, kas ir saistītas ar darījumu kategorijām.
4. Atlasiet kategoriju grupu.

## <a name="category-groups"></a>Kategoriju grupas

Kategoriju grupas izmanto, lai kopīgotu rekvizītus, galvenokārt grāmatošanas profilus, starp saistītām Projekta kategorijām. Katram darījuma veidam ir jābūt vismaz vienai kategoriju grupai, un katrai projekta kategorijai ir piešķirta grupa.

Grāmatojumu specifikācijas risinājumā Project Operations tiek definētas, izmantojot projekta izmaksu un ieņēmumu profila kārtulas, projekta kategorijas +un kategoriju grupas. Kategoriju grupas varat iestatīt, dodoties uz sadaļu **Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Kategoriju grupas**.
