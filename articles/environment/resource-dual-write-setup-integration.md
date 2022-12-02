---
title: Project Operations iestatīšanas un konfigurēšanas datu integrācija
description: Šajā rakstā ir sniegta informācija par Project Operations duālās rakstīšanas karšu iestatīšanu un konfigurēšanu.
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

Šajā rakstā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju entītiju iestatīšanai un konfigurēšanai.

## <a name="project-contracts-contract-lines-and-projects"></a>Projekta līgumi, līguma rindas un projekti

Projekta līgumi, līguma rindas un projekti tiek izveidoti risinājumā Dataverse un sinhronizēti ar finanšu un operāciju programmām, lai veiktu papildu grāmatvedību. Šo entītiju ierakstus var izveidot un dzēst tikai programmā Dataverse. Taču šiem ierakstiem finanšu un operāciju programmās var pievienot tādus grāmatvedības atribūtus kā pārdošanas nodokļu grupas noklusējuma vērtības un finanšu dimensijas.

  ![Projekta līguma integrācijas koncepcijas.](./media/1ProjectContract.jpg)

Pārdošanas darbību interesenti, iespējas un piedāvājumi tiek izsekoti risinājumā Dataverse un netiek sinhronizēti ar finanšu un operāciju programmām, jo ar šo darbību nav saistīta lejupstraumes grāmatvedība.

Projektu līgumu funkcionalitāte programmā Dataverse izveido projekta līguma ierakstu finanšu un operāciju programmās, izmantojot tabulas karti **Projektu līgumu galvenes (salesorders)**. Saglabājot projekta līgumu risinājumā Dataverse, tiek sākta arī projekta līguma klienta entītijas ieraksta izveide. Šis ieraksts tiek sinhronizēts ar finanšu un operāciju programmām, izmantojot tabulas karti **Projekta līdzekļu avots (msdyn\_projectcontractssplitbillingrules)**. Ar šo kartējumu tiek sinhronizēti arī projektu līgumu klientu papildinājumus, atjauninājumi un dzēšana. Norēķinu procentu sadali starp projektu līgumu klientiem var veikt tikai Dataverse, un tā netiek sinhronizēta ar finanšu un operāciju programmām.

Kad projekta līgums ir izveidots programmā Dataverse, projekta grāmatvedis var atjaunināt šī projekta līguma grāmatvedības atribūtus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Projekta līgumi** > **Iestatīšana** > **Rādīt noklusējuma grāmatvedību**. Grāmatvedis var pārskatīt darba projekta līguma atribūtus, piemēram, pieprasīto piegādes datumu un līguma summu, atlasot projekta līguma ID finanšu un operāciju programmās, tādējādi atverot saistīto projekta līguma ierakstu Dataverse.

Projekta entītija tiek sinhronizēta ar finanšu un operāciju programmām, izmantojot tabulas karti **Projects V2 (msdyn\_projects)**. Projekta grāmatvedis var:

  - pārskatīt projektus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti**. 
  - atjaunināt projekta grāmatvedības atribūtus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti** > **Iestatīšana** > **Rādīt noklusējuma grāmatvedību**.  
  - pārskatīt darbības projekta atribūtus, piemēram, prognozētos sākuma un beigu datumus, atlasot projekta ID finanšu un operāciju programmās, tādejādi atverot saistīto projekta ierakstu Dataverse.

Projekts tiek saistīts ar projekta līgumu, izmantojot entītiju **Projekta līguma rinda**.

Projekta līgumu rindas programmā Dataverse izveido projekta līguma norēķinu kārtulu finanšu un operāciju programmās, izmantojot tabulas karti **Projektu līgumu rindas (salesorderdetails)**. Izmantojot norēķinu metodi, projekta līguma norēķinu kārtulas tips tiek definēts lietojumprogrammās un operāciju programmās.

  - projekta līguma rindas ar laika un materiālu norēķinu metodi izveido laika un materiālu tipa norēķinu kārtulu;
  - fiksētas cenas norēķinu metodes līguma rindās izveido atskaites punkta norēķinu kārtulu.

