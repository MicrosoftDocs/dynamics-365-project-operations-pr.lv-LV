---
title: Jaunumi 2021. gada jūlijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā tēmā ir sniegta informācija par 2021. gada jūlijā pieejamajiem kvalitātes atjauninājumiem Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433527"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. gada jūlijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

   - Project Operations Microsoft Dataverse vides versijā 4.12.0.148.
   - Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.20.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Spēja administratoriem iestatījumu izvēlnē skatīt PSS žurnālus un operāciju kopu žurnālus. Ieraksti tiek glabāti 90 dienas.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu.

Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Aktivizējiet jaunu kartes versiju, atlasot **Tabulas karšu versijas**, atlasot jaunāko versiju un pēc tam saglabājot atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, sākot karti, rodas problēma, izpildiet instrukcijas dubultās rakstīšanas problēmu novēršanas ceļvedī sadaļā [Kartes trūkstošu tabulas kolonnu problēma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals**              | **Atsauces numurs** | **Kvalitātes atjauninājums**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cenu noteikšana un norēķini           | 2224046              | **Transakciju klases** lauks ir rediģējams cilnē **Piedāvājuma rindas detalizēta informācija**, bet tiek bloķēts, strādājat no lapas **Piedāvājuma rindas detalizēta informācija**.                                                                     |
| Cenu noteikšana un norēķini           | 2224400              | Darbība **Slēgt piedāvājumu kā iegūtu** neizdodas, ja piedāvājumam nav datuma atskaites punktu.                                                                                                                                    |
| Cenu noteikšana un norēķini           | 2234089              | Manuāli ievadot produkta aprakstu, pēc materiālu aprēķina daudzuma ievadīšanas tas tiek notīrīts.                                                                                                                         |
| Cenu noteikšana un norēķini           | 2234100              | Režģī **Uzdevumu norēķinu iestatījumi** nav iekļauta kolonna **Materiāli** un tās vērtība projekta cilnē **Uzdevumu norēķini**.                                                                                                       |
| Cenu noteikšana un norēķini           | 2277409              | Produkta ID nav pieejams līguma rindas detalizētajā informācijā materiālu veida rindai.                                                                                                                                        |
| Cenu noteikšana un norēķini           | 2281728              | Izveidojot līguma līniju, nevajadzīgi tiek pārvērtētas faktiskās vērtības, tādējādi ievērojami palielinot datu apjomu, kas ietekmē veiktspēju.                                                                                |
| Cenu noteikšana un norēķini           | 2298668              | Netiek noņemtas žurnāla rindas, kas saistītas ar atsauktiem un dzēstiem izdevumiem.                                                                                                                                     |
| Cenu noteikšana un norēķini           | 2300192              | Kad vairāki lietotāji rediģē rēķinu, apstiprinātā rēķinā var izveidot jaunu rēķina rindas detalizēto informāciju.                                                                                   |
| Cenu noteikšana un norēķini           | 2301569              | Rēķinus nevar izlabot, ja ir lietots \$0 summas honorārs.                                                                                                                                        |
| Cenu noteikšana un norēķini           | 2307965              | Rodas kļūda, ja kategorijas cena tiek izveidota ar trūkstošām vērtībām.                                                                                                                           |
| Cenu noteikšana un norēķini           | 2326870              | **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** rodas kļūda, ja **producttypecode** ir Null.                                                                            |
| Cenu noteikšana un norēķini           | 2332732              | Kļūda rodas, ja līguma rindas atskaites punkts tiek izveidots bez pasūtījuma rindas.                                                                                                                |
| Projektu plānošana un izsekošana | 2181094              | Projekta plānošanas API tagad atbalsta PSS žurnālus un operāciju kopu žurnālus, kas tiek glabāti 90 dienas.                                                                                                                  |
| Projektu plānošana un izsekošana | 2254201              | Etiķete **Plānošanas režīms** tiek atjaunināta ar detalizētu informāciju, kas apraksta noklusējuma loģiku.                                                                                                                                      |
| Projektu plānošana un izsekošana | 2300252              | Atbildes kešatmiņa **openProject** tiek atjaunināta un kešatmiņas atslēgā ietver marķiera īpašnieku,  **pamata URL** un **Segmenta URL**, lai **Pieprasījuma URL** vienmēr varētu tikt atkārtoti izveidots gadījumā, ja mainās **pamata URL**. |
| Projektu plānošana un izsekošana | 2301312              | **msdyn_membershipstatus** ir noņemts no skata **Projekta darba grupas dalībnieks**.                                                                                                                                        |
| Projektu plānošana un izsekošana | 2302759              | Produkti tiek nevajadzīgi ienesti cilnēs **Resursu piešķiršana**, **Aprēķini** un **Izmaksu aprēķini**.                                                                                                        |
| Projektu plānošana un izsekošana | 2308050              | **CopyProject** neizdodas šādas kļūdas dēļ: "Neizdevās iegūt marķieri, lai sazinātos ar attālo servisu".                                                                                                                           |
| Projektu plānošana un izsekošana | 2322650              | Skats **Projekta uzdevumu saraksts** ir atjaunināts, lai pēc noklusējuma parādītu uzdevuma datumu.                                                                                                            |
| Projektu plānošana un izsekošana | 2327266              | Kopējot aprēķinus, **CopyProject** ģenerē kļūdu "Atslēga nav atrasta vārdnīcā".                                                                                                      |
| Projektu plānošana un izsekošana | 2328123              | **CopyProject** ģenerē kļūdu "Neizdevās iegūt marķieri, lai sazinātos ar attālo servisu".                                                                                                                          |
| Projektu plānošana un izsekošana | 2336258              | **CopyProject** nepareizi kopē resursu pozīciju nosaukumus.                                                                                                                                                 |
| Cenu noteikšana un norēķini           | 2224476              | Lauks **Rezervējams resurss** neatbilst lietotājam, kurš ir pieteicies lapā **Materiālu lietojums**.                                                                                                            |
| Resursu pārvaldība           | 2277249              | Atjauninot resursu vajadzību, kas nav balstīta uz projektu, rodas kļūda.                                                                                                            |
| Resursu pārvaldība           | 2323869              | Resursu lietojums neatpazīst pareizi filtrētos resursus.                                                                                                                                             |
| Laiks un izdevumi              | 2176538              | Vadīklai **Laika ievade** tiek izmantoti nepareizi filtru operatori.                                                                                                                                                   |
| Laiks un izdevumi              | 2177462              | Dzēšot laika ierakstu režģī, pogu **Iesniegt**, **Atsaukt**, **Dzēst** un **Rediģēt ierakstu** statuss netiek atjaunināts kā paredzēts.                                                                                        |
| Laiks un izdevumi              | 2299985              | **TimeEntriesImportFromResourceAssignment** neuztur sākuma/beigu laiku no piešķīruma.                                                                                                  |
| Laiks un izdevumi              | 2318426              | Pēc laika ieraksta iesniegšanas bloķētus laukus joprojām var rediģēt.                                                                                                                                   |
| Laiks un izdevumi              | 2323749              | Kļūda rodas, ja izdevumi tiek izveidoti no rezervējamā resursa cilnes **Saistīts**.                                                                                                      |
| Laiks un izdevumi              | 2327678              | Izveidojot laika ierakstu no rezervējamā resursa cilnes **Saistīts**, primārais resurss netiek nodots laika ievades vadīklai.                                                                            |
| VispārīgI                       | 2296857              | Norises izsekošana ilgas darbības uzdevumiem.                                                                                                                                                                        |
| VispārīgI                       | 2253682              | Project Operations duālās rakstīšanas risinājums nav jāinstalē, ja duālās rakstīšanas kodols ir instalēts vidē bez duālās rakstīšanas saskaņošanas risinājuma.                                                |
| VispārīgI                       | 2316420              | Project Service pamata nodrošināšana neizdodas, ja tiek mainīta programmas lietotāja struktūrvienība.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projekta pārvaldība un uzskaite pakalpojumā Dynamics 365 Finance

| Līdzekļu apgabals                      | Atsauces numurs | Kvalitātes atjauninājums                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektu pārvaldība un uzskaite | 4620267          | Nevar personalizēt formas, lai pievienotu lauku **Mērķis** lapās **Projekta grāmatotā transakcija**, **Rēķina priekšlikuma izveide** un **Rēķina priekšlikums**.                                                                                                                                                                                         |
| Projektu pārvaldība un uzskaite | 4613449          | Atlasot projekta līguma ID sadaļā Finanses, Project Operations integrētā vide atver lapu, lai izveidotu jaunu ierakstu, nevis jau izveidoto projektu līgumu lapu.                                                                                                                                           |
| Projektu pārvaldība un uzskaite | 4614445          | Project Operations integrētajā scenāriju izvietošanā nevar rediģēt lauku **Krājumu PVN grupa** rēķina priekšlikumā, kas importēts no izstādīšanas. Krājumu PVN grupai ir jābūt rediģējamai atvērtā rēķina priekšlikumā visos transakciju veidos, tostarp attiecībā uz uzņēmumu, stundām, izdevumiem, maksām un krājumiem. |
| Projektu pārvaldība un uzskaite |                  | Nevar grāmatot rēķina priekšlikumu, kas izriet no negatīva laika transakcijas korekcijas.                                                                                                                                                                                                                                              |
| Projektu pārvaldība un uzskaite |                  | Rēķina priekšlikuma rindas tiek dublētas, jo vairāki periodiskie procesi **Importēt no izstādīšanas** tiek izpildīti vienlaikus.                                                                                                                                                                                                                |

