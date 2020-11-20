---
title: Cenu noteikšanas dimensiju pārskats
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensijām programmā Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128472"
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

Dynamics 365 Project Operations tiek piegādāta ar cenrāžu dimensiju noklusējuma kopu. Šīs cenrāžu dimensijas varat skatīt, dodoties uz **Project Operations** > **Parametri**. Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**. Ja šie lauki ir iespējoti, jūs varat iestatīt maksu un izmaksas katrai lomas un organizācijas vienības kombinācijai.

Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas.

## <a name="pricing-human-resource-time"></a>Cilvēkresursu laika cenu noteikšana
Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu. Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.

Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai. Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri. 

Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai. Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, jūs varētu izveidot entītiju, nevis opciju kopu. Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums lietotāju.

Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder. Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder. Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.

**Piemēra norēķinu likmes**

| Loma        | Org. struktūrvienība    |Vienība      |Cena      |Valūta  |
| ------------|-------------|----------|----------:|----------|
| Izstrādātājiem   | Contoso ASV  |Hour | 200|USD     |
| Izstrādātājiem   | Contoso India |Hour|   112|USD     |


**Piemēra izmaksu likmes**

| Algu grupa     | Org. struktūrvienība    |Vienība      |Cena      |Valūta  |
| ----------------|-------------|----------|----------:|----------|
| Mana company_Band1 | Contoso ASV  |Hour | 145|USD     |
| Mana company_Band2 | Contoso India |Hour|   67|USD     |
