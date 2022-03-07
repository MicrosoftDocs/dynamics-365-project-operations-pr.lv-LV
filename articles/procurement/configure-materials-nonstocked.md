---
title: Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu konfigurēšana
description: Šajā tēmā ir izskaidrots, kā iespējot krājumos neesošus materiālus un neapstiprinātus piegādātāju rēķinus.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003240"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu konfigurēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="minimum-version-requirement"></a>Nepieciešamās minimālās prasības

Lai izmantotu krājumos neesošus materiālus un neapstiprinātus piegādātāju rēķinus krājumos neesošiem/uz resursiem balstītiem Dynamics 365 Project Operations scenārijiem, ir nepieciešamas tālāk norādītās versijas.

Dynamics 365 Dataverse risinājumi:

- Project Operations — 4.9.0.221 vai jaunāka versija
- Duālās rakstīšanas lietojumprogrammas saskaņotais risinājums — 2.2.2.23 vai jaunāka versija

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) vai jaunāka versija. Pārliecinieties, ka jums ir jaunākā Finance vides versija un vai ir instalēti visi kvalitātes atjauninājumi, lai nodrošinātu atbilstību minimālajām versijas prasībām.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Duālās rakstīšanas karšu palaišana krājumos neesošu materiālu un piegādātāju rēķinu integrēšanai

Šajā sadaļā ir sniegta informācija par konkrētām kartēm, kas nepieciešamas krājumos neesošiem materiāliem un piegādātāju rēķiniem. Pārbaudiet, vai jūsu vidē darbojas tēmā [Jaunas vides nodrošināšana](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) uzskaitītās priekšnosacījuma kartes.

1. Dodieties uz Lifecycle Services (LCS), pārejiet uz savu LCS projektu un atveriet lapu **Vides informācija**.
2. Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām**. Pēc saites atlasīšanas tiksit novirzīts uz entītiju sarakstu kartējumos.
3. Pārliecinieties, ka darbojas tālāk minētās kartes. Ja tās nedarbojas, palaidiet tās un pārliecinieties, ka ir iekļautas visas saistītās tabulu kartes.

    - CDS izlaistie atšķirīgie produkti (products)
    - Vendors v2 (msdyn_vendors)
    - Project Operations tabula materiālu aprēķiniem (msdyn_estimatelines)
    - Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices)
    - Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija (msdyn_projectvendorinvoicelines)
    - Project Operations integrācijas faktiskie dati (msdyn_actuals). Pārliecinieties, ka izmantojat kartes versiju 1.0.0.14 vai jaunāku. Kartes aktīvā versija ir redzama kolonnas **Versija** lapā **Duālā rakstīšana**. Varat aktivizēt jaunu kartes versiju, atlasot **Tabulas kartes versija** un pēc tam saglabājot atlasīto versiju.

Ja izmantojat standarta demonstrācijas datus, iespējams, būs jāaptur un jārestartē arī tālāk uzskaitītās entītiju kartes ar sākotnēju sinhronizāciju.
  - Maksājumu datumu CDS V2 (msdyn_paymentdays)
  - Maksājumu grafiks (msdyn_paymentschedules)
  - Maksājumu nosacījumi (msdyn_paymentterms)
  - Piegādātāju grupas (msdyn_vendorgroups)
  - Vienības (uom)

> [!NOTE]
> Esošā demonstrācijas datu kopā sākotnējā piegādātāju grupu un vienību sinhronizēšana dažiem ierakstiem var neizdoties. Varat ignorēt šīs kļūmes, jo tās neliegs izmantot demonstrācijas datus programmā Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Priekšnosacījumu konfigurēšana platformā Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Darbplūsmas aktivizēšana, lai izveidotu uzņēmumus, balstoties uz piegādātāja entītiju

