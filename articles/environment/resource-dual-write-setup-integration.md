---
title: Project Operations iestatīšanas un konfigurēšanas datu integrācija
description: Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas karšu iestatīšanu un konfigurēšanu.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939015"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations iestatīšanas un konfigurēšanas datu integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju entītiju iestatīšanai un konfigurēšanai.

## <a name="project-contracts-contract-lines-and-projects"></a>Projekta līgumi, līguma rindas un projekti

Projekta līgumi, līguma rindas un projekti tiek izveidoti risinājumā Dataverse un sinhronizēti ar Finance and Operations programmām, lai veiktu papildu grāmatvedību. Šo entītiju ierakstus var izveidot un dzēst tikai programmā Dataverse. Taču šiem ierakstiem Finance and Operations programmās var pievienot tādus grāmatvedības atribūtus kā pārdošanas nodokļu grupas noklusējuma vērtības un finanšu dimensijas.

  ![Projekta līguma integrācijas koncepcijas](./media/1ProjectContract.jpg)

Pārdošanas darbību interesenti, iespējas un piedāvājumi tiek izsekoti risinājumā Dataverse un netiek sinhronizēti ar Finance and Operations programmām, jo ar šo darbību nav saistīta lejupstraumes grāmatvedība.

Projektu līgumu funkcionalitāte programmā Dataverse izveido projekta līguma ierakstu Finance and Operations programmās, izmantojot tabulas karti **Projektu līgumu galvenes (salesorders)**. Saglabājot projekta līgumu risinājumā Dataverse, tiek sākta arī projekta līguma klienta entītijas ieraksta izveide. Šis ieraksts tiek sinhronizēts ar Finance and Operations programmām, izmantojot tabulas karti **Projekta līdzekļu avots (msdyn\_projectcontractssplitbillingrules)**. Ar šo kartējumu tiek sinhronizēti arī projektu līgumu klientu papildinājumus, atjauninājumi un dzēšana. Norēķinu procentu sadali starp projektu līgumu klientiem var veikt tikai Dataverse, un tā netiek sinhronizēta ar Finance and Operations programmām.

Kad projekta līgums ir izveidots programmā Dataverse, projekta grāmatvedis var atjaunināt šī projekta līguma grāmatvedības atribūtus Finance and Operations programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Projekta līgumi** > **Iestatīšana** > **Rādīt noklusējuma grāmatvedību**. Grāmatvedis var pārskatīt darba projekta līguma atribūtus, piemēram, pieprasīto piegādes datumu un līguma summu, atlasot projekta līguma ID Finance and Operations programmās, tādējādi atverot saistīto projekta līguma ierakstu Dataverse.

Projekta entītija tiek sinhronizēta ar Finance and Operations programmām, izmantojot tabulas karti **Projects V2 (msdyn\_projects)**. Projekta grāmatvedis var:

  - pārskatīt projektus Finance and Operations programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti**; 
  - atjaunināt projekta grāmatvedības atribūtus Finance and Operations programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti** > **Iestatīšana** > **Rādīt noklusējuma grāmatvedību**;  
  - pārskatīt darbības projekta atribūtus, piemēram, prognozētos sākuma un beigu datumus, atlasot projekta ID Finance and Operations programmās, tādejādi atverot saistīto projekta ierakstu Dataverse.

Projekts tiek saistīts ar projekta līgumu, izmantojot entītiju **Projekta līguma rinda**.

Projekta līgumu rindas programmā Dataverse izveido projekta līguma norēķinu kārtulu Finance and Operations programmās, izmantojot tabulas karti **Projektu līgumu rindas (salesorderdetails)**. Norēķinu metode definē projekta līguma norēķinu kārtulas tipu Finance and Operations programmās:

  - projekta līguma rindas ar laika un materiālu norēķinu metodi izveido laika un materiālu tipa norēķinu kārtulu;
  - fiksētas cenas norēķinu metodes līguma rindās izveido atskaites punkta norēķinu kārtulu.

