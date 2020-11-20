---
title: Resursu pārvaldības režīma pārskats
description: Šajā tēmā ir sniegta informācija par resursu pārvaldības funkcionalitāti programmā Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118527"
---
# <a name="resource-management-modes-overview"></a>Resursu pārvaldības režīma pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Dynamics 365 Project Operations atbalsta divus režīmus, lai jūs varētu izpildīt vispārējo rezervācijas plūsmu. Pārvaldības režīms tiek definēts kā projekta parametrs, un to var modificēt, ja jūsu uzņēmumam ir nepieciešamas izmaiņas.    

## <a name="central-mode"></a>Centrālais režīms
Organizācijām, kas centralizē resursu piešķiršanu projektiem, centrālais režīms nodrošina veidu, kā projekta vadītāji var definēt resursu prasības projekta līmenī. Resursu prasību izpilde tiek deleģēta resursu pārvaldniekam. Projekta vadītāji var pieņemt vai noraidīt resursus, ko piedāvā resursu pārvaldnieks.

![Centrālais režīms](./media/resource-management-central.png)

Lai pārvaldītu resursus, izmantojot centrālo režīmu, skatiet:

- [Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervēt nosauktos resursus no resursu vajadzībām](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Submit a resource request](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Resursa pieprasījuma izpilde](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Piedāvātā projekta resursa pieņemšana vai noraidīšana, izmantojot resursa pieprasījumu](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibrīda režīms
Organizācijām, kurām ir nepieciešama elastība attiecībā uz resursu piešķiršanu, hibrīda režīms sniedz iespēju gan projekta vadītājiem, gan resursu pārvaldniekiem rezervēt resursus.

![Hibrīda režīms](./media/resource-management-hybrid.png)

Papildus atbalstītajam centrālā režīma procesam skatiet šīs tēmas, lai pārvaldītu visas citas atbalstītās rezervācijas plūsmas hibrīda režīmā:

Resursa rezervēšana tieši projektam:
- [Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Resursa rezervēšana no resursa prasības:
- [Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervēt nosauktos resursus no resursu vajadzībām](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
