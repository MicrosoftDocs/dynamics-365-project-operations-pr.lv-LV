---
title: Project Operations duālās rakstīšanas integrācija
description: Šajā tēmā ir sniegts pārskats par Project Operations duālās rakstīšanas integrāciju.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955667"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations duālās rakstīšanas integrācijas pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Project Operations izmanto [duālās rakstīšanas iespējas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), lai sinhronizētu datus starp Microsoft Dataverse un Dynamics 365 Finance.

Tālāk redzamajā attēlā ir parādīts, kā dati tiek sinhronizēti kā daļa no šīs integrācijas starp Dataverse un Finance.

![Project Operations datu plūsmu pārskats](./media/ProjectOperationsFlows.jpg)

Project Operations risinājumā Dataverse nodrošina modernu lietotāja interfeisu (UI) un ērtu paplašināmību bez kodēšanas/ar minimālu kodēšanu, izmantojot Power Platform iespējas. Projektu vadītāji, resursu vadītāji, projektu darba grupas dalībnieki un citi biroja darbinieki veic savas darbības Project Operations risinājumā Dataverse.

Project Operations risinājumā Finance nodrošina projektu grāmatvedību un ieņēmumu atpazīšanas atbalstu. Project Operations pieslēdzas Finance finanšu struktūrai, lai aprēķinātu pārdošanas nodokļus, valūtas maiņas kursu, finanšu dimensiju atskaites un veiktu citas darbības. Projekta grāmatvežu pieredzes lielākoties ir balstītas risinājumā Finance.

Project Operations integrācija sastāv no šādu komponentu integrācijas:


- [Project Operations iestatīšanas un konfigurēšanas datu integrācija](resource-dual-write-setup-integration.md) 
- [Projekta aprēķini un faktiskie dati](resource-dual-write-estimates-actuals.md)
- [Projekta rēķini](resource-dual-write-project-invoice.md)
- [Izdevumu pārvaldība](resource-dual-write-expense.md)
- [Piegādātāja rēķins](resource-dual-write-vendor-invoice.md)
