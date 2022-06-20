---
title: Project Operations iestatīšanas un konfigurēšanas datu integrācija
description: Šajā rakstā sniegta informācija par projektu operāciju duālās rakstīšanas karšu iestatīšanu un konfigurēšanu.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914549"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations iestatīšanas un konfigurēšanas datu integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā sniegta informācija par projektu operāciju divējādās rakstīšanas integrāciju uzstādīšanas un konfigurācijas entītijām.

## <a name="project-contracts-contract-lines-and-projects"></a>Projekta līgumi, līguma rindas un projekti

Projekta līgumi, līgumu rindas un projekti tiek izveidoti Dataverse finanšu un operāciju programmās un sinhronizēti ar tām papildu grāmatvedībai. Šo entītiju ierakstus var izveidot un dzēst tikai programmā Dataverse. Tomēr grāmatvedības atribūtus, piemēram, PVN grupas noklusējumus un finanšu dimensijas, var pievienot šiem ierakstiem programmās Finanses un operācijas.

  ![Projekta līguma integrācijas koncepcijas.](./media/1ProjectContract.jpg)

Pārdošanas darbību interesenti, iespējas un piedāvājumi tiek izsekoti Dataverse un netiek sinhronizēti ar finanšu un operāciju programmām, jo ar šo darbību nav saistīta pakārtota grāmatvedība.

Projekta līguma funkcionalitāte programmā Dataverse izveido projekta līguma ierakstu finanšu un operāciju programmās, **izmantojot tabulas karti Projekta līguma virsraksti (pārdevēji).** Saglabājot projekta līgumu risinājumā Dataverse, tiek sākta arī projekta līguma klienta entītijas ieraksta izveide. Šis ieraksts tiek sinhronizēts ar finance and operations programmām, **izmantojot tabulas karti Project Funding Source (msdyn\_ projectcontractssplitbillingrules).** Ar šo kartējumu tiek sinhronizēti arī projektu līgumu klientu papildinājumus, atjauninājumi un dzēšana. Sadalīt norēķinu procentus starp projekta līgumu debitoriem tiek apgūti tikai Dataverse finanšu un operāciju programmās, nevis sinhronizēti ar tām.

Pēc projekta līguma izveides Dataverse projekta grāmatvedis var atjaunināt šī projekta līguma uzskaites atribūtus programmās Finanses un operācijas, dodoties uz **Projektu vadība un grāmatvedība** > **Projekta līgumi** > **Iestatīt** > **Rādīt noklusējuma grāmatvedību**. Grāmatvedis var pārskatīt darbības projekta līguma atribūtus, piemēram, pieprasīto piegādes datumu un līguma summu, atlasot projekta līguma ID finanšu un operāciju programmās, kas atver saistīto projekta līguma ierakstu programmā Dataverse.

Projekta entītija tiek sinhronizēta ar Finance and Operations programmām, **izmantojot tabulas Projektu V2 (msdyn\_ projects)** karti. Projekta grāmatvedis var:

  - Pārskatiet projektus finanšu un operāciju lietotnēs, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti**. 
  - Atjauniniet projekta uzskaites atribūtus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un grāmatvedība** > **Visi projekti** > **Iestatiet** > **Rādīt noklusējuma grāmatvedību**.  
  - Pārskatiet darbības projekta atribūtus, piemēram, paredzamos sākuma un beigu datumus, atlasot projekta ID finanšu un operāciju programmās, kas atver saistīto projekta ierakstu programmā Dataverse.

Projekts tiek saistīts ar projekta līgumu, izmantojot entītiju **Projekta līguma rinda**.

Projekta līguma rindas programmā Dataverse izveido projekta līguma norēķinu kārtulu finanšu un operāciju programmās, **izmantojot tabulas karti Project contract lines (salesorderdetails).** Norēķinu metode definē projekta līguma norēķinu kārtulas tipu finanšu un operāciju programmās:

  - projekta līguma rindas ar laika un materiālu norēķinu metodi izveido laika un materiālu tipa norēķinu kārtulu;
  - fiksētas cenas norēķinu metodes līguma rindās izveido atskaites punkta norēķinu kārtulu.

