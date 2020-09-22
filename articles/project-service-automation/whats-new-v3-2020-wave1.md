---
title: Kas jauns vai mainīts Project Service Automation 3.x wave 1 2020 versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns un mainīts Project Service Automation 3. versijā, wave 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753481"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Kas jauns vai mainīts Project Service Automation 3 wave 1 2020 versijā
Šajā tēmā ir uzsvērti galvenie jaunināšanas apsvērumi, pārejot uz jaunāko versiju Project Service Automation (PSA), versija 3. x wave 1 2020.

## <a name="time-entry"></a>Laika ieraksts
Laika ievades pieredze ir paplašināta, lai nodrošinātu iespējas paplašināt laiku, ievadot vairāk klientu scenāriju. Tas ietver iespēju pievienot ierakstu tipus, kas tagad virza noteiktu uzvedību, pamatojoties uz lauku shēmas **Laika ieraksta iestatījumi** nosaukumu, kas tiek parādīti kā **Laika avots**.

### <a name="upgrade-consideration"></a>Apsvērumi atjaunināšanai
Lai atbalstītu šo funkcionalitāti, funkcijas, kas ietilpst PSA, ir atjauninātas, lai iekļautu jaunas atļaujas. Šīs atļaujas piešķir lasīšanas piekļuvi jaunajai entītijai **Laika ieraksta iestatījumi**.

Lietotājiem, kuriem nepieciešama iespēja reģistrēt laiku, jāpiešķir lietotāja lomas **Laika ieraksta lietotājs** papildus esošajām lomām. Šajā lomā iekļauta jaunā funkcionalitāte, un programma nodrošina, ka laika ieraksts turpina darboties.

### <a name="currently-extended-time-entry-changes"></a>Pašlaik paplašinātā laika ieraksta izmaiņas
Lai mazinātu ietekmi uz laika ievadīšanas pašreizējiem lietotājiem, šī lomu maiņa ir vienīgā būtiskā prasība, kas nepieciešama, lai turpinātu izmantot laika ievadni. Ja esat izveidojis pielāgotus skatus vai atdalītas laika ievadīšanas iespējas, lauki **Laika ievadnes iestatījums** ir jāiestata uz pareizo PSA vērtību.
