---
title: Resursu plānošana projektam
description: Resursu plānošana projektam programmā Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132154"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Resursu plānošana projektam (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Jūs varat pārbaudīt resursu pieejamību, lai iegūtu vispārēju priekšstatu par resursu rezervēšanas līmeni, vai arī varat veikt skata filtrēšanu pēc prasmēm, darba grupas, atrašanās vietas un citām opcijām.  
  
Plānošanas panelis parāda sarakstu ar resursiem un to pieejamību. Izvēlieties skata režīmu, lai parādītu pieejamību pēc vērtības **Stundas**, **Diena**, **Nedēļa** vai **Mēnesis**.  
  
Lai izmantotu plānošanas paneli, ir svarīgi to iestatīt. Lai iegūtu papildinformāciju, skatiet [Plānošanas paneļa konfigurēšana (Field Service vai Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Ja lietojat vecāku versiju, resursu pieejamību skatiet sadaļā [Resursu pieejamības skatīšana](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Lai izmantotu plānošanas paneļa rezervēšana funkcionalitāti, ģeogrāfiskās atrašanās vietas un atrašanās vietas noteikšanas pakalpojumus, nepieciešams ieslēgt kartes.  
> 
> 1. Galvenajā izvēlnē atlasiet **Resursu plānošana** > **Administrēšana**.  
> 2. Noklikšķiniet uz **Plānošanas parametri**.  
> 3. Atveriet ierakstu un ritiniet uz leju līdz sadaļai **Resource Scheduling Optimization**.  
> 4. Laukā **Izveidot savienojumu ar kartēm** izvēlieties **Jā**.  
> 5. Piekrītiet noteikumiem un saglabājiet ierakstu.  
> 6. Galvenajā izvēlnē atlasiet **Project Service** > **Plānošanas panelis**. Šeit ir vairāki veidi, kā manuāli plānot rezervācijas prasības. Izvēlieties jums piemēroto metodi.
  
## <a name="find-available-resources"></a>Pieejamo resursu atrašana

1.  Sarakstā **Rezervācijas prasības** ar peles labo pogu noklikšķiniet uz neplānotas rezervācijas un izvēlēties kādu no tālāk norādītajām darbībām.  
  
- Izvēlieties **Atrast pieejamību — pašreizējie resursi**, lai atrastu pieejamos resursus no plānošanas paneļa resursu saraksta.  
- Izvēlieties **Atrast pieejamību — visi resursi**, lai atrastu sistēmā pieejamos resursus.  
   > [!NOTE]
   >  Kad jūs to izdarāt, filtri parādīs izvēlēto rezervācijas prasību opcijas.  
  
2. Kad redzat brīvo laika sprīdi, ar peles labo pogu noklikšķiniet uz laika sprīža plānošanas panelī un izvēlieties **Rezervēt šeit**. Vai velciet un nometiet rezervācijas prasību pieejamajā laika sprīdī.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervējiet resursu, izmantojot ikdienas skatu, un uzziniet, kurš resurss ir maz rezervēts
  
1.  Plānošanas panelī atlasiet **Skata režīms** un atlasiet **Dienas**.  
  
    Tiks parādīts režģa skats ar dienā rezervēto stundu skaitu un to, kurās dienās nav rezervācijas.  
  
2.  Noklikšķiniet uz rezervējamā resursa nosaukuma un pēc tam atlasiet **Rezervēt**.  
  
3.  Dialoglodziņā **Resursa rezervēšana (izveide)** izvēlēties projektu, kuram vēlaties rezervēt resursu, rezervēšanas metodi un sākuma un beigu laiku.  
  
4.  Kad esat beidzis, atlasiet **Rezervēt**.  
  
## <a name="view-to-the-schedule-board"></a>Plānošanas paneļa skatīšana
  
1.  Atlasiet neplānotu rezervācijas prasību apakšdaļā esošajā sarakstā.  
  
2.  Velciet rezervācijas prasību uz pieejamu resursu/laika sprīdi plānošanas panelī.  
  
3.  Kad esat beidzis, atlasiet **Rezervēt**.  
  
### <a name="additional-resources"></a>Papildu resursi  
 [Resursu pārvaldnieka rokasgrāmata](../psa/resource-manager-guide.md)
