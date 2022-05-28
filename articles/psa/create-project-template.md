---
title: Projekta veidnes izveide
description: Projekta veidnes izveide programmā Project Service
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 127b6e43a15f19a42791e78b55865ab11ca50c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599003"
---
# <a name="create-a-project-template-project-service"></a>Projekta veidnes izveide (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekta veidnes ietaupa jūsu laiku, ja jūsu uzņēmums regulāri iesniedz piedāvājumus līdzīga veida projektos. Tie nodrošina standartu noteikumu kopumu un aplēsto stundu skaitu projekta tipam. Uzņēmumu vadītāji un projektu vadītāji var izveidot projektus, balstoties uz projekta veidni, vai nokopēt veidni un pārveidot to paši.  
  
## <a name="components-of-project-template"></a>Projekta veidnes komponenti
 Projekta veidne sastāv no trim komponentiem.  
  
- **Darba sadalījuma struktūra**: darba sadalījuma struktūrai projekta veidnē ir tāds pats elementu kopums kā projektā. Varat izveidot uzdevumu hierarhiju, piesaistīt lomas uzdevumam, noteikt plānošanas atribūtus, iestatīt atkarības un skatīt visus datus Ganta shēmā. Darba sadalījuma struktūra projekta veidnēs atbalsta arī uzdevumu režīmus katram uzdevumam. Nav nekādas atšķirības starp projekta veidni un projektu, veidojot darba grafiku.  
  
- **Projekta tāmes**: projekta tāmes veidnēs darbojas tāpat kā projektos, izņemot to, ka cenrāži noklusējuma izmaksu cenām un pārdošanas cenām vienmēr ir noklusējuma izmaksu cenu un pārdošanas cenu rāži, kas definēti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parametros. Pārējās funkcionalitātes ir tādas pašas kā projektā.  
  
- **Projekta darba grupas izveide**: kad veidojat projekta komandu projekta veidnei, nevarat rezervēt nosauktu resursu veidnē. Varat izmantot funkciju **Projekta darba grupas ģenerēšana** darba sadalījuma struktūrā, lai ģenerētu vispārējo resursu kopu. Varat norādīt arī vispārīgo resursu vajadzīgās prasmes un pieredzi. Projekta veidnēs nevarat aizstāt vispārīgu resursu ar rezervējamu resursu.  
  
## <a name="create-a-project-from-a-template"></a>Projekta izveidošana no veidnes  
 Projektu no veidnes var izveidot šādos veidos.  
  
-   Veidojot projektu no piedāvājuma, varat izvēlēties projekta veidni projekta ātrās izveides veidlapā.  
  
-   Veidojot projektu, noklikšķinot uz **Jauns projekts**, tiek parādīta projekta veidlapa, pirms saglabājat ierakstu. Šeit varat noklikšķināt uz lauka **Izvēlēties veidni**, lai izvēlētos no saraksta ar iepriekš definētām projekta veidnēm jūsu organizācijā.  
  
-   Noklikšķiniet uz **Izveidot projektu no veidnes** lapā **Projekta veidne**, lai izveidotu projektu no veidnes.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Veidnes komponentu kopēšana projektā  
 Kopējot veidnes komponentus projektu, jāņem vērā dažas lietas.  
  
 **Darba sadalījuma struktūras kopēšana**: kopējot darba sadalījuma struktūru no projekta veidnes, ja projektam ir cits projektu kalendārs nekā veidnei, uzdevumu grafikam tiks izmantotas darba stundas no projekta kalendāra. Tā grafiks tiek pielāgots atbalstošajam projekta kalendāram. Līdzīgi arī pirmajam uzdevumam darba sadalījuma struktūrā tiek paņemts projekta sākuma datums, bet pārējais uzdevumu hierarhiju grafiks tiek atjaunināts, pamatojoties uz ilgumu un atkarībām, kas norādītas veidnes darba sadalījuma struktūrā.  
  
 **Projekta tāmju kopēšana**: kopējot pa projekta tāmes rindiņām, cenrāži tiek atjaunoti, balstoties uz projekta atbildīgo vienību izmaksu cenrādim un uz klientu pārdošanas cenrādim. Vienības izmaksu un pārdošanas cenas nosaka no šiem cenrāžiem projektiem, kas saistīti ar pārdošanas vienību.  
  
 **Projekta darba grupas kopēšana**: kopējot projekta darba grupu no veidnes projektā, vispārīgie resursu tiek kopētas līdzi kopā ar veidnē noteiktajām prasmēm un pieredzi. Vispārīgo resursu piešķires arī tiek saglabātas kā projekta veidnē.  
  
### <a name="see-also"></a>Skatiet arī  
 [Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
