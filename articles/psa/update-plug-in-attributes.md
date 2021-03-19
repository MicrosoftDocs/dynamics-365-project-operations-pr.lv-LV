---
title: Spraudņu atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas
description: Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281802"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Spraudņu atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ja neizmantojat Project Service Automation (PSA) piedāvājuma un līguma funkcijas, varat izlaist šo tēmu.

Šajā tēmā tiek pieņemts, ka esat pabeidzis tēmā norādītās procedūras: [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md), [Pielāgotu lauku pievienošana cenas iestatīšanas un transakciju entītijām](field-references.md) un [Pielāgotu lauku iestatīšana kā cenu noteikšanas dimensijas](set-up-pricing-dimensions.md). Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas.

Kad piedāvājuma rindas papildinformācija tiek izveidota **Piedāvājuma rindas** lapā projekta piedāvājuma rindai, sistēma fonā izveido divas aprēķinu rindas — vienu rindu izmaksu aprēķiniem pusei un vienu pārdošanas aprēķiniem. Tas pats attiecas uz projekta līguma rindām.

Kad veicat izmaiņas daudzumā vai laukā izmaksu pusē, šīs izmaiņas tiek ieviestas pārdošanas pusē. Tas ir iespējams tālāk minēto spraudņu dēļ, kas ir atkārtoti jāreģistrē pēc izmaiņām cenu noteikšanas dimensijās.

- PreOperationContractLineDetailUpdate - Atjauninājumi **msdyn_orderlinetransaction**.
- PreOperationContractLineDetailUpdate - Atjauninājumi **msdyn_orderlinetransaction**.

Tālāk aprakstītās darbības izskaidro spraudņu reģistrēšanas procesu.

1. Atveriet **PluginRegistrationTool** un izveidojiet savienojumu ar tiešsaistes instanci.
2. Noklikšķiniet uz **Meklēšana** un meklējiet spraudni atjaunināšanai.

 ![Meklēšanas koka ekrānuzņēmums](media/PRT-1.png)

3. Kad spraudnis ir atrasts, atlasiet to un pēc tam noklikšķiniet uz **Atlasīt galvenajā veidlapā**.

4. Atlasiet atjaunināmā spraudņa darbību, noklikšķiniet ar peles labo pogu un pēc tam atlasiet **Atjaunināt**.

 ![Tiek atjaunināts spraudņa ekrānuzņēmums](media/PRT-2.png)
 
5. Atjaunināšanas logā noklikšķiniet uz daudzpunktes (**...**) filtrēšanas atribūtos.

 ![Esošās darbības konfigurācijas informācijas atjauninājuma ekrānuzņēmums](media/PRT-3.png)
 
6. Atzīmējiet cenu noteikšanas atribūtu izvēles rūtiņas.

 ![Ekrānuzņēmums, kas parāda izvēles rūtiņu atlasi cenu noteikšanas atribūtiem](media/PRT-4.png)

7. Noklikšķiniet uz **Labi**, lai aizvērtu lapu, un pēc tam atlasiet **Atjaunināšanas darbība**.

 ![Ekrānuzņēmums, kurā redzama poga “Atjaunināšanas darbība”](media/PRT-5.png)
 
8. Atkārtojiet šo procesu otrajam spraudnim, **PreOperationQuoteLineDetail msdyn_quotelinetransaction**.

9. Aizveriet spraudņa reģistrācijas rīku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]