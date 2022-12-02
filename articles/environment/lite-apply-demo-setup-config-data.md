---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana — Lite
description: Šajā rakstā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410000"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demonstrācijas iestatīšanas un konfigurācijas datu lietošana lietojumprogrammā Project Operations — Lite 

_**Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_



## <a name="prerequisites"></a>Priekšnoteikumi

Pirms konfigurēšanas sākšanas ir nepieciešama Dataverse vide, kas ir nodrošināta risinājumam Dynamics 365 Project Operations.


## <a name="instructions"></a>Norādījumi

1. Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Pārejiet uz mapi *ProjOpsSampleSetupData - CE only CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.
3. Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.

    ![Konfigurāciju migrēšana.](./media/1ConfigurationMigration.png)

4. CMT vedņa 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.
5. Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.
6. Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un pēc tam atlasiet **Pieteikties**.

   ![Konfigurācijas pierakstīšanās.](./media/2ConfigurationSignin.png)

7. 3. lappusē Nomnieka Organizāciju sarakstā atlasiet, kurā organizācijā vēlaties importēt demonstrācijas datus, un pēc tam atlasiet **Pieteikties**.
8. 4. lapā atlasiet zip failu *SampleSetupAndConfigData* no neizpakotās mapes *ProjOpsSampleSetupData - CE only CMT*.

   ![Tilpsaspiestais fails.](./media/3ZipFile.png)

   ![Atlasīt failu.](./media/4SelectAFile.png)

9. Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.

   ![Importēt datus.](./media/5ImportData.png)

10. Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes. Pēc pabeigšanas izejiet no CMT vedņa. 
11. Pārbaudiet savas organizācijas datus šajās 18 entītijās:

    -   Valūta
    -   Konts
    -   Organizācijas vienība
    -   Kontaktpersona
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

    ![Importēšanas pabeigšana.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
