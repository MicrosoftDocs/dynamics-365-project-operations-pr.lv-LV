---
title: Project Operations iestatīšanas un konfigurēšanas datu integrācija
description: Šajā rakstā ir sniegta informācija par project operations divrakstu karšu iestatīšanu un konfigurēšanu.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029161"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations iestatīšanas un konfigurēšanas datu integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir sniegta informācija par Project Operations divrakstīšanas integrāciju iestatīšanas un konfigurēšanas entītijām.

## <a name="project-contracts-contract-lines-and-projects"></a>Projekta līgumi, līguma rindas un projekti

Projektu līgumi, līgumu rindas un projekti tiek izveidoti Dataverse un sinhronizēti ar finanšu un operāciju programmām papildu uzskaitei. Šo entītiju ierakstus var izveidot un dzēst tikai programmā Dataverse. Tomēr grāmatvedības atribūtus, piemēram, PVN grupas noklusējumus un finanšu dimensijas, var pievienot šiem ierakstiem finanšu un operāciju programmās.

  ![Projekta līguma integrācijas koncepcijas.](./media/1ProjectContract.jpg)

Pārdošanas aktivitātes potenciālie pirkumi, iespējas un piedāvājumi tiek izsekoti Dataverse, un tie netiek sinhronizēti ar finance and operations lietotnēm, jo ar šo darbību nav saistīta pakārtota grāmatvedība.

Projekta līguma funkcionalitāte izveido Dataverse projekta līguma ierakstu finanšu un operāciju programmās, **izmantojot projekta līguma galveņu (pārdevēju)** tabulas karti. Saglabājot projekta līgumu risinājumā Dataverse, tiek sākta arī projekta līguma klienta entītijas ieraksta izveide. Šis ieraksts ir sinhronizēts ar finance and operations programmām, **izmantojot tabulas Projektu finansējuma avotu (msdyn\_ projectcontractssplitbillingrules).** Ar šo kartējumu tiek sinhronizēti arī projektu līgumu klientu papildinājumus, atjauninājumi un dzēšana. Sadalītās norēķinu procentuālās daļas starp projekta līguma klientiem tiek apstrādātas tikai un Dataverse netiek sinhronizētas ar finanšu un operāciju programmām.

Kad projekta līgums ir izveidots Dataverse, projekta grāmatvedis var atjaunināt šī projekta līguma uzskaites atribūtus finanšu un operāciju programmās, dodoties uz **Projektu vadības un uzskaites** > **projektu līgumi** > **Iestatiet** > **Rādīt noklusējuma uzskaiti**. Grāmatvedis var pārskatīt darbības projekta līguma atribūtus, piemēram, pieprasīto piegādes datumu un līguma summu, finanšu un operāciju lietotnēs atlasot projekta līguma ID, kas atver saistīto projekta līguma ierakstu.Dataverse

Projekta entītija tiek sinhronizēta ar finance and operations programmām, **izmantojot tabulas Projektu V2 (msdyn\_ projekti)** karti. Projekta grāmatvedis var:

  - Pārskatiet projektus finanšu un operāciju programmās, dodoties uz Sadaļu **Projektu vadība un uzskaite** > **Visi projekti**. 
  - Atjauniniet projekta uzskaites atribūtus finanšu un operāciju programmās, dodoties uz Sadaļu **Projektu vadība un uzskaite** > **Visi projekti** > **Iestatiet** > **Rādīt noklusējuma uzskaiti**.  
  - Pārskatiet darbības projekta atribūtus, piemēram, aplēstos sākuma un beigu datumus, atlasot projekta ID finanšu un operāciju programmās, kas atver saistīto projekta ierakstu sadaļā Dataverse.

Projekts tiek saistīts ar projekta līgumu, izmantojot entītiju **Projekta līguma rinda**.

Projekta līguma rindas izveido Dataverse projekta līguma norēķinu kārtulu finanšu un operāciju programmās, **izmantojot tabulas Karti Projekta līgumu rindas (salesorderdetails).** Norēķinu metode definē projekta līguma norēķinu kārtulas tipu finance and operations programmās:

  - projekta līguma rindas ar laika un materiālu norēķinu metodi izveido laika un materiālu tipa norēķinu kārtulu;
  - fiksētas cenas norēķinu metodes līguma rindās izveido atskaites punkta norēķinu kārtulu.

