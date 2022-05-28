---
title: Project Operations integrācijas konfigurēšana katrā juridiskā entītijā
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt juridisku entītiju integrāciju programmā Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585847"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations integrācijas konfigurēšana katrā juridiskā entītijā 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir soļi, kas nepieciešami, lai konfigurētu Dynamics 365 Project Operations katru juridisko personu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Līdzekļu taustiņu iespējošana programmā Dynamics 365 Finance

Lai iespējotu nepieciešamos līdzekļus, izpildiet tālāk norādītās darbības.

1. Programmā Dynamics 365 Finance dodieties uz **līdzekļu pārvaldības** darbvietu.
2. Laukā **Līdzekļu saraksts** atrodiet un iespējojiet tālāk norādītos līdzekļus.
  
    - **Iespējot vairākas projekta līguma rindas**
    - **Iespējot projekta operācijas Dynamics 365 Customer Engagement**

> [!NOTE]
> Ja sarakstā nav norādīti **Pamatlīdzekļi**, pārbaudiet, vai jūsu finanšu versija atbilst minimālās versijas prasībai (programmas versija 10.0.13 ar visiem piemērotajiem vai augstākajiem kvalitātes atjauninājumiem). Atlasiet **Pārbaudīt, vai nav atjauninājumu**, lai atsvaidzinātu līdzekļu sarakstu.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Project Operations izvietošanas scenārija definēšana juridiskai entītijai

Projekta operācijas var iespējot Dynamics 365 Customer Engagement juridiskās personas līmenī. Var būt viena juridiska persona, kas izmanto projekta operācijas Dynamics 365 Customer Engagement resursu/neuzkrātiem scenārijiem. Tajā pašā vidē var būt cita juridiska entītija, kas izmanto Project Operations, kas balstīti uz krājumiem un ražošanas pasūtījumiem.

1. Programmā Dynamics 365 Finance dodieties uz **Projektu vadības un uzskaites** > **iestatīšana Globālā** > **projektu vadības un uzskaites parametri**.
2. Pieejamo juridisko personu sarakstā atlasiet personas, kurās tiks iespējotas vairākas līguma rindas un projekta operācijas Dynamics 365 Customer Engagement līdzekļus. Atstājiet juridiskas entītijas, kas izmantos neatlasītus Project Operations scenārijus, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem.

> [!NOTE]
> Juridisku entītiju var atlasīt tikai tad, ja tai nav esošu projektu.

## <a name="configure-project-management-and-accounting-parameters"></a>Projekta pārvaldības un uzskaites parametru konfigurēšana

Katrai juridiskajai personai, kas Dynamics 365 Customer Engagement izmanto projekta operācijas, ir nepieciešama noklusējuma parametru kopa. Šie parametri ir konfigurēti **Project Operations** cilnes lapā **Projekta pārvaldības un uzskaites parametri**. Ir šādi parametri:

  - **Rēķina tipa noklusējuma iestatījumi**: Project Operations izmanto fiksētu norēķinu tipa noklusējuma kopu, kas ir jākartē uz rindas rekvizītu finansēm. Ierakstu izveide katram norēķinu tipam: **Nav norādīts**, **Rēķinā iekļaujams**, **Rēķinā neiekļaujams**, **Bezmaksas** un **Nav pieejams**.
  - **Projekta kategorijas noklusējumi**: atlasiet noklusējuma projekta kategorijas, kas jāizmanto katram transakcijas tipam. Šie noklusējuma iestatījumi tiks lietoti **Project Operations integrācijas žurnālā** un aprēķinos, kur projekta faktiskajai transakcijai nav norādīta transakciju kategorija.
  - **Prognozes**: atlasiet budžeta modeli, kas tiks izmantots laika un izdevumu novērtējumiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]