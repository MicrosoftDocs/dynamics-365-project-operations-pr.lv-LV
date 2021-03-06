---
title: Pielāgotu lauku kā cenu kategoriju iestatīšana
description: Šajā tēmā sniegta informācija par to, kā iestatīt cenu noteikšanas dimensijas, izmantojot pielāgotus laukus.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896605"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Pielāgotu lauku kā cenu kategoriju iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Pirms darba sākšanas šajā tēmā tiek pieņemts, ka esat pabeidzis tēmās norādītās procedūras, [Izveidot pielāgotus laukus un entītijas](create-custom-fields-entities-pricing-dimensions.md) un [Pievienot nepieciešamos pielāgotos laukus cenas iestatīšanai un transakciju entītijām](add-custom-fields-price-setup-transactional-entities.md). Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas. 

Šajā tēmā ir sniegta informācija par pielāgotu cenu noteikšanas dimensiju iestatīšanu. Lapas **Parametri** cilnē **Summā balstītas cenu noteikšanas dimensijas** tiek rādīti ieraksti cenu noteikšanas dimensiju entitījās. Šajā cilnē pēc noklusējuma režģī ir divas rindas:

- **msdyn_resourcecategory** (Loma);
- **msdyn_OrganizationalUnit** (Organizācijas struktūrvienība).

> [!IMPORTANT]
> Nedzēsiet šīs rindas. Ja tās nav nepieciešamas, varat tās padarīt par neattiecināmām noteiktā kontekstā, pielietojot **Nē** attiecībā uz visiem šiem iestatījumiem: **Attiecināms uz izmaksām**, **Attiecināms uz pārdošanu** un **Attiecināms uz pirkšanu**. Šo atribūtu vērtību iestatīšana uz **Nē** rada tādu pašu efektu, it kā nebūtu tāda lauka kā cenas noteikšanas dimensija.

Lai lauks kļūtu par cenas noteikšanas dimensiju, tam ir jābūt:

- izveidotam kā lauks entītijās **Lomas cena** un **Lomu cenas uzcenojums**. Lai iegūtu plašāku informācijai par to, kā tas darāms, skatiet [Pielāgotu lauku pievienošana cenas iestatījumam un transakciju entītijām](add-custom-fields-price-setup-transactional-entities.md).
- izveidotam kā rindai tabulā **Cenu noteikšanas dimensija**. Piemēram, pievienojiet cenu noteikšanas dimensiju rindas, kā parādīts šajā grafikā. 

Resursu darba stundas (**msdyn_resourceworkhours**) ir pievienotas kā uz uzcenojuma balstīta dimensija un ir pievienotas režģim cilnē **Uz uzcenojuma balstīta cenas noteikšanas dimensija**.

> [!IMPORTANT]
> Jebkādas izmaiņas cenu noteikšanas dimensiju datos šajā tabulā, esošas vai jaunas, tiek izplatītas cenu noteikšanas biznesa loģikā tikai pēc kešatmiņas atsvaidzināšanas. Kešatmiņas atsvaidzināšanas laiks var aizņemt līdz 10 minūtēm. Atvēliet šo laiku, lai skatītu izmaiņas cenas noklusējuma loģikā, kas izriet no izmaiņām Cenu noteikšanas dimensiju datos.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Cenu noteikšanas dimensiju tabulas atribūti
Šajās sadaļās ir sniegta informācija par dažādiem atribūtiem tabulā **Cenu noteikšanas dimensijas**.

