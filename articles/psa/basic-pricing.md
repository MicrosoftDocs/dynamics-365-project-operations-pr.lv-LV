---
title: Projekta izcenojums
description: Šajā tēmā ir sniegta informācija par to, kā programmā Dynamics 365 Project Service Automation darbojas izcenojums.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2337a1cef55ecc3b7625a0c9a643b9ed8a1d70e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291178"
---
# <a name="project-pricing"></a>Projekta izcenojums 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation paplašina programmā Dynamics 365 Sales esošo entītiju Cenrādis. 

## <a name="key-entities"></a>Galvenās entītijas

Cenrādis ietver informāciju, ko nodrošina četras dažādas entītijas.

- **Cenrādis** — šī entītija glabā informāciju par kontekstu, valūtu, spēkā stāšanās datumu un laika izcenojuma laika vienību. Konteksts parāda, vai cenrādis ir izteikts izmaksu likmēs vai pārdošanas likmēs. 
- **Valūta** — šī entītija glabā cenrādī esošo cenu valūtu. 
- **Datums** — šo entītiju izmanto, kad sistēma mēģina ievadīt noklusējuma cenu par transakciju. PSA izcenojums atlasa cenrādi ar spēkā stāšanās datumu, kas ietver transakcijas datumu. Ja PSA izcenojums atrod vairāk nekā vienu cenrādi, kas ir spēkā transakcijas datumam, kurš ir pievienots saistītajam piedāvājumam, līgumam vai organizācijas struktūrvienībai, neviena cena netiek iestatīta uz noklusējumu. 
- **Laiks** — šī entītija glabā laika vienību, kurā tiek izteiktas cenas, piemēram, dienas vai stundu likmes. 

Entītijai Cenrādis ir trīs saistītas tabulas, kurās tiek glabātas cenas.

  - **Lomas cena** — šajā tabulā tiek glabāta lomas un organizācijas struktūrvienības vērtību kombinācijas likme, un tā tiek izmantota, lai iestatītu no lomām atkarīgas cenas cilvēkresursiem.
  - **Transakciju kategorijas cena** — šajā tabulā tiek glabātas cenas pēc transakciju kategorijas, un tās tiek izmantotas izmaksu kategoriju cenu iestatīšanai.
  - **Cenrāža elementi** — šajā tabulā tiek glabātas kataloga preču cenas.

> ![Cenu konfigurēšana, izmantojot cenrādi](media/basic-guide-12.png)
 
Cenrādis ir likmju kartīte. Likmju kartīte ir kombinācija, ko veido entītija Cenrādis un saistītās rindas tabulās Lomas cena, Transakciju kategorijas cena un Cenrāža elementi.

## <a name="resource-roles"></a>Resursu lomas

Termins *resursa loma* attiecas uz prasmju, kompetenču un sertifikāciju kopu, kas personai ir nepieciešama, lai projektā varētu veikt noteiktu uzdevumu kopu.

Cilvēkresursu laiks parasti tiek norādīts, pamatojoties uz lomu, ko resurss aizpilda noteiktā projektā. Attiecībā uz cilvēkresursu laiku programmā PSA tiek atbalstīta izmaksu novērtēšana un rēķinu izrakstīšana, pamatojoties uz resursa lomu. Par laiku cena var tikt noteikta jebkurā vienību grupas **Laiks** vienībā.

Vienību grupa **Laiks** tiek izveidota, kad tiek instalēta programma PSA. Tās noklusējuma vienība ir **Stunda**. Vienību grupas **Laiks** un vienības **Stunda** atribūtus nevar dzēst, pārdēvēt vai rediģēt. Taču vienību grupai **Laiks** var pievienot citas vienības. Mēģinot izdzēst vienību grupu **Laiks** vai vienību **Stunda**, PSA biznesa loģikā var rasties kļūmes.

