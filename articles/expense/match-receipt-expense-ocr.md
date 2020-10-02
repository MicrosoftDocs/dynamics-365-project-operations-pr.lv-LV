---
title: Saskaņot ieejas plūsmu ar izdevumiem, izmantojot OCR
description: Šajā tēmā ir sniegta informācija par rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897010"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Saskaņot ieejas plūsmu ar izdevumiem, izmantojot OCR

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

Lai izmantotu šīs papildu izdevumu iespējas, instalējiet Izdevumu Pārvaldības Pakalpojums pievienojumprogrammu Microsoft programmai Dynamics 365 Finance un ieslēdziet līdzekļus savā instancē. Jūs varat piekļūt pievienojumprogrammai no sava projekta Microsoft Dynamics Lifecycle Services (LCS).

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

Pašlaik tiek atbalstītas Amerikas Savienotās Valstis.

**Kur nonāk manas kvītis?**

Finance sazinās ar Cognitive Services, lai izvilktu lauka datus. Cognitive Services paturēs jūsu kvīts kopiju 24 stundas, kamēr notiek apstrāde. Pēc apstrādes pabeigšanas Cognitive Services kvīti dzēsīs. Kvītis joprojām tiek glabātas Finance.

Papildinformāciju skatiet rakstā [Kvīšu izpratnes veicināšana ar Form Recognizer jauno iespēju](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