Projekta līguma rindas var pārskatīt projekta grāmatvedis finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Projektu līgumi** > **Iestatīšana** > **Rādīt noklusējuma uzskaiti** un pārskatot detalizēto informāciju cilnē **Līguma rindas**. Šajā cilnē grāmatvedis var iestatīt arī noklusējuma finanšu dimensijas fiksētas cenas norēķinu metodes līguma rindām.

## <a name="billing-milestones"></a>Norēķinu atskaites punkti

Par projekta līguma rindām, kurās tiek izmantota fiksētas cenas norēķinu metode, rēķins tiek izrakstīts, izmantojot norēķinu atskaites punktus. Norēķinu atskaites punkti tiek sinhronizēti ar projekta starpkontu transakcijām finanšu un operāciju programmās, izmantojot tabulas karti **Project Operations integrācijas līguma rindu atskaites punkti (msdyn\_contractlinescheduleofvalues)**.

  ![Norēķinu atskaites punktu integrācija.](./media/2Milestones.jpg)

Grāmatvedis var pārskatīt starpkontu transakcijas un pielāgot šo transakciju grāmatvedības atribūtus, dodoties uz **Projekta pārvaldība un uzskaite** > **Projekta līgumi** > **Uzturēšana** > **Starpkontu transakcijas** vai **Projekta pārvaldība un uzskaite** > **Visi projekti** > **Uzturēšana** > **Starpkontu transakcijas**.

Pirmoreiz izveidojot norēķinu atskaites punktu noteiktai projekta līguma rindai, sistēma automātiski izveido fiksētas cenas ieņēmumu aprēķinu projektu tam projektam, kas ir saistīts ar šo līguma rindu. Fiksētas cenas prognozējamo ieņēmumu projektus var pārskatīt, dodoties uz **Projekta pārvaldība un uzskaite** > **Fiksētas cenas prognozējamo ieņēmumu projekti**.

### <a name="project-tasks"></a>Projekta uzdevumi

Projekta uzdevumi tiek sinhronizēti ar finanšu un operāciju programmām tikai atsauces nolūkos, izmantojot tabulas karti **Projekta uzdevumi (msdyn\_projecttasks)**. Izveides, atjaunināšanas un dzēšanas darbības finanšu un operāciju programmās netiek atbalstītas.

  ![Projekta uzdevumu integrācija.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekta resursi

Entītija **Projekta resursu lomas** tiek sinhronizēta ar finanšu un operāciju programmām tikai atsauces nolūkos, izmantojot tabulas karti **Projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories)**. Tā kā Dataverse resursu lomas nav konkrētas uzņēmumam, sistēma automātiski izveido attiecīgo uzņēmumam konkrēto resursu lomu ierakstus finanšu un operāciju programmās automātiski visām juridiskajām entītijām, kas ir ietvertas duālās rakstīšanas integrācijas tvērumā.

![Resursu lomu integrācija.](./media/5Resources.jpg)

Projekta resursi programmā Project Operations tiek uzturēti risinājumā Dataverse un netiek sinhronizēti ar finanšu un operāciju programmām.

### <a name="transaction-categories"></a>Transakcijas kategorijas

Transakcijas kategorijas tiek uzturētas Dataverse un tiek sinhronizētas ar finanšu un operāciju programmām, izmantojot tabulas karti **Projekta transakcijas kategorijas (msdyn\_transactioncategories)**. Pēc transakcijas kategorijas ieraksta sinhronizēšanas sistēma automātiski izveido četrus kopīgotus kategoriju ierakstus. Katrs ieraksts atbilst transakcijas tipam finanšu un operāciju programmās un saista tos ar transakcijas kategorijas ierakstu.

![Transakcijas kategoriju integrācija.](./media/4TransactionCategories.jpg)

Lai prognozēm un faktiskajiem datiem varētu izmantot transakcijas kategorijas, projekta grāmatvedim vai sistēmas administratoram ir jāizveido atbilstošas projekta kategorijas katrā juridiskajā entītijā. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](../project-accounting/configure-project-categories.md).
