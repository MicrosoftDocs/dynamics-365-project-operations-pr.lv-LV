---
title: Jaunumi vai izmaiņas projektu darbībās, 2021. gada oktobris attiecībā uz uzkrātajiem/uz ražošanu balstītajiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada oktobra projektu operāciju laidienā uzkrātajiem/uz ražošanu balstītiem scenārijiem.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933685"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Jaunumi vai izmaiņas projektu darbībās, 2021. gada oktobris attiecībā uz uzkrātajiem/uz ražošanu balstītajiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.22
 
## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
|--------------|------------------|----------------|
| Projektu pārvaldība un uzskaite | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Nepabeigtais projekta darbs (NP) un uzkrātās ieņēmumu summas netiek pareizi anulētas, grāmatojot starpuzņēmumu debitora rēķinu. |
| Projektu pārvaldība un uzskaite | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcionalitāte **Novērst projekta slēgšanu, ja pastāv atvērtas** darbības, nedarbojas. |
| Projektu pārvaldība un uzskaite | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Norēķinu klasifikācija brīva teksta rēķinā automātiski neaizpilda projektu dimensijas, ja šī funkcionalitāte ir iespējota. |
| Projektu pārvaldība un uzskaite | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Scenārijos, kas nav starpuzņēmumi, NP un uzkrātās ieņēmumu summas netiek pareizi anulētas, grāmatojot projekta rēķinu. |
| Projektu pārvaldība un uzskaite | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debeta un kredīta vērtības tiek pārslēgtas, Microsoft Excel ja pievienojumprogramma tiek izmantota kopā ar projekta izdevumu žurnālu un **lauks Korespondējošā konta tips** ir iestatīts uz **Projekts**. |
| Projektu pārvaldība un uzskaite | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projekta darbībās grāmatotā summa ir pārspīlēta projekta pirkšanas pasūtījumā, kas ietver uzkrātos krājumus, un kam ir neatskaitāmas nodokļu summas, atzīmējot **UseTax**. |
| Projektu pārvaldība un uzskaite | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistēma sadala summu starp projekta peļņas un zaudējumu pārskatiem un projekta NP pārskatiem. |
| Projektu pārvaldība un uzskaite | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Rīcībā esošie krājumi nav pareizi pēc daļēji atgrieztās krājumu vajadzības koriģēšanas. |
| Projektu pārvaldība un uzskaite | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resursu nosaukumi tiek dublēti programmā Project Operations, kad tie tiek rediģēti programmā Microsoft Project. |
| Projektu pārvaldība un uzskaite | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Starpuzņēmumu izdevumu pārskati, kuriem ir kreditoru starpuzņēmumu gaidošās kreditora rēķina izmaksas, vispirms tiek grāmatoti **projekta NP izmaksu** grāmatošanas tipā. Tomēr apstrādes laikā ar budžetu saistītās izmaksas tiek grāmatotas **projekta izmaksu** grāmatošanas tipā, nevis paredzētajā **starpuzņēmumu izmaksu** grāmatošanas tipa vietā. |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Kreditora uzkrājumu rezultāti projekta izdevumu darbībās netiek rādīti. |
| Projektu pārvaldība un uzskaite | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Darba laika uzskaites tabulai ir jānoapaļo darbības summa transakcijas valūtā līdz noteiktam decimāldaļu skaitam visos uzskaites sadales un virsgrāmatas žurnāla piešķiršanas ierakstos. |
| Projektu pārvaldība un uzskaite | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekta krājumu vajadzību daudzumi tiek automātiski atjaunināti, kad plānotie pasūtījumi tiek apstiprināti. |
| Projektu pārvaldība un uzskaite | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Pirkšanas pasūtījuma priekšapmaksas rēķinā dokumenta numuru, darbības tipa kreditora bilanci un konta numuru nevar atsaukt. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Starpuzņēmumu kreditora rēķins tiek sadalīts, kad ir ieslēgta kreditora rēķinu integrācija. |
| Projektu pārvaldība un uzskaite | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Veidojot projekta izdevumu žurnālu, izmaksu summa tiek parādīta laukā **Kredīts**. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Apmaksas nosacījumi projektu rēķinos nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Darba laika uzskaites tabulas dokumentus var izmantot atkārtoti, ja numuru sērija ir iestatīta kā nepārtraukta. |
| Projektu pārvaldība un uzskaite | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: **manuālās ieturējumu summas** loģika neatbilst automātiskās **ieturējuma summas** loģikai projekta līguma rēķina priekšlikumā. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kad kreditora ieturējums ir nodots izpildei, dokumenta grāmatošanai ir nepareizas papildu rindas. |
| Projektu pārvaldība un uzskaite | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Mainot lapas Rēķina priekšlikuma** izveide lauku **Rēķina datums**, var rasties šāda kļūda: "Objekta atsauce nav iestatīta uz objekta instanci." |
| Projektu pārvaldība un uzskaite | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Mēģinot apstiprināt darba laika uzskaites tabulu no **TSLine** darbplūsmas, rodas kļūda, un sestdienai un svētdienai ir darba laika uzskaites tabulas politika. |
| Projektu pārvaldība un uzskaite | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Sākuma bilances projekta krājuma tips ir izslēgts no **rēķina priekšlikuma darbību kopsavilkumiem**, kad tiek aprēķināta rēķina priekšlikuma rēķina kopsumma. |
| Projektu pārvaldība un uzskaite | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ja patēriņa izmaksas projekta ražošanas pasūtījumā ir 0 (nulle), mēģinot novērtēt, rodas šāda kļūda: "Mēģināja dalīt ar nulli". |
| Projektu pārvaldība un uzskaite | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Projekta darba laika uzskaites tabulas mobilā programma Android pārstāj reaģēt. Problēma ir saistīta **ar TimeEntryDataManager ArgumentNullException**. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Projekta operāciju integrācijas žurnāls neizdodas, kad to grāmatojat, jo kontam trūkst dimensiju. Tomēr konts, kurā trūkst dimensiju, nav konts, kurā grāmatojat. |
| Projektu pārvaldība un uzskaite | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | **ToDate** filtrs meklēšanā netiek notīrīts, ja tas ir noņemts no dialoglodziņa **Atlasīt** **lapā Izmaksu** grāmatošana. |
| Projektu pārvaldība un uzskaite | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Atiestatīt visu sadali** neizdodas, un tiek parādīta kļūda darba laika uzskaites tabulās, kas izveidotas tikai **laika tipa projektam**. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Cilne **Projekts** nav rediģējama gaidošajā kreditora rēķinā, ja precei ir piešķirta sagādes kategorija. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigācijas rūts trūkst, ja neesat pieteicies projekta operācijās Dataverse. |
| Projektu pārvaldība un uzskaite | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Starpuzņēmumu projekta korekcijas darbībām mērķa uzņēmumā ir problēmas. |
| Projektu pārvaldība un uzskaite | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekta fiksētās izmaksas aprēķina nepareizu daudzumu un izmaksu cenu, ja pirkšanas pasūtījums tika apstrādāts pirkšanas **pasūtījuma gada beigu procesā** Virsgrāmatā. |
| Projektu pārvaldība un uzskaite | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kad projekta ražošanas pasūtījums, kuram ir kvalitātes pasūtījumi, tiek paziņots par pabeigtu, rodas šāda kļūda: "Nav virtuālas darbības, kas atzīmēta ar krājumu darbību." |
| Projektu pārvaldība un uzskaite | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Grāmatojot ar projektu saistītu kreditoru rēķinu, rodas šāda kļūda: "Uzskaitītais teksts Projekts - izmaksas - krājums nepastāv." |
| Projektu pārvaldība un uzskaite | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Netiešās izmaksas tiek dubultotas, manuāli uzkrājot ieņēmumus. |
| Projektu pārvaldība un uzskaite | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Uzkrāt ieņēmumus un NP grāmatošana nerada darbības. |
| Projektu pārvaldība un uzskaite | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Gaidošās cenas aktivizēšana standarta izmaksu krājumam neizdodas, ja pastāv saņemtais projekta pirkšanas pasūtījums. |
| Projektu pārvaldība un uzskaite | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Np-reversed vērtība no rēķina grāmatošanas atšķiras no sākotnēji iegrāmatotās DIS vērtības no laika ieraksta. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Attiecinātajos aizturētāju gadījumos, kad dokumenta darbības nav līdzsvarā, projekta rēķinos iekļautajiem ieņēmumiem ir grāmatošanas problēma. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Novērtējuma izveide pēc rēķina priekšlikuma iegrāmatošanas bloķē labojumu rindu importēšanu projekta operācijās. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nevajadzētu būt iespējai grozīt milestone record, par kuru ir pilnībā izrakstīts rēķins. |
| Projektu pārvaldība un uzskaite | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Ja tiek izmantotas automātiskās izmaksas, nevar grāmatot starpuzņēmumu debitora rēķinu darba laika uzskaites tabulai, un tiek parādīts kļūdas ziņojums. |
| Projektu pārvaldība un uzskaite | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adrese apakšprojektā nav pareizi atjaunināta. |
| Projektu pārvaldība un uzskaite | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Krājumu vajadzību izmaksu cena tiek atjaunināta ar pirkšanas cenu konsolidētajiem pirkšanas pasūtījumiem. |
| Projektu pārvaldība un uzskaite | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Grāmatotās izmaksas nav pareizas pēc pirkšanas cenas atjaunināšanas un parametra **Aktivizēt izmaiņu pārvaldību** aktivizēšanas. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visus lietotāja izdevumus var redzēt, meklējot kategoriju mobilajā lietotnē Izdevumi. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas kreditoru darbībām un PVN darbībām tiek grāmatotas no izdevumiem, kas izveidoti no kredītkartes darbības. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot izdevumu pārskata lapas, tiek parādīts neatbilstošs brīdinājuma ziņojums. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nepareizs pagaidu apstiprinātājs tiek izmantots, dzēšot pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzot darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas grāmatošanas kļūda, kas saistīta ar nobraukuma iestatīšanu. |
| Komandējumi un izdevumi | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Sadale neatjaunina juridisko personu, ja nepiesaistītā darbība tiek atkārtoti pievienota starpuzņēmumu izdevumu pārskatam. |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par finanšu un operāciju lietotņu regulatīvajiem atjauninājumiem skatiet rakstā [Regulatīvie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties Microsoft Dynamics dzīves cikla pakalpojumos (LKA) un izmantot problēmu meklēšanas rīku, lai skatītu plānotos regulatīvos atjauninājumus. Problēmu meklēšana ļauj meklēt pēc valsts vai reģiona, līdzekļa veida un izlaišanas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
