---
title: Piegādātāja maksājuma saglabāšanas nosacījumu izveide un lietošana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt un uzturēt saglabāšanas nosacījumus piegādātāju maksājumiem.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3961d18fcd53381ad43a1d3e598ac61652ba9843
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685111"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Piegādātāja maksājuma saglabāšanas nosacījumu izveide un lietošana

[!include [banner](../includes/banner.md)] 

Ja jūsu organizācija vēlas saglabāt daļu no piegādātājam veiktajiem maksājumiem, ir noderīgi iestatīt piegādātāja maksājumu saglabāšanas nosacījumus projektam. Piemēram, ja vēlaties, lai maksājums piegādātājam tiktu aizturēts, līdz piegādātie produkti atbilst jūsu vēlmēm. Piegādātāja maksājuma saglabāšanas nosacījumus var norādīt, vienojoties par piegādātāja līgumu.

## <a name="create-vendor-payment-retention-terms"></a>Piegādātāja maksājuma saglabāšanas nosacījumu izveide

Var ievadīt procentuālo daļu, kas jāsaglabā no piegādātāja maksājuma, kā arī procentuālo daļu no iepriekš saglabātajām summām, kas jāizlaiž. Summas tiek automātiski saglabātas piegādātāja rēķinos, līdz līgums sasniedz norādīto pabeigšanas statusu. Kad esat iestatījis saglabāšanas nosacījumus, varat tos lietot jebkuram šī piegādātāja projektam.

Izmantojiet tālāk norādītās darbības, lai iestatītu un uzturētu piegādātāja maksājumu saglabāšanas nosacījumus. 

1. Atveriet **Projekta pārvaldības un grāmatvedības** > **Saglabāšana** > **Piegādātāja maksājumu saglabāšanas nosacījumi**.
2. Atlasiet **Jauns**, lai pievienotu jaunu piegādātāja saglabāšanas nosacījumu. Lauka **Kārtulas ID** vērtība jaunajam nosacījumam tiek ievadīta automātiski. 
3. Laukā **Apraksts** ievadiet īsu aprakstu, bet FastTab cilnē **Nosacījumi** atlasiet **Pievienot rindu**, lai ievadītu nosacījuma vērtības tālāk minētajām opcijām.

   - **Piegādāto vienību procents**: ievadiet nosacījuma pabeigtības procentuālo daļu. Summas tiek automātiski saglabātas piegādātāja rēķinos, līdz projekta pabeigtības posms ir vienāds ar norādīto procentuālo daļu. Piemēram, ja ievadīsiet 50,00, summas tiek saglabātas, līdz projekta pabeigtība ir 50 procenti.
   - **Procentuālā vērtība, kas jāsaglabā**: ievadiet piegādātāja rēķina summas procentuālo vērtību, kas jāsaglabā. Piemēram, ja ievadīsiet 10,00, tad 10 procenti no piegādātāja rēķina summas tiek saglabāti, līdz projekts sasniedz pabeigtības procentuālo vērtību, kas iestatīta laukā **Piegādāto vienību procentuālā vērtība**.
   - **Atbrīvošanas procentuālā vērtība**: atlasiet **Pievienot rindu**, lai ievadītu jebkuras iepriekš saglabātās summas procentuālo vērtību, kas ir jāatbrīvo atbilstoši atlasītajam projekta izpildes līmenim.

> [!NOTE]
> Ja jums ir vairāk nekā viens atskaites punkts dažādiem projekta pabeigšanas līmeņiem, ievadiet atsevišķu piegādātāja saglabāšanas nosacījuma rindu katrai saglabāšanas kārtulai. Katrā rindā var norādīt citu saglabāšanas procentuālo vērtību un atšķirīgu atbrīvošanas procentuālo daļu katram piešķirtajam projekta pabeigšanas līmenim.

Kad esat izveidojis piegādātāja saglabāšanas nosacījumus, varat tos lietot projektam.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Piegādātāja saglabāšanas nosacījumu lietošana projektam

1. Atveriet **Projektu pārvaldība un grāmatvedība** > **Projekti** > **Visi projekti** un projektu saraksta lapā atveriet projektu.
2. Kopsavilkuma cilnē **Piegādātāju līgumi** atlasiet **Pievienot rindu**.
3. Laukā **Uzņēmuma kods** atlasiet vienu no tālāk minētajām opcijām. 

   - **Tabula**: piegādātāja saglabāšanas nosacījumi attiecas uz vienu piegādātāju.
   - **Grupa**: piegādātāja saglabāšanas nosacījumi attiecas uz visiem grupā esošajiem piegādātājiem.
   - **Visi**: piegādātāju saglabāšanas nosacījumi attiecas uz visiem piegādātājiem.

4. Laukā **Piegādātājs/piegādātāju grupa** atlasiet piegādātāju vai piegādātāju grupu, uz kuru attiecas piegādātāju saglabāšanas nosacījumi. Ja iepriekšējā darbībā atlasāt **Visi**, šis lauks nav pieejams.
5. Laukā **Piegādātāju saglabāšanas nosacījumi** atlasiet saglabāšanas nosacījumus, ko izveidojāt iepriekšējā procedūrā.
6. Ja projektā piegādātājam ir iestatīti arī maksāt-kad-apmaksāts (PWP) nosacījumi, ievadiet projekta sliekšņa procentuālo vērtību laukā **PWP sliekšņa procentuālā vērtība**.

Piegādātāja saglabāšanas nosacījumi tiek rādīti arī pirkšanas pasūtījumos, ko izveidojat šim piegādātājam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]