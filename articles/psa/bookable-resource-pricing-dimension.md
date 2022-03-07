---
title: Rezervējama resursa izmantošana par izcenojuma dimensiju
description: Šajā tēmā ir sniegta informācija par rezervējama resursa izmantošanu par izcenojuma dimensiju.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c551673708ae2d965979136e92326be98252304a601964c1fbc52a329c592712
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988975"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Rezervējama resursa izmantošana par izcenojuma dimensiju

[!include [banner](../includes/psa-now-project-operations.md)]

Šajā tēmā ir sniegta informācija par rezervējama resursa izmantošanu par izcenojuma dimensiju. Pirms darba sākšanas, ja vēl neesat izveidojis cenas noteikšanas dimensijas risinājumu, jums būs jāizveido jauns. Ja jums jau ir cenas noteikšanas dimensijas risinājums, varat veikt izmaiņas šajā risinājumā. Ja savai organizācijai neesat izveidojis jaunu cenas noteikšanas dimensijas risinājumu, izpildiet procedūru tēmā [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Rezervējama resursa pievienošana veidlapām un skatiem
Lai padarītu laukus redzamus lietotāja interfeisā, izmantojot izcenojumu dimensijas risinājumu, jums būs jāapskata visas galveno Project Service entītiju veidlapas un skati un šie lauki jāpievieno šo entītiju veidlapām un skatiem.
Tālāk sniegtajā tabulā ir pieejams visaptverošs iekļautu veidlapu un skatu saraksts, kas tiek parādīti pēc entītijas un kas ir jāatjaunina. Ja šo entītiju pielāgojumos ir papildu skati vai veidlapas, pievienojiet jaunos laukus arī tiem.
Atveriet risinājumu pārlūku izcenojumu dimensijas risinājumam un pēc tam noklikšķiniet uz **Publicēt visus pielāgojumus**.


|   Entītija        | Veidlapas   |Skati        |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena|• Informācija |• Aktīvu resursu kategoriju cenas<br> • Ar resursu kategorijas cenu saistītais skats|
|  Lomas cenas uzcenojums|• Informācija|• Aktīvais lomas cenas uzcenojums<br>• Ar lomas cenas uzcenojumu saistītais skats|
|  Piedāvājuma rindas informācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Aktīva piedāvājuma rindas papildinformācija<br>Apvienota piedāvājuma rindas papildinformācija<br>Piedāvājuma rindas papildinformācijas saistītais skats|
|  Projekta līguma rindas papildinformācija|• Projekta informācija<br>• Projekta ātrā izveidošana|Līguma rindas apvienotā papildinformācija<br>Aktīvās līguma rindas papildinformācija<br>Līguma rindas papildinformācijas saistītais skats|
|  Projekta uzdevums|• Informācija<br>• Jauna veidlapa||
|  Projekta grupas dalībnieks|• Informācija<br>• Jauna veidlapa|• Aktīvie projekta darba grupas dalībnieki<br>• Projekta darba grupas dalībnieki<br>• Projekta grupas dalībnieku saistītais skats|
|  Laika ieraksts|• Informācija<br>• Laika ieraksta izveide|• Mani laika ieraksti pēc datuma<br>• Mani laika ieraksti šajā nedēļā<br>• Laika ieraksti apstiprināšanai|
|  Žurnāla rinda|• Informācija<br>• Ātrā izveide|• Aktīvās žurnāla rindas<br>• Žurnāla rindas saistītais skats|
|  Rēķina rindas informācija|• Informācija<br>• Ātrā izveide|• Aktīva rēķina rindas papildinformācija<br>• Rēķinā iekļaujamas darbības<br>• Papildu rēķina darbības<br>• Rēķina rindas papildinformācijas saistītais skats<br>• Rēķinā neiekļaujamas darbības|
|  Faktiski|• Informācija<br>• Aktīvās faktiskās vērtības|• Faktiskais saistītais skats|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Rezervējama resursa iestatīšana par izcenojuma dimensiju

1. Tīmekļa interfeisā pārejiet uz **Project Service** > **Iestatījumi** > **Parametri**. Lapas **Parametrs** cilnē **Uz summu balstītās izcenojumu dimensijas** ievērojiet, ka režģis parāda ierakstus izcenojumu dimensiju entītijā. 
2. Pievienojiet šim izcenojumu dimensiju sarakstam vienumu **Rezervējamais resurss** kā **msdyn_bookableresource**. 
3. Norādiet kontekstu, kurā rezervējamais resurss darbojas kā izcenojuma dimensija, un iestatiet vienumu **Attiecināms uz izmaksām** un **Attiecināms uz pārdošanu** vērtības.
4. Laukā **Dimensijas tips** atlasiet vienumu **Balstīta uz summu**. 
5. Atlasiet rezervētā resursa izmaksu un pārdošanas prioritāti. Parasti rezervējamajam resursam ir visaugstākā prioritāte, ja tas ir iekļauts kā izcenojuma dimensija, tāpēc iestatīšana uz **1** (vai **0** atkarībā no tā, kā tiek noteikta prioritāte) nodrošinātu attiecīgo uzvedību.

## <a name="set-up-pricing-dimension-field-names"></a>Izcenojumu dimensiju lauku nosaukumu iestatīšana

Ja tabulas **Lomas cena** izcenojuma dimensijas lauka nosaukums ir atšķirīgs no tās lauka nosaukuma jebkurā no citām entītijām, kurā jādarbojas cenai pēc noklusējuma, izcenojuma dimensijas ierakstam ir jābūt informācijai par atšķirīgajiem nosaukumiem.    
Attiecībā uz rezervējamo resursu entītijai **Projekta darba grupas dalībnieki** lauka nosaukums (**msdyn_bookableresourceid**) nedaudz atšķiras no nosaukuma, kas laukam ir entītijā **Lomas cena** (**msdyn_ bookableresource**). **Msydn_bookableresource** izcenojuma dimensijas ierakstam ir jābūt par to informācijai. 
1. Lai to paveiktu, veiciet dubultklikšķi uz rindas režģī **Izcenojumu dimensijas**, lai atvērtu **msdyn_bookableresource** dimensiju lapu.
2. Dimensiju lapas cilnē **Saistītie** noklikšķiniet uz **Izcenojumu dimensiju lauku nosaukumi**.

 ![Izcenojumu dimensiju lauku nosaukumu cilne.](media/PD-fieldname.png)

4. Atvērtajā saistītajā skatā noklikšķiniet uz **Pievienot jaunu izcenojuma dimensijas lauka nosaukumu**.

 ![Jaunu izcenojumu dimensiju lauku nosaukumu pievienošana.](media/Add-NewPD-fieldname.png)


Šādi tiek atvērta **msdyn_bookableresource** lapa **Jauns izcenojuma dimensijas lauka nosaukums**. 

5. Pievienojiet **msdyn_projectteam** laukam **Entītijas loģiskais nosaukums** un pievienojiet **msdyn_bookableresourceid** laukam **Lauka nosaukums**. Saglabājiet ierakstu.

 ![Jauna izcenojuma dimensijas lauka nosaukuma veidlapa.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]