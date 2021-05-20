---
title: Projekta rēķinu priekšlikumu pārvaldība
description: Šajā tēmā sniegta detaizēta informācija par klientam sniegto rēķinu apstrādi ar Project Operations resursu/nekrājumu scenārijos.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6b8eacf2b43219a9adad897637b78a9c94351554
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950723"
---
# <a name="manage-project-invoice-proposals"></a>Projekta rēķinu priekšlikumu pārvaldība

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta rēķinu priekšlikumus var apstrādāt jūsu norēķinu departaments, ja tiek izpildīti šādi divi nosacījumi:

  - Projekta vadītājs apstiprina proformas rēķinu pakalpojumā Microsoft Dataverse.
  - Visas laika un materiālu pārdošanas transakcijas, par kurām nav izrakstīts rēķins un kuras tiek ietvertas proformas rēķinā, tiek uzskaitītas, izmantojot Dynamics 365 **Project Operations integrācijas** žurnālu.

Lai aizpildītu projekta rēķina priekšlikumu pakalpojumā Dynamics 365 Finance, izpildiet šādas darbības.

1. Pārskatiet norēķinu informāciju laika un materiālu transakcijām un uzskaitiet **Project Operations integrācijas** žurnālā.
2. Pārskatiet norēķinu informāciju fiksētu cenu norēķinu atskaites punktiem.
3. Pārskatiet un formatējiet projekta rēķina priekšlikumu.
4. Uzskaitiet un drukājiet projekta rēķinus.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Pārvaldiet norēķinu informāciju Project Operations integrācijas žurnālā

Projekta faktiskās vērtības, kas izveidotas Dataverse, pārskata un ievieto Finance projekta vadītājs. Papildinformāciju par darbu ar integrācijas žurnālu skatiet tēmā [Integrācijas žurnāls risinājumā Project Operations](../project-accounting/project-operations-integration-journal.md).

Izmaksu faktiskās vērtības un rēķinā neiekļautās pārdošanas faktiskās vērtības integrācijas žurnālā tiek pievienotas kā atsevišķas rindas:

  - Vienības izmaksu cena un izmaksu summa no izmaksu faktiskās vērtības veido noklusējumu no projekta faktiskās vērtības transakcijas programmā Dataverse.
  - Vienības pārdošanas cena un pārdošanas summa rēķinā neiekļautās pārdošanas transakcijā pēc noklusējuma ir no projekta faktiskās rēķinā neiekļautās pārdošanas transakcijas programmā Dataverse.

### <a name="billing-sales-tax"></a>Pārdošanas nodokļa iekļaušana rēķinā

Pārdošanas nodokļa aprēķināšanu iekļaušanai rēķinā nosaka lauku **Norēķinu pārdošanas nodokļa grupa** un **Norēķinu preces pārdošanas nodokļa grupa** kombinācija rēķinā neiekļautās pārdošanas ierakstā **Project Operations integrācijas** žurnālā. Sistēma nosaka šī lauka noklusējuma vērtības, pamatojoties uz iestatījumiem cilnē **Finanšu dati**, lapā **Projektu pārvaldības un uzskaites parametri**.

- **Pārdošanas nodokļu grupas metode** nosaka norēķinu pārdošanas nodokļu grupas noklusējuma loģiku.
  
  - **Projekts**: Vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no projekta. Jūs varat pārskatīt vai mainīt noklusējuma pārdošanas nodokļu grupu projektā, lapā **Visi projekti** atlasot **Rādīt noklusējuma uzskaiti**.
  - **Projekta līgums**: Vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no projekta līguma. Jūs varat pārskatīt vai mainīt noklusējuma pārdošanas nodokļu grupu projekta līgumā, lapā **Projekta līgumi** atlasot **Rādīt noklusējuma uzskaiti**.
  - **Klients**: Vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no klienta.
  - **Meklēt**: Meklēs augstākminētajās entitījās un atlasīt pirmo pieejamo vērtību. Meklēšana sākas ar entitīju **Projekts**, pēc tam — entitīju **Projekta līgums** un visbeidzot — entitīju **Klients**.

