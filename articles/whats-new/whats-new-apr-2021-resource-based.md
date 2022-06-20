---
title: Jaunumi 2021. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada aprīļa projekta operāciju laidienā resursu/neuzkrātu scenāriju gadījumā.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912433"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.9.0.221
- Projektu vadība un uzskaite Dynamics 365 Finance vidē versija 10.0.17

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Krājumos neesoši materiāli projektiem. Galvenās iespējas ietver:
  - Krājumos neesošu materiālu novērtēšanu un cenu noteikšanu projekta pārdošanas ciklā. Plašāka informācija: [Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem (Lite)](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Krājumos neesošu materiālu izmantošanas izsekošana projekta piegādes laikā. Papildinformāciju skatiet rakstā [Materiālu lietojuma reģistrēšana projektos un projektu uzdevumos](../material/material-usage-log.md).
  - Krājumos neesošu materiālu izmaksu izmantošana rēķinos. Papildinformāciju skatiet šeit: [Neizrakstīto rēķinu pārvaldība](../proforma-invoicing/manage-billing-backlog.md).
  - Informāciju par šī līdzekļa konfigurēšanu skatiet sadaļā [Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu konfigurēšana](../procurement/configure-materials-nonstocked.md).
- Uz uzdevumu balstīti rēķini: ir pievienota iespēja projekta uzdevumus saistīt ar projekta līguma rindām, šādi paātrinot tos pašus norēķinu veidus, rēķinu biežumu un klientus, kuri atrodas līguma rindā. Šī saistība nodrošina pareizu rēķinu izrakstīšanu, uzskaiti, ieņēmumu novērtēšanu un atpazīšanu, lai darbotos atbilstoši šim projekta uzdevumu iestatījumam.
- Jaunie API programmā Dynamics 365 Dataverse ļauj izveidot, atjaunināt un dzēst operācijas ar **plānošanas entītijām**. Papildinformāciju skatiet šeit: [Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā sarakstā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2021. gada aprīļa laidienā.

| **Entītiju karte** | **Atjauninātā versija** | **Komentāri** |
| --- | --- | --- |
| Project Operations integrācijas faktiskie dati (msdyn\_actuals) | 1.0.0.14 | Karte ir modificēta, lai sinhronizētu materiālu projekta faktiskās vērtības. |
| Project Operations integrācijas entītija izdevumu aprēķiniem (msdyn\_estimateslines) | 1.0.0.2 | Pievienota projekta līguma rindas sinhronizācija finanšu un operāciju programmām, lai saņemtu uz uzdevumiem balstītu norēķinu atbalstu. |
| Project Operations integrācijas entītija stundu aprēķiniem (msdyn\_resourceassignments) | 1.0.0.5 | Pievienota projekta līguma rindas sinhronizācija finanšu un operāciju programmām, lai saņemtu uz uzdevumiem balstītu norēķinu atbalstu. |
| Project Operations integrācijas tabula materiālu aprēķiniem (msdyn\_estimatelines) | 1.0.0.0 | Jauna tabulas karte materiālu novērtējumu sinhronizēšanai no Dataverse finanšu un operāciju programmām. |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn\_projectvendorinvoices) | 1.0.0.0 | Jauna tabulas karte, lai sinhronizētu kreditoru rēķinu virsrakstus no finanšu un operāciju programmām uz Dataverse. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Jauna tabulas karte kreditoru rēķinu rindu sinhronizēšanai no finanšu un operāciju programmām uz Dataverse. |

Atjauninot projektu operāciju Dataverse risinājumu un Finance and Operations risinājuma versiju, vienmēr jāpalaiž apkārtējā vidē jaunākā kartes versija un jāiespējo visas saistītās tabulu kartes. Ja nav aktivizēta jaunākā kartes versija, noteikti līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Varat aktivizēt jaunu kartes versiju, atlasot **Tabulas kartes versijas**, atlasot jaunāko versiju un pēc tam saglabājot atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma ar kartes startēšanu, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations platformā Dynamics 365 Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2124532 | Poga **Pareizais rēķins** tiek rādīta proformas rēķinā, kad honorāra summa vai lietotā honorāra summa ir iekļauta sākotnējā rēķinā. Šī poga tiek rādīta tikai vidēs ar Finance versiju 10.0.19 vai jaunākām versijām. |
| Cenu noteikšana un norēķini | 2224568 | Pievienota loģika, lai iespējotu pielāgojumus, kas ietver rēķina apstiprinājuma spraudņa aktivizēšanu. |
| Cenu noteikšana un norēķini | 2101098 | Ir uzlabota noklusējuma lauku loģika pro forma rēķinam: lauki **Rēķina adrese**, **Rēķina saņēmējs** un **Maksājumu nosacījumi** tagad pēc noklusējuma tiek aizpildīti ar informāciju no atbilstošā projekta līguma klienta ieraksta. |
| Cenu noteikšana un norēķini | 2021413 | Ir atjaunināti lauki **Faktiskās izmaksas** un **Pārdošana** entītijā **Uzdevums**, lai ietvertu pārdošanas vērtības no rēķinos ietvertajiem un neietvertajiem uzdevumu izdevumiem. |
| Cenu noteikšana un norēķini | 2182110 | Kopējot projekta līgumu, līguma rindas ID tiek atkārtoti ģenerēts mērķa projekta līgumā, lai nodrošinātu tā unikālitāti. |
| Iespēju pārvaldība | 2186741 | Ir pievienotas validācijas, lai lauku **Izcelsme** un **Transakcijas veids** nevarētu atjaunināt esoša piedāvājuma rindas informācijā. |
| Iespēju pārvaldība | 2191353 | Atskaites punktus nevar veidot laika un materiālu līguma rindās. |
| Iespēju pārvaldība | 2216956 | Novērstas problēmas ar **cenu atjaunināšanu**. |
| Plānošana un izsekošana | 2182979 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka izmaksu novērtējuma rindas tiek kopētas no sākotnējā projekta. |
| Plānošana un izsekošana | 2184144 | Ir uzlabota projekta kopēšanas funkcija, lai nodrošinātu, ka resursa pozīcijas nosaukums tiek kopēts no sākotnējā projekta. |
| Plānošana un izsekošana | 2184799 | Projekta kopija: pastiprināta kontrole, lai kopēšanas laikā nevarētu mainīt prognozēto sākuma datumu. |
| Plānošana un izsekošana | 2185134 | Projekta kopija: projekta prognozētais sākuma datums ir iestatīts uz šodienas datumu. |
| Plānošana un izsekošana | 2196373 | Projekta kopija: pārbaudiet, vai projekta vadītāja un darba grupas dalībnieku ieraksti netiek dublēti projekta darba grupā. |
| Plānošana un izsekošana | 2211833 | Projekta kopija: resursu piešķīrumi tiek kopēti no avota projekta uzdevuma uz mērķa projektu. |
| Plānošana un izsekošana | 2186541 | Novērstas problēmas režģī **Novērtējums**, kad tiek veikta grupēšana pēc resursa. |
| Plānošana un izsekošana | 2166906 | Transakcijas kategorija no uzdevuma ir jākopē uz entītiju **Resursu piešķiršana**. |
| Resursu pārvaldība | 2125362 | Novērstas problēmas ar vispārīgās darba grupas dalībnieka izveidi, izmantojot metodi, kuras pamatā ir stundas. |
| Laiks un izdevumi | 2113603 | Novērsta ar pielāgošanu saistītā problēma, noņemot atribūtus no lapas **Laika ievade**. Tagad sistēma pārbauda, vai lapā ir atribūts, pirms piekļūstat tiem, izmantojot skriptu. |
| Laiks un izdevumi | 2204377 | Kopētajiem laika intervāliem ir automātiski jāparādās, kad atlasāt **Kopēt nedēļu**, ievadot laiku. |
| Laiks un izdevumi | 2209059 | Lauku **Statuss** var rediģēt Dynamics 365 Field Service laika ierakstiem. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Apgriezto aprēķinu korekcijas nedarbojas sadaļā **Periodisks**.  |
| Projektu pārvaldība un uzskaite | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Līdzeklis **Uzskaites pielāgošana** rada problēmu ar virsgrāmatas kontiem, kuriem ir atlasīta opcija **Neatļaut manuālu ievadi**. |
| Projektu pārvaldība un uzskaite | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Pievienota biznesa loģika, lai apstrādātu korekcijas rēķinus, iekļaujot honorāra summu vai lietoto honorāra summu. |
| Projektu pārvaldība un uzskaite | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | NP — pārdošanas vērtību grāmatošanas funkcija, izrakstot starpuzņēmumu projektā rēķinu, atlasa neparedzētu uzņēmumu. |
| Projektu pārvaldība un uzskaite | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Strādājot ar honorāriem programmā Project Operations, līguma noklusējuma projekta maiņa pēc tam, kad ir izrakstīti rēķini par priekšmaksājumiem, vēlāk rada problēmu ar ienākošajiem atskaitījumiem. |
| Projektu pārvaldība un uzskaite | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Programmā Project Operations noņemot projektu no līguma, būtu jāatiestata līguma noklusējuma projekts. |
| Projektu pārvaldība un uzskaite | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Programmā Project Operations starpuzņēmumu rēķinā tiek rādītas nepareizas izdevumu rindas sarakstā **Pievienot rindu**. |
| Projektu pārvaldība un uzskaite | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations lapā **Pirkuma līgums** nav redzamas finanšu juridiskās entītijas, kas ir integrētas programmā Project Operations. |
| Projektu pārvaldība un uzskaite | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse integrācijas kļūdas dēļ nevar pārvērst piedāvājumu, kas ir uzvarēts programmā Project Operations. |
| Projektu pārvaldība un uzskaite | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** var iestatīt līdzekļu avota rēķina adresi no cita klienta.  |
| Projektu pārvaldība un uzskaite | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Programmā Project Operations veidojot grāmatotu rēķinu transakcijai, netiek atlasītas dimensijas. |
| Braucieni un izdevumi | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Ja izdevumu atskaite ir apstiprināta un grāmatota pa rindai, naudas līdzekļu iepriekšēja bilance netiek atjaunināta. |
| Komandējumi un izdevumi | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Nodokļi par detalizētiem starpuzņēmumu izdevumu pārskatiem netiek pareizi aprēķināti. |
| Komandējumi un izdevumi | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Papildu lauki, kas saistīti ar projektiem, tiek parādīti atkārtoti iedomātajā lapā **Starpuzņēmumu izdevumu pārskati**. |
| Komandējumi un izdevumi | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Izdevumu pārskatu galvenes kvītīs tiek parādīts nepareizs kļūdas ziņojums. |
| Komandējumi un izdevumi | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Izdevumu pārskats tiek nepareizi grāmatots starpuzņēmumu scenārijā, ja pārdošanas nodoklis tiek grāmatots mērķa juridiskajā entītijā. |
| Komandējumi un izdevumi | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Pārskatu iesniegšanas datumi netiek drukāti uz apstiprinātajiem izdevumu pārskatiem. |
| Komandējumi un izdevumi | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Pēc izdevumu apstiprināšanas netiek aizpildīts lauks **Apstiprināšanas datums** un **Noraidīšanas datums**. |
| Komandējumi un izdevumi | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Vienam darbiniekam izveidots brauciena pieprasījums var tikt izmantots cita darbinieka izdevumu pārskatā. |
| Komandējumi un izdevumi | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Pievienojot jaunu izdevumu rindu, izdevumu kategorijas tiek bloķētas. |
| Komandējumi un izdevumi | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Precizējot jau sadalītu izdevumu pārskatu, tiek nepareizi grāmatots kreditoru/virsgrāmatas kupons un sadalīts Accounting Source Explorer, jo **TRVEXPTRANS.SOURCEDOCUMENTLINE** ir dublēts. |
| Komandējumi un izdevumi | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Brauciena pieprasījumu politika nedarbojas, kā paredzēts. |
| Komandējumi un izdevumi | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Piegādātāja konta nosaukums netiek rādīts grāmatotajās projekta transakcijās izdevumu pārskatos. |
| Komandējumi un izdevumi | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Programmā Project Operations jūs nevarat apstiprināt laiku ar uzdevumu starpuzņēmumu projektam. |
| Komandējumi un izdevumi | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Grāmatojot naudas līdzekļu iepriekšējas atgriešanas kategoriju, naudas līdzekļu iepriekšēja bilance netiek atjaunināta. |
| Komandējumi un izdevumi | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Pārdošanas cena tiek aprēķināta nepareizi izdevumu pārskatos, kas tika izveidoti ārvalstu valūtā, izmantojot importētās kredītkartes transakcijas, un ir saistīti ar projektu. |
| Komandējumi un izdevumi | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Tika atsaukta entītija **TrvRequisitionLine** un saistītais unikālais indekss. |
| Komandējumi un izdevumi | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Paaudzei **SOURCEDOCUMENTLINE** tika pievienota instrumentācija. |
| Komandējumi un izdevumi | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Starpuzņēmumu scenārijā tiek rādīts nepareizs apakšgrāmatas žurnāls, ja pārdošanas nodoklis tiek grāmatots mērķa juridiskajā entītijā. |
| Komandējumi un izdevumi | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations ietvaros izdevumu novērtējums netiek dzēsts no Finance, kad tie tiek dzēsti no Dataverse. |
| Komandējumi un izdevumi | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ja izdevumu kategorija ir kategorija, kas nav projekta kategorija, lapā **Izdevumi** atlasītās finanšu dimensijas netiek kopētas izdevumu pārskatā. |
