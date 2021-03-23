---
title: Pielāgotu risinājumu izveide cenu noteikšanas dimensijām
description: Šajā tēmā izskaidrots, kā izveidot pielāgotu risinājumu, veidojot pielāgotas cenu noteikšanas dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284997"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Pielāgotu risinājumu izveide cenu noteikšanas dimensijām

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Visām pielāgoto cenu noteikšanas dimensiju izmaiņām jābūt atsevišķā risinājumā. Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā. Pēc nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenu noteikšanas iestatījumus.

1. Izvēlieties **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns**. 
2. Nosauciet risinājumu **\<your organization name>cenu noteikšanas dimensijas**, ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

> ![Pielāgota risinājuma izveide cenu noteikšanas dimensijām](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenu noteikšanas dimensijas risinājumam
Cenas risinājumam ir jāpievieno tālāk norādītās Project Service entītijas. Izpildiet šajā procedūrā norādītās darbības, lai veiktu dažas svarīgas shēmas izmaiņas cenas noteikšanas risinājumā un lai entītijas apzinātos jaunās cenu noteikšanas dimensijas.

1. Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.
3. Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:

- Faktiski
- Rezervējamais resurssss
- Novērtēšanas rinda
- Projekta uzdevums
- Rēķina rindas informācija
- Žurnāla rinda
- Projekta līguma rindas informācija
- Projekta grupas dalībnieks
- Piedāvājuma rindas informācija
- Lomas cenas uzcenojums
- Lomas cena 
- Laika ieraksts 

> ![Esošu entītiju pievienošana cenu dimensiju risinājumam](media/Existing-entities-to-PD-solution.png)

> ![Atlasiet risinājuma komponentus](media/Dimension-Components.png)

> [!NOTE]
> Pārliecinieties, vai visām atlasītajām entītijām ir atlasītas visas formas un skati.

4. Kad atlasītajām entītijām tiek piedāvāts iekļaut atkarīgās entītijas, atlasiet **Nē**.

> ![Neiekļaut nepieciešamos komponentus.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]