---
title: Kas jauns vai mainījies pakalpojumā Project Operations 2021. gada oktobrī attiecībā uz krājumu/ražošanas scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada oktobra laidienā Project Operations krājumu un ražošanas scenārijiem.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Kas jauns vai mainījies pakalpojumā Project Operations 2021. gada oktobrī attiecībā uz krājumu/ražošanas scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.22.
 
## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
|--------------|------------------|----------------|
| Projektu pārvaldība un uzskaite | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Notiekoša projekta (WIP) un uzkrāto ieņēmumu summas netiek pareizi atgrieztas, grāmatojot starpuzņēmumu klienta rēķinu. |
| Projektu pārvaldība un uzskaite | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcionalitāte **Novērst projekta slēgšanu, ja ir atvērtas transakcijas** nedarbojas. |
| Projektu pārvaldība un uzskaite | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Norēķinu klasifikācija brīvā teksta rēķinā netiek automātiski aizpildīta ar projektu dimensijām, ja šī funkcionalitāte ir iespējota. |
| Projektu pārvaldība un uzskaite | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Scenārijos, kas nav starpuzņēmumu scenāriji, WIP un uzkrāto ieņēmumu summas netiek pareizi atgrieztas, grāmatojot projekta rēķinu. |
| Projektu pārvaldība un uzskaite | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debeta un kredīta vērtības tiek samainītas vietām, kad pievienojumprogramma Microsoft Excel tiek izmantota kopā ar projekta izdevumu žurnālu un lauks **Nobīdes konta tips** ir iestatīts uz **Projekts**. |
| Projektu pārvaldība un uzskaite | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Summa, kas tiek grāmatota projekta transakcijās, ir pārmērīga projekta pirkuma pasūtījumā, kurā ir ietvertas krājumu vienības un kuram ir neatskaitāmas nodokļu summas, kad ir atzīmēts **UseTax**. |
| Projektu pārvaldība un uzskaite | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistēma sadala summu starp projekta peļņas un zaudējumu pārskatiem un projekta WIP pārskatiem. |
| Projektu pārvaldība un uzskaite | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Rīcībā esošie krājumi ir nepareizi pēc daļēji atgrieztas elementa prasības koriģēšanas. |
| Projektu pārvaldība un uzskaite | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resursu nosaukumi tiek dublēti programmā Project Operations, kad tie tiek rediģēti programmā Microsoft Project. |
| Projektu pārvaldība un uzskaite | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Starpuzņēmumu izdevumu pārskati, kuros ir kreditoru starpuzņēmumu gaidošas piegādātāju rēķinu izmaksas, vispirms tiek grāmatoti grāmatošanas tipā **Projekta WIP izmaksas**. Taču apstrādes laikā ar aprēķiniem saistītās izmaksas tiek grāmatotas grāmatošanas tipā **Projekta izmaksas**, nevis paredzētajā grāmatošanas tipā **Starpuzņēmumu izmaksas**. |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Netiek rādīti piegādātāju uzkrājumu rezultāti projekta izdevumu transakcijās. |
| Projektu pārvaldība un uzskaite | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Laika uzskaites tabulai ir jānoapaļo transakcijas summa transakcijas valūtā līdz noteiktam decimāldaļu skaitam visās uzskaites sadalēs un virsgrāmatas žurnāla sadalījuma ierakstos. |
| Projektu pārvaldība un uzskaite | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekta elementu prasību daudzums tiek automātiski atjaunināts, kad tiek apstiprināti plānotie pasūtījumi. |
| Projektu pārvaldība un uzskaite | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Dokumenta numuru, transakcijas tipa piegādātāja bilanci un uzņēmuma numuru nevar atgriezt pirkuma pasūtījuma priekšapmaksas rēķinā. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kad ir ieslēgta piegādātāju rēķinu integrācija, tiek pārtraukts starpuzņēmumu piegādātāju rēķins. |
| Projektu pārvaldība un uzskaite | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Izveidojot projekta izdevumu žurnālu, izmaksu summa tiek rādīta laukā **Kredīts**. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekta rēķinu apmaksas nosacījumi nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Laika uzskaites tabulu dokumentus var lietot atkārtoti, ja skaitļu secība ir iestatīta kā nepārtraukta. |
| Projektu pārvaldība un uzskaite | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJĀ: loģika **Manuālās saglabāšanas summa** neatbilst loģikai **Automātiskās saglabāšanas summa** projekta līguma rēķina priekšlikumā. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Izlaižot piegādātāja saglabāšanu, dokumentu grāmatojumam ir nepareizas papildu rindas. |
| Projektu pārvaldība un uzskaite | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kad lauks **Rēķina datums** lapā **Rēķina priekšlikuma izveide** tiek mainīts, var rasties šāda kļūda: “Kā objekta atsauce nav iestatīts objekta gadījums”. |
| Projektu pārvaldība un uzskaite | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Rodas kļūda, mēģinot apstiprināt laika uzskaites tabulu no **TSLine** darbplūsmas, un pastāv laika uzskaites tabula sestdienai un svētdienai. |
| Projektu pārvaldība un uzskaite | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Sākuma bilances projekta vienuma tips tiek izslēgts no sadaļas **Rēķinu priekšlikumu transakciju kopsavilkumi**, kad tiek aprēķināta rēķina priekšlikuma kopsumma. |
| Projektu pārvaldība un uzskaite | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ja projekta ražošanas pasūtījumā patēriņa izmaksas ir 0 (nulle), tad, mēģinot veikt aprēķinus, rodas šāda kļūda: “Mēģinājums dalīt ar nulli”. |
| Projektu pārvaldība un uzskaite | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Project Timesheet Android mobilā programma pārstāj reaģēt. Šī problēma ir saistīta ar **TimeEntryDataManager ArgumentNullException**. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kad tiek grāmatots Project Operations integrācijas žurnāls, tas neizdodas, jo kontam trūkst dimensiju. Tomēr konts, kuram trūkst dimensiju, nav tas konts, kurā notiek grāmatošana. |
| Projektu pārvaldība un uzskaite | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Meklēšanas filtrs **ToDate** netiek notīrīts, kad tas tiek noņemts no dialoglodziņa **Atlasīt** lapā **Grāmatot izmaksas**. |
| Projektu pārvaldība un uzskaite | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Atiestatīt visu sadali** neizdodas, un tiek parādīta kļūda laika uzskaites tabulām, kas izveidotas projektam ar tipu **Tikai laiks**. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Cilne **Projekts** nav rediģējama gaidošā piegādātāja rēķinā, kad sagādes kategorija ir piešķirta vienumam. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Nav navigācijas rūts, ja neesat pieteicies programmā Project Operations Dataverse. |
| Projektu pārvaldība un uzskaite | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Attiecībā uz starpuzņēmumu projektu korekciju transakcijām rodas problēmas mērķa uzņēmumā. |
| Projektu pārvaldība un uzskaite | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekta iesniegtās izmaksas aprēķina nepareizu daudzumu un izmaksas, ja pirkuma pasūtījumu virsgrāmatā apstrādā ar **Pirkuma pasūtījuma gada beigu procesu**. |
| Projektu pārvaldība un uzskaite | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kad projekta ražošanas pasūtījums, kam ir kvalitātes pasūtījumi, tiek ziņots kā pabeigts, rodas šāda kļūda: “Neviena virtuāla transakcija nav atzīmēta ar krājumu transakciju”. |
| Projektu pārvaldība un uzskaite | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kad tiek grāmatots ar projektu saistīts kreditoru rēķins, rodas šāda kļūda: “Uzskaitīts teksta projekts — izmaksas — vienums nepastāv”. |
| Projektu pārvaldība un uzskaite | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Netiešās izmaksas tiek dubultotas, kad manuāli tiek uzkrāti ieņēmumi. |
| Projektu pārvaldība un uzskaite | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Ieņēmumu uzkrāšana un WIP grāmatošana nerada transakcijas. |
| Projektu pārvaldība un uzskaite | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Gaidošās cenas aktivizēšana neizdodas standarta izmaksu vienumam, ja pastāv saņemts projekta pirkuma pasūtījums. |
| Projektu pārvaldība un uzskaite | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | WIP apgrieztā vērtība no rēķina grāmatošanas atšķiras no laika ieraksta sākotnējās iegrāmatotās WIP vērtības. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Rodas grāmatošanas problēma ar projekta rēķinu ieņēmumiem atbilstošos honorāru gadījumos, kad dokumenta transakcijas netiek pareizi līdzsvarotas. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Aprēķina izveide pēc rēķina priekšlikuma grāmatošanas bloķē labojumu rindu importēšanu programmā Project Operations. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nevar modificēt atskaites punktu ierakstus ar pilnībā izrakstītu rēķinu. |
| Projektu pārvaldība un uzskaite | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Lietojot automātiskās maksas, starpuzņēmumu klienta rēķinu par laika uzskaites tabulu nevar grāmatot, un tiek parādīts kļūdas ziņojums. |
| Projektu pārvaldība un uzskaite | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adrese apakšprojektā netiek pareizi atjaunināta. |
| Projektu pārvaldība un uzskaite | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Preču prasību izmaksas tiek atjauninātas ar konsolidēto pirkumu pasūtījumu iegādes cenu. |
| Projektu pārvaldība un uzskaite | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Grāmatotās izmaksas nav pareizas pēc tam, kad ir atjaunināta pirkuma cena un iespējots parametrs **Aktivizēt izmaiņu pārvaldību**. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visus lietotāja izdevumus var redzēt, meklējot kategoriju izdevumu mobilajā programmā. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas piegādātāju transakcijās un pārdošanas nodokļu transakcijās tiek grāmatotas no izdevumiem, kas tika izveidots no kredītkaršu transakcijām. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot izdevumu pārskatu lapas, tiek parādīts nesaistīts brīdinājums. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Tiek izmantots nepareizais pagaidu apstiprinātājs, kad dzēšat pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzat, izmantojot darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas ar nobraukuma iestatīšanu saistīta grāmatošanas kļūda. |
| Komandējumi un izdevumi | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Sadale neatjaunina juridisko personu, kad izdevumu pārskatam starpuzņēmumu izdevumos tiek atkārtoti pievienota nepiesaistīta transakcija. |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par reglamentējošajiem atjauninājumiem finanšu un operāciju programmās skatiet sadaļā [Reglamentējošie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties Microsoft Dynamics Lifecycle Services (LCS) un izmantot problēmu meklēšanas rīku, lai skatītu plānotos regulēšanas atjauninājumus. Problēmu meklēšana ļauj meklēt pēc valsts vai reģiona, līdzekļa tipa un laidiena.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