Projekta līguma rindas var pārskatīt projekta grāmatvedis finanšu un operāciju programmās, dodoties uz Sadaļu **Projektu vadība un grāmatvedība** > **Projekta līgumu** > **izveide** > **Rādīt noklusējuma uzskaiti** un pārskatot detalizētu informāciju cilnē **Līguma rindas** . Grāmatvedis var arī iestatīt noklusējuma finanšu dimensijas fiksētas cenas norēķinu metodes līguma rindām šajā cilnē.

## <a name="billing-milestones"></a>Norēķinu atskaites punkti

Par projekta līguma rindām, kurās tiek izmantota fiksētas cenas norēķinu metode, rēķins tiek izrakstīts, izmantojot norēķinu atskaites punktus. Norēķinu atskaites punkti tiek sinhronizēti ar projicēšanas darījumiem kontā finanšu un operāciju programmās, izmantojot **Project Operations integrācijas līguma rindiņas atskaites punktu (msdyn\_ contractlinescheduleofvalues)** tabulas karti.

  ![Norēķinu atskaites punktu integrācija.](./media/2Milestones.jpg)

Grāmatvedis var pārskatīt starpkontu transakcijas un pielāgot šo transakciju grāmatvedības atribūtus, dodoties uz **Projekta pārvaldība un uzskaite** > **Projekta līgumi** > **Uzturēšana** > **Starpkontu transakcijas** vai **Projekta pārvaldība un uzskaite** > **Visi projekti** > **Uzturēšana** > **Starpkontu transakcijas**.

Pirmoreiz izveidojot norēķinu atskaites punktu noteiktai projekta līguma rindai, sistēma automātiski izveido fiksētas cenas ieņēmumu aprēķinu projektu tam projektam, kas ir saistīts ar šo līguma rindu. Fiksētas cenas prognozējamo ieņēmumu projektus var pārskatīt, dodoties uz **Projekta pārvaldība un uzskaite** > **Fiksētas cenas prognozējamo ieņēmumu projekti**.

### <a name="project-tasks"></a>Projekta uzdevumi

Projekta uzdevumi tiek sinhronizēti ar finance and operations programmām, **izmantojot tabulas Projektu uzdevumi (msdyn\_ projectuzdevumuki)** karti tikai atsauces nolūkos. Darbību izveide, atjaunināšana un dzēšana netiek atbalstīta, izmantojot finanšu un operāciju programmas.

  ![Projekta uzdevumu integrācija.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekta resursi

Entītija **Projekta resursu lomas** tiek sinhronizēta ar finance and operations programmām, **izmantojot tabulas Projektu resursu lomas visiem uzņēmumiem (rezervējamas resursu kategorijas)** tikai atsauces vajadzībām. Tā kā resursu lomas nav saistītas ar uzņēmumu, sistēma automātiski izveido attiecīgos uzņēmumam raksturīgo resursu lomu ierakstus finanšu un operāciju lietotnēs visām juridiskajām personām, kas iekļautas divrakstu Dataverse integrācijas tvērumā.

![Resursu lomu integrācija.](./media/5Resources.jpg)

Project resursi programmā Project Operations tiek uzturēti Dataverse un netiek sinhronizēti ar finance and operations programmām.

### <a name="transaction-categories"></a>Transakcijas kategorijas

Transakciju kategorijas tiek uzturētas Dataverse un sinhronizētas ar finance and operations programmām, **izmantojot tabulas Projektu transakciju kategoriju (msdyn\_ transakciju kategorijas)** karti. Pēc transakcijas kategorijas ieraksta sinhronizēšanas sistēma automātiski izveido četrus kopīgotus kategoriju ierakstus. Katrs ieraksts atbilst transakcijas tipam finance and operations lietotnēs un saista to ar transakciju kategorijas ierakstu.

![Transakcijas kategoriju integrācija.](./media/4TransactionCategories.jpg)

Lai prognozēm un faktiskajiem datiem varētu izmantot transakcijas kategorijas, projekta grāmatvedim vai sistēmas administratoram ir jāizveido atbilstošas projekta kategorijas katrā juridiskajā entītijā. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](../project-accounting/configure-project-categories.md).