Risinājumā Dual Write Orchestration ir nodrošināta [piegādātāju galvenā integrācija](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Lai varētu izmantot šo līdzekli, entītijā **Uzņēmumi** ir jāizveido piegādātāja dati. Aktivizējiet veidnes darbplūsmas procesu, lai tabulā **Uzņēmumi** izveidotu piegādātājus, kā aprakstīts tēmā [Pārslēgšanās starp piegādātāju noformējumiem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Produktu iestatīšana, lai tie tiktu izveidoti kā aktīvi

Krājumos neesoši materiāli risinājumā Finance ir jākonfigurē kā **Izlaistie produkti**. Risinājumā Dual Write Orchestration ir nodrošināta gatava [izlaisto produktu integrēšana Dataverse preču katalogā](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Pēc noklusējuma produkti no Finance tiek sinhronizēti ar Dataverse melnraksta statusā. Lai sinhronizētu produktu ar aktīvu statusu un to varētu tieši izmantot materiālu lietojuma dokumentos vai neapstiprinātos piegādātāju rēķinos, pārejiet uz **Sistēma** > **Administrācija** > **Sistēmas administrācija** > **Sistēmas iestatījumi** un cilnē **Pārdošana** iestatiet **Izveidot produktus ar aktīvu statusu** uz **Jā**.

## <a name="configure-prerequisites-in-finance"></a>Priekšnosacījumu konfigurēšana platformā Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Līdzekļa atslēgas iespējošana neapstiprinātiem piegādātāju rēķiniem

Lai iespējotu produktu informācijas pievienošanas funkcionalitāti neapstiprināto piegādātāju rēķinu rindām, veiciet tālāk norādītās darbības.

1. Programmā Finance pārejiet uz darbvietu **Līdzekļu pārvaldība**.
2. Līdzekļu sarakstā atrodiet līdzekli **Iespējot neapstiprināto piegādātāju rēķinus risinājumā Project Operations uz resursiem balstītiem/uz krājumiem nebalstītiem scenārijiem** un atlasiet **Iespējot**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Vienumu kategoriju grupu un projektu kategoriju definēšana

Konfigurējiet vismaz vienu kategoriju grupu transakcijas tipam **Vienums** un vismaz vienu projekta kategoriju, izmantojot šo grupu. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](../project-accounting/configure-project-categories.md#category-groups).

Pārskatiet projekta izmaksu un ieņēmumu profilus un konfigurējiet krājumu transakciju virsgrāmatas grāmatošanas iestatījumus. Papildinformāciju skatiet rakstā [Apmaksājamo projektu uzskaites konfigurēšana](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Ierakstāmā produkta iestatīšana

Programmā Project Operations varat ierakstīt materiālu aprēķinus un lietojumu kataloga produktiem, kas ir konfigurēti izlaisto preču katalogā un ierakstāmajiem produktiem. Lai varētu izmantot ierakstāmos produktus, ir nepieciešams viens izlaists produkts, kas šim nolūkam ir konfigurēts programmā Finance. Lai konfigurētu ierakstāmu produktu, veiciet tālāk norādītās darbības. Atkārtojiet šīs darbības katrā juridiskā entītijā, kurā izmanto Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.

1. Programmā Finance dodieties uz **Produktu informācijas pārvaldība** > **Produkti** > **Izlaistie produkti** un atlasiet **Jauns**.
2. Laukā **Produkta tips** atlasiet **Vienums** un laukā **Produkta apakštips** atlasiet **Produkts**.
3. Ievadiet produkta numuru (WRITEIN) un produkta nosaukumu (Write-in Product).
4. Atlasiet krājumu modeļu grupu. Pārliecinieties, ka jūsu atlasītās krājumu modeļu grupas lauks **Krājumu politika — krājumos esošs produkts** ir iestatīts kā **Aplams**.
5. Atlasiet vērtības laikos **Krājumu grupa**, **Noliktavas dimensiju grupa** un **Izsekošanas dimensijas grupa**. Izmantojiet **Noliktavas dimensiju** tikai **Vietai**, un laukā **Izsekošanas dimensija** atlasiet **Nav**.
6. Atlasiet vērtības laukā **Krājumu vienība**, **Pirkuma vienība** un **Pārdošanas vienība** un pēc tam saglabājiet veiktās izmaiņas.
7. Cilnē **Plāns** iestatiet noklusējuma pasūtījuma iestatījumus un cilnē **Krājumi** iestatiet noklusējuma vietu un noliktavu.
8. Dodieties uz **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldības un uzskaites parametri** un atveriet **Project Operations risinājumā Dynamics 365 Dataverse**. 
9. Cilnes **Materiāli** laukā **Ierakstāms produkts** atlasiet izveidoto produktu.
10. Dataverse vidē vietnes kartē atveriet entītiju **Produkti** un atrodiet ierakstāmā produkta ierakstu. 
11. Atveriet ieraksta detalizēto informāciju un iestatiet produkta statusu kā **Slēgts**. Šis produkta statuss neļauj nevienam nejauši izmantot šo ierakstu tieši materiālu aprēķinos un lietojuma dokumentos.

### <a name="set-up-a-procurement-integration-account"></a>Sagādes integrācijas konta iestatīšana

Sagādes integrācijas konts tiek izmantots kā klīringa konts, grāmatojot neapstiprinātu piegādātāja rēķinu ar rindām, kas attiecas uz projektu.

Kad sistēma grāmato neapstiprinātu piegādātāja rēķinu, šis konts tiek izmantots projekta izmaksu summai. Piegādātāja rēķina informācija tiek apstrādāta risinājumā Dataverse, un tiek izveidota atbilstoša projekta faktiskā summa. Projekta faktiskās summas informācija tiek pievienota Project Operations integrācijas žurnālam. Grāmatojot integrācijas žurnālu, summa tiek dzēsta no sagādes integrācijas konta un ierakstīta projekta izmaksās.

1. Lai iestatītu sagādes integrācijas kontu, dodieties uz **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldības un uzskaites parametri** un atveriet **Project Operations risinājumā Dynamics 365 Dataverse**. 
2. Atlasiet cilni **Materiāli** un atlasiet vērtību laukā **Sagādes integrācijas konts**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Projekta kategorijas noklusējumu iestatīšana vienumam

1. Programmā Finance dodieties uz **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldības un uzskaites parametri** un atveriet **Project Operations risinājumā Dynamics 365 Dataverse**. 
2. Cilnes **Projekta kategorijas noklusējumi** laukā **Vienums** atlasiet kādu vērtību. Šī projekta kategorija tiek lietota materiālu transakcijām, ja projekta faktiskajos ierakstos nav iestatīta projekta kategorija.
