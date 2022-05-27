---
title: Spraudņu atribūtu atjaunināšana ar jaunām cenu noteikšanas dimensijām
description: Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575037"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Spraudņu atribūtu atjaunināšana ar jaunām cenu noteikšanas dimensijām

Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.

> [!NOTE]
> Šī tēma attiecas tikai uz piedāvājumu un līgumu līdzekļiem risinājumā Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izpildītu šajā tēmā aprakstītās darbības, ir jāizpilda tālāk uzskaitītajās tēmās norādītās procedūras.

  - [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities-pricing-dimensions.md) 
  - [Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām ](add-custom-fields-price-setup-transactional-entities.md)
  - [Pielāgotu lauku kā cenu kategoriju iestatīšana](set-up-custom-fields-pricing-dimensions.md). 
  
Ja šīs procedūras neesat pabeidzis, pabeidziet tās un pēc tam atgriezieties pie šīs tēmas.

## <a name="register-a-plug-in"></a>Spraudņa reģistrēšana
Ja projekta piedāvājuma rindai tiek izveidota piedāvājuma rindas detaļa lapā **Piedāvājuma rinda**, sistēma izveido divas novērtējuma rindas. Viena rinda ir novērtējuma izmaksu puse, un otra rinda ir pārdošanas puse. Tas pats attiecas uz projekta līguma rindām.

Kad veicat izmaiņas daudzumā vai laukā izmaksu pusē, šīs izmaiņas tiek ieviestas arī pārdošanas pusē. Tas ir iespējams tāpēc, ka, izmantojot spraudņus PreOperation Quotelinedetail un contractline detaļu entītijās, noteikti atribūti izmaksu pusē tiek savienoti ar transakcijas pārdošanas pusi. Ja cenu noteikšanas dimensiju vērtībām pārdošanas pusē veiktās izmaiņas ir nepieciešams veikt arī izmaksu pusē, pēc izmaiņu veikšanas cenu noteikšanas dimensijā ir atkārtoti jāreģistrē tālāk minētie spraudņi.

Šie ir spraudņi, kas jāatjaunina un atkārtoti jāreģistrē.

- PreOperationContractLineDetailUpdate — **Atjaunina msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate — **Atjaunina msdyn_quotelinetransaction**

Izpildiet tālāk aprakstītās darbības, lai atjauninātu un atkārtoti reģistrētu spraudņus.

1. Atveriet **PluginRegistrationTool** un izveidojiet savienojumu ar Project Operations Dataverse vidi.
2. Atlasiet **Meklēt** un ierakstiet dažus pirmos atjaunināmā spraudņa burtus.
3. Kad spraudnis ir atrasts, atlasiet to un pēc tam atlasiet **Atlasīt galvenajā veidlapā**.
4. Atlasiet darbību **Update msdyn_orderlinetransaction**, ar peles labo pogu noklikšķiniet un pēc tam atlasiet vienumu **Atjaunināt**.
5. Dialoglodziņā **Atjaunināt** atlasiet daudzpunkti (**...**) filtrēšanas atribūtos.
6. Tiek filtrēšanas atribūtu logs, kurā ir pieejams saraksts ar visiem entītijas atribūtiem un cenu noteikšanas dimensijām. Atzīmējiet cenu noteikšanas dimensiju atribūtu izvēles rūtiņas.
7. Atlasiet **Labi**, lai aizvērtu lapu, un pēc tam atlasiet **Atjaunināšanas darbība**.
8. Otrajā spraudnī **PreOperationQuoteLineDetail** atkārtojiet 2.–7. darbību. Šim spraudnim ir nepieciešams atjaunināt darbību **Update of msdyn_quotelinetransaction**.
9. Aizveriet **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]