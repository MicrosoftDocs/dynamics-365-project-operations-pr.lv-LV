---
title: Kas jauns vai mainīts Project Operations, 2021. gada oktobris, krājumos/ražošanā balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada oktobra projekta operāciju laidienā uz krājumiem/ražošanu balstītiem scenārijiem.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029952"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Kas jauns vai mainīts Project Operations, 2021. gada oktobris, krājumos/ražošanā balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.22
 
## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
|--------------|------------------|----------------|
| Projektu pārvaldība un uzskaite | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projekta darbs procesā (WIP) un uzkrātās ieņēmumu summas netiek pareizi apgrieztas, kad tiek grāmatots starpuzņēmumu debitora rēķins. |
| Projektu pārvaldība un uzskaite | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcionalitāte **Novērst projekta slēgšanu, ja pastāv** atvērtas transakcijas, nedarbojas. |
| Projektu pārvaldība un uzskaite | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Norēķinu klasifikācija brīvā teksta rēķinā automātiski neaizpilda projektu dimensijas, ja šī funkcionalitāte ir iespējota. |
| Projektu pārvaldība un uzskaite | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Scenārijos, kas nav saistīti ar starpuzņēmumiem, NP un uzkrātās ieņēmumu summas netiek pareizi apgrieztas, kad tiek grāmatots projekta rēķins. |
| Projektu pārvaldība un uzskaite | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debeta un kredīta vērtības tiek mainītas, Microsoft Excel ja pievienojumprogramma tiek izmantota kopā ar žurnālu Projekta izdevumi un lauks **Offset konta tips** ir iestatīts uz **Projekts**. |
| Projektu pārvaldība un uzskaite | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Summa, kas ir grāmatota projekta transakcijās, ir pārvērtēta projekta pirkšanas pasūtījumā, kurā ir iekļauti krājumos glabātie krājumi un kuram ir neatskaitāmas nodokļu summas, kad **tiek atzīmēts UseTax**. |
| Projektu pārvaldība un uzskaite | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistēma sadala summu starp projekta peļņas un zaudējumu pārskatiem un projekta WIP pārskatiem. |
| Projektu pārvaldība un uzskaite | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Rīcībā esošie krājumi ir nepareizi pēc tam, kad tiek koriģēta daļēji atgrieztā krājuma prasība. |
| Projektu pārvaldība un uzskaite | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resursu nosaukumi tiek dublēti project operācijās, kad tie tiek rediģēti programmā Microsoft Project. |
| Projektu pārvaldība un uzskaite | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Starpuzņēmumu izdevumu atskaites, kurās ir kreditoru parādu starpuzņēmumu gaidošās kreditoru rēķinu izmaksas, vispirms tiek grāmatotas tipā **Project WIP izmaksu** grāmatošana. Tomēr apstrādes laikā ar tāmi saistītās izmaksas tiek grāmatotas tipā **Projekta izmaksu** grāmatošana, nevis paredzētajā **starpuzņēmumu izmaksu** grāmatošanas tipā. |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Kreditoru paturēšanas rezultāti projekta izdevumu transakcijās netiek rādīti. |
| Projektu pārvaldība un uzskaite | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Darba laika uzskaites tabulā ir jānoapaļo transakcijas summa transakcijas valūtā līdz noteiktam decimāldaļu skaitam visos grāmatvedības sadalījumos un vispārējos žurnāla sadalījuma ierakstos. |
| Projektu pārvaldība un uzskaite | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekta krājumu prasību daudzumi tiek automātiski atjaunināti, kad tiek apstiprināti plānotie pasūtījumi. |
| Projektu pārvaldība un uzskaite | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Pirkšanas pasūtījuma priekšapmaksas rēķinā nevar anulēt dokumenta numuru, transakcijas tipa kreditora bilanci un konta numuru. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Starpuzņēmumu kreditora rēķins tiek bojāts, ja ir ieslēgta kreditora rēķina integrācija. |
| Projektu pārvaldība un uzskaite | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Veidojot projekta izdevumu žurnālu, izmaksu summa tiek parādīta laukā **Kredīts**. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Apmaksas noteikumi projekta rēķinos nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Darba laika uzskaites tabulas kuponi var tikt izmantoti atkārtoti, ja numerācijas secība ir iestatīta kā nepārtraukta. |
| Projektu pārvaldība un uzskaite | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: manuālās **saglabāšanas summas** loģika neatbilst automātiskās **saglabāšanas summas** loģikai projekta līguma rēķina priekšlikumā. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kad kreditora noturēšana tiek izlaista, dokumenta grāmatošanai ir nepareizas papildu rindas. |
| Projektu pārvaldība un uzskaite | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ja tiek mainīts **lauks** Rēķina datums **lapā Rēķina priekšlikuma** izveide, var rasties šāda kļūda: "Objekta atsauce nav iestatīta uz objekta instanci." |
| Projektu pārvaldība un uzskaite | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Mēģinot apstiprināt darba laika uzskaites tabulu no **TSLine** darbplūsmas, rodas kļūda, un sestdienai un svētdienai ir laika uzskaites tabulas politika. |
| Projektu pārvaldība un uzskaite | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Sākuma bilances projekta krājuma tips tiek izslēgts no **rēķina priekšlikuma transakciju kopsavilkumiem**, ja tiek aprēķināta rēķina priekšlikuma rēķina kopsumma. |
| Projektu pārvaldība un uzskaite | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ja projekta ražošanas pasūtījuma patēriņa izmaksas ir 0 (nulle), mēģinot aprēķināt, rodas šāda kļūda: "Mēģināts dalīt ar nulli". |
| Projektu pārvaldība un uzskaite | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Programma Project Timeheet Mobile, kas Android nodrošina atbildes reakcijas apturēšanu. Problēma ir saistīta **ar TimeEntryDataManager ArgumentNullException**. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations integrācijas žurnāls neizdodas, kad to publicējat, jo kontā trūkst dimensiju. Tomēr konts, kurā trūkst dimensiju, nav konts, kurā publicējat ziņojumus. |
| Projektu pārvaldība un uzskaite | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | ToDate **filtrs meklēšanā netiek notīrīts, kad tas tiek noņemts no** dialoglodziņa **Atlasīt** lapā Izmaksu likšana **.** |
| Projektu pārvaldība un uzskaite | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Visu sadalījuma atiestatīšana** neizdodas un tiek parādīta kļūda darba laika uzskaites tabulās, kas izveidotas tikai **laika tipa projektam**. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Cilne **Projekts** nav rediģējama gaidošā kreditora rēķinā, ja krājumam ir piešķirta sagādes kategorija. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Trūkst navigācijas rūts, ja neesat pieteicies project operations Dataverse. |
| Projektu pārvaldība un uzskaite | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Starpuzņēmumu projektu pielāgošanas transakcijām galamērķa uzņēmumā ir problēmas. |
| Projektu pārvaldība un uzskaite | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projektam piesaistītās izmaksas aprēķina nepareizu daudzumu un izmaksu cenu, ja pirkšanas pasūtījums tika apstrādāts, izmantojot **pirkšanas pasūtījuma gada beigu procesu** vispārējā virsgrāmatā. |
| Projektu pārvaldība un uzskaite | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kad projekta ražošanas pasūtījums, kurā ir kvalitātes pasūtījumi, tiek ziņots kā pabeigts, rodas šāda kļūda: "Nav virtuālas transakcijas, kas atzīmēta ar krājumu transakciju." |
| Projektu pārvaldība un uzskaite | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kad tiek grāmatots ar projektu saistīts kreditoru rēķins, tiek parādīta šāda kļūda: "Uzskaitīts teksts Projekts - izmaksas - krājums nepastāv." |
| Projektu pārvaldība un uzskaite | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Netiešās izmaksas tiek dubultotas, kad manuāli uzkrājat ieņēmumus. |
| Projektu pārvaldība un uzskaite | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Uzkrājiet ieņēmumus, un NP grāmatošana nerada transakcijas. |
| Projektu pārvaldība un uzskaite | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Neapstiprinātās cenas aktivizēšana standarta izmaksu krājumam neizdodas, ja pastāv saņemtais projekta pirkšanas pasūtījums. |
| Projektu pārvaldība un uzskaite | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | NP apgrieztā vērtība no rēķina grāmatošanas atšķiras no sākotnējās ievietotās NP vērtības no laika ieraksta. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ir radusies grāmatošanas problēma par projekta ieņēmumiem, par kuriem izrakstīti rēķini, lietotajos paturēšanas gadījumos, kad transakcijas kuponā nav līdzsvarā. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Aplēses izveide pēc rēķina priekšlikuma grāmatošanas bloķē labojumu rindu importēšanu programmā Project Operations. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nevajadzētu būt iespējai grozīt atskaites punktu skaitu, par kuru ir izrakstīts rēķins, pilnībā izstādītu atskaites punktu. |
| Projektu pārvaldība un uzskaite | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Ja tiek izmantotas automātiskās maksas, starpuzņēmumu debitora rēķinu par darba laika uzskaites tabulu nevar grāmatot un tiek parādīts kļūdas ziņojums. |
| Projektu pārvaldība un uzskaite | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Apakšprojekta adrese nav pareizi atjaunināta. |
| Projektu pārvaldība un uzskaite | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Krājumu prasību izmaksu cena tiek atjaunināta ar pirkšanas cenu konsolidētajiem pirkšanas pasūtījumiem. |
| Projektu pārvaldība un uzskaite | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Pēc pirkuma cenas atjaunināšanas un parametra **Activate change management (Aktivizēt izmaiņu pārvaldību**) izmaksas nav pareizas. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visi lietotāju izdevumi ir redzami, meklējot kategoriju mobilajā lietotnē Izdevumi. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas kreditoru transakciju un PVN transakciju summas tiek grāmatotas no izdevumiem, kas izveidoti no kredītkartes transakcijas. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot izdevumu pārskatu lapas, tiek parādīts neatbilstošs brīdinājuma ziņojums. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nepareizs starpposma apstiprinātājs tiek izmantots, kad izdzēšat pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzat darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas grāmatošanas kļūda, kas ir saistīta ar nobraukuma iestatīšanu. |
| Komandējumi un izdevumi | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Izplatīšana neatjaunina juridisko personu, ja transakcija bez piesaistes tiek atkārtoti pievienota izdevumu pārskatam par starpuzņēmumu izdevumiem. |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par finanšu un operāciju programmu regulatīvajiem atjauninājumiem skatiet sadaļā [Regulatīvie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties Microsoft Dynamics Lifecycle Services (LCS) un izmantot problēmu meklēšanas rīku, lai skatītu plānotos normatīvos atjauninājumus. Problēmu meklēšana ļauj meklēt pēc valsts vai reģiona, līdzekļa veida un laidiena.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
