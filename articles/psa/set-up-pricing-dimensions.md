---
title: Pielāgotu lauku kā cenu noteikšanas dimensiju iestatīšana
description: Šajā tēmā ir sniegta informācija par pielāgotu cenu noteikšanas dimensiju iestatīšanu.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
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
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150362"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Pielāgotu lauku kā cenu noteikšanas dimensiju iestatīšana 

[!include [banner](../includes/psa-now-project-operations.md)]

Pirms darba sākšanas šajā tēmā tiek pieņemts, ka esat pabeidzis tēmās norādītās procedūras, [Izveidot pielāgotus laukus un entītijas](create-custom-fields-entities.md) un [Pievienot pielāgotus laukus cenas iestatīšanai un transakciju entītijām](field-references.md). Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas. 

Šajā tēmā ir sniegta informācija par pielāgotu cenu noteikšanas dimensiju iestatīšanu. Project service tīmekļa interfeisā, lapā **Parametri**, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** ir parādīti ieraksti cenu noteikšanas dimensiju entītijās. Pēc noklusējuma programmas Project Service instalēšanas laikā šīs cilnes režģī tiek izveidotas 2 rindas:

- **msdyn_resourcecategory** (Loma);
- **msdyn_OrganizationalUnit** (Organizācijas struktūrvienība).

> [!IMPORTANT]
> Nedzēsiet šīs rindas. Ja tās nav nepieciešamas, varat tās padarīt par neattiecināmām noteiktā kontekstā, pielietojot **Nē** attiecībā uz visiem šiem iestatījumiem: **Attiecināms uz izmaksām**, **Attiecināms uz pārdošanu** un **Attiecināms uz pirkšanu**. Šo atribūtu vērtību iestatīšana uz **Nē** rada tādu pašu efektu, it kā nebūtu tāda lauka kā cenas noteikšanas dimensija.

Lai lauks kļūtu par cenas noteikšanas dimensiju, tam ir jābūt:

- izveidotam kā lauks entītijās **Lomas cena** un **Lomu cenas uzcenojums**. Lai iegūtu plašāku informācijai par to, kā tas darāms, skatiet [Pielāgotu lauku pievienošana cenas iestatījumam un transakciju entītijām](field-references.md).
- izveidotam kā rindai tabulā **Cenu noteikšanas dimensija**. Piemēram, pievienojiet cenu noteikšanas dimensiju rindas, kā parādīts šajā grafikā. 

![Uz summu balstītas cenu noteikšanas dimensiju rindas](media/Amt-based-PD.png)

Ņemiet vērā, ka Resursu darba stundas (**msdyn_resourceworkhours**) ir pievienotas kā uz uzcenojuma balstīta dimensija un ir pievienotas režģim cilnē **Uz uzcenojuma balstīta cenas noteikšanas dimensija**.

![Uz uzcenojuma balstītas cenu noteikšanas dimensiju rindas](media/Markup-based-PD.png)

> [!IMPORTANT]
> Jebkādas izmaiņas cenu noteikšanas dimensiju datos šajā tabulā, esošas vai jaunas, tiek izplatītas Project Service cenu noteikšanas biznesa loģikā tikai pēc kešatmiņas atsvaidzināšanas. Kešatmiņas atsvaidzināšanas laiks var aizņemt līdz 10 minūtēm. Atvēliet šo laiku, lai skatītu izmaiņas cenas noklusējuma loģikā, kas izriet no izmaiņām Cenu noteikšanas dimensiju datos.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Cenu noteikšanas dimensiju tabulas atribūti
Šajās sadaļās ir sniegta informācija par dažādiem atribūtiem tabulā **Cenu noteikšanas dimensijas**.

### <a name="pricing-dimension-name"></a>Cenas noteikšanas dimensijas nosaukums
Šai vērtībai ir jāsakrīt ar tā lauka shēmas nosaukumu, kas ir pievienots tabulai **Lomas cena** pielāgotām cenu dimensijām. Lai iegūtu plašāku informāciju par lauku pievienošanu tabulai **Lomas cena**, skatiet [Pielāgotu lauku pievienošana cenas iestatījumam un transakciju entītijām](field-references.md).

