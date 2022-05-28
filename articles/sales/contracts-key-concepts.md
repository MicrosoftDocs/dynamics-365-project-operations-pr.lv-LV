---
title: Projektu līgumi — pamata koncepti
description: Šajā tēmā sniegta informācija par projekta līgumu pamata konceptiem risinājumā Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f87a29893ca3d9bec6fbd07dded66a282ff597c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582949"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Projektu līgumiem raksturīgie koncepti

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_



Šajā tēmā ir sniegti galvenie jēdzieni, kas jāzina, pirms sākat izmantot projektu līgumus programmā Dynamics 365 Project Operations:

## <a name="owning-company"></a>Atbildīgais uzņēmums

Īpašnieks uzņēmums ir juridiska persona no **projektu vadības un uzskaites** moduļa projektu operācijām no Dynamics 365 Finance. Atbildīgais uzņēmums pārstāv juridisko personu, kas būs atbildīga par izmaksām un ieņēmumiem, kas uzkrājas no darījuma.

## <a name="contracting-unit"></a>Līgumslēdzēja vienība

Līgumslēdzēja vienība pārstāv struktūrvienību vai praksi, kurai pieder projekta nodrošinājums. Katrai līgumslēdzējai vienībai var iestatīt resursu izmaksas. Norādot resursa izmaksas, var iestatīt arī dažādas resursu izmaksu likmes. Šī Līgumslēdzēja struktūrvienība aizņemas šos resursus citām uzņēmuma struktūrvienībām vai praksēm. Resursu izmaksu likmes sauc par pārsūtīšanas cenām, resursu aizņēmumiem vai apmaiņas cenām. Kad iestatāt resursu aizņēmumu izmaksu likmes no citām struktūrvienībām, izmantojiet aizdodošās struktūrvienības valūtu.

## <a name="cost-currency"></a>Izmaksu valūta

Izmaksu valūta ir valūta, kurā ekrānā tiek ziņotas izmaksas. Šī valūta ir atvasināta no valūtas, kas ir piesaistīta laukam **Līgumslēdzēja vienība** līgumā un projektā. Izmaksas var reģistrēt jebkurā valūtā attiecībā pret projektu. Taču tiek veikta valūtas konvertēšana no valūtas, kurā tika ierakstītas izmaksas, uz projekta izmaksu valūtu, ja tā tiek rādīta ekrānā.

Common Data Service (CDS) platformā valūtas kursam nevar būt spēkā esamības datuma, tāpēc laika gaitā ekrānā redzamās summas var mainīties, atjauninot valūtas maiņas kursus. Tomēr datubāzē ierakstītās izmaksas paliek nemainīgas, jo summas tiek glabātas valūtā, kādā tās radušās.

## <a name="sales-currency"></a>Pārdošanas valūta

Pārdošanas valūta risinājumā Project Operations ir valūta, kādā tiek reģistrētas un parādītas prognozētās un faktiskās pārdošanas summas. Pārdošanas valūta ir arī valūta, kurā klientam tiek izrakstīts rēķins par darījumu. Projekta līgumā pārdošanas valūtas noklusējuma vērtība tiek ņemta no klienta vai uzņēmuma ieraksta, un to var mainīt tikai laikā, kad tiek izveidots līgums. Kad līgums ir izveidots, slēdzot piedāvājumu kā iegūtu, līgumā norādītā valūta tiek iestatīta kā noklusējuma no piedāvājuma valūtas.

Kad no nulles izveidojat projekta līgumu, lauku **Pārdošanas valūta** nevar rediģēt. Produktu un projektu cenrāžu noklusējuma vērtības ir balstītas uz šī līguma valūtu.

Atšķirībā no izmaksām pārdošanas vērtības var reģistrēt tikai pārdošanas valūtā.

## <a name="billing-method"></a>Rēķinu izrakstīšanas metode

Parasti projektiem ir divu veidu līgumu modeļi — fiksētas maksas un uz patēriņu balstīti. Šie modeļi projekta operācijās tiek attēloti kā norēķinu metodes ar divām iespējamām vērtībām.

