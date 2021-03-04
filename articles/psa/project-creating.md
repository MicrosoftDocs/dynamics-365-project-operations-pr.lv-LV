---
title: Projektu grafiki
description: Šajā tēmā ir sniegta informācija par to, kā izveidot grafiku.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 2877f12a9ea3d288c4cf41f406cd8ca3e6cee821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148427"
---
# <a name="project-schedules"></a>Projektu grafiki 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekta grafikā ir pateikts, kāds darbs ir jāpaveic, kuri resursi šo dabu paveiks un kādā laika posmā šis darbs ir jāpabeidz. Tas atspoguļo visu darbu, kas ir saistīts ar savlaicīgu attiecībā projekta nodošanu. Programmatūrā Dynamics 365 Project Service Automation projekta grafiku jūs izveidojat, visu darbu sadalot izpildāmos uzdevumos, aplēšot laiku, kāds ir nepieciešams katra uzdevuma izpildīšanai, iestatot uzdevumu atkarības, iestatot uzdevumu ilgumus un aplēšot vispārējos resursus, kuri šos uzdevumus izpildīs. Projekta grafiks tiek izveidots projekta lapas cilnē **Grafiks**.
 
## <a name="tasks"></a>Uzdevumi

Projekta grafika izveidošanas pirmais posms ir visa darba sadalīšana pārvaldāmās daļās. Programmatūrā PSA grafiks atbalsta tālāk norādītos līdzekļus.

- Projekta saknes mezgls
- Kopsavilkuma vai konteinera uzdevumi
- Lapas mezgla uzdevumi

### <a name="project-root-node"></a>Projekta saknes mezgls

Projekta saknes mezgls ir attiecīgā projekta augšējā līmeņa kopsavilkuma uzdevums. Visi citi projekta uzdevumi tiek izveidoti saskaņā ar to. Saknes mezgla nosaukums vienmēr ir iestatīts uz projekta nosaukumu. Saknes mezgla piepūles, datumu un ilguma kopsavilkums ir balstīts uz vērtībām, kuras hierarhijā atrodas zem tā. Saknes mezgla rekvizītus nevar rediģēt. Turklāt saknes mezglu nevar arī izdzēst.

### <a name="summary-or-container-tasks"></a>Kopsavilkuma vai konteinera uzdevumi 

Kopsavilkuma uzdevumiem pakārtoti ir apakšuzdevumi jeb konteinera uzdevumi. Tiem nav pašiem savas darba piepūles vai izmaksu. Tā vietā šo uzdevumu darba piepūli un izmaksas veido apkopojums no darba piepūles un izmaksām to konteineru uzdevumos. Kopsavilkuma uzdevuma sākuma datums ir konteinera uzdevumu sākuma datums, un tā beigu datums ir konteinera uzdevumu beigu datums. Kopsavilkuma uzdevuma nosaukumu var rediģēt, bet plānošanas rekvizītus (piepūli, datumus un ilgumu) nevar rediģēt. Ja izdzēšat kādu kopsavilkuma uzdevumu, tiek izdzēsti arī visi tā konteinera uzdevumi.

### <a name="leaf-node-tasks"></a>Lapas mezgla uzdevumi

Lapas mezgla uzdevumi pārstāv projekta darba vissīkāko iedalījumu. Tiem ir aplēstā piepūle, resursi, plānotais sākuma un beigu datums un ilgums.
 
## <a name="creating-a-task-hierarchy"></a>Uzdevumu hierarhijas izveidošana

Uzdevumu hierarhiju varat izveidot, izmantojot tālāk minētās opcijas.

- Poga **Pievienot uzdevumu**
- Poga **Pielikt uzdevumam atkāpi**
- Poga **Pielikt uzdevumam pārkaru atkāpi**
- Pogas **Pārvietot uz augšu** un **Pārvietot uz leju**
- Pieejamība un īsinājumtaustiņi

### <a name="add-task"></a>Pievienot uzdevumu

Izmantojot pogu **Pievienot uzdevumu**, hierarhijā varat izveidot jaunu uzdevumu. Ja neatlasāt nekādu pozīciju, uzdevums tiek pievienots beigās. 

Katram uzdevumam tiek piešķirts grafika ID. Grafika ID norāda uzdevuma dziļumu un pozīciju hierarhijā. Tajā tiek izmantota strukturējuma numerācija. Uzdevumiem, kas atrodas pirmajā līmenī zem projekta saknes mezgla, tiek izmantota numerācijas shēma 1, 2, 3 un tā tālāk. Uzdevumiem, kas atrodas zem pirmā līmeņa, tiek izmantota numerācijas shēma 1.1, 1.2, 1.3 un tā tālāk.

