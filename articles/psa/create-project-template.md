---
title: Projekta veidnes izveide
description: Projekta veidnes izveide programmā Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177435"
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

## <a name="create-a-project-template-from-an-existing-project"></a>Jaunas projekta veidnes izveidošana no esoša projekta
Projekta veidni no projekta var izveidot tālāk norādītajos veidos.

- **Darba sadalījuma struktūra**: darba sadalījuma struktūra veidnē, kas atvasināta no projekta, kopē visus uzdevumus un atkarības. Izveidoto piešķīrumu pamatā ir vispārīgie darba grupas dalībnieki, kas ir pievienoti projekta darba grupai projekta veidnes izveides laikā.
- **Projekta aprēķini**: kad projekta veidne tiek izveidota no esoša projekta, avota projekta aprēķini tiek kopēti uz projekta veidni.
- **Projekta darba grupas dalībnieki**: kad veidne tiek izveidota no esoša projekta, visi nosauktie darba grupas dalībnieki tiek aizstāti ar organizācijas vispārējo resursu. Tiek saglabāti visi pozīciju nosaukumi un lomas.

## <a name="create-a-project-from-a-template"></a>Projekta izveidošana no veidnes  
 Projektu no veidnes var izveidot tālāk norādītajos veidos.  
  
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
