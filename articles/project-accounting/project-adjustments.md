---
title: Projekta korekcijas
description: Šajā rakstā ir sniegta informācija par projektu korekcijām.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788369"
---
# <a name="project-adjustments"></a>Projekta korekcijas

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

## <a name="adjustments-overview"></a>Korekciju pārskats

Sistēmu Microsoft var konfigurēt tā Dynamics 365 Project Operations , lai lietotāji varētu veikt izmaiņas grāmatotajās transakcijās. Varat pielāgot projekta transakcijas atsevišķi vai arī atlasīt vairākas transakcijas vienlaikus visu projekta transakciju sarakstā. Projekta korekcijas tiek izmantotas, piemēram, lai masveidā atjauninātu apmaksājamo statusu, pārrēķinātu izmaksas pēc konfigurācijas maiņas vai atjauninātu finansējuma avotus.

Lietotāji var piekļūt projekta pielāgošanas funkcionalitātei vairākos veidos:

- Izmantojot **lapu Transakciju** pielāgošana, kurai var piekļūt no sadaļas **Projektu vadība un uzskaites** \> **iestatīšana**.
- Izmantojot pogu Korekcija lapā Grāmatotās projektu transakcijas, kurai var piekļūt no sadaļas **Projektu vadība un uzskaites** transakcijas **·** . **·** \> **·**
- Izmantojot **pogu** Korekcija **lapā Grāmatotās projekta transakcijas** projekta kontekstā. Šai lapai var piekļūt no Projektu **vadība un uzskaite** \> **Visi projekti**.

Lai atļautu korekcijas, ir jāiespējo viens vai vairāki transakciju statusi no **projektu vadības un grāmatvedības projektu vadības un grāmatvedības** \> **paramateriem**  **cilnes Vispārīgi** sadaļā **Atļaut transakcijas statusa** korekciju. Transakciju statusu piemēri ir grāmatotās transakcijas, rēķinā norādītās transakcijas vai izslēgtās transakcijas. Jebkuram transakcijas statusam, kas ir iestatīts uz **Nē**, šajā statusā būs transakcijas, kas korekcijas procesā netiks rādītas kā atlasāmas korekcijai.

Konfigurācijas opcija ar nosaukumu **Vienmēr izveidot korekcijas transakciju** pašlaik ir pieejama sadaļā Projektu vadības un uzskaites parametri. Varat atspējot šo opciju, lai atjauninātu sākotnējo transakciju, nevis izveidotu jaunas transakcijas korekcijas laikā scenāriju apakškopā. Ir paziņots, ka šis parametrs būs novecojis līdz 2023. gada 1. martam. Pēc 2023. gada 1. marta sistēma vienmēr darbosies tā, it kā opcija būtu iespējota.

## <a name="adjustments-process-flow"></a>Pielāgošanas procesa plūsma

Tālāk norādītajās darbībās ir parādīta tipiskā apstrādes pielāgojumu plūsma.

1. Atveriet lapu Projekta **korekcijas** .
2. Atlasiet **Atlasīt**, lai meklētu transakcijas, kas atbilst paredzamajiem korekcijas kritērijiem.
3. Darījumu sarakstā atlasiet visus darījumus vai koriģējamo darījumu apakškopu.
4. Atlasiet **Pielāgot** un modificējiet līnijas atribūtus. Vai arī, ja transakcijas ievades laikā vērtības tika norādītas manuāli, varat atlasīt, lai ievadītu noklusējuma sistēmas vērtības.
5. Tiek atgriezts transakciju saraksts, un kolonnā Neapstiprinātā korekcija **tiek parādīta** atzīme, lai norādītu, kur tika veiktas izmaiņas. Visas korekcijas, kurās ir gaidošas izmaiņas, tiek rādītas lapas apakšējā daļā. Tur jūs varat veikt papildu detalizētas izmaiņas, kas pārsniedz to, kas tika parādīts iepriekšējā lapā.
6. Atlasiet **Izlikt**, lai grāmatotu korekcijas transakcijas.

Atkarībā no konfigurācijas korekcijai parasti tiek izveidotas jaunas transakcijas.

- Sākotnējās **transakcijas lauks Rēķina statuss** ir iestatīts uz **Pielāgots**.
- Tiek izveidota reversā transakcija, lai atsauktu sākotnējo transakciju, un lauks Statuss **ir iestatīts uz** Pielāgots **·**.
- Tiek izveidota jauna transakcija, kurā ir izmaiņas, kas tika veiktas korekcijas procesa laikā.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Vairāku iegrāmatotu projekta transakciju atlasīšana vienlaikus korekcijām un kredīta piezīmēm