### <a name="indent-task"></a>Pielikt uzdevumam atkāpi

Kad uzdevumam tiek pielikta atkāpe, tas kļūst par bērnelementu uzdevumam, kurš atrodas tieši virs tā. Pēc tam šī uzdevuma grafika ID tiek pārrēķināts, lai tas būtu balstīts uz tā jaunā vecākelementa grafika ID un atbilstu strukturējuma numerācijas shēmai. Tagad šis pamatuzdevums ir kopsavilkuma uzdevums vai konteinera uzdevums. Līdz ar to tas kļūst par savu pakārtoto uzdevumu apkopojumu.

### <a name="outdent-task"></a>Pielikt uzdevumam pārkaru atkāpi 

Kad uzdevumam tiek pielikta pārkaru atkāpe, tas vairs nav bērnelements tam uzdevumam, kurš bija tā pamatuzdevums. Pēc tam grafika ID tiek pārrēķināts tā, lai tas atspoguļotu uzdevuma atjaunināto dziļumu un pozīciju hierarhijā. Iepriekšējā pamatuzdevuma piepūle, izmaksas un datumi tiek pārrēķināti, lai tie neiekļautu šo uzdevumu.

### <a name="move-up-and-move-down"></a>Pārvietot uz augšu un Pārvietot uz leju 

Pogas **Pārvietot uz augšu** un **Pārvietot uz leju** maina uzdevuma pozīciju tā vecākelementu hierarhijā. Šāda tipa izmaiņas neietekmē uzdevuma piepūli, izmaksas, datumus un ilgumu. Tiek ietekmēts tikai uzdevuma grafika ID. Grafika ID tiek pārrēķināts, lai tas atspoguļotu uzdevuma jauno pozīciju pakārtoto uzdevumu vecākelementu sarakstā.

### <a name="accessibility-and-keyboard-shortcuts"></a>Pieejamība un īsinājumtaustiņi

Režģis **Grafiks** ir pilnībā pieejams, un to var izmantot ar tādiem ekrāna lasītājiem kā Diktors, JAWS un NVDA. Pa režģa laukumu varat pārvietoties, izmantojot bulttaustiņus (tāpat kā programmā Microsoft Excel), varat izmantot tabulēšanas taustiņu, lai pārvietotos pa interaktīvajiem UI elementiem, kā arī varat izmantot lejupvērsto bultiņu, taustiņu Enter vai atstarpes taustiņu, lai atlasītu un izsauktu nolaižamās izvēlnes. Arī kolonnu virsraksti ir interaktīvi. Varat paslēpt un parādīt kolonnas, izmantot tabulēšanas taustiņu un bulttaustiņus, lai pārvietotos pa kolonnu virsrakstiem, un varat izmantot rīkjoslas darbību pogas. Turklāt varat izmantot tālāk norādītos īsinājumtaustiņus.

- **Atsvaidzināt**: ALT+SHIFT+F5
- **Pievienot**: ALT+SHIFT+Insert
- **Dzēst**: ALT+SHIFT+Delete
- **Pārvietot uz augšu/uz leju**: ALT+SHIFT+bultiņa uz augšu/uz leju
- **Pielikt atkāpi/pārkaru atkāpi**: ALT_SHIFT+bultiņa pa kreisi/pa labi
- **Izvērst/Sakļaut hierarhijas**: ALT+SHIFT+taustiņš Plus/Mīnus

## <a name="task-attributes"></a>Uzdevuma atribūti

Uzdevuma nosaukums apraksta darbu, kas ir jāizpilda. Programmatūrā PSA ar uzdevumu saistītie atribūti apraksta šī uzdevuma grafiku un tā personāla komplektēšanas prasības.

> ![Uzdevuma atribūti](media/project-2.png)
 
### <a name="schedule-attributes"></a>Grafika atribūti

Atribūti **Piepūle**, **Sākuma datums**, **Beigu datums** un **Ilgums** nosaka grafiku attiecīgajam uzdevumam.

Papildu grafika atribūti tostarp ir tālāk norādītie.

- **Piepūles stundas**: ievadiet tāmi par stundu skaitu, kāds ir nepieciešams uzdevuma izpildīšanai. 
- **Ilgums**: norādiet darbdienu skaitu, kāds ir nepieciešams šī uzdevuma izpildīšanai.
- **Grafika ID**: šis automātiski ģenerētais ID tiek izmantots, lai uzdevumus sakārtotu hierarhijā. Atkarības starp uzdevumiem regulē faktisko secību, kādā pie šiem uzdevumiem tiek strādāts.
 
### <a name="staffing-attributes"></a>Darbspēka atribūti

