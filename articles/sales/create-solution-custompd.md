---
title: Risinājuma izveide pielāgotām cenu noteikšanas dimensijām
description: Šajā tēmā ir sniegta informācija par to, kā izveidot risinājumus pielāgotām cenu noteikšanas dimensijām.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010345"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Risinājuma izveide pielāgotām cenu noteikšanas dimensijām

 _**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_ 

>[!IMPORTANT]
>Visām pielāgoto cenu noteikšanas dimensiju izmaiņām jābūt atsevišķā risinājumā. Šī svarīgā paraugprakse nodrošina elastību, lai atjauninātu vai noņemtu nepieciešamās izmaiņas, tā arī palīdz atkārtoti izmantot darbu un vienkāršo izmaiņu saglabāšanu citās instancēs. Pēc nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldītu risinājumu** un pēc tam importējiet to citās instancēs atkārtotai izmantošanai.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Risinājuma izveide pielāgotām cenu noteikšanas dimensijām

1.  Izvēlieties **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns**.
2.  Piešķiriet risinājumam nosaukumu *<your organization name> cenu noteikšanas dimensijas*.
3. Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.

  ![Pielāgotas cenu noteikšanas dimensijas risinājuma izveide](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenu noteikšanas dimensijas risinājumam

Pievienojiet tālāk norādītās Project Service entītijas savam cenu noteikšanas risinājumam, lai veiktu svarīgas shēmas izmaiņas cenu noteikšanas risinājumā. Pēc procedūras pabeigšanas entītijas atpazīs jaunās cenu noteikšanas dimensijas.

1.  Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **<*Organizācijas nosaukums*> Cenu noteikšanas dimensijas**.
2.  Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.
3.  Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:
 
   - **Faktiski**
   - **Rezervējamais resurssss**
   - **Novērtēšanas rinda**
   - **Projekta uzdevums**
   - **Rēķina rindas informācija**
   - **Žurnāla rinda**
   - **Projekta līguma rindas informācija**
   - **Projekta grupas dalībnieks**
   - **Piedāvājuma rindas informācija**
   - **Lomas cenas uzcenojums**
   - **Lomas cena**
   - **Laika ieraksts**
 
   ![Esošu entītiju pievienošana pielāgotu cenu noteikšanas dimensiju risinājumam](./media/Existing-entities-to-PD-solution.png)
 
 4. Katrai entītijai pārskatiet pievienojamos komponentus un entītiju līdzekļu galīgo sarakstu. 

   >[!NOTE]
   > Iekļaujiet visas veidlapas un skatus katrai atlasītajai entītijai.

  ![Pievienotās entītijas](./media/solution-component-selection.png)


5.  Kad tiek piedāvāts iekļaut jebkādas atlasīto entītiju atkarīgās entītijas, atlasiet **Nē, neiekļaut nepieciešamos komponentus.**

    ![Atkarīgo entītiju iekļaušana](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]