- **Preču pārdošanas nodokļu grupas metode** nosaka norēķinu preču pārdošanas nodokļu grupas noklusējuma loģiku.
  
  - Attiecībā uz laika, izdevumu un papildmaksas darījumu veidiem norēķinu preču pārdošanas nodokļu grupas noklusējuma vērtība vienmēr tiks iegūta no entitījas **Projekta kategorija**.
  - Materiālu transakciju veidiem norēķinu preču pārdošanas nodokļu grupas noklusējuma vērtības nosaka, pamatojoties **Preču pārdošanas nodokļu grupas metodes** iestatījumā **Projektu pārvaldības un uzskaites parametros**. Preces numu pēc noklusējuma nosaka preču pārdošanas nodokļu grupa no entitījas **Izlaistais produkts**. Kategoriju pēc noklusējuma nosaka preču pārdošanas nodokļu grupa no entitījas **Projekta kategorija**.

### <a name="financial-dimensions"></a>Finanšu dimensijas

Finanšu dimensijas rēķinā neiekļautas pārdošanas ierakstiem **Project Operations integrācijas** žurnālā pēc noklusējuma nosaka no **Projekta** entitījas. Finanšu dimensijas var pārskatīt un pielāgot, atlasot **Sadalīt summas**. Ja ir nepieciešams mainīt rēķinā neiekļauta pārdošanas ieraksta finanšu dimensijas pēc tam, kad ir izlikts integrācijas žurnāls, taču pirms proformas rēķina apstiprināšanas, dodieties uz **Visi projekti** > **Pārvaldīt** > **Izliktās transakcijas**, atlasiet transakciju un pēc tam atlasiet **Apstrādāt** > **Pielāgot uzskaiti**.

### <a name="exchange-rates"></a>Valūtas kursi

Rēķinā neiekļauto transakcijas valūtu programmā Dataverse izmanto kā transakcijas valūtu programmā Finance un konvertē uz uzņēmuma uzskaites valūtu, izmantojot Finance definēto valūtas kursu.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Pārvaldiet norēķinu atskaites punktu finanšu atribūtus 