### <a name="pricing-dimension-name"></a>Cenas noteikšanas dimensijas nosaukums
Šai vērtībai ir jāsakrīt ar tā lauka shēmas nosaukumu, kas ir pievienots tabulai **Lomas cena** pielāgotām cenu dimensijām. Lai iegūtu plašāku informāciju par lauku pievienošanu tabulai **Lomas cena**, skatiet [Pielāgotu lauku pievienošana cenas iestatījumam un transakciju entītijām](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimensijas tips
Pastāv divi cenu noteikšanas dimensiju tipi:
  
  - **Uz summu balstītas dimensijas**: dimensiju vērtības no ievades konteksta atbilst dimensiju vērtībām, kas norādītas rindā **Lomas cena**, un cena/izmaksas pēc noklusējuma tiek izmantotas tieši no tabulas **Lomas cena**;
  - **Uz uzcenojumu balstītas dimensijas**: tās ir dimensijas, kurās izmanto šādu triju posmu procesu cenas/izmaksu iegūšanai.
 
    1. Pamatlikmes iegūšanai uz uzcenojumu nebalstītās dimensiju vērtības no ievades konteksta tiek saskaņotas ar Lomas cenas rindu.
    2. Uzcenojuma procentu likmes iegūšanai visas dimensiju vērtības no ievades konteksta tiek saskaņotas ar rindu **Lomas cenas uzcenojums**.
    3. Gala cenas/izmaksu iegūšanai tiek pielietoti uzcenojuma procenti no otrās darbības pamatlikmei, kas iegūta no tabulas **Lomas cena** pirmajā darbībā.
   
   Tālāk sniegtajā tabulā ir parādīts cenu uzcenojumu aprēķins.
  
| Loma        | Org. struktūrvienība    |Darba atrašanās vieta      |Standarta nosaukums      |Resursu darba stundas      |  Atzīmēt|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | “Contoso India”|Uz vietas            |                    |Virsstundas                 |15     |
|             | “Contoso India”|Lokāls             |                    |Virsstundas                 |10     |
|             | Contoso ASV   |Lokāls             |                    |Virsstundas                 |20     |


Ja resurss no “Contoso India”, kura pamatlikme ir 100 USD, strādā uz vietas un laika ierakstā norāda 8 stundas Parasta darbadienas laika un 2 virsstundas, cenu noteikšanas programma izmantos pamatlikmi 100 uz 8 stundām, lai ierakstītu 800 USD. 2 virsstundām tiks lietots 15% uzcenojums pamatlikmei 100, iegūstot vienības cenu 115 USD apmērā un ierakstot kopējās izmaksas 230 USD apmērā.

### <a name="applicable-to-cost"></a>Piemērojams izmaksām 
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** izmaksu un uzcenojuma likmju izgūšanas laikā.

### <a name="applicable-to-sales"></a>Attiecināms uz pārdošanu
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** norēķinu un uzcenojuma likmju izgūšanas laikā.

### <a name="applicable-to-purchase"></a>Attiecināms uz iegādi
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** pirkšanas cenas izgūšanas laikā. Apakšlīgumu scenāriji netiek atbalstīti, tāpēc šis lauks netiek lietots. 

### <a name="priority"></a>Prioritāte
Dimensijas prioritātes iestatīšana palīdz noteikt cenu pat tad, ja netiek atrasta precīza atbilstība starp ievades dimensiju vērtībām un vērtībām no **Lomas cenas** vai **Lomas cenas uzcenojuma** tabulām. Šādā gadījumā neatbilstošām dimensijas vērtībām tiks izmantotas Null vērtības, novērtējot dimensijas pēc to prioritātes.

- **Izmaksu prioritāte**: dimensijas izmaksu prioritātes vērtība norāda šīs dimensijas nozīmīgumu, salīdzinot ar izmaksu cenu iestatīšanu. **Izmaksu prioritātes** vērtībai ir jābūt unikālai visās dimensijās, kas **Attiecināmas uz izmaksām**.
- **Pārdošanas prioritāte**: dimensijas pārdošanas prioritātes vērtība norāda šīs dimensijas nozīmīgumu, salīdzinot ar pārdošanas cenu vai norēķinu cenu iestatīšanu. **Pārdošanas prioritātes** vērtībai ir jābūt unikālai visās dimensijās, kuras **Attiecināmas uz pārdošanu**.
