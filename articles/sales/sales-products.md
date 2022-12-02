---
title: PRECES
description: Šajā rakstā sniegta informācija par produktu katalogu, kuru varat izmantot, lai klientiem sniegtu informāciju par jūsu organizācijas piedāvātajiem produktiem un cenām.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d45a705c48df84a8f5b3f60121fbcc25e225e6e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933087"
---
# <a name="products"></a>Produkti

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Produkti ir jūsu uzņēmuma pamatā. Preču katalogs programmā Dynamics 365 Sales Professional ir produktu un to izcenojuma informācijas kolekcija. Atvieglojiet pārdošanas apjomu palielināšanu saviem pārdošanas pārstāvjiem, ātri izveidojot preču katalogu.

## <a name="add-a-product"></a>Produkta pievienošana

1.  Pārliecinieties, ka jums ir Sales Professional vadītāja vai sistēmas administratora loma, lai jūs varētu pievienot produktus programmā Dynamics 365 Sales Professional.
2.  Vietnes kartes sadaļā **Iestatīšana** atlasiet **Produkti**.
3.  Atlasiet **Pievienot produktu** un aizpildiet šādu informāciju:

    -  **Nosaukums**
    -  **Produkta ID**
    -  **Vecākelements:** Atlasiet galveno produktu saimi. Ja pakārtotu produktu veidojat produktu saimē, šeit tiek aizpildīts primārās produktu saimes nosaukums. To nevar mainīt pēc tam, kad ieraksts ir saglabāts.
    -  **Derīgs no**/**Derīgs līdz**: definējiet produkta derīguma periodu, atlasot vienuma **Derīgs no** un **Derīgs līdz** datumu.
    -  **Vienību grupa**: atlasiet vienību grupu. Vienību grupa ir dažādu vienību kolekcija, kādās produkts tiek pārdots, un tā nosaka, kā atsevišķi vienumi tiek grupēti lielākos daudzumos. Piemēram, kā produktu pievienojot sēklas, varat izveidot vienību grupu “Sēklas” un noteikt tās primāro vienību — “paciņa”.
    -  **Noklusējuma vienība**: atlasiet biežāk lietoto vienību, kādā produkts tiks pārdots. Vienības daudzums vai mērvienības, kādā produkts tiek pārdots. Piemēram, ja pievienojat preci “Sēklas”, tās varat pārdot paciņās, kastēs vai paletēs. Tās visas kļūst par produkta par vienību. Ja sēklas visbiežāk tiek pārdotas paciņās, atlasiet to kā vienību.
    -  **Noklusējuma cenrādis**: ja šis produkts ir jauns, šis lauks ir tikai lasāms. Lai varētu atlasīt noklusējuma cenrādi, vispirms ir jāaizpilda visi obligātie lauki un jāsaglabā ieraksts. Kaut arī noklusējuma cenrādis nav obligāts, pēc produkta ieraksta saglabāšanas ir ieteicams iestatīt noklusējuma cenrādi katram produktam. Pēc tam, ja klienta ierakstā nav ietverts cenrādis, programma Sales var izmantot noklusējuma cenrādi, lai ģenerētu piedāvājumus, pasūtījumus un rēķinus.
    -  **Atbalstītais zīmju skaits aiz komata**: ievadiet veselu skaitli no 0 līdz 5. Ja produktu nevar iedalīt daļējos daudzumos, ievadiet 0. Ja ar produktu nav saistīts cenrādis, šī lauka vērtība tiek izmantota, lai pārbaudītu piedāvājuma, pasūtījuma vai rēķina preces ieraksta lauka **Daudzums** vērtības precizitāti.
    -  **Tēma**: saistiet šo produktu ar kādu tēmu. Tēmas var izmantot, lai kategorizētu produktus un filtrētu atskaites.

4.  Atlasiet vienumu **Saglabāt**.
5.  Cilnes **Papildinformācija** sadaļā **Cenrāža elementi** atlasiet ikonu **Vairāk komandu** un pēc tam atlasiet **Pievienot jaunu cenrāža elementu**.
7.  Cilnes **Papildinformācija** sadaļā **Produktu relācija** atlasiet ikonu **Vairāk komandu** un pēc tam atlasiet **Pievienot jaunu produktu relāciju**.
8.  Veidlapā **Jauna produktu relācija** ievadiet tālāk norādīto informāciju un komandjoslā atlasiet **Saglabāt un aizvērt**.

    -   **Saistītais produkts**: Atlasiet produktu, ko vēlaties pievienot kā saistīto produktu jau esošajam produkta ierakstam, ar kuru strādājat.
    -   **Pārdošanas relāciju veids**: Atlasiet, vai produktu vēlaties pievienot kā papildu produktu, šķērspārdošanas produktu, piederumu vai aizstājējproduktu.
    -   **Virziens**: Atlasiet, vai produktu relācija ir vienvirziena vai divvirzienu. Atlasot vienvirziena opciju, sadaļā **Saistītais produkts** atlasītais produkts tiks parādīts kā ieteikums esošajam produktam, bet ne otrādi.

9.  Produkta veidlapā atlasiet **Saglabāt**.

## <a name="import-products"></a>Importēt produktus

Varat izmantot importēšanas veidnes, lai pārvietotu lielapjoma produktu datus uz programmu Dynamics 365 Sales.

## <a name="revise-a-product"></a>Produkta mainīšana

Uzturiet produktu krājumus vienmēr atjauninātus, pēc nepieciešamības ātri pārskatot produktu rekvizītus un atkārtoti publicējot informāciju, lai pārdošanas aģenti redzētu jaunākās izmaiņas saistībā ar krājumiem.

1.  Pārliecinieties, ka jums ir viena no šīm drošības lomām vai ekvivalentām atļaujām: sistēmas administratora, sistēmas pielāgotāja, pārdošanas vadītāja, pārdošanas viceprezidenta, mārketinga viceprezidenta vai izpilddirektora.
2.  Vietnes kartē atlasiet **Produkti**.
3.  Atveriet aktīvu produktu, kuru vēlaties mainīt, un komandjoslā atlasiet **Pārskatīt**.
4.  Dialoglodziņā **Pārskatīšanas apstiprināšana** atlasiet **Apstiprināt**. Produkta statuss tādējādi tiks mainīts uz **Tiek pārskatīts**.
5.  Kad esat beidzis veikt izmaiņas, komandjoslā atlasiet **Publicēt**.

    > [!TIP]
    > Lai atceltu izmaiņas un turpinātu izmantot pēdējo aktīvo produkta versiju, atlasiet **Atjaunot iepriekšējo versiju**. Produkta statuss tādējādi tiek mainīts atpakaļ uz iestatījumu **Aktīvs**.

## <a name="clone-a-product"></a>Produkta klonēšana 

Veidojot jaunu produktu, ietaupiet laiku, klonējot esošo. Tādējādi tiek izveidota sākotnējā ieraksta kopija ar visiem datiem, izņemot nosaukumu un ID.

1.  Pārliecinieties, ka jums ir viena no šīm drošības lomām vai ekvivalentām atļaujām: sistēmas administratora, sistēmas pielāgotāja, pārdošanas vadītāja, pārdošanas viceprezidenta, mārketinga viceprezidenta vai izpilddirektora.
2.  Vietnes kartē atlasiet **Produkti**.
3.  Atlasiet produkta ierakstu, ko vēlaties klonēt, un komandjoslā atlasiet **Klonēt**. Tiek atvērts apstiprinājuma dialoglodziņš.
4.  Atlasiet **Apstiprināt**.

Tiek atvērts jauns produkta ieraksts ar tiem pašiem datiem, kas ir sākotnējā ierakstā, izņemot nosaukumu un ID.

## <a name="retire-a-product"></a>Produkta slēgšana 

Ja jūsu organizācija vairs nepārdod kādu produktu, slēdziet to, lai šis produkts vairs nebūtu pieejams pārdošanas aģentiem.

1.  Pārliecinieties, ka jums ir sistēmas administratora vai Sales Professional vadītāja loma vai līdzvērtīgas atļaujas.
2.  Vietnes kartē atlasiet **Produkti**.
3.  Atveriet aktīvu produktu, kuru vēlaties slēgt, un komandjoslā atlasiet **Slēgt**.
4.  Dialoglodziņā **Norakstīšanas apstiprināšana** atlasiet **Apstiprināt**.


## <a name="delete-a-product"></a>Dzēst produktu

Lai pārtrauktu produkta pārdošanu, dzēsiet to.

> [!IMPORTANT]
> Dzēstu ierakstu nevar atgūt.

1.  Pārliecinieties, ka jums ir sistēmas administratora vai Sales Professional vadītāja loma vai līdzvērtīgas atļaujas.
2.  Vietnes kartē atlasiet **Produkti**.
3.  Atlasiet produkta ierakstu, ko vēlaties dzēst, un komandjoslā atlasiet **Dzēst**.
4.  Dialoglodziņā **Apstiprināt dzēšanu** atlasiet **Turpināt**.
 
 ## <a name="quantity-factors-for-products"></a>Daudzuma koeficienti produktiem

Lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, tiek izmantoti daudzuma faktori. Uz abonēšanu balstītiem produktiem daudzums piedāvājumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.

Parasti abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī. Taču varat izmantot arī citus laika aprakstus. Pārdošanas procesa laikā cena piedāvājuma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents. Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits. Daudzums, kas tiek izmantots piedāvājuma rindas summas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.

Daudzuma faktori izmanto produktu atribūtus. Kad kādam produktam konfigurējat konkrētus rekvizītus, jūs varat atzīmēt šo rekvizītu apakškopu vai visus rekvizītus kā daudzuma faktorus.

Sistēma pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips. Ja produkts, kuram ir konfigurēti daudzuma koeficienti, tiek pievienots piedāvājuma rindai, lauks **Daudzums** šajā piedāvājuma rindā kļūst par tikai lasāmu lauku. Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, tiek aprēķināts piedāvājuma rindas daudzums.

Piemēram, ja ir šādi rekvizīti: 

- **Lietotāju skaits**: Lietotāju skaits 
- **Mēnešu skaits**: Abonēšanas mēnešu skaits
- **Produkta SKU** 

Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** var atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]