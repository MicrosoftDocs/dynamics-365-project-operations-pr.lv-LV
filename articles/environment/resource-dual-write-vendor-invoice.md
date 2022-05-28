---
title: Piegādātāja rēķina integrācija
description: Šajā tēmā ir sniegta informācija par piegādātāju rēķinu integrāciju programmā Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591184"
---
# <a name="vendor-invoice-integration"></a>Piegādātāja rēķina integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Ar projektu saistītu Dynamics 365 Project Operations sagādi var ierakstīt, dodoties uz **Kreditori** > **Rēķini** > **Neapstiprinātie piegādātāju rēķini** un izmantojot neapstiprināto piegādātāju rēķinu dokumentu. Papildinformāciju skatiet sadaļā [Krājumos neesošu materiālu iegāde, izmantojot neapstiprinātu piegādātāju rēķinu](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Pirms šajā tēmā aprakstītās funkcionalitātes izmantošanas pārskatiet un lietojiet nepieciešamās konfigurācijas. Papildinformāciju skatiet sadaļā [Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu iespējošana](../procurement/configure-materials-nonstocked.md).

Programmā Project Operations ar projektiem saistītie piegādātāju rēķini tiek grāmatoti, izmantojot īpašas grāmatošanas kārtulas.

- Ar projektiem saistītās izmaksas (ieskaitot neatgūstamos nodokļus) netiek nekavējoties grāmatotas projekta izmaksu kontā virsgrāmatā. Tā vietā izmaksas tiek grāmatotas **sagādes integrācijas kontā**. Šis konts tiek konfigurēts sadaļas **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldības un uzskaites parametri** cilnē **Project Operations on Dynamics 365 Customer engagement**.
- Duālā rakstīšana sinhronizē piegādātāja informāciju ar Microsoft Dataverse, izmantojot tālāk norādītās tabulu kartes.

     - **Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices)**: šī tabulas karte sinhronizē piegādātāju rēķinu galvenes informāciju. Ar Dataverse tiek sinhronizēti tikai to piegādātāju rēķini, kuriem ir vismaz viena rinda ar projekta ID.
     - **Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines)**: šī tabulas karte sinhronizē piegādātāju rēķinu rindu informāciju. Ar Dataverse tiek sinhronizētas tikai tās rindas, kurās ir projekta ID.

     > [!NOTE]
     > Risinājumā Dataverse nav iespējams rediģēt piegādātāju rēķinu informāciju.

Nodokļu apakšgrāmatas, kreditoru apakšgrāmatas un citi finanšu grāmatojumi tiek reģistrēti kā piemērojami Dynamics 365 Finance kad tiek grāmatots kreditora rēķins.

![Piegādātāja rēķina integrācija.](media/DW7VendorInvoice.png)

Kad ieraksti tiek ierakstīti Dataverse entītijā **Piegādātāja rēķins**, sākas automatizēts ierakstu apstiprināšanas process. Ja nepieciešams, automatizēto apstiprināšanas statusu var pārskatīt risinājumā Dataverse, dodoties uz **Papildu iestatījumi** > **Sistēma** > **Sistēmas uzdevumi**. Pēc apstiprinājuma pabeigšanas sistēma izveido materiālu transakciju klases ierakstus entītijā **Faktiskie dati**.

Ar materiāliem saistītie faktiskie dati pēc tam tiek apstrādāti, izmantojot duālās rakstīšanas tabulas karti **Project Operations integrācijas faktiskie dati (msdyn_actuals)**. Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md).

Periodiskais process **Importēt no izstādīšanas** izveido ar piegādātāja rēķinu saistītas Project Operations integrācijas žurnāla rindas. Nobīdes konts pēc noklusējuma tiek mainīts uz sagādes integrācijas kontu. Kad tiek grāmatots integrācijas žurnāls, tiek notīrīta piegādātāja rēķina transakcijas konta bilance, un rindas summa tiek pārvietota uz projekta izmaksu kontu. Projekta apakšgrāmatas transakcijas tiek izveidotas arī lejupstraumes rēķinu izrakstīšanas un ieņēmumu atpazīšanas nolūkiem.
