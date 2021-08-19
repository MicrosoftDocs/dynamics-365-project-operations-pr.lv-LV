---
title: Projekta cenrāžu sarakstu ignorēšana
description: Šajā tēmā ir sniegta informācija par pielāgotu pārdošanas cenrāžu izveidi.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b26947822eb8e87b3b36fcde9c99c6ee69375aa942a5641112b9b1109dcaa26c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009585"
---
# <a name="override-project-sales-price-lists"></a>Projekta cenrāžu sarakstu ignorēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

## <a name="customer-specific-project-price-lists"></a>Klientam noteikts projekta cenrādis

Klientam noteiktas cenas var tikt iestatītas kā projekta cenrāži uzņēmuma ierakstā risinājumā Dynamics 365 Project Operations.

Lai iestatītu klientam noteiktu projekta cenrādi, zonā **Pārdošana** pārejiet uz uzņēmuma ierakstu.

1. Atveriet saraksta lapu **Konts**.
2. Atrodiet un veiciet dubultklikšķi uz klienta ieraksta, lai atvērtu informācijas lapu **Konts**.
3. Cilnē **Projekta cenrāži** atlasiet **+ Jauns projekta cenrādis**.
4. Lapas **Jauns projekta cenrādis** nolaižamajā sarakstā atlasiet cenrādi. Ir iekļauti tikai tie cenrāži, kuru konteksts ir iestatīts kā **Pārdošana** un kuru valūta atbilst uzņēmuma valūtai.
5. Ierakstiet saistības nosaukumu un pēc tam atlasiet vienumu **Saglabāt**. Tiek izveidots klientam noteikts projekta cenrādis. Šis cenrādis tiks izmantots, lai ievietotu noklusējuma projekta cenas projekta piedāvājumos vai līgumos, kas izveidoti šim klientam, ja piedāvājuma vai projekta līguma izveidošanas datums atbilst cenrāža darbības laikam.

## <a name="custom-pricing-on-project-quotes"></a>Pielāgotas cenas projekta piedāvājumos

Projekta piedāvājumos var būt projekta izcenojums, kas sākas ar noklusējuma standarta cenrādi, kas pēc noklusējuma tiek ņemts no klienta vai no projekta parametriem.

Kad konkrētam piedāvājumam ir nepieciešama pielāgota cenu noteikšana ar projektu saistītam darbam, to var iegūt no projekta cenrāža saistītās entītijas.

Izpildiet tālāk aprakstītās darbības, lai iestatītu piedāvājumam specifiskas projekta cenas.

1. Atveriet projekta piedāvājumu un atlasiet cilni **Projekta cenrāži**.
2. Apakšrežģī atlasiet **Izveidot pielāgotu izcenojumu**.

Visi piedāvājumam pievienotie projekta cenrāži tiek pārkopēti uz jauniem cenrāžiem. Jauno cenrāžu nosaukumi atspoguļo piedāvājuma nosaukumu ar datuma laikspiedolu, kad ir izveidoti šie cenrāži.

Varat izmantot katru no šiem cenrāžiem un veikt darba (lomas cena) un izmaksu (kategorijas cena) cenu atjauninājumus. Šīs cenas ir piemērojamas tikai šim projekta piedāvājumam.

## <a name="price-lists-on-a-project-contract"></a>Projekta līguma cenrāži

Projekta līgumā projekta cenas vienmēr pēc noklusējuma tiek iestatītas kā pielāgots cenrādis, kura nosaukumam pievienots līguma nosaukums un izveides datuma laikspiedols. Tas attiecas gan uz līgumiem, kas izveidoti uzvarētiem piedāvājumiem, gan arī uz pilnīgi jauniem izveidotiem līgumiem. Ja nepieciešams, varat noņemt šo saistību ar pielāgoto cenrādi un tā vietā projekta līgumam piesaistīt standarta cenrādi.

Kad standarta cenrādis tiek saistīts ar piedāvājuma vai līguma projekta cenrāžiem, jebkuras izmaiņas cenrāža cenās ietekmēs visus piedāvājumus un līgumus, kas izmanto cenrādi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]