---
title: Project Operations integrācijas konfigurēšana katrā juridiskā entītijā
description: Šajā rakstā ir sniegta informācija par to, kā iestatīt juridisku entītiju integrāciju programmā Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914687"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations integrācijas konfigurēšana katrā juridiskā entītijā 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir soļi, kas nepieciešami, lai konfigurētu Dynamics 365 Project Operations katru juridisko personu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Iespējojiet programmā Dynamics 365 Finance galvenos taustiņus.

Lai iespējotu nepieciešamos līdzekļus, izpildiet tālāk norādītās darbības.

1. Programmā Dynamics 365 Finance dodieties uz darbvietu **Līdzekļu pārvaldība**.
2. Laukā **Līdzekļu saraksts** atrodiet un iespējojiet tālāk norādītos līdzekļus.
  
    - **Iespējot vairākas projekta līguma rindas**
    - **Iespējot Project Operations pakalpojumā Dynamics 365 Customer Engagement**

> [!NOTE]
> Ja sarakstā nav norādīti **Pamatlīdzekļi**, pārbaudiet, vai jūsu finanšu versija atbilst minimālās versijas prasībai (programmas versija 10.0.13 ar visiem piemērotajiem vai augstākajiem kvalitātes atjauninājumiem). Atlasiet **Pārbaudīt, vai nav atjauninājumu**, lai atsvaidzinātu līdzekļu sarakstu.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Project Operations izvietošanas scenārija definēšana juridiskai entītijai

Project Operations var iespējot risinājuma Dynamics 365 Customer Engagement juridiskās entītijas līmenī. Var būt viena juridiskā entītija, kas izmanto Project Operations risinājumā Dynamics 365 Customer Engagement scenārijiem, kas nav balstīti uz resursiem/krājumiem. Tajā pašā vidē var būt cita juridiska entītija, kas izmanto Project Operations, kas balstīti uz krājumiem un ražošanas pasūtījumiem.

1. Risinājumā Dynamics 365 Finance dodieties uz **Projektu pārvaldība un uzskaite**  >  **Iestatīšana**  > **Vispārīgie projektu pārvaldības un uzskaites parametri**.
2. Pieejamo juridisko entītiju sarakstā atlasiet entītijas, kurās ir iespējotas vairākas līguma rindas un Project Operations risinājumā Dynamics 365 Customer Engagement. Atstājiet juridiskas entītijas, kas izmantos neatlasītus Project Operations scenārijus, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem.

> [!NOTE]
> Juridisku entītiju var atlasīt tikai tad, ja tai nav esošu projektu.

## <a name="configure-project-management-and-accounting-parameters"></a>Projekta pārvaldības un uzskaites parametru konfigurēšana

Katrai juridiskajai entītijai, kas izmanto Project Operations risinājumā Dynamics 365 Customer Engagement, ir vajadzīgas noklusējuma parametru kopas. Šie parametri ir konfigurēti **Project Operations** cilnes lapā **Projekta pārvaldības un uzskaites parametri**. Ir šādi parametri:

  - **Rēķina tipa noklusējuma iestatījumi**: Project Operations izmanto fiksētu norēķinu tipa noklusējuma kopu, kas ir jākartē uz rindas rekvizītu finansēm. Ierakstu izveide katram norēķinu tipam: **Nav norādīts**, **Rēķinā iekļaujams**, **Rēķinā neiekļaujams**, **Bezmaksas** un **Nav pieejams**.
  - **Projekta kategorijas noklusējumi**: atlasiet noklusējuma projekta kategorijas, kas jāizmanto katram transakcijas tipam. Šie noklusējuma iestatījumi tiks lietoti **Project Operations integrācijas žurnālā** un aprēķinos, kur projekta faktiskajai transakcijai nav norādīta transakciju kategorija.
  - **Prognozes**: atlasiet budžeta modeli, kas tiks izmantots laika un izdevumu novērtējumiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]