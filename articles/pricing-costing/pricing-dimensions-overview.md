---
title: Cenu noteikšanas dimensiju pārskats
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensijām risinājumā Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001980"
---
# <a name="pricing-dimensions-overview"></a>Cenu noteikšanas dimensiju pārskats

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dimensijas, kas tiek izmantotas cilvēkresursos, lai iestatītu cenu un izmaksu noteikšanu, ir iedalāmas divās tālāk norādītajās kategorijās.

- Personas
- Plānotais darbs

Šī iemesla dēļ ir pieejamas divu tālāk norādīto tipu cenu noteikšanas dimensiju vērtības:

- **Opciju kopas**: Dimensijas, kas ir fiksēti uzskaitījumi kādai vērtību kopai.
- **Uz entītiju balstītas vērtības**: Dimensijas, kas var būt dažādu vērtību kopa.

## <a name="pricing-dimensions"></a>Cenu noteikšanas dimensijas

Dynamics 365 Project Operations tiek piegādāta ar cenu noteikšanas dimensiju noklusējuma kopu. Šīs cenrāžu dimensijas varat skatīt, dodoties uz **Project Operations** > **Parametri**. Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**. Ja šie lauki ir iespējoti, jūs varat iestatīt maksu un izmaksas katrai lomas un organizācijas vienības kombinācijai.

![Project Service parametru ekrānuzņēmums ar izceltu lauku “Attiecināms uz pārdošanu”.](media/PS-OOB-parameters.png)

Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas. Papildinformāciju skatiet nākamajās tēmās. 
  
  > [!NOTE]
  > Procedūras ir jāaizpilda tādā secībā, kādā tās ir norādītas.

1. [Risinājuma izveide pielāgotām cenu noteikšanas dimensijām](../sales/create-solution-custompd.md)
2. [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities-pricing-dimensions.md)
3. [Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām ](add-custom-fields-price-setup-transactional-entities.md)
4. [Pielāgotu lauku kā cenu kategoriju iestatīšana ](set-up-custom-fields-pricing-dimensions.md)
5. [Spraudņa atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Cilvēkresursu laika cenu noteikšana
Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu. Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.

Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai. Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri. 

Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai. Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, jūs varētu izveidot entītiju, nevis opciju kopu. Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums lietotāju.

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