### <a name="type-of-dimension"></a>Dimensijas tips
Pastāv divi cenu noteikšanas dimensiju tipi:
  
  - **Uz summu balstītas dimensijas**: dimensiju vērtības no ievades konteksta atbilst dimensiju vērtībām, kas norādītas rindā **Lomas cena**, un cena/izmaksas pēc noklusējuma tiek izmantotas tieši no tabulas **Lomas cena**;
  - **Uz uzcenojumu balstītas dimensijas**: tās ir dimensijas, kurās Project Service pieņems šādu 3 posmu procesu cenas/izmaksu iegūšanai.
 
    1. Pamatlikmes iegūšanai programma Project Service saskaņo uz uzcenojumu nebalstītās dimensiju vērtības no ievades konteksta ar Lomas cenas rindu.
    2. Uzcenojuma procentu likmes iegūšanai programma Project Service saskaņo visas dimensiju vērtības no ievades konteksta ar rindu **Lomas cenas uzcenojums**.
    3. Gala cenas/izmaksu iegūšanai programma Project Service pielieto uzcenojuma procentus no otrās darbības pamatlikmei, kas iegūta no tabulas **Lomas cena** pirmajā darbībā.
   
   Tālāk sniegtajā tabulā ir parādīts cenu uzcenojumu aprēķins.
  
| Loma        | Org. struktūrvienība    |Darba atrašanās vieta      |Standarta nosaukums      |Resursu darba stundas      |  Atzīmēt|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | “Contoso India”|Uz vietas            |                    |Virsstundas                 |15     |
|             | “Contoso India”|Lokāls             |                    |Virsstundas                 |10     |
|             | Contoso ASV   |Lokāls             |                    |Virsstundas                 |20     |


Ja resurss no “Contoso India”, kura pamatlikme ir 100 USD, strādā uz vietas un laika ierakstā norāda 8 stundas Parasta darbadienas laika un 2 virsstundas, Project Service cenu noteikšanas programma izmantos pamatlikmi 100 uz 8 stundām, lai ierakstītu 800 USD. 2 virsstundām tiks lietots 15% uzcenojums pamatlikmei 100, iegūstot vienības cenu 115 USD apmērā un ierakstot kopējās izmaksas 230 USD apmērā.

### <a name="applicable-to-cost"></a>Piemērojams izmaksām 
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** izmaksu un uzcenojuma likmju izgūšanas laikā.

### <a name="applicable-to-sales"></a>Attiecināms uz pārdošanu
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** norēķinu un uzcenojuma likmju izgūšanas laikā.

### <a name="applicable-to-purchase"></a>Attiecināms uz iegādi
Ja iestatīts uz **Jā**, tas norāda, ka dimensijas vērtība no ievades konteksta ir jāizmanto, lai panāktu atbilstību **Lomas cenai** un **Lomas cenas uzcenojumam** pirkšanas cenas izgūšanas laikā. Pašlaik progrsmma Project Service neatbalsta apakšlīgumu scenārijus, tāpēc šis lauks netiek izmantots. 

### <a name="priority"></a>Prioritāte
Dimensijas prioritātes iestatīšana palīdz programmai Project Service noteikt cenu pat tad, ja netiek atrasta precīza atbilstība starp ievades dimensiju vērtībām un vērtībām no **Lomas cenas** vai **Lomas cenas uzcenojuma** tabulām. Šādā gadījumā programma Project Service neatbilstošām dimensijas vērtībām izmantos Null vērtības, novērtējot dimensijas pēc to prioritātes.

- **Izmaksu prioritāte**: dimensijas izmaksu prioritātes vērtība norāda šīs dimensijas nozīmīgumu, salīdzinot ar izmaksu cenu iestatīšanu. **Izmaksu prioritātes** vērtībai ir jābūt unikālai visās dimensijās, kas **Attiecināmas uz izmaksām**.
- **Pārdošanas prioritāte**: dimensijas pārdošanas prioritātes vērtība norāda šīs dimensijas nozīmīgumu, salīdzinot ar pārdošanas cenu vai norēķinu cenu iestatīšanu. **Pārdošanas prioritātes** vērtībai ir jābūt unikālai visās dimensijās, kuras **Attiecināmas uz pārdošanu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]