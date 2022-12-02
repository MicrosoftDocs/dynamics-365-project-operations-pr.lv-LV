---
title: Organizācijas vienības
description: Šajā rakstā ir aprakstīts organizācijas vienību jēdziens un izskaidrots, kā izveidot un uzturēt organizācijas vienības programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921633"
---
# <a name="organizational-units-overview"></a>Organizācijas vienību pārskats

Pakalpojumā Microsoft Dynamics 365 Project Operations *organizācijas struktūrvienība* ir atsevišķa grupa vai nodaļa profesionālu pakalpojumu uzņēmumā, kas izmanto apmaksājamus resursus, kam ir izmaksu likmes.

Profesionālo pakalpojumu uzņēmumiem, kas izmanto tehniskos resursus dažādās darbības jomās vai uzņēmējdarbības veidos, izmaksas, kas jāievada lomai vienā darbības jomā vai uzņēmējdarbības veidā, var atšķirties atkarībā no darbības jomas vai uzņēmējdarbības veida. Šādā gadījumā organizācijas struktūrvienību koncepcija šajā scenārijā ir noderīga tādējādi, ka tā nodrošina veidu, kādā grupēt apmaksājamo lomu kopu tāda uzņēmuma nodaļā, kas šīm lomām ir izveidojis noteiktu izmaksu struktūru.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organizācijas vienību jēdziens pakalpojumā Project Operations

Pakalpojumā Project Operations organizācijas vienībai ir noteikta valūta un izmaksu cenrāži.

Organizācijas struktūrvienības valūta ir primārā valūta, kas tiek izmantota izmaksu izsekošanai.

Katrai organizācijas struktūrvienībai var pievienot vienu vai vairākus izmaksu cenrāžus. Project Operations piedāvā tālāk norādītos ierobežojumus cenrāžiem, ko var pievienot organizācijas struktūrvienībai.

- Cenrāžiem jābūt organizācijas struktūrvienības valūtā.
- Cenrāžiem ir jābūt izmaksu cenrāžiem.

Turklāt entitījai Resurss ir organizācijas vienības atribūts. Katru resursu var piešķirt vienai organizācijas struktūrvienībai.

### <a name="roles-of-organizational-units"></a>Organizācijas struktūrvienību lomas

Programmā Project Operations organizācijas struktūrvienībai ir divas lomas.

- **Līgumslēdzēja struktūrvienība** — organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību. Līgumslēdzēja struktūrvienību norāda lauks **Līgumslēdzēja struktūrvienība** lapu **Iespēja**, **Piedāvājums**, **Projekta līgums** un **Projekts** virsraksta sadaļā.
- **Resursu struktūrvienība** — organizācijas struktūrvienība, kam pieder vai ir piešķirts resurss. Šī organizācijas struktūrvienība tās resursiem var nodrošināt atsevišķas lomas darba paziņojumos (SOW) un projektos, kas pieder līgumslēdzējai struktūrvienībai.

