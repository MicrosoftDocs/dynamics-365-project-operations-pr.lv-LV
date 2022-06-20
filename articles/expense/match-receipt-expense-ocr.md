---
title: Apliecinājuma tveršana, izmantojot OCR
description: Šajā rakstā sniegta informācija par optiskās rakstzīmju atpazīšanas (OCR) apstrādi kvītīm.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ee16a43fa544af793676072f304d732359d3d9ec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917815"
---
# <a name="capture-a-receipt-using-ocr"></a>Apliecinājuma tveršana, izmantojot OCR

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Izdevumu ievade ir uzlabota, ieviešot rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm. Šī funkcionalitāte ir paredzēta, lai uzlabotu lietotāju pieredzi, veidojot izdevumu atskaites.

## <a name="key-features"></a>Galvenie līdzekļi

- Sistēma no kvītīm izgūst tirgotāja nosaukumu, datumu un kopējo summu.
- Sistēma centīsies saskaņot nepievienotās kvītis nepievienotām izdevumu transakcijām.
- Varat izveidot manuāli ievadītās izdevumu transakcijas no kvītīm.

## <a name="attach-receipts-to-an-expense-report"></a>Kvīšu pievienošana izdevumu atskaitei

Lai automātiski pievienotu kvītis, kas ietver kredītkaršu transakcijas, kad ir izveidota izdevumu atskaite, izpildiet šādas darbības:

  1. Atveriet **Izdevumu pārvaldības** darbvietu.
  2. Cilnē **Kvītis** pārliecinieties, ka pastāv nepievienotas kvītis. Kvītis varat arī augšupielādēt cilnē **Kvītis**.
  3. Cilnē **Izdevumi** pārliecinieties, ka pastāv nepievienoti izdevumi. Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.
  4. Atlasiet **Jauna izdevumu atskaite**. Ņemiet vērā, ka, veidojot izdevumu atskaiti, varat iekļaut arī izdevumus un kvītis. Ja pievienojat gan izdevumus, gan kvītis, tiek aktivizēta automātiska kvīšu saskaņošana ar izdevumiem.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Kvīšu izveide vai saskaņošana ar izdevumu atskaiti
Lai izveidotu izdevumu vai to saskaņotu no kvīts, izpildiet šādas darbības:

  1. Izdevumu atskaites cilnē **Kvītis** pievienojiet kvīti, atlasot **Pievienot kvītis**.
  2. Zem augšupielādētā kvīts attēla ņemiet vērā opcijas **Izveidot** un **Saskaņot**.

      - Atlasiet **Izveidot**, lai izveidotu manuāli ievadīto izdevumu transakciju un aizpildītu no kvīts izvilktās vērtības.
      - Atlasot **Saskaņot**, sistēma cenšas saskaņot esošu izdevumu ar kvīti.

## <a name="installation"></a>Instalēšana

Lai izmantotu šīs papildu izdevumu iespējas, instalējiet izdevumu pārvaldības pakalpojuma pievienojumprogrammu Microsoft Dynamics 365 Finance un ieslēdziet līdzekļus savā gadījumā. Jūs varat piekļūt pievienojumprogrammai no sava projekta Microsoft Dynamics Lifecycle Services (LCS).

1. Pierakstieties LCS un atveriet vēlamo vidi.
2. Pārejiet uz **Pilna informācija**.
3. Atlasiet **Uzturēt** vai ritiniet uz leju līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.
4. Atlasiet **Instalēt jaunu pievienojumprogrammu**.
5. Atlasiet **Izdevumu Pārvaldības Pakalpojums**.
6. Izpildiet instalēšanas rokasgrāmatas norādījumus un piekrītiet noteikumiem un nosacījumiem.
7. Atlasiet **Instalēt**.

**Līdzekļu pārvaldības** darbvietā ieslēdziet šādus līdzekļus:

- Atjaunotas izdevumu atskaites
- Izdevumu automātiska saskaņošana un izveide no kvīts

Ieslēdzot šos līdzekļus, notiek šādas darbības:

- Esošā **Izdevumu pārvaldības** darbvieta tiek aizstāta ar jauno darbvietu.
- Tiek pievienota jauns izvēlnes vienums izdevumu lauka redzamībai.
- Joprojām varat atvērt kādreizējo **Izdevumu atskaišu** lapu, dodoties uz **Izdevumu pārvaldība > Mani izdevumi > Izdevumu atskaites**.
- Darbplūsmas un visi apstiprinājumi joprojām aizved uz esošo izdevumu atskaišu lapu.
- Kvītis apstrādās ar Microsoft Azure Cognitive Services, bet metadati tiks izvilkti un pievienoti.
- Tiek pievienota opcija, kas ļauj izveidot izdevumu atskaiti, kas ietver saskaņotas nepievienotās kvītis.
- Opcija, kas tiek pievienota izdevumu atskaitēm, ļauj izveidot izdevumu rindu no kvīts vai mēģina saskaņot esošu kvīti ar esošu izdevumu rindu.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

**Vai Microsoft savos modeļos izmanto manus datus?**

Nē, Microsoft ir iebūvēts vispārīgās algoritmiskās mācīšanās modelis, lai apstrādātu kvītis. Šis modelis netiek balstīts jūsu augšupielādētajās kvītīs.

**Kur šis līdzeklis ir pieejams un kur to apstrādā?**

Šī līdzekļa pieejamība dažādos reģionos ir norādīta šajā tabulā. Ja jūsu reģions pašlaik netiek atbalstīts, iesniedziet pieprasījumu par prioritāti noteikt OCR pakalpojuma pieejamību jūsu reģionā. 

| Reģions | Atbalstīts                         |
|--------|-----------------------------------|
| ASV    | Jā                               |
| CAN    | Jā                               |
| Apvienotā Karaliste     | Jā                               |
| AUS    | Jā                               |
| ES     | Daļēji. Tikai angļu valodas kvītis. |
| Āzija   | Nē.                                |
| Japāna  | Nē.                                |
| Āfrika | Nē.                                |

**Kur nonāk manas kvītis?**

Finance sazinās ar Cognitive Services, lai izvilktu lauka datus. Cognitive Services paturēs jūsu kvīts kopiju 24 stundas, kamēr notiek apstrāde. Pēc apstrādes pabeigšanas Cognitive Services kvīti dzēsīs. Kvītis joprojām tiek glabātas Finance.

Papildinformāciju skatiet rakstā [Kvīšu izpratnes veicināšana ar Form Recognizer jauno iespēju](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
