---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana
description: Šajā tēmā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948967"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Demonstrācijas iestatīšanas un konfigurācijas datu lietošana Project Operations Lite izvietošanā — pāreja uz proforma rēķinu izrakstīšanu

_**Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_

1. Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Pārejiet uz mapi *ProjOpsDemoDataSetupAndMaster - Integrated CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.
3. Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. CMT vedņa 2. lapā atlasiet **Office 365** kā **Izvietošanas tips** vērtību.
5. Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.
6. Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un pēc tam atlasiet **Pieteikties**.

![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. 3. lappusē Nomnieka Organizāciju sarakstā atlasiet, kurā organizācijā vēlaties importēt demonstrācijas datus, un pēc tam atlasiet **Pieteikties**.
8. 4. lappusē no izpakotās mapes *ProjOpsDemoDataSetupAndMaster - Integrated CMT* atlasiet zip failu *MasterAndSetupData*.

![Tilpsaspiestais fails](./media/3ZipFile.png)

![Atlasīt failu](./media/4SelectAFile.png)

9. Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.

![Importēt datus](./media/5ImportData.png)

10. Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes. Pēc pabeigšanas izejiet no CMT vedņa. 
11. Pārbaudiet savas organizācijas datus šajās 20 entītijās:

- Valūta
- Organizācijas vienība
- Kontaktinformācija
- Nodokļu grupa
- Klientu grupa
- Vienība
- Vienību grupa
- Cenrādis
- Projekta parametru cenrādis
- Rēķina izrakstīšanas biežums
- Rēķinu biežuma informācija
- Rezervējamo resursu kategorija
- Darījuma kategorija
- Izdevumu kategorija
- Lomas cena
- Transakcijas kategorijas cena
- Īpašību
- Rezervējamais resurssss
- Rezervējamo resursu kategorijas saistība
- Rezervējamā resursa īpašība

![Pabeigt importēšanu](./media/6CompleteImport.png)
