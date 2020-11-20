---
title: Projekta statusa izsekošana
description: Projekta statusa izsekošana programmā Project Service
author: ruhercul
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
ms.openlocfilehash: 00b6d874b42a415fe567d17e49c0ea319d8952a0
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127842"
---
# <a name="track-a-projects-status-project-service"></a>Projekta statusa izsekošana (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Izmantojiet [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], lai izsekotu klienta projekta norisei.  

Turpinoties sadarbībai, projekta posmi tiek atjaunināti, atspoguļojot sadarbības pakāpi:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Jauns**    | Kad veidojat projektu, posms tiek iestatīts uz **Jauns**. Ja projektu izveidojāt no veidnes, šajā posmā projektam var būt grafiks, tāmes un darba grupas dati. Pretējā gadījumā tās būs projekta aprises, un pārējie projekta komponenti jums būs jāievada manuāli. |
|  **Piedāvājums**   |      Kad projektu saistāt ar piedāvājumu vai to izveidojat no piedāvājuma, projekta posms tiek iestatīts kā **Piedāvājums** un tiek atjaunināti arī prognozētie sākuma un beigu datumi. Kad projekts atrodas piedāvājuma posmā, detalizēta informācija par piedāvājumu tiek rādīta cilnē **Pārdošana**, lapā **Projekts**.      |
|   **Plāns**   |                                     Kad iegūstat ar kādu projektu saistītu piedāvājumu un kad sadarbība pāriet līguma posmā, projekta posms atjauninās uz **Plāns**. Detalizēta informācija par līgumu tiek rādīta cilnē **Pārdošana**, lapā **Projekts**.                                      |
| **Pabeigt** |                    Kad projekta darbs ir pabeigts, posmu varat pārslēgt uz **Pabeigts**. Kad projekta posms ir iestatīts uz pabeigtu, tiek pieņemts, ka darbs ir 100% pabeigts, bet projekts tiek saglabāts atvērts uz jebkādu gaidīšanas laiku vai ar mērķi reģistrēt izdevumu ierakstus.                     |
|  **Aizvērt**   |           Kad visas transakcijas projektam ir reģistrētas un nav paredzēts, ka vēl kaut ko vajadzēs reģistrēt, varat posmu manuāli iestatīt uz **Slēgt**. Kad projekts ir iestatīts uz **Slēgt**, šajā projektā vairs nevarat reģistrēt nekādas transakcijas un projekts kļūst tikai lasāms.           |

## <a name="to-track-a-projects-status"></a>Lai izsekotu projekta statusu  

1.  Dodieties uz **Project Service > Projekti**.  

2.  Noklikšķiniet uz projekta, pie kura gribat strādāt.  

3.  Ekrāna augšdaļā esošajā joslā atlasiet lejupvērsto bultiņu pie projekta nosaukuma un pēc tam noklikšķiniet uz **Projekta izsekošana**.  

4.  Nolaižamajā sarakstā virs uzdevumu saraksta atlasiet **Piepūles izsekošana** vai **Izmaksu izsekošana**.  

5.  Veiciet dubultklikšķi uz jebkuru uzdevumu, lai to rediģētu. Varat arī pārvietot joslas Ganta diagrammā vai mainīt to izmērus, lai mainītu uzdevuma laiku un progresu.  

### <a name="see-also"></a>Skatiet arī  
 [Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md)
