---
title: Rēķinu izrakstīšanas procesa pārskats
description: Šajā tēmā sniegts rēķinu izrakstīšanas procesa pārskats programmā Project Operations resursu/nekrājumu scenārijos.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582719"
---
# <a name="invoicing-process-overview"></a>Rēķinu izrakstīšanas procesa pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Project Operations resursu/nekrājumu scenārijos piedāvā plašas iespējas, kas pielāgotas gan projektu vadītāja, gan debitora/projekta grāmatveža vajadzībām. Rēķina izrakstīšanas procesam projekta vadītājs pārvalda nepabeigto projekta norēķinu un debitors/projekta grāmatvedis izveido atbilstošu un precīzu klientam paredzētu rēķina dokumentu.

![Rēķinu izrakstīšanas plūsmas shēma.](./media/invoicing-flow.png)

Projekta līguma rinda nosaka norēķinu metodi saistītajām projekta transakcijām. Kad projektu vadītājs apstiprina laika un izdevumu darbības, sistēma reģistrē darbības entītijā **Projekta faktiskais** un nosūta informāciju uz **projektu vadības un uzskaites** moduli Dynamics 365 Finance. Pēc tam projekta grāmatvedis pārskata un izliek ierakstus, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Šajā žurnālā ir iekļauta svarīga uzskaites informācija par projekta faktiskajiem datiem, piemēram, norēķiniem, pārdošanas nodokļu grupu, norēķinu preču pārdošanas nodokļu grupu un finanšu dimensijām.

Projekta vadītājs var pārskatīt rēķinā neiekļautās pārdošanas transakcijas, izmantojot laika un materiālu norēķinu metodi [Nepabeigtajos laika un materiālu norēķinos](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) un fiksētās cenas norēķinus [Fiksētās cenas atskaites punktos](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Šie skati ļauj filtrēt un atlasīt transakcijas, kuras jāiekļauj nākamajā norēķinu ciklā, un pēc tam atzīmēt tās kā **Gatavas iekļaušanai rēķinā**.

Jūs varat [manuāli izveidot proformas rēķinu](../proforma-invoicing/create-manual-proforma-invoice.md) vai izmantot [periodisko apstrādi](../proforma-invoicing/configure-automated-invoice-creation.md). Projekta vadītājs var pēc nepieciešamības [pielāgot proformas rēķina melnrakstu](../proforma-invoicing/manage-proforma-invoice.md) un pēc tam to apstiprināt.

Apstiprināto proformas rēķinu nosūta uz Finance moduli **Projekta pārvaldība un uzskaite**. Projekta grāmatvedis formatē un atjaunina projekta rēķina priekšlikumu un pēc tam izliek un drukā šo dokumentu. Izliktos projekta rēķinus ieraksta Virsgrāmatā, kā arī Klienta un Projekta apakšgrāmatās.


[!INCLUDE[footer-include](../includes/footer-banner.md)]