---
title: Izdevumu kvīšu apstrāde
description: Šajā rakstā sniegta informācija par optiskās rakstzīmju atpazīšanas (OCR) apstrādi kvītīm. Šis līdzeklis ir paredzēts, lai uzlabotu lietotāja pieredzi, kad izdevumu pārskati tiek izveidoti Microsoft Dynamics programmā 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5a72802e3c52b6a9e55ac779aa36c32072dc8b8b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911421"
---
# <a name="expense-receipt-processing"></a>Izdevumu kvīšu apstrāde

Izdevumu ievade ir uzlabota, ieviešot rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm. Šis līdzeklis ir paredzēts, lai uzlabotu lietotāju pieredzi, veidojot izdevumu atskaites.

## <a name="key-features"></a>Galvenie līdzekļi

- No kvītīm tiek izgūts tirgotāja nosaukums, datums un kopējā summa.
- Līdzeklis mēģina saskaņot nepievienotās kvītis nepievienotām izdevumu transakcijām.
- Lietotāji var izveidot manuāli ievadītās izdevumu transakcijas no kvītīm.

## <a name="usage-examples"></a>Lietošanas piemēri

Lai automātiski pievienotu kvītis, kas ietver kredītkaršu transakcijas, kad ir izveidota izdevumu atskaite, izpildiet šādas darbības.

  1. Atveriet **Izdevumu pārvaldības** darbvietu.
  2. Cilnē **Kvītis** pārliecinieties, ka pastāv nepievienotas kvītis. Kvītis varat arī augšupielādēt cilnē **Kvītis**.
  3. Cilnē **Izdevumi** pārliecinieties, ka pastāv nepievienoti izdevumi. Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.
  4. Atlasiet **Jauna izdevumu atskaite**. Ņemiet vērā, ka, veidojot izdevumu atskaiti, varat iekļaut arī izdevumus un kvītis. Ja pievienojat gan izdevumus, gan kvītis, tiek aktivizēta automātiska kvīšu saskaņošana ar izdevumiem.

Lai izveidotu izdevumu vai to saskaņotu no kvīts, izpildiet šādas darbības.

  1. Izdevumu atskaites cilnē **Kvītis** pievienojiet kvīti, atlasot **Pievienot kvītis**.
  2. Zem augšupielādētā kvīts attēla ņemiet vērā opcijas **Izveidot** un **Saskaņot**.

      - Atlasiet **Izveidot**, lai izveidotu manuāli ievadīto izdevumu transakciju un aizpildītu no kvīts izvilktās vērtības.
      - Atlasot **Saskaņot**, sistēma cenšas saskaņot esošu izdevumu ar kvīti.

## <a name="installation"></a>Instalēšana

Šis līdzeklis darbojas kopā ar līdzekli **Uzlabotas izdevumu atskaites**, lai vienkāršotu izmaksu pieredzi. Šis līdzeklis ir pieejams vismaz 2. līmeņa vidēm, kas ir smilškastes un ražošanas instances.

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

Lai iegūtu papildinformāciju par līdzekli Uzlabotas izmaksu atskaites, skatiet rakstu [I Uzlabotas izmaksu atskaites](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

**Vai Microsoft savos modeļos izmanto manus datus?**

Nē, Microsoft ir iebūvēts vispārīgās algoritmiskās mācīšanās modelis, lai apstrādātu kvītis. Šis modelis netiek balstīts jūsu augšupielādētajās kvītīs.

**Kur šis līdzeklis ir pieejams un kur to apstrādā?**

Pašlaik tiek atbalstītas Amerikas Savienotās Valstis.

**Kur nonāk manas kvītis?**

Finance sazinās ar Cognitive Services, lai izvilktu lauka datus. Cognitive Services paturēs jūsu kvīts kopiju 24 stundas, kamēr notiek apstrāde. Pēc apstrādes pabeigšanas Cognitive Services kvīti dzēsīs. Kvītis joprojām tiek glabātas Finance.

Papildinformāciju skatiet rakstā [Kvīšu izpratnes veicināšana ar Form Recognizer jauno iespēju](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]