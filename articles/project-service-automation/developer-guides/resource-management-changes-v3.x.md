---
title: Resursu pārvaldības izmaiņas (Project Service Automation 3.x)
description: Šajā tēmā ir sniegta informācija par izmaiņām resursu pārvaldības apgabalā.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753503"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Resursu pārvaldības izmaiņas (Project Service Automation 3.x)

Šīs tēmas sadaļās ir sniegta informācija par izmaiņām, kas veiktas attiecībā uz resursu pārvaldības apgabalu programmas Dynamics 365 Project Service Automation versijā 3.x.

## <a name="project-estimates"></a>Projekta tāmes

Projektu tāmes ir balstītas nevis uz entītiju **msdyn\_projecttask** (**Projekta uzdevums**), bet uz entītiju **msdynuz\_resourceassignment** (**Resursu piešķiršana**). Resursu piešķires ir kļuvušas par “patiesās informācijas avotu” uzdevumu plānošanai un cenu noteikšanai.

## <a name="line-tasks"></a>Rindu uzdevumi

Programmā PSA 3.x rindas uzdevumi ir novecojuši. Uzdevumi tagad norāda uz visu uzdevumu, nevis uz rindu uzdevumiem.

Tālāk minētajā piemērā norādīts, kā uzdevums ar nosaukumu “Testa uzdevums”, ir piešķirts darba grupas dalībniekiem A un B iepriekšējās PSA versijās un PSA versijā 3.x.

- **Pirms PSA 3.x:**

    - Testa uzdevums

        - Testa uzdevuma — 1. rindas uzdevums

            - Piešķiršana dalībniekam A

        - Testa uzdevuma — 2. rindas uzdevums

            - Piešķiršana dalībniekam B

- **PSA 3.x:**

    - Testa uzdevums

        - Piešķiršana dalībniekam A
        - Piešķiršana dalībniekam B

## <a name="unassigned-assignment"></a>Nepiešķirta piešķire

Programmā PSA 3.x, nepiešķirta piešķire ir tāda piešķire, kas piešķirta darba grupas dalībniekam **NULL** un resursam **NULL**. Nepiešķirtas piešķires var rasties vairākos scenārijos:

- Ja uzdevums ir izveidots, bet tas vēl nav piešķirts nevienam darba grupas dalībniekam, vienmēr tiek izveidota nepiešķirta piešķire. 
- Ja tiek noņemti visi uzdevuma saņēmēji, attiecīgajam uzdevumam tiek atkārtoti izveidota nepiešķirta piešķire.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Entītijas Projekta uzdevums plānošanas lauki

Entītijas **msdyn\_projecttask** lauki ir novecojuši vai pārvietoti uz entītiju **msdyn\_resourceassignment**, vai arī uz tiem tagad ir atsauce no entītijas **msdyn\_projectteam** (**Projekta darba grupas dalībnieks**).

| Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums) | Jauns lauks entītijā msdyn\_resourceassignment (Resursa piešķiršana) | Komentārs |
|---|---|---|
| msdyn\_assignedresources | Nav | |
| msdyn\_assignedteammembers | Nav | |
| msdyn\_numberofresources | Nav | |
| msdyn\_scheduledhours | Nav | |
| msdyn\_effortcontour | msdyn\_plannedwork | Ir mainīts JavaScript Object Notation (JSON) datu struktūras formāts, kas tiek glabāts laukā. |

## <a name="schedule-contour"></a>Plānošanas kontūra

Plānošanas kontūra tiek glabāta laukā **Plānotais darbs** (**msdyn\_plannedwork**) katrai entītijai **Resursa piešķiršana** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktūra

Plānošanas kontūras jaunā struktūra sastāv no elastīgiem laika sektoriem, kas ir definēti katrai grafika dienai. Katram laika sektoram ir šādi rekvizīti:

- **Sākums** — dienas darba stundu sākums atbilstoši projekta kalendāram.
- **Beigas** — dienas darba stundu beigas atbilstoši projekta kalendāram.
- **Stundas** — dienā piešķirto stundu skaits.

**Piemērs**

Šajā piemērā tiek izmantots projekta kalendārs, kurā darba diena ir no 9:00 līdz 17:00 UTC-8 laika joslā.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automātiska plānošana un manuāla plānošana

Ja uzdevums tiek plānots automātiski, stundas tiek koncentrētas perioda sākumā un uzdevuma ilgums var tikt samazināts.

**Piemērs**

Šis uzdevums ir plānots automātiski, paredzot 18 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Ja uzdevums tiek plānots manuāli, stundas tiek vienmērīgi sadalītas visos datumos.

**Piemērs**

Šis uzdevums ir plānots manuāli, paredzot 18 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Piešķires vienība

Piešķires vienība ir novecojusi programmā PSA 3.x. Tagad uzdevuma ieguldījuma stundas ir vienlīdzīgi sadalītas pa dienām visiem piešķirtajiem resursiem.

**Piemērs**

Šajā piemērā uzdevums tiek piešķirts diviem resursiem un tas tiek plānots automātiski, paredzot 36 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).

- 1. piešķire:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 2. piešķire:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Cenu noteikšanas dimensijas

Programmā PSA 3.x dimensijas lauki, kas saistīti ar cenas noteikšanu resursam (piemēram, **Loma** un **Organizācijas vienība**), ir noņemti no entītijas **msdyn\_projecttask**. Šos laukus tagad var izgūt no resursu piešķiršanas (**msdyn\_resourceassignment**) atbilstošā projekta darba grupas dalībnieka (**msdyn\_projectteam**), kad tiek ģenerētas projektu tāmes. Entītijai **msdyn\_projectteam** ir pievienots jauns lauks **msdyn\_organizationalunit**.

| Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums) | Lauks no msdyn\_projectteam (Projekta darba grupas dalībnieks), kas tiek izmantots tā vietā |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontūras

Entītijā **msdyn\_projecttask** ir novecojuši cenu noteikšanas un novērtējuma kontūru lauki. Tie ir pārvietoti uz entītiju **msdyn\_resourceassignment**.

| Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums) | Jauns lauks entītijā msdyn\_resourceassignment (Resursa piešķiršana) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Šie lauki ir pievienoti entītijai **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Entītijai **msdyn\_projecttask** nav mainīti šādi lauki attiecībā uz plānotajām, faktiskajām un atlikušajām izmaksām un pārdošanas darījumiem:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
