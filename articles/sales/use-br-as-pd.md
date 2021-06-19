---
title: Rezervējamu resursu kā cenu noteikšanas dimensiju izmantošana
description: Šajā tēmā ir sniegta informācija par rezervējama resursa izmantošanu kā izcenojuma dimensiju.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d46d4659a5f60226f80b29f3dd8607249cb91ac2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011200"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Rezervējamu resursu kā cenu noteikšanas dimensiju izmantošana

 _**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_ 

Šajā tēmā ir sniegta informācija par rezervējama resursa izmantošanu kā izcenojuma dimensiju. Ja jūsu cenu noteikšanas stratēģija ir iestatīta tā, lai katram rezervējamajam resursam būtu noteikta cena vai izmaksu likme, izmantojiet rezervējamo resursu kā cenu noteikšanas dimensiju.

## <a name="prerequisites"></a>Priekšnosacījumi
Pirms šajā tēmā aprakstīto procedūru veikšanas ir nepieciešams jauns organizācijas cenu dimensiju risinājums. Ja tas vēl nav paveikts, skatiet tēmu [Pielāgotu lauku un entītiju izveide](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Rezervējamu resursu lauka pievienošana veidlapām un skatiem
Lai lauks **Rezervējamais resurss** būtu redzams cenu noteikšanas dimensijas risinājumā, šis lauks ir jāpievieno visām veidlapām un skatiem kā entītija.

Tālāk redzamajā tabulā ir uzskaitītas visas iebūvētās veidlapas un skati pēc entītijas. Turklāt jaunais lauks būs jāpievieno arī visām papildu veidlapām vai skatiem jūsu pielāgotajās entītijās.

|   Elements        | Veidlapas   |Skati        |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena| Informācija | - Aktīvu resursu kategoriju cenas<br> - Resursu kategorijas cenu saistītais |
|  Lomas cenas uzcenojums| Informācija| - Aktīvais lomas cenas uzcenojums<br>- Lomas cenas uzcenojuma saistītais |
|  Piedāvājuma rindas informācija| - Projekta informācija<br>- Projekta ātrā izveidošana| - Aktīva piedāvājuma rindas detalizēta informācija<br>- Apvienota piedāvājuma rindas detalizēta informācija<br>- Piedāvājuma rindas detalizētās informācijas saistītais |
|  Projekta līguma rindas papildinformācija| - Projekta informācija<br>- Projekta ātrā izveidošana| - Līguma rindas apvienotā informācija<br>- Aktīvās līguma rindas informācija<br>- Līguma rindas papildinformācijas saistītais |
|  Projekta uzdevums| - Informācija<br>- Jauna veidlapa| &nbsp; |
|  Projekta grupas dalībnieks| - Informācija<br>- Jauna veidlapa| - Aktīvie projekta grupas dalībnieki<br>- Projekta darba grupas dalībnieki<br>- Projekta grupas dalībnieku saistītais |
|  Laika ieraksts| - Informācija<br>- Izveidot laika ierakstu| - Mani laika ieraksti pēc datuma<br>- Mani laika ieraksti šajā nedēļā<br>- Laika ieraksti apstiprināšanai|
|  Žurnāla rinda| - Informācija<br>- Ātrā izveide| - Aktīvās žurnāla rindas<br>- Žurnāla rindas saistītais |
|  Rēķina rindas informācija| - Informācija<br>- Ātrā izveide| - Aktīva rēķina rindas informācija<br>- Rēķinā iekļaujamas transakcijas<br>- Papildu rēķina transakcijas<br>- Rēķina rindas informācijas saistītais <br>- Rēķinā neiekļaujamas transakcijas|
|  Faktiski| - Informācija<br>- Aktīvās faktiskās vērtības| Faktiskais saistītais |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Rezervējama resursa iestatīšana par izcenojuma dimensiju
Lai iestatītu rezervējamu resursu kā izcenojuma dimensiju, izpildiet tālāk minētās darbības.

1. Pārejiet uz **Iestatījumi** > **Parametri**. 
2. Lapā **Parametrs**, cilnē **Uz summu balstītās cenu noteikšanas dimensijas** pārliecinieties, ka režģis parāda ierakstus entītijā **Cenu noteikšanas dimensijas**. 
2. Pievienojiet šim izcenojumu dimensiju sarakstam vienumu **Rezervējamais resurss** kā **msdyn_bookableresource**. 
3. Atlasiet vērtību vienumiem **Attiecināms uz izmaksām** un **Attiecināms uz pārdošanu**.
4. Laukā **Dimensijas tips** atlasiet vienumu **Balstīta uz summu**. 
5. Atlasiet rezervētā resursa izmaksu un pārdošanas prioritāti. Parasti rezervējamajam resursam ir visaugstākā prioritāte, ja tas ir iekļauts kā cenas noteikšanas dimensija. Lai nodrošinātu šādu darbību, iestatiet prioritāti **1** (vai **0** atkarībā no tā, kā tiek skaitīta prioritāte).

## <a name="set-up-pricing-dimension-field-names"></a>Izcenojumu dimensiju lauku nosaukumu iestatīšana

Ja tabulas **Lomas cena** izcenojuma dimensijas lauka nosaukums ir atšķirīgs no lauka nosaukuma jebkurā no citām entītijām, kurā tiek izmantota noklusējuma cena, izcenojuma dimensijas ierakstam ir jābūt informācijai par atšķirīgajiem nosaukumiem.  

Attiecībā uz rezervējamo resursu entītijai **Projekta darba grupas dalībnieki** lauka nosaukums nedaudz atšķiras no nosaukuma, kas laukam ir entītijā **Lomas cena**. 

 - **Projekta grupas dalībnieki** entītija = **msdyn_bookableresourceid**
 - **Lomas cena** entītija = **msdyn_bookableresource**

**Msydn_bookableresource** izcenojuma dimensijas ierakstam ir jābūt par to informācijai.

1. Veiciet dubultklikšķi uz rindas režģī **Izcenojumu dimensijas**, lai atvērtu **msdyn_bookableresource** dimensiju lapu.
2. Dimensiju lapas cilnē **Saistītie** atlasiet **Izcenojumu dimensiju lauku nosaukumi**.

  ![Izcenojumu dimensiju lauku nosaukumu cilne](media/PD-fieldname.png)

3. Atvērtajā saistītajā skatā atlasiet **Pievienot jaunu izcenojuma dimensijas lauka nosaukumu**.

  ![Jaunu izcenojumu dimensiju lauku nosaukumu pievienošana](media/Add-NewPD-fieldname.png)

  Šādi tiek atvērta **msdyn_bookableresource** lapa **Jauns izcenojuma dimensijas lauka nosaukums**. 

4. Lapā **Pievienot jaunu izcenojuma dimensijas lauka nosaukumu** pievienojiet **msdyn_projectteam** **Entītijas loģiskajam nosaukumam**.
5. Pievienojiet **msdyn_bookableresourceid** **Lauka nosaukumam**.

 ![Jauna izcenojuma dimensijas lauka nosaukuma veidlapa](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]