---
title: Projekta iespēju kopēšana
description: Šajā tēmā ir sniegta informācija par projekta iespēju kopēšanu risinājumā Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83fe41cb16be6bdd91219fc59e517ae0e5848afec5f771edde575bb5c24f9865
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999730"
---
# <a name="copy-project-based-opportunities"></a>Projekta iespēju kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Projekta iespējas var vienkārši kopēt, lai izveidotu jaunas projekta iespējas. 

1. Atveriet lapu **Projekta iespēju** saraksts un atlasiet iespēju sarakstā. Vai atveriet noteiktas iespējas detalizētās informācijas lapu. 
2. Jebkurā no lapām atlasiet **Kopēt**. Tiks atvērta dialoga lapa, kurā ir šāda lauka informācija. Atkarībā no dialogā atlasītajām vērtībām kopēšanas process var mainīties.

    | **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
    | --- | --- | --- |
    | Tēma | Ievadiet mērķa iespējai atbilstošu tēmu. Kad tiek atvērts dialogs, sistēma to iestata uz to avota iespējas tēmu, kam pievienots **-copy**. | Šim laukam nav lejupstraumes ietekmes. |
    | Konts | Atsauces uz klienta uzņēmuma vai konta ierakstu. Kad tiek atvērts dialogs, sistēma to iestata uz avota iespējas uzņēmumu. | Šis lauks ir iespējas primārais klients. |
    | Līgumslēdzēja vienība | Organizācijas vienība, kas atbild par ar šo darījumu saistīto projektu nodrošināšanu. Kad tiek atvērts dialogs, sistēma to iestata uz avota iespējas līgumslēdzēja vienību. | Līgumslēdzēja vienība ir uzņēmuma nodaļa, kas izpildīs projektus pēc darījuma slēgšanas. Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas. |
    | Valūta | Valūta, kādā notiek šī piedāvājuma darījumi. Kad tiek atvērta dialoga lapa, sistēma to iestata uz avota iespējas valūtu. | Valūta tiek izmantota atjaunotu cenrāža noklusējuma vērtības un veidotu piedāvājuma tāmju aprēķinu. Galu galā valūta tiek izmantota, lai klientam izrakstītu rēķinu, kad ir iegūts darījums. |
    | Kopēt izcenojumu | Vērtība Jā/Nē, kas norāda, vai iespējas cenas ir jākopē no avota iespējas. | Ja ir atlasīta vērtība **Jā**, cenrāži tiek kopēti no avota uz mērķa iespēju. Ja ir atlasīta vērtība **Nē**, cenrāžu noklusējuma vērtības tiek noteiktas, pamatojoties uz jaunākajiem cenrāžiem, kas tika iestatīti. |

3. Atlasiet **Labi**. Sistēma izveido projekta iespējas kopiju, kuras pamatā ir atlasītie parametri, un tiek atvērta jaunā projekta iespēja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]