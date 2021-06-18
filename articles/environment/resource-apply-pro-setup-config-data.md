---
title: Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service
description: Šajā tēmā ir sniegta informācija par konfigurācijas datu iestatīšanu un lietošanu programmā Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001300"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms varat sākt datu konfigurēšanu Common Data Service (CDS), ir jāizpilda tālāk norādītie priekšnosacījumi.

1.  Nodrošināt CDS vidi un Dynamics 365 Finance vidi risinājumam Project Operations.
2.  Informācija par juridiskajām entītijām no Dynamics 365 Finance tiek kopīgota ar CDS vidi. Tas nozīmē, ka entītijai **Uzņēmums** pakalpojumā CDS ir šādi uzņēmumu ieraksti:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Iestatīšanas un konfigurācijas datu instalēšana

1. Lejupielādējiet, atbloķējiet un izgūstiet no ZIP arhīva [iestatīšanas un konfigurācijas datu pakotni](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Pārejiet uz mapi, kas izgūta no ZIP arhīva, un palaidiet izpildāmo failu *DataMigrationUtility*.
3. Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.
5. Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.
6. Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un atlasiet **Pieteikties**.

![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. 3. lappusē nomnieka organizāciju sarakstā atlasiet organizāciju, kurā vēlaties importēt demonstrācijas datus, un atlasiet **Pieteikties**.
8. 4. lappusē no izpakotās mapes atlasiet .zip failu *SampleSetupAndConfigData*.

![.zip faila atlase](./media/3ZipFile.png)

![Atlasīt failu](./media/4SelectAFile.png)

9. Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.

![Importēt datus](./media/5ImportData.png)

10. Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes. Pēc importēšanas pabeigšanas izejiet no CMT vedņa. 
11. Pārbaudiet savas organizācijas datus šajās 26 entītijās:

  - Valūta
  - Uzņēmumu tabula
  - Finanšu kalendārs
  - Valūtas maiņas kursu tipi
  - Maksājuma diena
  - Maksājumu grafiks
  - Maksājuma termiņš
  - Organizācijas vienība
  - Kontaktpersona
  - Nodokļu grupa
  - Klientu grupa
  - Piegādātāju grupa
  - Vienība
  - Vienību grupa
  - Cenrādis
  - Projekta parametru cenrādis
  - Rēķina izrakstīšanas biežums
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

## <a name="update-project-operations-configurations"></a>Project Operations konfigurāciju atjaunināšana

1. Pārejiet uz CE vidi. To var atrast, atverot [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/environments), atlasot vidi un pēc tam atlasot **Atvērt vidi**. 

![Atvērt vidi](./media/7OpenEnvironment.png)

2. Atveriet sadaļas **Projekti** > **Resursi** un pēc tam atlasiet **Jauns**, lai savam lietotājam izveidotu rezervējamu resursu.

![Rezervējamie resursi](./media/8BookableResources.png)

3. Cilnē **Vispārīgi** atlasiet savu lietotāju ar administratora atļaujām. Pārbaudiet, vai laika josla atbilst tai, kurā atrodaties. 

![Jauns rezervējamais resurss](./media/9NewBookableResource.png)

4. Cilnes **Plānošana** laukā **Uzņēmums** izvēlieties **USPM** uzņēmumu un pēc tam atlasiet **Saglabāt**. 

![Cilne Plānošana](./media/10SchedulingTab.png)

5. Atlasiet cilni **Darba stundas**.  

![Darba stundas](./media/11WorkHours.png)

6. Veiciet dubultklikšķi uz jebkuras kalendārā ievadītās vērtības un atlasiet **Rediģēt** > **Visi sērijas notikumi**. 

![Darba kalendārs](./media/12WorkCalendar.png)

7. Mainiet darba stundas uz astoņu (8) stundu darba dienu, atzīmējiet nedēļas nogales kā nestrādājamās dienas un pārliecinieties, vai laika josla atbilst jūsu laika joslai. 
8. Atlasiet **Saglabāt un aizvērt**.

![Atjaunināt kalendāru](./media/13UpdateCalendar.png)

9. Dodieties uz **Iestatījumi** > **Kalendāra veidnes** un atlasiet **Jauna**.
 
 ![Kalendāra veidnes](./media/14CalendarTemplates.png)
 
 10. Ievadiet nosaukumu, atlasiet izveidoto veidnes resursu un pēc tam atlasiet **Saglabāt**. 
 
 ![Saglabāt kalendāra veidni](./media/15SaveCalendarTemplate.png)
 
 11. Dodieties uz **Parametri** un veiciet dubultklikšķi uz ieraksta. 
 
 ![Projekta parametri](./media/16ProjectParameters.png)
 
12. Atjauniniet šos laukus:

 - **Noklusējuma uzņēmums**: USPM
 - **Noklusējuma organizācijas vienība**: Contoso Robotics Global
 - **Rēķina izrakstīšanas biežums**: septītā un pēdējā diena
 - **Darba stundu veidne**: mainiet uz izveidoto veidni

13. Atlasiet vienumu **Saglabāt**. 

![Atjaunināti projekta parametri](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
