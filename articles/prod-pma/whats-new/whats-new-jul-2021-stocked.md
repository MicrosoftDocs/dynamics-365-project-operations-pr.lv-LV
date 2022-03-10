---
title: Jaunumi vai izmaiņas 2021. gada jūlijā Project Operations krājumos/ražošanā balstītiem scenārijiem
description: Šajā tēmā ir sniegta informācija par 2021. gada jūlijā pieejamajiem kvalitātes atjauninājumiem Project Operations krājumos/ražošanā balstītiem scenārijiem.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992710"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Jaunumi vai izmaiņas 2021. gada jūlijā Project Operations krājumos/ražošanā balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.20
 
### <a name="quality-updates"></a>Kvalitātes atjauninājumi
                                                                                                                                                                                  
| Līdzekļu apgabals                      | Atsauces numurs| Kvalitātes atjauninājums                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektu pārvaldība un uzskaite | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Izmaksu saistību ieraksti no pirkšanas pieprasījuma tiek notīrīti, tiklīdz pirkuma pasūtījums ir atbrīvots no pirkšanas pieprasījuma problēmas.                                                                           |
| Projektu pārvaldība un uzskaite | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budžeta pārbaude pirkšanas pieprasījumam notiek divreiz. Šī dublēšanās nozīmē, ka pieprasījumu nevar aizvērt un atbilstošais pirkšanas pasūtījums nav izveidots.                                                                                                                        |
| Projektu pārvaldība un uzskaite | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Norēķinu kārtulu **Procenti, par kuriem jāizraksta rēķins** nevarēja pabeigt noapaļošanas problēmas dēļ.                                                                              |
| Projektu pārvaldība un uzskaite | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Pielāgojot transakciju, ja procentuālajai vērtībai ir decimāldaļas, izmaksu un pārdošanas cena netiek pareizi pielāgota.                                      |
| Projektu pārvaldība un uzskaite | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Uzskaites avota pārlūks rāda stundas atsevišķai darba laika uzskaites tabulas rindai vairākām rindām ar dažādām darbībām.                                      |
| Projektu pārvaldība un uzskaite | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Saglabātie skati un darba laika uzskaites tabulas rindu informācijas personalizēšana izraisa to, ka, mēģinot atvērt darba laika uzskaites tabulu, sistēma vienmēr atver sarakstā pirmās darba laika uzskaites tabulas informāciju.  |
| Projektu pārvaldība un uzskaite | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Pēc importēšanas projekta saknes mezgls pazūd un darba sadalījuma struktūras ieraksti tiek dzēsti.                                                                                             |
| Projektu pārvaldība un uzskaite | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Kad krājumi ir saņemti un daļēji izsniegti no krājumu vajadzībām, sistēma atjaunina nepareizu budžeta patēriņa bilanci. |
| Projektu pārvaldība un uzskaite | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Projekta uzkrājuma pirkuma pasūtījumos kopsummas netiek rādītas pareizi rūtī **Kopsummas** vai režģī **Neizlemts rēķins**.                                                                  |
| Projektu pārvaldība un uzskaite | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Noslēdzot krājumus, projekta vienumu izmaksu pielāgojumi tiek grāmatoti bilances kontā, nevis peļņas un zaudējumu kontā.                                                            |
| Projektu pārvaldība un uzskaite | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Projekta grāmatotajā transakcijas dokumentā un novērtējuma dokumentā kā uzskaites valūta tiek izmantots USD, bet summa parāda CAD ekvivalentu.              |
| Projektu pārvaldība un uzskaite | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Fiksētās izmaksas ar krājumu vajadzību un pirkuma pasūtījumu ir nepareizas pirkuma pasūtījuma rēķina procesā, kur daļēji ir produktu saņemšana un daļēji – rēķina izrakstīšana.       |
| Projektu pārvaldība un uzskaite | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projekta korekcija nepareizi atjaunina pārdošanas summu ar netiešajām izmaksām.                                                                                    |
| Projektu pārvaldība un uzskaite | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **Darba laika uzskaites** tabulai trūkst definētas relācijas ar skatu **Darbinieks/Resurss**.                                                                                   |
| Projektu pārvaldība un uzskaite | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nevar aizpildīt lauku **Darbības numurs**, to atlasot no starpuzņēmuma darba laika uzskaites tabulas nolaižamās izvēlnes.                                                                 |
| Projektu pārvaldība un uzskaite | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nevar pievienot personalizētu lauku **Mērķis** vai **Darbības apraksts** šajās lapās: **Projekta grāmatotā transakcija**, **Rēķina priekšlikuma izveide** vai **Rēķina priekšlikums**.  |
| Projektu pārvaldība un uzskaite | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Izveidojot krājumu vajadzības, izmantojot datu pārvaldību (**ProjSalesItemRequirementEntity)**, tiek nodrošināta nepareiza piegādes datuma vadīkla.                                              |
| Projektu pārvaldība un uzskaite | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Atlasot projekta līguma ID sadaļā Finanses, Project Operations integrētā vide atver lapu, lai izveidotu jaunu ierakstu, nevis atver esošo projekta līgumu.                                                                                                                 |
| Projektu pārvaldība un uzskaite | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Etiķete "@SYS4083080" ("Nevar atrast unikālu darbinieka ierakstu, kas atbilst ievadītajām vērtībām") netiek tulkota dāņu valodā.                                |
| Projektu pārvaldība un uzskaite | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Lauks **Krājumu PVN grupa** nav rediģējams rēķina priekšlikumā.                                                                               |
| Projektu pārvaldība un uzskaite | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Fiksētās izmaksas ir pārmērīgas ar neatskaitāmo nodokļu summām.                                                                                                    |
| Projektu pārvaldība un uzskaite | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Grāmatojot starpuzņēmuma darba laika uzskaites tabulu ar vairākiem projektiem un dažādām finanšu dimensijām, tiek ģenerētas neparedzētas vērtības virsgrāmatā.                             |
| Projektu pārvaldība un uzskaite | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Rēķina priekšlikuma rindas tiek dublētas, jo vairāki periodiskā procesa **Importēt no izstādīšanas** gadījumi tiek izpildīts vienlaikus.                                      |
| Projektu pārvaldība un uzskaite | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Kredīta notas rēķina priekšlikumā ir kļūda, tāpēc transakcijas dokumentā nav līdzsvarotas.    |
| Projektu pārvaldība un uzskaite | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Projekta fiksētās izmaksas kļūst nepareizas pēc aizturēto neizlemto rēķinu atbrīvošanas.                                                                             |
| Projektu pārvaldība un uzskaite | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Projekta pārdošanas pasūtījumam nevar izveidot kredīta notu, ja nodokļu valūta atšķiras no uzņēmuma valūtas.                                      |
| Projektu pārvaldība un uzskaite | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Dzēšot līgumu, tiek dzēsta arī ar klientu saistītā adrese.                                                                                     |
| Projektu pārvaldība un uzskaite | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Nevar grāmatot rēķina priekšlikumu, kas izriet no negatīva laika transakcijas korekcijas.                                                                    |
| Komandējumi un izdevumi                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Izdevumu pārskatos nodoklis tiek aprēķināts atšķirīgi.                                                                                                                  |
| Komandējumi un izdevumi                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Laidiena atjauninājums **DB72_Expense.updateTrvExpTransProjTransId()** neļauj **trvExpTrans.ReferenceDataAreaId** izveidot jaunu numuru sēriju.                    |
| Komandējumi un izdevumi                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Summas lauks netiek rādīts ar obligāto lauku.                                                                                                             |
| Komandējumi un izdevumi                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Uzlabojumi, kas saistīti ar izdevumu pievienošanu izdevumu pārskatam, izmantojot lietotāja saskarni Jauna veida izdevumi.                                                            |
| Komandējumi un izdevumi                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Varat dzēst grāmatotās izdevumu atskaites.                                                                                           |
| Komandējumi un izdevumi                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Izdevumu politikas ziņojums tiek parādīts vairākas reizes.                                                                                                       |
| Komandējumi un izdevumi                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Lauks **Maksāšanas metode** tiek iekļauts rūtī **Jaunas izmaksas**.                                                                                                      |
| Komandējumi un izdevumi                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Ja darbplūsma nav atrasta, rīkam **Atiestatīt izdevumu dokumenta statusu** vajadzētu atiestatīt izdevumu atskaites statusu uz **Melnraksts**. 

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi
Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties Lifecycle Services (LCS) un skatīt plānotos regulēšanas atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
