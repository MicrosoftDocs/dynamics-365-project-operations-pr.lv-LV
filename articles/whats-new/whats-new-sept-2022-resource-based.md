---
title: 2022. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada septembra laidienā uz resursiem/nepiegādātiem scenārijiem.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621346"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. gada septembra jaunumi — Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.46.0.60
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.29

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Citātu pārskatīšana un aktivizēšana**<br>Project Operations nodrošina pilnu pārdošanas procesa atbalstu. Projekta citātus var aktivizēt, lai attēlotu stāvokli, kurā piedāvājums ir tikai lasāms un tiek pārskatīts. Aktivizētos citātus var pārskatīt, lai izveidotu jaunus citātus, kuriem ir palielināts pārskatījuma numurs. Aktivizētos projekta citātus vai citātu pārskatījumus var aizvērt kā uzvarētus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **Laika joslas agnostiskās cenas saistību neizpilde**<br>Project Operations ir ieviesis laika joslas agnostiskā datuma jēdzienu visos projekta faktiskajos datos. Jauns lauks **— Transakcijas datums** — tagad ir pieejams žurnāla rindās un faktiskajos datos, un tas tiks izmantots, lai saglabātu transakcijas veikšanas datumu, bet nekonvertējot šo datumu par universālo koordinēto laiku. Šis datums tiks izmantots pakārtotiem procesiem, piemēram, cenu saistību neizpildei un rēķinu izveidei. | <p>[Uz projektiem balstītu aplēšu un faktisko izmaksu likmju noteikšana](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Pārdošanas cenu noteikšana uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Cenu noteikšana un norēķini | **Datuma spēkā esošās cenas ignorēšana programmā Project Operations**<br>Datuma spēkā stāšanās cenu ignorēšana nodrošina veidu, kā ignorēt vai mainīt konkrētas cenas cenrādī. | [Datuma spēkā esošā cena ignorē](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Apakšuzņēmuma līgumi | **Apakšuzņēmuma līgumu slēgšana un kreditoru rēķinu saskaņošana**<br>Šis līdzeklis ļauj klientiem izveidot apakšlīgumus, lai iegādātos resursu laiku, izdevumu kategorijas un materiālus, kas tiek izmantoti projekta darbam. Tas arī ļauj klientiem finanšu un operāciju programmās ierakstīt kreditoru rēķinus, kas būs pieejami projektu vadītājiem Dataverse verifikācijai. | <p>[Apakšuzņēmuma līgumu pārvaldība](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreditoru rēķinu izveide](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīgu programmatūras piegādātāju (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |
| Izdevumu pārvaldība | **Spēja publicēt izdevumu saistības kreditora valūtā**<br>Šis līdzeklis ļauj izdevumu pārskatus grāmatot kreditora valūtā, kas paredzēta maksājuma veidam skaidrā naudā. | [Spēja publicēt izdevumu saistības kreditora valūtā](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekta iepirkums | **Maksājiet, kad kreditors ir samaksājis par maksājumiem**<br>Šis līdzeklis ļauj izmantot līdzekli "Maksā, kad maksā, kad maksā" (PWP) ar Project Operations nesaistītās vidēs. Tas ļauj bloķēt/paturēt kreditora maksājumus, pamatojoties uz saglabāšanas nosacījumiem, līdz maksājums tiek saņemts no debitora. | [Maksājiet, kad kreditors ir samaksājis par maksājumiem](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekta iepirkums | **Projekta iegādes pieprasījumi**<br>Šis līdzeklis ļauj lietotājiem izveidot ar projektiem saistītus pirkšanas pasūtījumus juridiskās personās, kurās ir iespējotas project operations on Dynamics 365 Customer Engagement integrācija. Projektu iegādes pasūtījumus var izmantot, lai reģistrētu neiekrāto materiālu iepirkumu pret projektu, ko veic Iepirkumu nodaļas persona. Projekta pirkšanas pasūtījumi netiks sinhronizēti ar Dataverse. Tomēr varat izmantot virtuālo entītiju, lai parādītu projekta iegādes pasūtījuma rindas Dataverse projekta vadītāja informācijai. Ar projektu saistītās kreditora rēķina izmaksas ir integrētas entītijā Projekta faktiskie dati .Dataverse Projekta izmaksas tiek reģistrētas apakšsadaļā Projekts, izmantojot project operations integrācijas žurnālu. | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Nākamajā tabulā ir parādītas divu rakstu kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada septembra laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Project Operations integrācijas faktiskie dati (msdyn_actuals) | 1.0.0.15 | Šī karte atbalsta apakšuzņēmuma līgumu faktisko apstrādi, izmantojot Project Operations uz resursiem balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.2 | Šī karte atbalsta apakšuzņēmuma līgumu faktisko apstrādi, izmantojot Project Operations uz resursiem balstītiem scenārijiem. |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Šī karte atbalsta apakšuzņēmuma līgumu faktisko apstrādi, izmantojot Project Operations uz resursiem balstītiem scenārijiem. |

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja kartes jaunākā versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis lietošanai gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas sniegti [divrakstīšanas problēmu novēršanas ceļveža sadaļā Trūkstošās tabulas kolonnas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kartēs.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Materiālu un izdevumu aplēses neplūst uz finanses, kad projekti tiek kopēti Dataverse. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt ierakstu par laiku, kas nav saistīts ar projektu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes validāciju pasūtījuma rindām, kurās ir karodziņi. |
| Laiks un izdevumi | 2842253 | Nulles izņēmuma apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Nespēja iegūt korelācijas ID bloķē rēķina izveidi. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD - aplēses cenrāža izšķirtspējai jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšuzņēmuma līgumi | 2893222 | Ja apakšlīguma līnijai nav norādīta neviena loma, vajadzētu būt iespējai izvēlēties šo rindu no komandas dalībnieka jebkurai lomai. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finanšu jomā

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Līdzekļi, kas pēc noklusējuma ir ieslēgti gaidāmajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgti versijā 10.0.30. Lielāko daļu līdzekļu, kas ir automātiski ieslēgti, var izslēgt līdzekļu [pārvaldībā](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Nākotnē daži līdzekļi, kas ir automātiski ieslēgti, var tikt noņemti no funkciju pārvaldības un kļūt obligāti. Šīs izmaiņas nodrošina, ka klienti izmanto pašreizējo funkcionalitāti, lai uzlabojumi varētu balstīties uz pašreizējo funkcionalitāti, kad tie tiek pievienoti. Funkcijas nekad netiks automātiski iespējotas mazāk nekā viena gada laikā, ja vien tās netiks atzītas par būtiskām.

| Līdzekļa nosaukums | Datuma iespējošana | Pievienots līdzeklis | Līdzekļa statuss | Modulis |
| --- | --- | --- |--- |--- |
| Iespējot asinhrono darbību, kad lietotājam ir jāpārslēdzas starp sinhronizācijas un asinhronizācijas operācijām | 2022. gada 21. oktobris | 2021. gada 9. aprīlis | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Izdevumu politikas novērtējums nepieciešamajiem ieņēmumiem | 2022. gada 21. oktobris | 2021. gada 20. decembris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| To izdevumu pārskatu saraksta skats, kas izveidoti, deleģējot darbiniekus | 2022. gada 21. oktobris | 2020. gada 19. februāris | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
| Nobraukuma kopsummas aprēķins pēc finanšu gads | 2022. gada 21. oktobris | 2022. gada 10. maijs | Ieslēgts pēc noklusējuma | Izdevumu pārvaldība |
