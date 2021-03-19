---
title: Azure abonementa pievienošana LCS projektam
description: Šajā tēmā ir sniegta informācija par to, kā pievienot Azure abonementu LCS projektam.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289918"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure abonementa pievienošana LCS projektam

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Mākoņpakalpojumā viesotas vides ir jāizvieto, izmantojot esošu Azure abonementu. Šajā tēmā ir izskaidrots, kā pievienot esošu Azure abonementu LCS projektam. 

## <a name="grant-admin-consent"></a>Administratora piekrišanas piešķiršana

1. Sava LCS projekta sadaļā **Vides** atlasiet **Microsoft Azure iestatījumi**.

![Microsoft Azure iestatījumi](./media/1MicrosoftAzureSettings.png)

2. Lapas **Projekta iestatījumi** cilnē **Azure savienotāji** atlasiet **Autorizēt**. Tas ļauj izvietot vides šajā projektā.

![Azure savienotāji](./media/2AzureConnectors.png)

3. Vēlreiz atlasiet **Autorizēt**, lai sniegtu administratora piekrišanu.

![Administratora piekrišanas piešķiršana](./media/3GrantAdminConsent.png)

4. Piekrītiet atļauju pieprasījumam.

![Piekrist atļaujas pieprasījumam](./media/4AcceptPermissionRequest.png)

Autorizācija tagad ir pabeigta. 

![Autorizācija ir veiksmīga](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Piekļuves sniegšana pakalpojumam Dynamics Deployment Services jūsu Azure abonementam

1. Dodieties uz [Microsoft Azure norēķini](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) un atlasiet savu abonementu. Pakalpojumam Dynamics Deployment Services ir nepieciešama piekļuve šim abonementam, lai varētu izvietot vides.

![Azure abonementa informācija](./media/6AzureSubscription.png)

2. Navigācijas rūtī atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Pievienot lomas piešķiri**.
3. Labajā pusē esošajā slīdnī atlasiet **Līdzstrādnieka loma** un piedāvātajā sarakstā atrodiet un atlasiet **Dynamics Deployment Services**. 
4. Atlasiet vienumu **Saglabāt**.

![Piekļuve abonementam](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Abonementa savienotāja pievienošana LCS projektam

1. Sava LCS projekta lapā **Microsoft Azure iestatījumi** atlasiet **Pievienot**, lai pievienotu jaunu savienotāju.
2. Ievadiet sava Azure abonementa ID. Sava Azure abonementa ID varat atrast [Azure portāla](https://ms.portal.azure.com/) sadaļā **Iestatījumi** ekrāna apakšējā kreisajā stūrī.
3. Laukā **Konfigurēt Azure Resource Manager izmantošanu** atlasiet **Jā**.
4. Pārliecinieties, vai Azure abonementa AAD nomnieka domēns atbilst jūsu izmantotajam Azure abonementam, kam pieder domēns, un atlasiet **Tālāk**.
5. Ekrānā **Microsoft Azure iestatīšana** atlasiet **Tālāk**, lai apstiprinātu. Ja šajā ekrānā tiek parādīts kļūdas ziņojums, atgriezieties šīs tēmas sadaļā [Piekļuves sniegšana pakalpojumam Dynamics Deployment Services jūsu Azure abonementam](#provide) un pārliecinieties, vai esat izpildījis visas darbības.
6. Lejupielādējiet Azure pārvaldības sertifikātu lokālā mapē savā datorā un pēc tam augšupielādējiet to Azure pārvaldības portālā, atverot **Iestatījumi** > **Pārvaldības sertifikāti**. Šis sertifikāts ļaus LCS sazināties ar Azure jūsu vārdā. Ja lietotājam ir piekļuve abonementam, varat izlaist šo darbību.
7. Atlasiet **Tālāk**.
8. Atlasiet Azure reģionu, kurā veikt izvietošanu, un atlasiet datu centru, kas atrodas tuvu vietai, kurā plānojat lietot šo sistēmu.
9.  Atlasiet **Pievienot**.

Esat veiksmīgi pievienojis savu Azure abonementu. Tagad varat izvietot Dynamics 365 Finance mākoņpakalpojumā viesotas vides.




[!INCLUDE[footer-include](../includes/footer-banner.md)]