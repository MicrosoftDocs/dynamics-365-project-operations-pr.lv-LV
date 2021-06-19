---
title: Cenu un izmaksu noteikšanas dimensiju sākumlapa
description: Šajā tēmā ir sniegts pārskats par cenu noteikšanas dimensijām.
author: rumant
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
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009265"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Cenu un izmaksu noteikšanas dimensiju sākumlapa

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensijas, ko izmanto, lai iestatītu darbaspēka izcenojumu un izmaksu aprēķināšanu uz projektiem bāzētās organizācijās, ietekmē tālāk uzskaitītie atribūti.

- Personas dara darbu, kas ir līdzīgs to pieredzei, lomai vai ģeogrāfijai
- Darbs jāveic līdzīgi tā sarežģītībai vai diennakts laikam

Ņemot vērā šo darba atribūtu un darba veikšanai nepieciešamo darbinieku raksturīgās īpašības, platformā Project Service Automation ir pieejamas divu veidu izcenojuma dimensijas vērtības: 

- **Opciju kopas**: atribūti, kas ir fiksēti uzskaitījumi kādai vērtību kopai;
- **Entītiju bāzes vērtības**: atribūti, kam var būt dažādi vērtību kopumi, kas ir ierobežoti, bet ar laiku var mainīties.

## <a name="pricing-dimensions"></a>Cenu noteikšanas dimensijas

Programma PSA tiek piegādāta ar cenu noteikšanas dimensiju noklusējuma kopu. Šo sarakstu varat apskatīt, dodoties uz **Project Service** > **Parametri**. Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**. Tas ļaus jums iestatīt cenas un izmaksas katrai lomas un organizācijas struktūrvienības kombinācijai.

![Project Service parametru ekrānuzņēmums ar izceltu lauku “Attiecināms uz pārdošanu”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ja pirms PSA versijas 3 kā cenu noteikšanas dimensijas lietojāt lomas un organizācijas struktūrvienības standarta laukus, nekādas izmaiņas nebūs manāmas. Varat turpināt lietot programmu Project Service kā parasti. 

Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas. Lai iegūtu plašāku informāciju, skatiet tālāk norādītās tēmas, taču ņemiet vērā, ka šīs procedūras ir jāizpilda tālāk norādītajā secībā.

- [Pielāgotu lauku un entītiju izveidošana](create-custom-fields-entities.md)
- [Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām](field-references.md)
- [Pielāgotu lauku kā cenu kategoriju iestatīšana ](set-up-pricing-dimensions.md)
- [Spraudņa atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Cilvēkresursu laika cenu noteikšana
Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu. Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.

Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai. Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri. 

Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai. Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, izveidojiet entītiju, nevis opciju kopu. Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums biznesa lietotāju.

Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder. Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder. Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.

**Piemēra norēķinu likmes**

| Loma        | Org. struktūrvienība    |Vienība      |Cenrādis      |Valūta  |
| ------------|-------------|----------|----------:|----------|
| Izstrādātājiem   | Contoso US  |stunda | 200|USD     |
| Izstrādātājiem   | Contoso India |stunda|   112|USD     |


**Piemēra izmaksu likmes**

| Algu grupa     | Org. struktūrvienība    |Vienība      |Cenrādis      |Valūta  |
| ----------------|-------------|----------|----------:|----------|
| Mana company_Band1 | Contoso US  |stunda | 145|USD     |
| Mana company_Band2 | Contoso India |stunda|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]