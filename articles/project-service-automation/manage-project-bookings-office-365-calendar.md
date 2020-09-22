---
title: Projektu pārvaldība un rezervācija Office 365 kalendārā
description: Kā pārvaldīt projektus un rezervācijas Office 365 kalendārā
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753402"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Projektu un rezervāciju pārvaldība jūsu kalendārā (Project Service)

> [!Note]
> NOVECOJIS: šis līdzeklis ir novecojis un vairs nav pieejams.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Skatiet personiskās tikšanās, projekta darbu rezervācijas un field service darbu pasūtījumu piešķires, izmantojot [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendāru.  
  
 Ja viss ir pieejams vienuviet, ir viegli strādāt. Sapulces, tikšanās, rezervācijas un uzdevumi ir pieejami [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendārā.  
  
 Ja izmantojat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], personiskās tikšanās varat ievadīt Project Service laika ieraksta logā. Tas ļauj projekta un resursu vadītājiem zināt par jūsu pieejamību projektiem. Tas arī ļaus ietaupīt laiku, jo jums nav divreiz jāievada informācija par savu personisko tikšanos. Varat vienkārši importēt savas personiskās tikšanās no kalendāra Project Service laika ieraksta skatā.  
  
 Jūsu kalendārs sinhronizēs projektu un darbu pasūtījumu rezervācijas no šodienas līdz nākamajām četrām nedēļām. Šo iestatījumu nevar mainīt.  
  
 Sinhronizēšana tiek atbalstīta tikai vienā virzienā: no PSA uz [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendāru. Varat sinhronizēt apgrieztā secībā. 
  
 Lai uzzinātu, kā lietot [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendāru, skatiet tēmu [Uzņēmuma kalendārs tīmekļa programmā Outlook](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>Iestatīšana  
 Lai varētu skatīt un pārvaldīt savas rezervācijas [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendārā, nepieciešams iestatīt tālāk minēto.  
  
- Jums jābūt [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] globālā administratora vai sistēmas administratora akreditācijas datiem.  
  
- Jūsu administratoram vajadzēs konfigurēt e-pasta servera profilu, un katram lietotājam būs nepieciešams konfigurēt savu pastkasti. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Iestatīt e-pasta apstrādi, izmantojot servera puses sinhronizāciju](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Ieslēgt sinhronizāciju savai organizācijai (administrēšanas uzdevums)  
  
1.  Galvenajā izvēlnē noklikšķiniet uz **Iestatījumi** > **Administrēšana**.  
  
2.  Noklikšķiniet uz **Sistēmas iestatījumi**.  
  
3.  Noklikšķiniet uz cilnes **Sinhronizācija**.  
  
4.  Sadaļā **Atlasīt, vai iespējot resursu rezervāciju sinhronizēšanu ar** atzīmējiet **Sinhronizēt resursu rezervācijas ar Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Ieslēgt sinhronizāciju lietotāja profilam (lietotāja uzdevums)  
  
1.  Ekrāna augšējā labajā stūrī noklikšķiniet uz pogas **Iestatījumi**.  
  
2.  Noklikšķināšana uz **Opcijas**.  
  
3.  Noklikšķiniet uz cilnes **Sinhronizācija**.  
  
4.  Sadaļā **Sinhronizēt resursu rezervācijas ar Outlook** atzīmējiet **Sinhronizēt resursu rezervācijas ar Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importēt savas personiskās tikšanās (lietotāja uzdevums)  
 Varat importēt savas personiskās tikšanās no kalendāra Project Service Automation laika ieraksta skatā.  
  
1. Atveriet [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendāru un noklikšķiniet uz **Importēt datus**.  
  
2. Ekrānā Filtri atlasiet **Tikšanās no Exchange** un pēc tam noklikšķiniet uz **Lietot**.  
  
3. Sistēma tikšanās ievietos laikā ieraksta skatā kā ieteiktos ierakstus no pašreizējās nedēļas. Lai pievienotu citas nedēļas ierakstus, noklikšķiniet uz **Iepriekšējā** vai **Nākamā**.  
  
4. Izvēlieties tikšanos, kuru vēlaties pievienot Project Service Automation laika ieraksta skatam.  
  
5. Uznirstošajā tekstlodziņā **Laika ieraksts** atlasiet atbilstošās opcijas, lai pārvērstu tikšanos projekta Project Service Automation ieraksta skatā.  
  
6. Noklikšķiniet uz **Saglabāt**.  
  
### <a name="see-also"></a>Skatiet arī  
 [Laika, izmaksu un sadarbības ceļvedis](../project-service/time-expense-collaboration-guide.md)
