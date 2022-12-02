---
title: 2022. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada septembra laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634815"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.46.0.60
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.29.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Piedāvājumu pārskatīšana un aktivizēšana**<br>Project Operations pilnībā atbalsta pārdošanas procesu. Projektu piedāvājumus var aktivizēt, lai atspoguļotu statusu, kurā piedāvājums ir tikai lasāms un tiek pārskatīts. Aktivizētos piedāvājumus var pārskatīt, lai izveidotu jaunus piedāvājumus ar palielinātu pārskatīšanas numuru. Aktivizētos projektu piedāvājumus vai piedāvājumu pārskatījumus var aizvērt kā iegūtus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **No laika joslas neatkarīga cenas noklusējuma izmantošana**<br>Project Operations ir ieviesusi no laika joslas neatkarīgu datumu koncepciju visos projekta faktiskajos datos. Žurnāla rindās un faktiskajos datos tagad ir pieejams jauns lauks **Transakcijas datums**, kas tiks izmantots transakcijas datuma saglabāšanai, nepārvēršot šo datumu universālajā koordinētajā laikā. Šis datums tiks lietots lejupstraumes procesiem, piemēram, cenu noklusējumam un rēķinu izveidei. | <p>[Izmaksu likmju noteikšana projekta aprēķinos un faktiskajos datos](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Pārdošanas cenu noteikšana projekta aprēķinos un datos](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Cenu noteikšana un norēķini | **Datuma un spēkā esošās cenas pārlabošana programmā Project Operations**<br>Datuma un spēkā esošās cenas pārlabošana nodrošina veidu, kā pārlabot vai mainīt konkrētas cenas cenrādī. | [Datuma un spēkā esošās cenas pārlabošana](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Apakšlīgumu slēgšana | **Apakšlīgumu slēgšana un piegādātāju rēķinu saskaņošana**<br>Šis līdzeklis ļauj klientiem izveidot apakšlīgumus, lai iegādātos resursu laiku, izdevumu kategorijas un materiālus, kas tiek izmantoti projekta darbiem. Turklāt klienti var ierakstīt finanšu un operāciju programmās piegādātāju rēķinus, kas būs pieejami projektu vadītājiem programmā Dataverse pārbaudei. | <p>[Pakārtotā pārvaldība](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreditoru rēķinu izveide](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīga programmatūras izstrādātāja (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |
| Izdevumu pārvaldība | **Spēja grāmatot izdevumu saistību piegādātāja valūtā**<br>Šis līdzeklis iespējo izdevumu pārskatu grāmatošanu piegādātāja valūtā skaidras naudas maksājumu metodei. | [Spēja grāmatot izdevumu saistību piegādātāja valūtā](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekta iepirkums | **"Apmaksāt pēc apmaksas" tipa piegādātāju maksājumi**<br>Izmantojot šo līdzekli, līdzeklis "Apmaksāt pēc apmaksas" (PWP) tiek izmantots Project Operations krājumos nebalstītās vidēs. Tas ļauj bloķēt/saglabāt piegādātāju maksājumus, pamatojoties uz saglabāšanas nosacījumiem, līdz maksājums ir saņemts no klienta. | ["Apmaksāt pēc apmaksas" tipa piegādātāju maksājumi](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekta iepirkums | **Projekta pirkšanas pieprasījumi**<br>Izmantojot šo līdzekli, lietotāji var izveidot ar projektiem saistītus pasūtījumus juridiskās personās, kur ir iespējota Project Operations Dynamics 365 Customer Engagement integrācija. Projektu pirkumu pasūtījumus var izmantot, lai ierakstītu krājumos neesošu materiālu iepirkumus attiecībā pret projektu, ko veic sagādes departamenta persona. Projekta pirkumu pasūtījumi netiks sinhronizēti ar Dataverse. Tomēr varat izmantot virtuālu entītiju, lai projekta pirkuma pasūtījuma rindas parādītu programmā Dataverse projekta vadītāja informācijai. Ar projektu saistītās piegādātāja rēķina izmaksas ir integrētas ar projekta faktisko datu entītiju programmā Dataverse. Projekta izmaksas tiek ierakstītas projekta apakšgrāmatā, izmantojot Project Operations integrācijas žurnālu. | |
|Projektu plānošana un izsekošana|**Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām** </br> </br>Resursu piešķiršanas kontūras rediģēšanas API ļauj izstrādātājiem programmiski norādīt uzdevuma saņēmēja ieguldījumu jebkurā atbalstītajā datumu diapazonā, lai ļautu detalizētāk plānot ieguldījuma laika sadalījumu.|[Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā tabulā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada septembra laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Project Operations integrācijas faktiskie dati (msdyn_actuals) | 1.0.0.15 | Šī karte atbalsta apakšlīguma faktisko datu apstrādi ar Project Operations resursos balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.2 | Šī karte atbalsta apakšlīguma faktisko datu apstrādi ar Project Operations resursos balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Šī karte atbalsta apakšlīguma faktisko datu apstrādi ar Project Operations resursos balstītiem scenārijiem. |

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Kad projekti tiek kopēti Dataverse, materiālu un izmaksu aprēķini neplūst uz Finance. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt projektam nepiederīgu laika ierakstu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes apstiprināšanu pasūtījuma rindām, kas ietver karodziņus. |
| Laiks un izdevumi | 2842253 | Nulles izņēmumu apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Neizdevās iegūt korelācijas ID, tāpēc tiek bloķēta rēķina izveide. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD — aprēķinātajam cenrāža risinājumam ir jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšlīgumu slēgšana | 2893222 | Ja apakšlīguma rindai nav norādīta loma, šo rindu vajadzētu varēt atlasīt darba grupas dalībniekam jebkurai lomai. |

### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Līdzekļi, kas nākamajā laidienā ir ieslēgti pēc noklusējuma

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgtas versijā 10.0.30. Lielāko daļu līdzekļu, kas ir automātiski ieslēgti, var izslēgt [Līdzekļu pārvaldībā](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Turpmāk daži automātiski ieslēgtie līdzekļi var tikt noņemti no līdzekļu pārvaldības un kļūt obligāti. Šīs izmaiņas nodrošina, ka klienti izmanto pašreizējo funkcionalitāti, lai uzlabojumi varētu balstīties uz pašreizējo funkcionalitāti pievienošanas laikā. Līdzekļi nekad netiks automātiski iespējoti pēc mazāk nekā viena gada, ja vien tie nav noteikti kā būtiski.

| Līdzekļa nosaukums | Iespējošanas datums | Līdzeklis pievienots | Līdzekļa statuss | Modulis |
| --- | --- | --- |--- |--- |
| Asinhronas darbības iespējošana, kad lietotājam jāpārslēdzas starp sinhronām un asinhronām darbībām | 2022. gada 21. oktobris | 2021. gada 9. aprīlis | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Izdevumu politikas novērtēšana nepieciešamajiem čekiem | 2022. gada 21. oktobris | 2021. gada 20. decembris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Sarakstu skats ar izdevumu pārskatiem, kas izveidoti, deleģējot darbiniekus | 2022. gada 21. oktobris | 2020. gada 19. februāris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Kopējā nobraukuma aprēķināšana pēc finanšu gada | 2022. gada 21. oktobris | 2022. gada 10. maijs | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
