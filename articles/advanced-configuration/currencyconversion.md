---
title: Valūtas konvertēšanas iestatīšana, lai aprēķinātu pārdošanas cenas no izmaksu kursiem
description: Šajā rakstā ir paskaidrots, kā konfigurēt valūtas konvertēšanas darbību, kas tiks izmantota korporācijā Microsoft Dynamics 365 Project Operations , kad pārdošanas transakcijas tiek ģenerētas no izmaksu transakcijām.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816694"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Valūtas konvertēšanas iestatīšana, lai aprēķinātu pārdošanas cenas no izmaksu kursiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Korporācijā Microsoft Dynamics 365 Project Operations pārdošanas cenas izdevumu kategorijām var iestatīt kā skaitliskas vērtības vai arī tās var iestatīt tā, lai tās tiktu aprēķinātas, pamatojoties uz izmaksām, kas radušās.

Ja tie ir iestatīti aprēķināšanai, pamatojoties uz radītajām izmaksām, ir pieejamas tālāk norādītās opcijas.

- Pašizmaksa
- Uzcenojums procentos pret izmaksām

Scenārijos, kuros izdevumu izmaksas rodas valūtā, kas atšķiras no projekta līguma pārdošanas valūtas, ir nepieciešama valūtas konvertēšana, lai aprēķinātu pārdošanas cenu, pamatojoties uz izmaksām.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valūtas konvertēšanas darbība, kas izmanto vietējos Dataverse valūtas maiņas kursus

Pēc noklusējuma Project Operations izmanto valūtas maiņas kursus, kas tiek glabāti tabulā Valūta Dataverse. Lai konfigurētu Project Operations izmantot vietējos valūtas maiņas kursus pārdošanas cenu aprēķināšanai no izmaksām, veiciet tālāk norādītās darbības.

1. Dodieties uz Projekta **operāciju \> iestatījumu \> parametri**.
1. Atveriet lapu Detalizēta informācija par **projekta parametru** .
1. Laukā Valūtas konvertēšanas loģika **iestatiet** tukšu vērtību.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valūtas konvertēšanas darbība, kas izmanto valūtas maiņas kursus no Finance and Operations programmām

Valūtas maiņas kursi tabulā, kas ir vietēji pieejami Dataverse , nav spēkā. Tāpēc tie, iespējams, ne vienmēr tiks pielāgoti prasībām, kas jums ir, lai aprēķinātu pārdošanas cenas no izmaksu likmēm.

Varat izmantot valūtas maiņas kursus no finance and operations vides, lai pārdošanas cenu pārdošanas valūtā aprēķinātu no izmaksu kursa izmaksu valūtā. Lai konfigurētu šo valūtas konvertēšanas darbību, veiciet tālāk norādītās darbības.

1. Lapā **Projekta parametri** pievienojiet **lauku Valūtas konvertēšanas loģika** . Pēc tam saglabājiet un publicējiet pielāgojumu.
1. Dodieties uz Projekta **operāciju \> iestatījumu \> parametri**.
1. Atveriet lapu Detalizēta informācija par **projekta parametru** . 
1. Iestatiet **lauka Valūtas konvertēšanas darbība** vērtību **Paplašināts ar atkāpšanos uz noklusējumu**.
1. Piešķiriet **duālās rakstīšanas lietotnes lietotājam**  drošības loma **globālās lasīšanas** atļauju tālāk norādītajām tabulām.

    - MSDYN\_ valūtasmaiņas kursi
    - msdyn\_ valūtasmaiņaspairs
    - MSDYN\_ valūtas kursu tipi

1. Finance and Operations vidē palaidiet tālāk norādītās dubultās rakstīšanas kartes ar sākotnējo sinhronizāciju.

    - Valūtas kursa tips (msdyn\_ valūtas kursa tipi)
    - Valūtas kursa valūtu pāris (msdyn\_ currencyexchangepairs)
    - CDS maiņas kursi (msdyn\_ valūtas maiņas kursi)

Pēc tam, kad šīs izmaiņas ir pabeigtas, dubultā rakstīšana padarīs pieejamus Dataverse valūtas kursus no finanšu un operāciju vides. Pēc tam projekta operācijas izmantos šos valūtas maiņas kursus, lai konvertētu izmaksu kursus līguma pārdošanas valūtā.

> [!NOTE]
> Šī valūtas konvertēšanas darbība attiecas tikai uz pārdošanas cenu aprēķināšanu no izmaksu kursiem. Tas netiks izmantots, lai vispārīgi aprēķinātu bāzes valūtas vērtības. Bāzes valūtas vērtības vienmēr izmantos vietējos Dataverse valūtas kursus neatkarīgi no tā, vai esat pabeidzis šo procedūru.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
