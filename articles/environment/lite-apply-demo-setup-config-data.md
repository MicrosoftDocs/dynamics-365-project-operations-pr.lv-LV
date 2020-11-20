---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana — Lite
description: Šajā tēmā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401272"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demonstrācijas iestatīšanas un konfigurācijas datu lietošana lietojumprogrammā Project Operations — Lite 

_**Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms konfigurēšanas sākšanas ir nepieciešama Common Data Service (CDS) vide, kas ir nodrošināta līdzeklim Dynamics 365 Project Operations.


## <a name="instructions"></a>Norādījumi

1. Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Pārejiet uz mapi *ProjOpsDemoDataSetupAndMaster - Integrated CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.
3. Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.
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

-   Valūta
-   Konts
-   Organizācijas vienība
-   Kontaktinformācija
-   Nodokļu grupa
-   Klientu grupa
-   Vienība
-   Vienību grupa
-   Cenrādis
-   Projekta parametru cenrādis 
-   Rēķina izrakstīšanas biežums
-   Rezervējamo resursu kategorija
-   Darījuma kategorija
-   Izdevumu kategorija
-   Lomas cena
-   Transakcijas kategorijas cena
-   Īpašību
-   Rezervējamais resurssss
-   Rezervējamo resursu kategorijas saistība
-   Rezervējamā resursa īpašība

![Pabeigt importēšanu](./media/6CompleteImport.png)
