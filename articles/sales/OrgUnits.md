---
title: Organizācijas vienības
description: Šajā rakstā ir aprakstīts organizatorisko vienību jēdziens un paskaidrots, kā izveidot un uzturēt organizācijas vienības programmā Microsoft Dynamics 365 Project Operations.
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

Programmā Microsoft Dynamics 365 Project Operations organizācijas struktūrvienība *ir atsevišķa grupa vai nodaļa profesionālu pakalpojumu uzņēmumā,* kas nodarbina apmaksājamus resursus, kuriem ir izmaksu likmes.

Profesionālo pakalpojumu uzņēmumiem, kas izmanto tehniskos resursus dažādās prakses jomās vai darbības virzienos, lomas aizpildīšanas izmaksas var atšķirties atkarībā no prakses jomas vai uzņēmējdarbības jomas, kurā loma ir aizpildīta. Šajā scenārijā organizatorisko vienību jēdziens palīdz, nodrošinot veidu, kā grupēt apmaksājamo lomu kopumu uzņēmuma nodaļā, kurai šīm lomām ir atšķirīga izmaksu struktūra.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organizatorisko vienību jēdziens projektu operācijās

Projekta operācijās organizācijas vienībai ir noteikta valūta un noteikti izmaksu cenrāži.

Organizācijas struktūrvienības valūta ir primārā valūta, kas tiek izmantota izmaksu izsekošanai.

Katrai organizācijas struktūrvienībai var pievienot vienu vai vairākus izmaksu cenrāžus. Projekta operācijas cenrāžiem, kurus var pievienot organizācijas vienībai, ir šādi ierobežojumi:

- Cenrāžiem jābūt organizācijas vienības valūtā.
- Cenrāžiem jābūt izmaksu cenrāžiem.

Turklāt entītijā Resurss ir iekļauts organizācijas vienības atribūts. Katru resursu var piešķirt vienai organizācijas struktūrvienībai.

### <a name="roles-of-organizational-units"></a>Organizācijas struktūrvienību lomas

Organizatoriskajai vienībai ir divas lomas projektu operācijās:

- **Līgumslēdzēja struktūrvienība** — organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību. Līgumslēdzēja struktūrvienību norāda lauks **Līgumslēdzēja struktūrvienība** lapu **Iespēja**, **Piedāvājums**, **Projekta līgums** un **Projekts** virsraksta sadaļā.
- **Resursu struktūrvienība** — organizācijas struktūrvienība, kam pieder vai ir piešķirts resurss. Šī organizācijas struktūrvienība tās resursiem var nodrošināt atsevišķas lomas darba paziņojumos (SOW) un projektos, kas pieder līgumslēdzējai struktūrvienībai.