Personāla komplektēšanas atribūtiem piekļūst, grafikā izmantojot lauku **Resursi**. Varat vai nu meklēt jau esošu resursu, vai rūtī **Ātrā izveide** noklikšķināt uz **Izveidot** un pievienot projekta darba grupas dalībnieku kā jaunu resursu.

Uzdevuma personāla komplektēšanas prasību aprakstīšanai tiek izmantoti lauki **Loma**, **Resursu vienība** un **Amata nosaukums**. Šie personāla komplektēšanas atribūti kopā ar uzdevuma grafiku tiek izmantoti, lai atrastu pieejamos resursus šī uzdevuma veikšanai.

**Loma** — norādiet resursa tipu, kāds ir nepieciešams šī uzdevuma veikšanai.

**Resursu vienība** — norādiet struktūrvienību, no kuras ir jāpiešķir resursi šim uzdevumam. Ja resursa izmaksu un norēķinu likmes ir iestatītas, pamatojoties uz resursu vienībām, šis atribūts uzdevumam ietekmē izmaksu un pārdošanas tāmi.

**Amata nosaukums** — ievadiet draudzīgu nosaukumu vispārējam resursam, kas tiek izmantots kā vietturis resursam, kurš galu galā darīs šo darbu.

Laukā **Resursi** ir vispārējā resursa amata nosaukums vai nosaukts resurss, ja tāds tiek atrasts.

Laukā **Kategorija** ir vērtības, kas norāda plašāku darba tipu, kurā šo uzdevumu var ieļaut. Šis lauks neietekmē plānošanu un personāla komplektēšanu. Tas tiek izmantots tikai atskaišu veidošanai.

### <a name="task-dependencies"></a>Uzdevuma atkarības 

Grafiku programmatūrā PSA varat izmantot, lai starp uzdevumiem izveidotu pirmstecīgas aktivitātes attiecības. Lauks **Pirmstecīga aktivitāte** sadaļā **Uzdevumi** pieņem vienu vai vairākas vērtības, lai norādītu uzdevumus, no kuriem kāds uzdevums ir atkarīgs. Ja kādam uzdevumam ir piešķirtas pirmstecīgas aktivitātes vērtības, šis uzdevums var sākties tikai pēc tam, kad ir pabeigti visi tā pirmstecīgie uzdevumi. Atkarības dēļ uzdevuma plānotais sākuma datums tiek atiestatīts uz datumu, kad ir pabeigti pirmstecīgie uzdevumi.

Uzdevuma režīms neietekmē atjauninājumus, kas tiek veikti pirmstecīgo/atkarīgo uzdevumu sākuma un beigu datumiem.

## <a name="task-mode"></a>Uzdevuma režīms 

Uzdevuma režīms nosaka lapu mezglu uzdevumu plānošanu. Programmatūrā PSA katram uzdevumam tiek atbalstīti divi uzdevuma režīmi: automātiskā plānošana un manuālā plānošana.

### <a name="auto-scheduling"></a>Automātiskā plānošana 
 
Ja uzdevuma režīms kādam uzdevumam ir iestatīts uz **Plānots automātiski**, lai šim uzdevumam noteiktu grafiku, uzdevuma plānošanas programma uzdevuma atribūtiem izmanto plānošanas kārtulas.

#### <a name="scheduling-rules"></a>Plānošanas kārtulas

Ja lapas mezgla uzdevumam nav pirmstecīgu aktivitāšu, tā sākuma datums tiek iestatīts uz projekta ieplānoto sākuma datumu. Lapas mezgla uzdevuma ilgums vienmēr tiek aprēķināts kā darba dienu skaits no tā sākuma līdz beigu datumam. Ja uzdevums tiek plānots automātiski, plānošanas programma ievēro tālāk aprakstītās kārtulas.

- Uzdevuma sākuma un beigu datumam ir jābūt darbdienās atbilstoši projekta plānošanas kalendāram. 
- Visiem uzdevumiem, kam ir pirmstecīgi uzdevumi, sākuma datums automātiski tiek iestatīts uz to pirmstecīgo uzdevumu vēlāko beigu datumu.
- Piepūle tiek aprēķināta, izmantojot šādu formulu: Personu skaits x Ilgums × Stundas standarta darbdienā šajā projekta kalendārā.

### <a name="manual-scheduling"></a>Manuāla plānošana

Ja automātiskās plānošanas kārtulas neatbilst jūsu prasībām, uzdevuma režīmu šim uzdevumam varat iestatīt uz **Plānots manuāli**. Šis iestatījums neļauj plānošanas programmai aprēķināt citu plānošanas atribūtu vērtības. Neatkarīgi no uzdevuma režīma, ja uzdevumiem iestatāt pirmstecīgas aktivitātes, tās vienmēr ietekmē atkarīgā uzdevuma sākuma datumu.
