---
title: 2022. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada septembra laidienā scenārijiem, kuru pamatā ir resursi/krājumi.
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

- Projekta operācijas Dataverse vides versijā 4.46.0.60
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.29

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Citātu pārskatīšana un aktivizēšana**<br>Project Operations nodrošina pilnu pārdošanas procesa atbalstu. Projekta citātus var aktivizēt, lai attēlotu stāvokli, kurā citāts ir tikai lasāms un tiek pārskatīts. Aktivizētos citātus var pārskatīt, lai izveidotu jaunus citātus ar palielinātu pārskatīšanas numuru. Aktivizētos projektu citātus vai citātu pārskatījumus var aizvērt kā uzvarētus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **Laika joslas agnostiskā cenas noklusēšana**<br>Project Operations ir ieviesis laika joslas agnostiskā datuma koncepciju visos projekta faktiskajos apstākļos. Jauns lauks **Transakcijas datums** tagad ir pieejams žurnāla rindās un faktiskajos datumos, un tas tiks izmantots, lai saglabātu datumu, kad transakcija notika, bet nepārvēršot šo datumu par universālo koordinēto laiku. Šis datums tiks izmantots pakārtotajiem procesiem, piemēram, cenu noklusēšanai un rēķinu izveidei. | <p>[Nosakiet izmaksu likmes uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Nosakiet pārdošanas cenas uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Cenu noteikšana un norēķini | **Datuma efektīvās cenas ignorēšana projekta darbībās**<br>Datuma spēkā stāšanās cenu ignorēšana nodrošina veidu, kā ignorēt vai mainīt konkrētas cenas cenrādī. | [Datuma spēkā stāšanās cenu ignorēšana](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Apakšuzņēmuma līgumi | **Apakšuzņēmuma līgumu un kreditoru rēķinu saskaņošana**<br>Šis līdzeklis ļauj klientiem izveidot apakšlīgumus, lai iegādātos resursu laiku, izdevumu kategorijas un materiālus, kas tiek izmantoti projekta darbā. Tas arī ļauj klientiem finance and operations programmās ierakstīt kreditoru rēķinus, kas būs pieejami projektu vadītājiem verifikācijai Dataverse. | <p>[Apakšlīgumu pārvaldība](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreditoru rēķinu izveide](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīgu programmatūras piegādātāju (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |
| Izdevumu pārvaldība | **Spēja grāmatot izdevumu saistības kreditora valūtā**<br>Šis līdzeklis iespējo izdevumu pārskatu grāmatošanu kreditora valūtā, izmantojot skaidras naudas maksājuma veidu. | [Spēja grāmatot izdevumu saistības kreditora valūtā](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekta iepirkums | **Maksāšana, kad tiek apmaksāti kreditoru maksājumi**<br>Šis līdzeklis ļauj līdzekli Maksāt, kad maksā (PWP) izmantot projekta operāciju vidēs, kas nav krājuma vide. Tas ļauj bloķēt/saglabāt kreditoru maksājumus, pamatojoties uz saglabāšanas noteikumiem, līdz maksājums tiek saņemts no debitora. | [Maksāšana, kad tiek apmaksāti kreditoru maksājumi](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekta iepirkums | **Projekta pirkšanas pieprasījumi**<br>Šis līdzeklis ļauj lietotājiem izveidot ar projektu saistītus pirkšanas pasūtījumus juridiskajās personās, kur ir iespējota Project Operations Dynamics 365 Customer Engagement integrācija. Projekta pirkšanas pasūtījumus var izmantot, lai iepirkumu nodaļas persona reģistrētu neuzkrāto materiālu iepirkumu pret projektu. Projekta pirkšanas pasūtījumi netiks sinhronizēti ar Dataverse. Tomēr varat izmantot virtuālo entītiju, lai parādītu projekta pirkšanas pasūtījuma rindas projekta Dataverse vadītāja informācijai. Ar projektu saistītā kreditora rēķina izmaksas ir integrētas ar entītiju Project Actuals pakalpojumā Dataverse. Projekta izmaksas tiek reģistrētas projekta apakšgrāmatā, izmantojot žurnālu Project Operations Integration. | |
|Projektu plānošana un izsekošana|**Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām** </br> </br>Resursu piešķiršanas kontūras rediģēšanas API ļauj izstrādātājiem programmiski norādīt uzdevuma saņēmēja pūles jebkurā atbalstītajā datumu diapazonā, lai iegūtu detalizētāku laika pakāpenisku piepūles plānošanu.|[Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk esošajā tabulā ir parādītas dubultās rakstīšanas kartes, kas ir modificētas vai pievienotas projekta operāciju 2022. gada septembra laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Project Operations integrācijas faktiskie dati (msdyn_actuals) | 1.0.0.15 | Šī karte atbalsta apakšlīgumu faktisko apstrādi ar Project Operations uz resursiem balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.2 | Šī karte atbalsta apakšlīgumu faktisko apstrādi ar Project Operations uz resursiem balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Šī karte atbalsta apakšlīgumu faktisko apstrādi ar Project Operations uz resursiem balstītiem scenārijiem. |

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulu kartes, atjauninot Project Operations Dataverse risinājumu un Finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja nav aktivizēta kartes jaunākā versija. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis standarta komplektācijā iekļauto tabulu karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus [sadaļā Trūkstošas tabulas kolonnas problēma kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps), kas atrodas dubultrakstīšanas problēmu novēršanas rokasgrāmatā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Materiālu un izdevumu aprēķini neplūst uz programmu Finance, kad projekti tiek kopēti Dataverse programmā. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt ar projektu nesaistītu laika ierakstu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes validāciju pasūtījuma rindām, kurās ir karodziņi. |
| Laiks un izdevumi | 2842253 | Nulles izņēmuma apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Ja neizdodas iegūt korelācijas ID, tiek bloķēta rēķina izveide. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD — novērtējuma cenrāža izšķirtspējā jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšuzņēmuma līgumi | 2893222 | Ja apakšuzņēmuma līguma rindai nav norādīta neviena loma, vajadzētu būt iespējai atlasīt šo līniju no komandas dalībnieka jebkurai lomai. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un uzskaite programmā Finance

Lai iegūtu informāciju par šajā atjauninājumā iekļautajiem kļūdu labojumiem, piesakieties Lifecycle Microsoft Dynamics Services un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Līdzekļi, kas pēc noklusējuma ir ieslēgti gaidāmajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgti versijā 10.0.30. Lielāko daļu funkciju, kas ir ieslēgtas automātiski, [var izslēgt līdzekļu pārvaldībā](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Nākotnē daži līdzekļi, kas ir ieslēgti automātiski, var tikt noņemti no līdzekļu pārvaldības un kļūt obligāti. Šīs izmaiņas nodrošina, ka klienti izmanto pašreizējo funkcionalitāti, lai uzlabojumi varētu balstīties uz pašreizējo funkcionalitāti, kad tie tiek pievienoti. Līdzekļi nekad netiks automātiski iespējoti mazāk nekā viena gada laikā, ja vien netiks noteikts, ka tie ir būtiski.

| Līdzekļa nosaukums | Iespējot datumu | Pievienota funkcija | Līdzekļa statuss | Modulis |
| --- | --- | --- |--- |--- |
| Iespējot asinhrono darbību, ja lietotājam ir jāpārslēdzas starp sinhronizācijas un asinhronizācijas operācijām | 2022. gada 21. oktobris | 2021. gada 9. aprīlis | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Nepieciešamo ieņēmumu politikas novērtējums | 2022. gada 21. oktobris | 2021. gada 20. decembris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Izdevumu pārskatu, kas izveidoti, deleģējot darbiniekus, saraksta skats | 2022. gada 21. oktobris | 2020. gada 19. februāris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Nobraukuma kopsummas aprēķins pēc finanšu gads | 2022. gada 21. oktobris | 2022. gada 10. maijs | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