Projekta līguma rindas, izmantojot fiksētās cenas norēķinu metodi, tiek iekļautas rēķinā, izmantojot [Fiksētas cenas atskaites punktus](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Projekta grāmatvedis var pārskatīt norēķinu atskaites punktus programmā Finance, dodoties uz **Projekta pārvaldība un uzskaite** > **Visi projekti** > **Pārvaldīt** > **Starpkonta transakcijas**.

### <a name="billing-sales-tax"></a>Pārdošanas nodokļa iekļaušana rēķinā

Programmā Dataverse izveidojot jaunu norēķinu atskaites punktu, **Pārdošanas nodokļu grupas** un **Preču pārdošanas nodokļu grupas** noklusējuma vērtības iegūst no iestatījumiem. Sistēma nosaka šo lauku noklusējuma vērtības, pamatojoties uz iestatījumiem cilnē **Finanšu dati**, lapā **Projektu pārvaldības un uzskaites parametri**.

- **Pārdošanas nodokļu grupas metode** nosaka **Norēķinu pārdošanas nodokļu grupas** noklusējuma loģiku:

    - **Projekts**: vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no projekta. Jūs varat pārskatīt vai mainīt noklusējuma pārdošanas nodokļu grupu projektā, lapā **Visi projekti** atlasot **Rādīt noklusējuma uzskaiti**.
    - **Projekta līgums**: vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no projekta līguma. Jūs varat pārskatīt vai mainīt noklusējuma pārdošanas nodokļu grupu projekta līgumā, lapā **Projekta līgumi** atlasot **Rādīt noklusējuma uzskaiti**.
    - **Klients**: vienmēr noteiks norēķinu pārdošanas nodokļu grupas noklusējuma vērtību no klienta.
    - **Meklēt**: meklēs augstākminētajās entitījās šajā sarakstā un atlasīs pirmo pieejamo vērtību. Meklēšana sākas ar entitīju **Projekts**, pēc tam — entitīju **Projekta līgums** un pēc tam — entitīju **Klients**.

- **Fiksētas cenas atskaites punkta vienumu pārdošanas nodokļu grupa** tiek izmantota kā norēķinu atskaites punkta noklusējuma vērtība laukā **Vienumu pārdošanas nodokļu grupa**. Grāmatvedis var pārskatīt un modificēt šo vērtību lapā **Starpkonta darbības**. Sistēma izmanto vērtību no starpkonta darbības, veidojot projekta rēķina priekšlikuma rindu.
 

### <a name="financial-dimensions"></a>Finanšu dimensijas

Noklusējuma finanšu dimensijas fiksētās cenas norēķinu atskaites punktam iestata Projekta līguma rindās. Dodieties uz **Projekta līgumi** > **Rādīt noklusējuma uzskaiti** un cilnē **Līguma rindas** atlasiet **cenas līguma rinda**, pēc tam iestaties tās finanšu dimensijas vērtības, kuras vēlaties izmantot kā noklusējumu.

Projekta grāmatvedis var rediģēt pārdošanas nodokļu un finanšu dimensiju informāciju rēķina atskaites punktos līdz pat Projekta rēķina priekšlikuma izveidei.


## <a name="create-project-invoice-proposals"></a>Projekta rēķina priekšlikumu izveide

Projekta rēķina priekšlikumus var pārskatīt modulī **Projekta pārvaldība un uzskaite**, dodoties uz **Projekta rēķini** > **Projekta rēķinu priekšlikumi**.

Pakalpojumā Finance tiek izveidota Projekta rēķina priekšlikuma galvene, kad programmā Dataverse tiek apstiprināta proforma. Vieglākai saskaņošanai sistēma iestata Projekta rēķina priekšlikuma numuru programmā Finance uz to pašu numuru, kāds ir proformas rēķina ID programmā Dataverse. Tā kā proformas rēķini ne vienmēr tiek apstiprināti tādā pašā secībā, kādā tos izveido, Projekta rēķina priekšlikuma numuru secībai programmā Finance ir jābūt ar iespēju to mainīt uz augstākiem vai zemākiem skaitļiem. Konfigurējiet numuru secību, izpildot šādas darbības:

1. Programmā Finance dodieties uz **Organizācijas administrācija** > **Numuru secība** > **Numuru secība**.
2. Filtrā **Apgabals** atlasiet **Projekti**.
3. Filtrā **Atsauce** atlasiet **Rēķina priekšlikums**.
4. Izmantojiet lauku **Uzņēmums**, lai filtrētu katru juridisko entitīju ar iespējotu Project Operations Dataverse integrāciju.
5. Atveriet **Numuru secības informācija** un cilnē **Vispārīgi** iestatiet:

    - **Ļaut lietotājam mainīt: uz zemāku numuru** = **Jā**
    - **Ļaut lietotājam mainīt: uz augstāku numuru** = **Jā**

Projekta rēķina priekšlikuma rindas sistēma pievieno, izmantojot periodisko procesu **Importēt no sagatavošanas tabulas** (**Projekta pārvaldība un uzskaite** > **Periodiski** > **Project Operations integrācija** > **Importēt no sagatavošanas tabulas**). Šo procesu var palaist manuāli vai, izmantojot periodisku grafiku. Sistēma nepievienos rindas rēķina priekšlikuma dokumentam, iekams visas rindas nebūs gatavas iekļaušanai rēķinā. Laika un materiālu transakcijas ir gatavas iekļaušanai rēķinā vienīgi tad, ja tās ieliek, izmantojot **Project Operations integrācijas** žurnālu.

## <a name="format-and-print-invoice-proposals"></a>Rēķina priekšlikumu formatēšana un drukāšana

Projekta grāmatvedis var pielāgot projekta rēķina izdruku, izmantojot lapu **Formatēt rēķina priekšlikumu** un drukāt pārvaldības iespējas.

### <a name="format-invoice-proposals"></a>Rēķina priekšlikumu formatēšana

Lapa **Rēķina priekšlikumu formatēšana** ļauj pielāgoti grupēt transakcijas, kuras rādīt klienta projekta rēķinā.

1. Lapā **Projekta rēķina priekšlikums** atlasiet **Drukāt** > **Formatēt rēķina priekšlikumu**.
2. Atlasiet **Jauns**, lai izveidotu jaunu Projekta rēķina izdrukas grupējumu.
3. Laukā **Informācija/kopsavilkums** atlasiet šī grupējuma opcijas:

    - Atlasiet **Informācija**, lai drukāt klienta rēķina transakcijas informāciju.
    - Atlasiet **Kopsavilkums**, lai drukāt klienta rēķina transakcijas kopsavilkumu.

> [!NOTE]
> Lapā **Formatēt rēķina priekšlikumu** atlasot lauku **Informācija/kopsavilkums**, tiek pārrakstīta opcija, kas atlasīta lapas **Rēķina priekšlikumi** laukā **Rēķina formāts**, lai drukāt detalizētu rēķinu vai apkopotu rēķinu.

- Atlasiet transakcijas rindas, kuras iekļaut šajā sadaļā, cilnē **Pieejamās transakcijas** un atlasiet **Iekļaut transakcijas**, lai tās pārvietotu uz cilni **Atlasītās transakcijas**.
- Atlasiet **Pārvietot uz augšu** un **Pārvietot uz leju**, lai mainītu sadaļu secību.
- Atlasiet **Drukas priekšskatījums**, lai priekšskatītu formatēto rēķinu.

### <a name="print-management"></a>Drukāšanas pārvaldība

Drukāšanas pārvaldībā izmanto atšķirīgus atskaišu failus, lai drukātu, norādītu galamērķus un pielāgotu rēķina kājenes tekstu. Drukāšanas pārvaldību var iestatīt moduļa līmenī, taču šie iestatījumi var tikt ignorēti noteiktam klientam, līgumam vai rēķina priekšlikumam. Lai piekļūtu šai funkcijai, lapā **Projekta rēķina priekšlikums** atlasiet **Drukāt** > **Drukāšanas pārvaldība**.

Drukāšanas pārvaldības iestatījums tiek rādīts kā koka skats, kurā katrs mezgla līmenis rāda pielāgošanai pieejamos dokumentus. Jūs varat piešķirt pielāgotās izdrukas moduļa, klienta, līguma vai rēķina priekšlikuma dokumenta līmenī. Lai modificētu sākotnējo dokumenta izdruku, izvērsiet vēlamo mezglu un atlasiet **Sākotnējais vienums**. Laukā **Atskaites formāts** atlasiet atskaites formātu, kuru izmantot drukāšanai. Jūs varat izmantot pielāgotos atskaišu formātus, izmantojot [Biznesa dokumentu pārvaldības struktūru](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Rēķina priekšlikumu izlikšana

Pēc tam, kad rēķins ir pārskatīts un rediģēts un rēķina rindas ir apmierinošas, pārbaudiet rēķina kopsummas un pārdošanas nodokli. Grupā **Detalizēti** atlasiet **Kopsumma** un pēc tam atlasiet **Izlikt**, lai izliktu rēķinu.

Lai pirms izlikšanas skatītu rēķinu, notīriet izvēles rūtiņu **Izlikšana**. Uz rēķina tiks drukāts uzraksts **Pro forma**, lai norādītu, ka tas ir parauga rēķins. Lai drukātu rēķinu, atlasiet izvēles rūtiņu **Drukāt rēķinu**.

Līdztekus lapai **Rēķina priekšlikums**, rēķina priekšlikumus var arī izlikt, palaižot periodisku darbu, **Izlikt rēķina priekšlikumus**. Lai atrastu šo darbu, dodieties uz **Projekta pārvaldība un uzskaite** > **Periodiski** > **Projekta rēķini** > **Izlikt rēķina priekšlikumus**.

Šajā lapā tiek rādīti visi rēķina priekšlikumi, kuri ir gatavi izlikšanai. Jūs varat ieplānot rēķina priekšlikumu izlikšanu, atlasot **Pakete**. Iestatiet **Pakešapstrādes parametru** uz **Jā** un iestatiet pakešapstrādes periodiskumu, atlasot opciju **Periodiskums**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
