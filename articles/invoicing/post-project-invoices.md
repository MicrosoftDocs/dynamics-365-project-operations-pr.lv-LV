---
title: Rēķinu izrakstīšanas procesa pārskats
description: Šajā tēmā sniegts rēķinu izrakstīšanas procesa pārskats programmā Project Operations resursu/nekrājumu scenārijos.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369025"
---
# <a name="invoicing-process-overview"></a>Rēķinu izrakstīšanas procesa pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Project Operations resursu/nekrājumu scenārijos piedāvā plašas iespējas, kas pielāgotas gan projektu vadītāja, gan debitora/projekta grāmatveža vajadzībām. Rēķina izrakstīšanas procesam projekta vadītājs pārvalda nepabeigto projekta norēķinu un debitors/projekta grāmatvedis izveido atbilstošu un precīzu klientam paredzētu rēķina dokumentu.

![Rēķinu izrakstīšanas plūsmas shēma](./media/invoicing-flow.png)

Projekta līguma rinda nosaka norēķinu metodi saistītajām projekta transakcijām. Kad projekta vadītājs apstiprina laika un izdevumu transakcijas, sistēma fiksē transakcijas entitījā **Projekta faktiskās vērtības** un nosūta informāciju Dynamics 365 Finance modulim **Projekta pārvaldība un uzskaite**. Pēc tam projekta grāmatvedis pārskata un izliek ierakstus, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Šajā žurnālā ir iekļauta svarīga uzskaites informācija par projekta faktiskajiem datiem, piemēram, norēķiniem, pārdošanas nodokļu grupu, norēķinu preču pārdošanas nodokļu grupu un finanšu dimensijām.

Projekta vadītājs var pārskatīt rēķinā neiekļautās pārdošanas transakcijas, izmantojot laika un materiālu norēķinu metodi [Nepabeigtajos laika un materiālu norēķinos](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) un fiksētās cenas norēķinus [Fiksētās cenas atskaites punktos](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Šie skati ļauj filtrēt un atlasīt transakcijas, kuras jāiekļauj nākamajā norēķinu ciklā, un pēc tam atzīmēt tās kā **Gatavas iekļaušanai rēķinā**.

Jūs varat [manuāli izveidot proformas rēķinu](../proforma-invoicing/create-manual-proforma-invoice.md) vai izmantot [periodisko apstrādi](../proforma-invoicing/configure-automated-invoice-creation.md). Projekta vadītājs var pēc nepieciešamības [pielāgot proformas rēķina melnrakstu](../proforma-invoicing/manage-proforma-invoice.md) un pēc tam to apstiprināt.

Apstiprināto proformas rēķinu nosūta uz Finance moduli **Projekta pārvaldība un uzskaite**. Projekta grāmatvedis formatē un atjaunina projekta rēķina priekšlikumu un pēc tam izliek un drukā šo dokumentu. Izliktos projekta rēķinus ieraksta Virsgrāmatā, kā arī Klienta un Projekta apakšgrāmatās.


[!INCLUDE[footer-include](../includes/footer-banner.md)]