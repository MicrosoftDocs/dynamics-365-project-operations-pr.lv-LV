---
title: Resursu pārvaldības režīma pārskats
description: Šajā tēmā ir sniegta informācija par resursu pārvaldību risinājumā Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000895"
---
# <a name="resource-management-modes-overview"></a>Resursu pārvaldības režīmu pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Dynamics 365 Project Operations atbalsta divus režīmus, lai jūs varētu izpildīt kopējo rezervācijas plūsmu. Pārvaldības režīms tiek definēts kā projekta parametrs, un to var modificēt, ja jūsu uzņēmumam ir nepieciešamas izmaiņas.    

## <a name="central-mode"></a>Centrālais režīms
Organizācijām, kas centralizē resursu piešķiršanu projektiem, centrālais režīms nodrošina veidu, kā projekta vadītāji var definēt resursu prasības projekta līmenī. Resursu prasību izpilde tiek deleģēta resursu pārvaldniekam. Projekta vadītāji var pieņemt vai noraidīt resursus, ko piedāvā resursu pārvaldnieks.

![Centrālais režīms](./media/resource-management-central.png)

Lai pārvaldītu resursus, izmantojot centrālo režīmu, skatiet:

- [Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervēt nosauktos resursus no resursu vajadzībām](/dynamics365/project-service/book-named-resource)
- [Resursa pieprasījuma iesniegšana](/dynamics365/project-service/submit-resource-request)
- [Resursa pieprasījuma izpilde](/dynamics365/project-service/resource-management-fulfill-requests)
- [Piedāvātā projekta resursa pieņemšana vai noraidīšana, izmantojot resursa pieprasījumu](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibrīda režīms
Organizācijām, kurām ir nepieciešama elastība attiecībā uz resursu piešķiršanu, hibrīda režīms sniedz iespēju gan projekta vadītājiem, gan resursu pārvaldniekiem rezervēt resursus.

![Hibrīda režīms](./media/resource-management-hybrid.png)

Papildus atbalstītajam centrālā režīma procesam skatiet šīs tēmas, lai pārvaldītu visas citas atbalstītās rezervācijas plūsmas hibrīda režīmā:

Resursa rezervēšana tieši projektam:
- [Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana](/dynamics365/project-service/assign-named-bookable-resource)

Resursa rezervēšana no resursa prasības:
- [Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervēt nosauktos resursus no resursu vajadzībām](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]