Projekta līguma rindas var pārskatīt projekta grāmatvedis Finance and Operations programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Projektu līgumi** > **Iestatīšana** > **Rādīt noklusējuma grāmatvedību** un pārskatot detalizēto informāciju cilnē **Līguma rindas**. Šajā cilnē grāmatvedis var iestatīt arī noklusējuma finanšu dimensijas fiksētas cenas norēķinu metodes līguma rindām.

## <a name="billing-milestones"></a>Norēķinu atskaites punkti

Par projekta līguma rindām, kurās tiek izmantota fiksētas cenas norēķinu metode, rēķins tiek izrakstīts, izmantojot norēķinu atskaites punktus. Norēķinu atskaites punkti tiek sinhronizēti ar projekta starpkontu transakcijām Finance and Operations programmās, izmantojot tabulas karti **Project Operations integrācijas līguma rindu atskaites punkti (msdyn\_contractlinescheduleofvalues)**.

  ![Norēķinu atskaites punktu integrācija](./media/2Milestones.jpg)

Grāmatvedis var pārskatīt starpkontu transakcijas un pielāgot šo transakciju grāmatvedības atribūtus, dodoties uz **Projekta pārvaldība un uzskaite** > **Projekta līgumi** > **Uzturēšana** > **Starpkontu transakcijas** vai **Projekta pārvaldība un uzskaite** > **Visi projekti** > **Uzturēšana** > **Starpkontu transakcijas**.

Pirmoreiz izveidojot norēķinu atskaites punktu noteiktai projekta līguma rindai, sistēma automātiski izveido fiksētas cenas ieņēmumu aprēķinu projektu tam projektam, kas ir saistīts ar šo līguma rindu. Fiksētas cenas prognozējamo ieņēmumu projektus var pārskatīt, dodoties uz **Projekta pārvaldība un uzskaite** > **Fiksētas cenas prognozējamo ieņēmumu projekti**.

### <a name="project-tasks"></a>Projekta uzdevumi

Projekta uzdevumi tiek sinhronizēti ar Finance and Operations programmām tikai atsauces nolūkos, izmantojot tabulas karti **Projekta uzdevumi (msdyn\_projecttasks)**. Izveides, atjaunināšanas un dzēšanas darbības Finance and Operations programmās netiek atbalstītas.

  ![Projekta uzdevumu integrācija](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekta resursi

Entītija **Projekta resursu lomas** tiek sinhronizēta ar Finance and Operations programmām tikai atsauces nolūkos, izmantojot tabulas karti **Projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories)**. Tā kā Dataverse resursu lomas nav konkrētas uzņēmumam, sistēma automātiski izveido attiecīgo uzņēmumam konkrēto resursu lomu ierakstus Finance and Operations programmās automātiski visām juridiskajām entītijām, kas ir ietvertas duālās rakstīšanas integrācijas tvērumā.

![Resursu lomu integrācija](./media/5Resources.jpg)

Projekta resursi programmā Project Operations tiek uzturēti risinājumā Dataverse un netiek sinhronizēti ar Finance and Operations programmām.

### <a name="transaction-categories"></a>Transakcijas kategorijas

Transakcijas kategorijas tiek uzturētas Dataverse un tiek sinhronizētas ar Finance and Operations programmām, izmantojot tabulas karti **Projekta transakcijas kategorijas (msdyn\_transactioncategories)**. Pēc transakcijas kategorijas ieraksta sinhronizēšanas sistēma automātiski izveido četrus kopīgotus kategoriju ierakstus. Katrs ieraksts atbilst transakcijas tipam Finance and Operations programmās un saista tos ar transakcijas kategorijas ierakstu.

![Transakcijas kategoriju integrācija](./media/4TransactionCategories.jpg)

Lai prognozēm un faktiskajiem datiem varētu izmantot transakcijas kategorijas, projekta grāmatvedim vai sistēmas administratoram ir jāizveido atbilstošas projekta kategorijas katrā juridiskajā entītijā. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](../project-accounting/configure-project-categories.md).