> ![Cenu konfigurēšana pēc lomas](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Transakciju kategorijas un izdevumu kategorijas

Par komandējumu un citiem izdevumiem, kas rodas projekta konsultantiem, parasti rēķins tiek izrakstīts klientam. PSA atbalsta izmaksu kategoriju izcenojumu, izmantojot cenrāžus. Izmaksu kategoriju piemēri ietver lidmašīnu biļetes, viesnīcu un automašīnas nomu. Katrā izdevumu cenrāža rindā ir noradītas konkrētas izdevumu kategorijas cenas. Attiecībā uz izdevumu kategoriju izcenojumu PSA atbalsta tālāk norādītās trīs izcenojuma metodes.

- **Pašizmaksa** — klienta rēķinā tiek iekļautas izdevumu izmaksas, un netiek piemērots uzcenojums.
- **Uzcenojuma procenti** — klienta rēķinā tiek iekļauti procenti no faktiskajām izmaksām. 
- **Vienības cena** — katrai izdevumu kategorijas vienībai tiek iestatīta norēķinu cena. Summa, par kādu tiek izrakstīts rēķins klientam, tiek aprēķināta, pamatojoties uz konsultanta norādīto izdevumu vienību skaitu. Nobraukumam tiek izmantota izcenojuma metode ar vienības cenu. Piemēram, nobraukuma izdevumu kategoriju var konfigurēt uz 30 ASV dolāriem (USD) dienā vai 2 USD par jūdzi. Kad konsultants ziņo par nobraukumu projektā, rēķina summu aprēķina, pamatojoties uz konsultanta norādīto jūdžu skaitu.

> ![Izmaksu kategoriju izcenojuma konfigurēšana](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Projekta pārdošanas izcenojums un pārlabošana

Attiecībā uz projektu piedāvājumiem un līgumiem projekta cenrādim ir no preču cenrāža atšķirīgs cenas pārlabošanas modelis. Preču kataloga piedāvājuma rindā varat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā, jo katra piedāvājuma rinda norāda uz vienu kataloga vienumu. Taču projekta piedāvājuma rindā nevarat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā. Lai atbalstītu šos abus atšķirīgos pārlabošanas modeļus, programmā PSA ir ieviesta jauna cenrāža saistīšana, projekta cenrādis.

> [!NOTE]
> Ieteicams projekta resursiem un kataloga vienumiem izmantot atsevišķus cenrāžus, jo starp abiem pastāv uzvedības atšķirības, kad pārlabojat cenas.

Katrai no tālāk minētajām entītijām var būt viens vai vairāki piesaistītie pārdošanas cenrāži projekta izcenojumam.

- Klients (uzņēmums) 
- Iespēja 
- Piedāvājums 
- Projekta līgums

Šo entītiju saistību ar cenrādi norāda projekta cenrāži. Varat saistīt vienu vai vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līguma pārdošana.

Noklusējuma projekta cenrādis netiek automātiski ievadīts klienta ierakstā. Tomēr varat manuāli pievienot projekta cenrādi klienta ierakstam. Taču projekta cenrādi drīkst manuāli pievienot tikai tad, ja jums ir pielāgots izcenojuma līgums ar klientu. 

Kad pārdošanas entītijai tiek pievienots projekta cenrādis, PSA pārbauda tālāk norādīto informāciju.

- Cenrādim ir entītijas **Pārdošana** konteksts. 
- Cenrāža valūta atbilst klienta valūtai. 

Projekta līgumā PSA izmanto tālāk norādīto prioritāšu secību, lai automātiski iestatītu saistītos projekta cenrāžus.

1. Piedāvājums
2. Iespēja
3. Klients 
4. PSA globālie iestatījumi

Kad projekta cenrādis tiek ievadīts pēc noklusējuma, PSA pārbauda, vai šī valūta atbilst klienta valūtai un vai ievadītajiem noklusējuma cenrāžiem ir entītijas **Pārdošana** konteksts.

Varat saistīt vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līgums. Šī iespēja atbalsta datumam specifiskas noklusējuma cenas ilgstošam projekta līgumam, kam var būt nepieciešams vairāk nekā viens cenrādis, lai uzskaitītu cenas atjauninājumus, kas rodas inflācijas dēļ. Tomēr, ja cenrāžos, ko saistāt ar entītiju Klients, Iespēja, Piedāvājums vai Projekta līgums, pārklājas spēkā stāšanās datumi, noklusējuma cenas var būt nepareizas. Tāpēc ir jāpārliecinās, vai projekta cenrāži, kam pārklājas spēkā esošie datumi, netiek saistīti ar šīm entītijām.

### <a name="deal-specific-price-overrides"></a>Darījumam specifiska cenas pārlabošana

Programmā PSA varat izveidot darījumam specifisku pārlabošanu noteiktām projekta cenrāža cenām, kas pēc noklusējuma tiek ievadītas piedāvājuma vai projekta līgumā.

Pēc noklusējuma projekta līgums vienmēr saņem pamata pārdošanas cenrāža kopiju, nevis tiešu saiti uz to. Šī uzvedība palīdz garantēt, ka cenu līgumi, kas tiek noslēgti ar klientu par darba paziņojumu (SOW), nemainās, ja tiek mainīts pamata cenrādis.

Taču piedāvājumā varat izmantot arī pamata cenrādi. Vai arī varat kopēt pamata cenrādi un rediģēt to, lai izveidotu pielāgotu cenrādi, kas attiecas tikai uz šo piedāvājumu. Lai izveidotu jaunu cenrādi, kas ir paredzēts konkrētam piedāvājumam, lapā **Piedāvājums** atlasiet opciju **Izveidot pielāgotu izcenojumu**. Darījumam specifiskam projekta cenrādim var piekļūt tikai no piedāvājuma. 

Kad veidojat pielāgotu projekta cenrādi, tiek kopēti tikai cenrāža projekta komponenti. Citiem vārdiem sakot, jauns cenrādis tiek izveidots kā kopija esošam projekta cenrādim, kas ir pievienots piedāvājumam, un šim jaunajam cenrādim ir tikai saistītās lomu cenas un transakciju kategoriju cenas.

> ![Pielāgota projekta līguma izcenojuma skatīšana un konfigurēšana](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Izmaksu izsekošana

PSA izseko projektos izmantotā cilvēkresursu laika izmaksas. Tā arī izseko citu projekta laikā radušos izdevumu, piemēram, ceļa izdevumu, izmaksas.

Tāpat kā norēķinu likmes, arī cilvēkresursu izmaksu likmes iestata, izmantojot cenrāžus. Tālāk ir norādītas izmaksu cenrāža un pārdošanas cenrāža uzvedības galvenās atšķirības.

- Resursa izmaksu likmi nevar pārlabot noteiktā projektā, līgumā vai piedāvājumā. Taču norēķinu likmes var pārlabot katram darījumam, ja tiek veiktas izmaiņas, kas ir raksturīgas darījumam. 

- Izmaksu cenrāža atrisināšanai tiek izmantota tālāk norādītā kārtība.

    1. Izmaksu cenrādis, kas ir pievienots organizācijas struktūrvienībai.
    2. Izmaksu cenrādis, kas ir pievienots projekta pakalpojumu parametriem. Tā kā projekta pakalpojumu parametriem var pievienot izmaksu cenrāžus daudzās valūtās, PSA veic valūtu saskaņošanu starp projekta, līguma vai piedāvājuma līgumslēdzēja organizācijas struktūrvienību un izmaksu cenrādi.
    3. Attiecībā uz izdevumiem pašizmaksas un izmaksu uzcenojuma izcenojuma metodes neattiecas uz izmaksu cenrāžiem. Pat ja šīs izcenojuma metodes tiek izmantotas izmaksu cenrāža rindās, lai iestatītu transakciju kategoriju izmaksas, sistēma tās ignorē un netiek ievadīta noklusējuma izmaksu cena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]