Projekta līguma rindas projekta grāmatvedis var pārskatīt programmās Finanses un operācijas, dodoties uz **Projektu vadības un uzskaites** > **projektu līgumi** > **Iestatīt Rādīt** > **noklusējuma grāmatvedību** un pārskatot detalizētu informāciju cilnē **Līguma rindas** . Grāmatvedis šajā cilnē var iestatīt arī noklusējuma finanšu dimensijas fiksētas cenas norēķinu metodes līguma rindām.

## <a name="billing-milestones"></a>Norēķinu atskaites punkti

Par projekta līguma rindām, kurās tiek izmantota fiksētas cenas norēķinu metode, rēķins tiek izrakstīts, izmantojot norēķinu atskaites punktus. Norēķinu atskaites punkti tiek sinhronizēti ar projekta starpkontu darbībām finanšu un operāciju programmās, izmantojot **tabulas karti Project Operations integration contract line milestones (msdyn\_ contractlinescheduleofvalues).**

  ![Norēķinu atskaites punktu integrācija.](./media/2Milestones.jpg)

Grāmatvedis var pārskatīt starpkontu transakcijas un pielāgot šo transakciju grāmatvedības atribūtus, dodoties uz **Projekta pārvaldība un uzskaite** > **Projekta līgumi** > **Uzturēšana** > **Starpkontu transakcijas** vai **Projekta pārvaldība un uzskaite** > **Visi projekti** > **Uzturēšana** > **Starpkontu transakcijas**.

Pirmoreiz izveidojot norēķinu atskaites punktu noteiktai projekta līguma rindai, sistēma automātiski izveido fiksētas cenas ieņēmumu aprēķinu projektu tam projektam, kas ir saistīts ar šo līguma rindu. Fiksētas cenas prognozējamo ieņēmumu projektus var pārskatīt, dodoties uz **Projekta pārvaldība un uzskaite** > **Fiksētas cenas prognozējamo ieņēmumu projekti**.

### <a name="project-tasks"></a>Projekta uzdevumi

Projekta uzdevumi tiek sinhronizēti ar finanšu un operāciju programmām, **izmantojot tabulas Project tasks (msdyn\_ projecttasks)** karti tikai atsauces nolūkiem. Darbību izveide, atjaunināšana un dzēšana netiek atbalstīta, izmantojot finanšu un operāciju programmas.

  ![Projekta uzdevumu integrācija.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekta resursi

Entītija **Project resource roles** tiek sinhronizēta ar Finance and Operations programmām, izmantojot **projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories)** tabulas karti tikai atsauces nolūkiem. Tā kā resursu lomas programmā Dataverse nav specifiskas uzņēmumam, sistēma automātiski automātiski izveido atbilstošus uzņēmumam raksturīgus resursu lomu ierakstus finanšu un operāciju programmās visām juridiskajām personām, kas iekļautas duālās rakstīšanas integrācijas tvērumā.

![Resursu lomu integrācija.](./media/5Resources.jpg)

Projekta resursi projekta operācijās tiek uzturēti Dataverse un netiek sinhronizēti ar finanšu un operāciju programmām.

### <a name="transaction-categories"></a>Transakcijas kategorijas

Darbību kategorijas tiek uzturētas Dataverse finanšu un operāciju programmās un sinhronizētas ar tām, **izmantojot tabulas projektu darbību kategoriju (msdyn\_ transactioncategories)** karti. Pēc transakcijas kategorijas ieraksta sinhronizēšanas sistēma automātiski izveido četrus kopīgotus kategoriju ierakstus. Katrs ieraksts atbilst darbības tipam finanšu un operāciju programmās un saista tos ar darbību kategorijas ierakstu.

![Transakcijas kategoriju integrācija.](./media/4TransactionCategories.jpg)

Lai prognozēm un faktiskajiem datiem varētu izmantot transakcijas kategorijas, projekta grāmatvedim vai sistēmas administratoram ir jāizveido atbilstošas projekta kategorijas katrā juridiskajā entītijā. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](../project-accounting/configure-project-categories.md).