![Līgumslēdzēja struktūrvienības un resursu struktūrvienības.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Bieži uzdotie jautājumi par organizācijas vienību

Šie ir daži no bieži uzdotajiem jautājumiem par organizācijas struktūrvienībām.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kā entītija Organizācijas vienība projekta operācijās ir saistīta ar entītiju Organizācija, kas jau pastāv programmā Dynamics 365?

Dynamics 365 entītija Organizācija attēlo globālās Dynamics 365 instances nosaukumu. Šis nosaukums parasti ir globālā uzņēmuma nosaukums.

Entītija Organizācijas struktūrvienība norāda grupu vai nodaļu globālajā uzņēmumā. Šai grupai vai nodaļai ir lomu kopa un izmaksu cenrādis šīm lomām, un šīs lomas un cenrādis atšķiras no citu uzņēmuma grupu vai nodaļu lomām un cenrāžiem.

Instalējot projekta operācijas, tiek izveidota noklusējuma organizatoriskā vienība, pamatojoties uz organizāciju. Visi esošie resursi tiek piešķirti noklusējuma organizācijas struktūrvienībai. Ja pakalpojumā Dynamics 365 tiek importēti jauni Active Directory lietotāji vai resursi, lietotāja importēšanas process tos piešķir noklusējuma organizācijas vienībai project operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kā entītija Organizācijas vienība atšķiras no entītijas Struktūrvienība?

Programmā Dynamics 365 entītija Uzņēmuma struktūrvienība ir drošības konstrukcija. Lietotāja saistība ar uzņēmuma struktūrvienību nosaka entītijas un entītiju ierakstus, kam lietotājs var piekļūt. Tā arī nosaka atļaujas (Izveidot, Lasīt, Rakstīt, Dzēst, Pievienot, Pievienot pie, Piešķirt vai Kopīgot), kas lietotājam ir attiecībā uz šo entītiju ierakstiem.

Entītija Organizācijas struktūrvienība norāda uzņēmuma grupu vai nodaļu, kam ir noteiktas izmaksu likmes darbiniekiem, kas tai ir piešķirti. Resursa saistība ar organizācijas struktūrvienību nosaka resursa izmaksas projekta darbībai.

Ieviešot Dynamics 365, optimizējiet drošības autorizāciju uzņēmuma struktūrvienību hierarhijai un lietotāju piešķiršanai uzņēmuma struktūrvienībām. Piešķiriet visus lietotājus, kam parasti ir jāpiekļūst vienai ierakstu kopai, tai pašai uzņēmuma struktūrvienībai. Organizācijas struktūrvienība neietekmē drošības autorizāciju vai piekļuvi.

**Piemērs, kas parāda vienu potenciālu atšķirību organizatorisko vienību un struktūrvienību modelēšanā**

Uzņēmumā Contoso Ltd. ir attīstīta Microsoft tehnoloģiju darbības joma. Konrāds un Antra ir C\# izstrādātāji, taču Antra atrodas Amerikas Savienotajās Valstīs, turpretim Konrāds — Indijā. Lielākajai daļai projektu iesaistes ir vajadzīgi resursi gan no Contoso Indijas, gan Contoso ASV, un Prakašai un Trisijai ir nepieciešama vienāda drošības līmeņa piekļuve projektiem šajā prakses jomā. Tomēr Contoso Indija izstrādātāju izmaksas ievērojami atšķiras no to izstrādātāju izmaksām uzņēmumā Contoso ASV.

Tālāk ir sniegts optimāls veids, kā noformēt šo scenāriju, izmantojot Dynamics 365 un Project Operations.

1. Izveidojiet Microsoft tehnoloģiju darbības jomu kā uzņēmuma struktūrvienību un piesaistiet tai Konrādu un Antru. Tādā veidā jūs palīdzat nodrošināt, ka abiem darbiniekiem ir vienāds drošības līmenis, lai piekļūtu jebkuriem projektiem šajā prakses jomā. Viņi abi varēs pārbaudīt progresu un ziņot par laiku, izdevumiem, materiālu lietojumu un uzdevumu atjauninājumiem.
2. Izveidojiet divas organizatoriskas vienības, lai palīdzētu nodrošināt, ka projekta izmaksas tiek pareizi atspoguļotas.
3. Saistīt Tricia ar Contoso ASV un Prakašu ar Contoso Indiju.
4. Piešķiriet abām organizācijas struktūrvienībām atbilstošos izmaksu cenrāžus. Tādā veidā jūs palīdzat nodrošināt, ka prakaša un Tricia projektā reģistrētās izmaksas precīzi atspoguļo izmaksu atšķirību starp Contoso ASV un Contoso Indiju.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Vai organizācijas struktūrvienības ir saistītas ar pārdošanas teritorijām programmā Dynamics 365?

Starp pārdošanas teritorijām un organizācijas struktūrvienībām nav saistības vai relācijas. Pārdošanas teritorija parasti ir ģeogrāfiskais apgabals, kurā notiek pārdošana. Pārdošanas cenrādi var saistīt ar katru pārdošanas teritoriju.

Organizācijas struktūrvienība ir iekšēja grupa vai nodaļa uzņēmumā, kas izseko izmaksas lomu kopai, ko tā pārdod citām nodaļām vai ārējiem klientiem.

**Piemērs, kas parāda vienu potenciālu atšķirību organizatorisko vienību un pārdošanas teritoriju modelēšanā**

Uzņēmumam Contoso Ltd ir divi izstrādes centri: Contoso ASV un Contoso Indija. Resursu izmaksas starp šiem diviem attīstības centriem ievērojami atšķiras. Contoso pārdod savus informācijas tehnoloģiju (IT) pakalpojumus daudzos starptautiskos tirgos, piemēram, Latīņamerikā, Ziemeļamerikā, Āzijas un Klusā okeāna reģionā, Rietumeiropā un Tuvajos Austrumos. Viena projekta lomu norēķinu likmes var ievērojami atšķirties šajos tirgos. Contoso ASV un Contoso Indija ir jāiestata kā organizācijas struktūrvienības, un katrai organizācijas struktūrvienībai ir nepieciešams savs izmaksu cenrādis. Āzijas Klusā okeāna daļa, Latīņamerika, Ziemeļamerika, Rietumeiropa un Tuvie Austrumi ir jāiestata kā pārdošanas teritorijas, un katrai pārdošanas teritorijai ir nepieciešams savs pārdošanas cenrādis.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Kāpēc pastāv ierobežojums attiecībā uz cenrāžu saistīšanu ar organizācijas struktūrvienībām?

Pārdošanas izcenojums parasti ir unikāls katrā ģeogrāfiskajā apgabalā vai tirgū, kurā tiek pārdoti pakalpojumi. Uzņēmuma iekšējām nodaļām parasti nav sava pārdošanas izcenojuma viena veida pakalpojumiem. Tomēr iekšējām nodaļām ir atšķirīga pārdoto preču pašizmaksa (PPPI) atkarībā no nodarbināto personu prasmēm un darba apstākļiem reģionā, kurā tās strādā. Tā kā organizācijas struktūrvienības tiek modelētas kā uzņēmuma iekšējās nodaļas, tām var būt tikai izmaksu cenrāži.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Kāpēc mēs nevaram saistīt pārdošanas cenrāžus ar organizatoriskām vienībām?

Projektu operācijās pārdošanas cenrāžus var saistīt ar debitoriem un pārdošanas teritorijām. Transakciju entītijas, piemēram, Iespēja, Piedāvājums, Projekta līgums un Projekts, izmanto pārdošanas cenrāžus, kas pievienoti debitora kontam vai pārdošanas teritorijai, lai noteiktu rēķinu likmes un potenciālos ieņēmumus projekta iesaistei.

Izmaksu cenrāži tiek saistīti ar organizācijas struktūrvienībām. Transakciju entītijas, piemēram, Iespēja, Piedāvājums, Projekta līgums un Projekts, izmanto izmaksu cenrāžus, kas pievienoti līgumslēdzējai vienībai, lai noteiktu projekta iesaistes izmaksas.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Vai projekta operācijās organizatoriskās vienības ir hierarhiskas?

Nē. Pašreizējā projekta operāciju laidienā organizatoriskās vienības nav hierarhiskas. Tāpēc nevar veikt šādus uzdevumus:

- Konfigurējiet modeli noklusējuma izmaksu cenu ievadīšanai, kas šķērso hierarhiju.
- Pārskatiet ieņēmumus vai izmaksas, kas tiek ieviestas dažādos organizācijas vienību hierarhijas līmeņos.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mēs esam liels daudznacionāls uzņēmums, kam ir sarežģīta, daudzlīmeņu izmaksu centru, nodaļu un norēķinu biroju hierarhija. Kā mēs varam vislabāk izmantot organizatorisko vienību jēdzienu pašreizējā projektu operāciju versijā?

Ja jums ir sarežģīta izmaksu centru, nodaļu, norēķinu biroju utt.

Šajā piemērā parādīta tipiska hierarhija.

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

Ja jūsu hierarhija atgādina šo piemēru, tas ir jāiestata kā plakans saraksts, kā parādīts šeit:

- Contoso Indija — SAP darbības joma — tehniskie konsultanti
- Contoso Indija — SAP darbības joma — funkcionālie konsultanti
- Contoso Indija — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti
- Contoso Indija — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti
- Contoso ASV — SAP darbības joma — tehniskie konsultanti
- Contoso ASV — SAP darbības joma — funkcionālie konsultanti
- Contoso ASV — Microsoft tehnoloģiju darbības joma — tehniskie konsultanti
- Contoso ASV — Microsoft tehnoloģiju darbības joma — funkcionālie konsultanti

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mēs esam neliels profesionālo pakalpojumu uzņēmums, kurā ir tikai viena nodaļa. Kā mēs varam vislabāk izmantot organizatorisko vienību jēdzienu pašreizējā projektu operāciju versijā?

Ja uzņēmums darbojas kā viena struktūrvienība ar vienu izmaksu cenrādi, jums nav jāiestata neviena organizācijas struktūrvienība. Projekta operāciju instalēšana izveido vienu noklusējuma organizatorisko vienību, kurai ir tāds pats nosaukums kā organizācijai. Visi lietotāji pēc noklusējuma tiek piešķirti šai organizācijas struktūrvienībai. Katru reizi, kad sistēma pieprasa, lai tiktu atlasīta organizācijas struktūrvienība, pēc noklusējuma tiek atlasīta šī organizācijas struktūrvienība.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kad projekts tiek izveidots no piedāvājuma vai projekta līguma rindas, noklusējuma līgumslēdzēja struktūrvienība tiek iegūta no piedāvājuma vai projekta līguma. Kāda ir noklusējuma līgumslēdzēja vienība, ja projekts ir izveidots pirms pārdošanas entītijām, piemēram, Piedāvājums vai Projekta līgums?

Kad projekts tiek izveidots patstāvīgi, projekta noklusējuma līgumslēdzēja struktūrvienības pamatā ir lietotājs, kas to izveido. Šis lietotājs ir arī noklusējuma projekta vadītājs. Ja projekts ir kartēts uz pārdošanas entītiju, piemēram, piedāvājumu vai projekta līgumu, projekta līgumslēdzēja vienība ir balstīta uz pārdošanas entītiju. Šajā gadījumā var tikt no jauna veikti projekta novērtējumi, jo izmaksu cenrādis tiek lietots, lai aprēķinātu izmaksu novērtējuma izmaiņas tad, ja tiek mainīta līgumslēdzēja struktūrvienība. Pārdošanas cenrādis tiek izmantots, lai aprēķinātu pārdošanas novērtējumus, kas tiks mainīti tā, lai tie būtu sinhronizēti ar piedāvājuma projekta cenrādi.

**Projekta lauki Līgumslēdzēja vienība** un **Valūta** ir bloķēti rediģēšanai, jo tiem jābūt sinhronizētiem ar pārdošanas entītijas (piedāvājuma vai projekta līguma) vērtībām, uz kurām projekts ir kartēts.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Izveidot un uzturēt organizācijas vienības projektu operācijās

Lai izveidotu organizācijas vienību projektu operācijās, rīkojieties šādi.

1. Dodieties uz **Iestatījumu \> organizācijas vienības**.
2. Atlasiet **Jauns**.
3. **Apgabala** Vispārīgi **laukā Nosaukums** ievadiet organizācijas vienības nosaukumu. Pēc tam iestatiet pārējos laukus pēc vajadzības.
4. Atlasiet **Saglabāt**, lai izveidotu ierakstu un turpinātu to rediģēt.
5. Sadaļā **Izmaksu cenrāži** atlasiet pluszīmi (**+**), lai pievienotu cenrādi. Šeit var pievienot tikai tos cenrāžus **, kuriem ir izmaksu** konteksts.
6. Laukā **Nosaukums** atlasiet **pogu Meklēt** un atlasiet cenrādi, kuru vēlaties padarīt pieejamu organizācijas vienībai. Turpiniet pievienot cenrāžus pēc vajadzības.
7. Kad esat pabeidzis pievienot cenrāžus, lapas apakšējā labajā stūrī atlasiet **Saglabāt**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
