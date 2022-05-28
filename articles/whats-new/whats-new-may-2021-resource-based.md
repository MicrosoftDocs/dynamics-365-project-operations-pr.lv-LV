---
title: Jaunumi 2021. gada maijā — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada maija Project Operations laidienam, kas paredzēts scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723777"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. gada maijā — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dynamics 365 Dataverse vidē versija 4.10.0.186
- Projektu vadība un uzskaite Finance and Operations lietotņu vidē versija 10.0.18

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- [Plānošanas režīmi](../project-management/scheduling-modes.md): projektu vadītāji var definēt, vai projektu vajadzētu pārvaldīt, izmantojot fiksēta ilguma, fiksēta darba vai fiksētu vienību plānošanas režīmu.
- [Nobraukuma iestatīšana, izmantojot nobraukuma likmes pakāpes](../expense/set-up-mileage.md): nobraukuma likmju pakāpju jaunināšana darbinieku izdevumu atskaitēs.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā sarakstā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2021. gada maija laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Projekta līdzekļu avots (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Projekta līguma klienta apmaksas nosacījumu sinhronizācija. |
| Projekta rēķinu priekšlikums V2 (invoices) | 1.0.0.3 | Pro formas rēķinu apmaksas nosacījumu sinhronizēšana. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kvalitātes atjauninājumi |
| Projekti V2 (msdyn\_projects) | 1.0.0.2 | Kvalitātes atjauninājumi |

Atjauninot projektu operāciju Dataverse risinājumu un Finance and Operations programmu risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas  **Versija**  lapā  **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma ar kartes startēšanu, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2227635 | Vērtības laukos **Vienību grupa** un **Vienība** tiek aizpildītas pēc noklusējuma no produkta režģī **Materiālu aprēķini**. |
| Cenu noteikšana un norēķini | 2234127 | Tagad lauks **Uzdevuma ID** pareizi tiek integrēts Dataverse projekta faktiskajos datos, kad tiek grāmatots piegādātāja rēķins. |
| Cenu noteikšana un norēķini | 2235564 | Saglabājot žurnāla rindu, tiek nodrošināts, ka pēc saglabāšanas valūta, kas redzama žurnāla rindas ierakstā, atbilst rindas noklusējuma valūtai. |
| Cenu noteikšana un norēķini | 2246671 | Rēķina izrakstīšanas laikā pārveidojot transakciju par rēķinā neiekļaujamu, tiek apvērsts sākotnējais rēķinā neiekļautais pārdošanas ieraksts un tiek izveidots jauns rēķinā neiekļauts pārdošanas ieraksts, kurš ir rēķinā neiekļaujams. |
| Cenu noteikšana un norēķini | 2264042 | Derīgs rēķina labojums nedrīkst tikt bloķēts, ja vidē ir nederīga rēķina labošanas informācija. |
| Cenu noteikšana un norēķini | 2146367 | Projekta rēķina galvenes duālās rakstīšanas kartējums tiek paplašināts, lai ietvertu maksājuma nosacījumus. |
|   Iespēju pārvaldība | 2086888 | Nepievienojiet lomas un kategorijas, kas tiek deaktivizētas pirms piedāvājuma kopēšanas, tikko nokopēta piedāvājuma rēķinā iekļaujamajām lomām un kategorijām. |
|   Iespēju pārvaldība | 2234376 | Tikai lasāmi lauki režģī **Materiālu aprēķini** ir pelēkoti. |
|   Iespēju pārvaldība | 2238337 | Piedāvājumu, kas ir balstīts uz kontaktpersonu, var saglabāt pat tad, ja tas nav saistīts ar projekta cenrādi. |
|   Iespēju pārvaldība | 2239810 | Slēdzot piedāvājumu kā zaudētu, tiek slēgts arī saistītais projekts un tiek atceltas visas rezervācijas. |
| Projektu plānošana un izsekošana | 2099559 | Pirms režģa **Projekta uzdevumi** atvēršanas tika pievienotas sistēmas darbspējas papildu validācijas. |
| Projektu plānošana un izsekošana | 2178987 | Novērsta īslaicīga kļūda, kas rodas, atlasot **Nākamais posms** lapā **Projekts**. |
| Resursu pārvaldība | 2224817 | Funkcionalitātei, kas ļauj paplašināt rezervācijas, pēc noklusējuma tiek iestatīts pareizais rezervācijas statuss. |
| Laika ieraksts | 2202476 | Lapā **Laika ieraksts** tagad tiek izmantota reaktīvā režģa vadīkla, un tiek novērstas tādas problēmas kā režģa nesalāgotība. |
| Laika ieraksts | 2223377 | Laika ieraksts ir paslēpts no sadaļas **Saistīts** lapā **Rezervējams resurss**, lai izvairītos no lietojamības pārpratumiem. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Programmā Project Operations uz resursiem balstītie scenāriji: integrācijas kļūdas dēļ piedāvājumu nevar pārvērst kā iegūtu. |
| Projektu pārvaldība un uzskaite | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: rodas kļūda, mēģinot saistīt līguma līniju ar projekta ID, jo tiek pārbaudīta līguma rindu un darījumu veidu pārklāšanās. |
| Projektu pārvaldība un uzskaite | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** iestata līdzekļu avota rēķina adresi no cita klienta. |
| Komandējumi un izdevumi | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Var rasties ar nobraukuma iestatīšanu saistīta grāmatošanas kļūda. |
| Komandējumi un izdevumi | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Izdevumu transakcijām ārzemju valūtā nedarbojas funkcionalitāte **Sadalīt pie personīgajām**. |
| Komandējumi un izdevumi | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Izdevumu kategorijas nolaižamajā vērtību sarakstā tiek rādītas nepareizas pārstāvju kategorijas neatkarīgi no tā, vai tie ir iestatīti kā resurss. |
| Komandējumi un izdevumi | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Nevar saglabāt starpuzņēmumu izdevumu atskaiti, jo radusies kļūda **Resursu/kategorijas validācija**. |
| Komandējumi un izdevumi | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Nepareizajam attāluma aprēķinam izdevumu atskaites grāmatojumā ir sadalītas rindas. |
| Komandējumi un izdevumi | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Kad ir iekļauts pārdošanas rēķins un nobīdes konta tips apmaksas metodē ir **Darbinieks**, nevar grāmatot cita veida starpuzņēmumu izdevumu atskaiti. |
| Komandējumi un izdevumi | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Atsauktā datu entītija **TrvRequisitionLine** un unikālais indekss ir saistīti. |
| Komandējumi un izdevumi | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Izmaksu atskaite atbalsta avota dokumentu rindu izveidi un atjaunināšanu. |
| Komandējumi un izdevumi | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Starpuzņēmumu scenārijā tiek rādīts nepareizs apakšgrāmatas žurnāls, ja pārdošanas nodoklis tiek grāmatots mērķa juridiskajā entītijā. |
| Komandējumi un izdevumi | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: izdevumu novērtējums netiek dzēsts no Finance, kad tas tiek dzēsts no Dataverse. |
| Komandējumi un izdevumi | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ja izdevumu kategorija ir kategorija, kas nav projekta kategorija, lapā **Izdevumi** atlasītās finanšu dimensijas netiek kopētas izdevumu pārskatā. |