- Laiks un materiāli: uz patēriņu balstīts līguma modelis, kurā visām radītajām izmaksām ir atbilstoši ieņēmumi. Aprēķinot vai radot vairāk izmaksu, palielinās arī aplēstais un faktiskais pārdošanas apjoms. Līguma rindās, kurām ir šāda norēķinu metode, kas pabeidz faktiskos ieņēmumus, norādiet ierobežojumus, ko nedrīkst pārsniegt. Nepārsniedzamie ierobežojumi neietekmē prognozējamos ieņēmumus.
- Fiksēta cena: fiksētas maksas līguma modelis, kas norāda, ka pārdošanas vērtības ir neatkarīgas no izmaksām, kas radušās. Pārdošanas vērtība ir fiksēta un nemainās, aplēšot vai radot vairāk izmaksu.

## <a name="project-price-lists"></a>Projekta cenrāži

Projekta cenrāži tiek izmantoti cenu, nevis izmaksu likmju noklusējuma vērtību iestatīšanai laika, izdevumu un citos ar projektu saistītos komponentos. Var būt vairāki cenrāži. Katra projekta līguma cenrādim ir sava datumu efektivitāte. Projekta operācijas neatbalsta spēkā esamības datumu pārklāšanos projektu cenrāžos.

Ja projekta līgums tiek izveidots, iegūstot projekta piedāvājumu, projekta cenrāži tiek kopēti kopā ar līguma nosaukumu un iekļauto datumu. Šīs informācijas kopēšana ir nozīmē pielāgotas cenas projekta komponentiem šajā projekta līgumā.

## <a name="transaction-classes"></a>Darījumu klases

Project Operations atbalsta četru veidu transakciju klases:

- Laiks
- Izdevumi
- Materiāls
- Maksa

Izmaksu un pārdošanas vērtības var aprēķināt un radīt laika, izmaksu un materiālu transakciju klasēs. Maksa ir tikai ieņēmumu darījumu klase.

## <a name="work-entities-and-billing-entities"></a>Darba entītijas un norēķinu entītijas

Entītijas, kas atspoguļo darbu, ir projekti un uzdevumi. Entītijas, kas atspoguļo norēķinu aspektus, ir līguma rindas. Varat saistīt dažādas darba entītijas ar norēķinu opcijām, saistot tās ar līguma rindām.

## <a name="multi-customer-deals"></a>Vairāku klientu darījumi

Vairāku klientu darījumiem ir nekā viens klients, kas jāiekļauj darījuma rēķinā. Tālāk ir norādīti visbiežāk sastopamie piemēri.

- OEM uzņēmumi un to partneri: partneri un tālākpārdevēji pārdod produktu ar dažiem pievienotās vērtības pakalpojumiem, kas parasti ietver noteiktu darījumu ar klientu. OEM piedāvājumi piedāvā finansēt daļu projekta. 

- Publiskā sektora projekti: vairāki vietējās valdības departamenti vienojas par projekta finansēšanu, un tiem tiek izrakstīts rēķins atbilstoši iepriekš saskaņotam sadalījumam. Piemēram, skolas rajons un vietējā pašvaldība vienojas par peldbaseina būvniecības finansēšanu.

## <a name="invoice-schedules"></a>Rēķina izrakstīšanas grafiki

Rēķinu izrakstīšanas grafiki ir specifiski katrai līguma rindai un ir nepieciešami, lai automātiska rēķinu izrakstīšana darbotos. Rēķinu grafiki ir izveidoti, pamatojoties uz noteiktiem sākuma un beigu datumiem un rēķina biežumu. Grafiki tiek izmantoti līguma posmā, kad ir konfigurēts automātiskais rēķinu izveides process. Kad no piedāvājuma tiek izveidots projekta līgums, rēķinu izrakstīšanas grafiks no piedāvājuma tiek kopēts uz projekta līgumu.

## <a name="changes-from-dynamics-365-sales-orders"></a>Izmaiņas no Dynamics 365 Sales pasūtījumiem

Project Operations līgumi ir veidoti, izmantojot Dynamics 365 Sales pasūtījumus. Tomēr ir būtiskas novirzes un atšķirības funkcionalitātē. Līgumiem ir savas veidlapas un lietotāja interfeisa elementi, biznesa kārtulas, biznesa loģika spraudņi, kā arī klienta puses skripti, kas atšķir tos no pasūtījumiem. Šo iemeslu dēļ pārdošanas pasūtījumu un Project Operations līgumu nedrīkst izmantot kā savstarpējus aizstājējus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