![Līgumslēdzēja struktūrvienības un resursu struktūrvienības.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>BUJ par organizācijas vienībām

Šie ir daži no bieži uzdotajiem jautājumiem par organizācijas struktūrvienībām.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kā entītija Organizācijas struktūrvienība programmā Project Operations ir saistīta ar entītiju Organizācija, kas jau pastāv programmā Dynamics 365?

Organizācijas entītija programmā Dynamics 365 norāda globālās Dynamics 365 instances nosaukumu. Šis nosaukums parasti ir globālā uzņēmuma nosaukums.

Entītija Organizācijas struktūrvienība norāda grupu vai nodaļu globālajā uzņēmumā. Šai grupai vai nodaļai ir lomu kopa un izmaksu cenrādis šīm lomām, un šīs lomas un cenrādis atšķiras no citu uzņēmuma grupu vai nodaļu lomām un cenrāžiem.

Instalējot programmu Project Operations, tiek izveidota noklusējuma organizācijas struktūrvienība, kuras pamatā ir organizācija. Visi esošie resursi tiek piešķirti noklusējuma organizācijas struktūrvienībai. Ja programmā Dynamics 365 tiek importēti jauni Active Directory lietotāji vai resursi, lietotāja importēšanas process tos piešķir noklusējuma organizācijas struktūrvienībai programmā Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kā entītija Organizācijas struktūrvienība atšķiras no entītijas Uzņēmuma struktūrvienība?

Programmā Dynamics 365 entītija Uzņēmuma struktūrvienība ir drošības konstrukcija. Lietotāja saistība ar uzņēmuma struktūrvienību nosaka entītijas un entītiju ierakstus, kam lietotājs var piekļūt. Tā arī nosaka atļaujas (Izveidot, Lasīt, Rakstīt, Dzēst, Pievienot, Pievienot pie, Piešķirt vai Kopīgot), kas lietotājam ir attiecībā uz šo entītiju ierakstiem.

Entītija Organizācijas struktūrvienība norāda uzņēmuma grupu vai nodaļu, kam ir noteiktas izmaksu likmes darbiniekiem, kas tai ir piešķirti. Resursa saistība ar organizācijas struktūrvienību nosaka resursa izmaksas projekta darbībai.

Ieviešot Dynamics 365, optimizējiet drošības autorizāciju uzņēmuma struktūrvienību hierarhijai un lietotāju piešķiršanai uzņēmuma struktūrvienībām. Piešķiriet visus lietotājus, kam parasti ir jāpiekļūst vienai ierakstu kopai, tai pašai uzņēmuma struktūrvienībai. Organizācijas struktūrvienība neietekmē drošības autorizāciju vai piekļuvi.

**Piemērs, kurā parādīta viena iespējamā organizācijas struktūrvienību un uzņēmuma struktūrvienību modelēšanas atšķirība**

Uzņēmumā Contoso Ltd. ir attīstīta Microsoft tehnoloģiju darbības joma. Konrāds un Antra ir C\# izstrādātāji, taču Antra atrodas Amerikas Savienotajās Valstīs, turpretim Konrāds — Indijā. Lielākajai daļai projektu ir nepieciešami resursi no Contoso Indija un Contoso ASV, turklāt Konrādam un Antrai ir nepieciešams vienāds drošības līmenis projektiem šajā darbības jomā. Tomēr Contoso Indija izstrādātāju izmaksas ievērojami atšķiras no to izstrādātāju izmaksām uzņēmumā Contoso ASV.

Tālāk parādīts optimāls veids, kā izstrādāt šo scenāriju, izmantojot Dynamics 365 un Project Operations.

1. Izveidojiet Microsoft tehnoloģiju darbības jomu kā uzņēmuma struktūrvienību un piesaistiet tai Konrādu un Antru. Šādi tiek nodrošināts, ka abiem darbiniekiem ir vienāds drošības līmenis piekļuvei visiem projektiem šajā darbības jomā. Viņi abi varēs pārbaudīt norisi un iekļaut atskaitē laiku, izdevumus, materiālu lietojumu un uzdevumu atjauninājumus.
2. Izveidojiet divas organizācijas struktūrvienības, lai palīdzētu nodrošināt, ka projekta izmaksas tiks pareizi atspoguļotas.
3. Saistiet Antru ar Contoso ASV, bet Konrādu — ar Contoso Indija.
4. Piešķiriet abām organizācijas struktūrvienībām atbilstošos izmaksu cenrāžus. Šādi palīdzēsit nodrošināt, ka Konrāda un Antras projektā ierakstītās izmaksas pareizi atspoguļos izmaksu atšķirību starp Contoso ASV un Contoso Indija.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Vai organizācijas struktūrvienības ir saistītas ar pārdošanas teritorijām programmā Dynamics 365?

Starp pārdošanas teritorijām un organizācijas struktūrvienībām nav saistības vai relācijas. Pārdošanas teritorija parasti ir ģeogrāfiskais apgabals, kurā notiek pārdošana. Pārdošanas cenrādi var saistīt ar katru pārdošanas teritoriju.

Organizācijas struktūrvienība ir iekšēja grupa vai nodaļa uzņēmumā, kas izseko izmaksas lomu kopai, ko tā pārdod citām nodaļām vai ārējiem klientiem.

**Piemērs, kurā parādīta viena iespējamā organizācijas struktūrvienību un pārdošanas teritoriju modelēšanas atšķirība**

Uzņēmumam Contoso Ltd ir divi izstrādes centri: Contoso ASV un Contoso Indija. Resursu izmaksas starp šiem diviem izstrādes centriem ievērojami atšķiras. Contoso savus informāciju tehnoloģiju (IT) pakalpojumus pārdod daudzos starptautiskajos tirgos, piemēram, Latīņamerikā, Ziemeļamerikā, Āzijas Klusā okeāna daļā, Rietumeiropā un Tuvajos Austrumos. Viena projekta lomu norēķinu likmes var ievērojami atšķirties šajos tirgos. Contoso ASV un Contoso Indija ir jāiestata kā organizācijas struktūrvienības, un katrai organizācijas struktūrvienībai ir nepieciešams savs izmaksu cenrādis. Āzijas Klusā okeāna daļa, Latīņamerika, Ziemeļamerika, Rietumeiropa un Tuvie Austrumi ir jāiestata kā pārdošanas teritorijas, un katrai pārdošanas teritorijai ir nepieciešams savs pārdošanas cenrādis.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Kāpēc pastāv ierobežojums attiecībā uz cenrāžu saistīšanu ar organizācijas struktūrvienībām?

Pārdošanas izcenojums parasti ir unikāls katrā ģeogrāfiskajā apgabalā vai tirgū, kurā tiek pārdoti pakalpojumi. Uzņēmuma iekšējām nodaļām parasti nav sava pārdošanas izcenojuma viena veida pakalpojumiem. Tomēr iekšējām nodaļām ir atšķirīga pārdoto preču pašizmaksa (PPPI) atkarībā no nodarbināto personu prasmēm un darba apstākļiem reģionā, kurā tās strādā. Tā kā organizācijas struktūrvienības tiek modelētas kā uzņēmuma iekšējās nodaļas, tām var būt tikai izmaksu cenrāži.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Kāpēc nevar saistīt pārdošanas cenrāžus ar organizācijas struktūrvienībām?

Programmā Project Operations pārdošanas cenrāžus var saistīt ar klientiem un pārdošanas teritorijām. Tādas transakciju entītijas kā Iespēja, Piedāvājums, Projekta līgums un Projekts izmanto pārdošanas cenrāžus, kas ir pievienoti klienta uzņēmumam vai pārdošanas teritorijai, lai noteiktu norēķinu likmes un iespējamos ieņēmumus projektā.

Izmaksu cenrāži tiek saistīti ar organizācijas struktūrvienībām. Tādas transakciju entītijas kā, piemēram, Iespēja, Piedāvājums, Projekta līgums un Projekts izmanto izmaksu cenrāžus, kas ir pievienoti līgumslēdzēja struktūrvienībai, lai noteiktu izmaksas projektā.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Vai organizācijas struktūrvienības programmā Project Operations ir hierarhiskas?

Nē. Pašreizējā Project Operations laidienā organizācijas struktūrvienības nav hierarhiskas. Tāpēc nevarat veikt tālāk uzskaitītos uzdevumus:

- Konfigurēt modeli to izmaksu cenu noklusējuma ievadīšanai, kas augšupšķērso hierarhiju.
- Iekļaujiet atskaitē ieņēmumus vai izmaksas, kas apkopoti dažādos organizācijas struktūrvienību hierarhijas līmeņos.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mēs esam liels, starptautisks uzņēmums ar sarežģītu vairāklīmeņu izmaksu centru, nodaļu un norēķinu biroju hierarhiju. Kā mēs varam vislabāk izmantot organizācijas struktūrvienību koncepciju pašreizējā Project Operations versijā?

Ja jums ir sarežģīta izmaksu centru, nodaļu, norēķinu biroju u.c. hierarhija, iestatiet šīs hierarhijas lapu mezglus kā atsevišķas organizācijas struktūrvienības.

Tālāk esošajā piemērā ir parādīta tipiska hierarhija.

**Contoso Indija**

- SAP darbības joma

    - Tehniskie konsultanti
    - Funkcionālie konsultanti

- Microsoft tehnoloģiju darbības joma

    - Tehniskie konsultanti
    - Funkcionālie konsultanti

**Contoso ASV**

- SAP darbības joma

    - Tehniskie konsultanti
    - Funkcionālie konsultanti

- Microsoft tehnoloģiju darbības joma

    - Tehniskie konsultanti
    - Funkcionālie konsultanti

Ja jūsu hierarhija ir līdzīga šim piemēram, tā ir jāiestata kā nekārtots saraksts, kā parādīts tālāk.

- Contoso Indija — SAP darbības joma — tehniskie konsultanti
- Contoso Indija — SAP darbības joma — funkcionālie konsultanti
- Contoso Indija — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti
- Contoso Indija — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti
- Contoso ASV — SAP darbības joma — tehniskie konsultanti
- Contoso ASV — SAP darbības joma — funkcionālie konsultanti
- Contoso ASV — Microsoft tehnoloģiju darbības joma — tehniskie konsultanti
- Contoso ASV — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mēs esam neliels profesionālo pakalpojumu uzņēmums, kurā ir tikai viena nodaļa. Kā mēs varam vislabāk izmantot organizācijas struktūrvienību koncepciju pašreizējā Project Operations versijā?

Ja uzņēmums darbojas kā viena struktūrvienība ar vienu izmaksu cenrādi, jums nav jāiestata neviena organizācijas struktūrvienība. Project Operations instalēšanas laikā izveido vienu noklusējuma organizācijas struktūrvienību ar tādu pašu nosaukumu kā organizācijai. Visi lietotāji pēc noklusējuma tiek piešķirti šai organizācijas struktūrvienībai. Katru reizi, kad sistēma pieprasa, lai tiktu atlasīta organizācijas struktūrvienība, pēc noklusējuma tiek atlasīta šī organizācijas struktūrvienība.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kad projekts tiek izveidots no piedāvājuma vai projekta līguma rindas, noklusējuma līgumslēdzēja struktūrvienība tiek iegūta no piedāvājuma vai projekta līguma. Kāda ir noklusējuma līgumslēdzēja vienība, ja projekts tiek izveidots pirms pārdošanas entītijām, piemēram, piedāvājuma vai projekta līguma entitījai?

Kad projekts tiek izveidots patstāvīgi, projekta noklusējuma līgumslēdzēja struktūrvienības pamatā ir lietotājs, kas to izveido. Šis lietotājs ir arī noklusējuma projekta vadītājs. Ja projekts tiek kartēts uz pārdošanas entītiju, piemēram, piedāvājumu vai projekta līgumu, projekta līgumslēdzēja struktūrvienības pamatā ir pārdošanas entītija. Šajā gadījumā var tikt no jauna veikti projekta novērtējumi, jo izmaksu cenrādis tiek lietots, lai aprēķinātu izmaksu novērtējuma izmaiņas tad, ja tiek mainīta līgumslēdzēja struktūrvienība. Pārdošanas cenrādis tiek izmantots, lai veiktu pārdošanas novērtējumus, kas tiks mainīti tā, lai tie būtu sinhronizēti ar piedāvājuma projekta cenrādi.

Projekta lauki **Līgumslēdzēja struktūrvienība** un **Valūta** ir bloķēti rediģēšanai, jo tiem ir jābūt sinhronizētiem ar vērtībām pārdošanas entītijā (piedāvājumā vai projekta līgumā), uz kuru projekts ir kartēts.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organizācijas struktūrvienību izveide un uzturēšana programmā Project Operations

Lai programmā Project Operations izveidotu organizācijas struktūrvienību, veiciet turpmāk uzskaitītās darbības.

1. Dodieties uz **Iestatījumi \> Organizācijas struktūrvienības**.
2. Atlasiet **Jauns**.
3. Apgabalā **Vispārīgi** ievadiet organizācijas struktūrvienības nosaukumu laukā **Nosaukums**. Pēc tam pēc vajadzības iestatiet pārējos laukus.
4. Atlasiet **Saglabāt**, lai izveidotu ierakstu, lai to varētu turpināt rediģēt.
5. Sadaļā **Izmaksu cenrāži** noklikšķiniet uz pluszīmes (**+**), lai pievienotu cenrādi. Šajā vietā var pievienot tikai cenrāžus ar kontekstu **Cena**.
6. Laukā **Nosaukums** noklikšķiniet uz pogas **Meklēt** un atlasiet cenrādi, kura pieejamību vēlaties iespējot šai struktūrvienībai. Turpiniet pēc vajadzības pievienot cenrāžus.
7. Pēc cenrāžu pievienošanas atlasiet ikonu **Saglabāt** lapas apakšējā labajā stūrī.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
