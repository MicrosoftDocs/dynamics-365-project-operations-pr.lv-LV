---
title: Uz produktu balstītas piedāvājuma rindas
description: Šajā tēmā ir sniegta informācija par piedāvājuma rindām, kuras ir balstītas uz produktu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284097"
---
# <a name="product-based-quote-lines"></a>Uz produktu balstītas piedāvājuma rindas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Programmā Dynamics 365 Project Service Automation varat izveidot uz produktu balstītas piedāvājuma rindas. Uz produktu balstītas piedāvājuma rindas var būt “ierakstāmas” rindas, vai tās var būt vienumi no produkti kataloga.

## <a name="product-catalog"></a>Preču katalogs

Produktiem Dynamics 365 produktu katalogā ir noklusējuma vienība un vienību grupa. Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai arī ir šie atribūti. Visi produkti vienā produktu saimē pārmanto vienādu atribūtu kopu.

Piemēram, uzņēmums pārdod abonementa licences dažāda veida programmatūrai. Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.

- Lietotāju skaits 
- Abonementa ilgums (mēnešos)

Labs veids, kā uzturēt šāda tipa katalogu, ir izveidot produktu saimi, kuras nosaukums ir **Abonējama programmatūra** un kurai ir atribūti **Lietotāju skaits** un **Abonementa ilgums**. Pēc tam produktu saimei **Abonējama programmatūra** varat pievienot atsevišķus produktus, piemēram, **Dynamics 365 Sales** vai **Dynamics 365 Field Service**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Produktu kataloga vienumu pievienošana projekta piedāvājumam

Projekta piedāvājuma un projekta līguma lapās ir sadaļas divu tipu rindām: uz projektu balstītām rindām un uz produktu balstītām rindām. Rindām, kas ir balstītas uz produktu, programmatūra Dynamics 365 tiek izmantota, lai piedāvājumam pievienotu vienumus no produktu kataloga. Piedāvājuma rindas vai projekta līguma rindas nolaižamajā sarakstā ir iekļauti visi produkti un vienības attiecīgajā produktu cenrādī, kurš ir pievienots šim piedāvājumam vai projekta līgumam. Varat arī pievienot produktus, kas neveido daļu no piedāvājuma produktu cenrāža.

Turklāt varat atlasīt produktus no citiem cenrāžiem, kā arī varat atlasīt produktus tieši no produktu kataloga. Ja produktus atlasāt tieši no kāda produktu kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis. Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz 0 (nulle).

Ja piedāvājuma rinda ir balstīta uz produktu katalogu, pārdošanas cenu varat pārlabot tieši piedāvājuma rindā. Ņemiet vērā, ka piedāvājuma rindai programmatūrā Dynamics 365 ir lauks **Cenu noteikšana**. Ir pieejamas divas vērtības:

- Pārlabot izcenojumu  
- Izmantot noklusējumu

Ja šo lauku iestatāt uz **Pārlabot izcenojumu**, Dynamics 365 neiestata noklusējuma cenu. Jums ir jāievada cena šim produktam piedāvājuma rindā. Ja šo lauku iestatāt uz **Izmantot noklusējumu**, Dynamics 365 izmanto noklusējuma pārdošanas cenu un bloķē šo lauku, lai nepieļautu turpmāku rediģēšanu.

Pēc PSA instalēšanas piedāvājuma uz produktu balstītajās rindās tiek ievadītas noklusējuma pārdošanas cenas. Pēc tam lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot izcenojumu**, lai jūs varētu rediģēt noteiktā cenu piedāvājuma rindās.

> ![Cenu pārlabošanas iestatīšana](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Daudzuma koeficienti produktiem

Lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, PSA izmanto daudzuma koeficientus. Uz abonēšanu balstītiem produktiem daudzums piedāvājumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.

Parasti abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī. Taču varat izmantot arī citus laika aprakstus. Pārdošanas procesa laikā cena piedāvājuma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents. Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits. Daudzums, kas tiek izmantots piedāvājuma rindas summas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.

Lai atbalstītu šāda tipa pārdošanu, PSA ieviesa daudzuma koeficientu jēdzienu. Daudzuma koeficienti izmanto produkta atribūtus programmā Dynamics 365. Kad kādam produktam konfigurējat konkrētus rekvizītus, PSA ļauj jums atzīmēt šo rekvizītu apakškopu vai visus rekvizītus kā daudzuma faktorus.

PSA pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips. Ja produkts, kuram ir konfigurēti daudzuma koeficienti, tiek pievienots piedāvājuma rindai, lauks **Daudzums** šajā piedāvājuma rindā kļūst par tikai lasāmu lauku. Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, PSA aprēķina piedāvājuma rindas daudzumu.

Programmatūrā Dynamics 365 varētu būt, piemēram, tālāk norādītie rekvizīti. 

- **Lietotāju skaits** — lietotāju skaits 
- **Mēnešu skaits** — abonēšanas mēnešu skaits
- **Produkta SKU** 

Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** var atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus. 

> ![Lietotāju skaita un mēnešu skaita kā kvalitātes koeficientu atzīmēšana](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]