Jauns līdzeklis, kas tika ieviests 10.0.30 laidienā, ļauj atlasīt vairākas korekcijas transakcijas vienlaikus no **lapas Grāmatotās projektu transakcijas** .

Lai varētu izmantot šo funkciju, tai jābūt iespējotai jūsu sistēmā. Administratori var izmantot **darbvietu Līdzekļu pārvaldība**, lai pārbaudītu līdzekļa statusu un iespējotu to, ja tas ir nepieciešams.  **Darbvietā Līdzekļu pārvaldība** meklējiet un atlasiet Vairākas atlasītas grāmatotās projektu transakcijas korekcijām un kredītzīmēm **un pēc tam atlasiet** **Iespējot tūlīt**.

Šis līdzeklis iespējo šādu galveno funkcionalitāti:

- Tam var piekļūt no projekta grāmatotās transakcijas lapas, izmantojot esošo **pogu Pielāgošana** .
- Tas iespējo vairāku rindu atlases vadīklu lapā Izliktās **projekta transakcijas** . Saraksta lapai varat lietot filtrus un atlasīt ierakstus, pirms sākat pielāgošanu.
- Tas atspējo pogu Korekcija **,** ja kādu atsevišķu transakciju nevar pielāgot vai ja atlasāt kredīta notu un žurnālu kombināciju kopā, nevis atsevišķi.
- Tā kā ir pievienota vairāku rindu atlases vadīkla, **lentes saite Saistītās izmaksas** vairs netiek atspējota, ja ir atlasītas vairākas rindas.
- Tas pievieno šādu brīdinājuma ziņojumu: "Pielāgošanai esat atlasījis vairāk nekā (atlasīto skaitu) ierakstus. Šīs darbības turpināšana var aizņemt kādu laiku. Vai esat pārliecināts, ka vēlaties turpināt šo darbību?"

Šis līdzeklis arī noņem 2. darbību no procesa plūsmas, kas tika aprakstīta iepriekš šajā rakstā. Tāpēc visas transakcijas, kas tika atlasītas **pirms lapas Koriģēt transakcijas atvēršanas, tiks iekļautas koriģējamo transakciju** sarakstā. Lai tos meklētu, nav jāizmanto **poga Atlasīt** .

> [!NOTE] 
> Pat ja šī funkcija ir atspējota, pielāgošanai joprojām varat atlasīt vairākus ierakstus. Tomēr tiks atlasīts *tikai viens ieraksts*, un dialoglodziņš **Transakciju** atlasīšana tiks parādīts uzreiz pēc tam, kad atlasīsit korekcijas atvēršanai.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Korekciju transakciju statusi, kurus var iespējot vai atspējot korekcijām

Tālāk norādītos statusus var iespējot vai atspējot **lapas Projektu vadības un uzskaites parametri** cilnē **Vispārīgi** :

- Publicēts
- Rēķina priekšlikums
- Izrakstīts rēķins
- Novērtēts
- Likvidēta
- Sākuma atlikums (stunda)

## <a name="adjustment-parameters"></a>Regulēšanas parametri

Šie parametri ir uzskaitīti **cilnes Vispārīgi lapā** Projektu vadības un uzskaites parametri **grupā Korekcija**  **, un tie modificēs** korekciju apstrādes uzvedību. 

| Parametra nosaukums | Apraksts |
|----------------|-------------
| Vienmēr izveidojiet korekcijas darījumu | Ja šis parametrs ir iespējots, korekcijas process vienmēr radīs jaunu reverso darījumu un jaunu koriģētu darījumu, ja tam ir finansiāla vai pārskatu sniegšanas ietekme. Ja parametrs ir atspējots, korekcijas procesā tiks atjaunināta sākotnējā transakcija, nevis izveidots reverss un jauna transakcija scenārijam, piemēram, transakcijas teksta atjauninājumam. |
| Lauks Automātiskā atjaunināšana | Ja šis parametrs ir iespējots, sistēma pārrēķinās pašizmaksu un pārdošanas cenu. |
| Korekcijas datuma izmantošana kā jauns projekts | Šis parametrs tiek izmantots, lai pārvietotu darījumus uz nākamo finanšu periods, pirms sistēma atbalstīja šo funkciju. Mēs neiesakām to izmantot, jo tas maina transakcijas darbības datumu un nākamajā laidienā būs novecojis. |
| Atļaut slēgtas darbības | Parasti transakcijas nevar izveidot slēgtām darbībām. Ja šis parametrs ir iespējots, šī darbība tiek ignorēta. Tāpēc slēgtajām darbībām var izveidot korekcijas. |
